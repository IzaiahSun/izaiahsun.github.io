---
permalink: /publication/
title: "Full List of Publications"
excerpt: ""
author_profile: true
redirect_from: 
  - /publication.html
---

<div id="show_bib"></div>

<script src="https://cdn.jsdelivr.net/npm/jquery@3.7.1/dist/jquery.min.js"></script>
<script src="/assets/js/bibtex_js.js"></script>
<script>
    // load the bibtex file from the server: /assets/bibtex/myref.bib
    let bibtex_file = "/assets/bibtex/myref.bib";
    let myname = "Yuqiang Sun";
    let parser = new BibtexParser();
    var fixValue = function (value) {
        value = value.replace(/\\glqq\s?/g, "&bdquo;");
        value = value.replace(/\\grqq\s?/g, '&rdquo;');
        value = value.replace(/\\ /g, '&nbsp;');
        value = value.replace(/\\url/g, '');
        value = value.replace(/---/g, '&mdash;');
        value = value.replace(/{\\"a}/g, '&auml;');
        value = value.replace(/\{\\"o\}/g, '&ouml;');
        value = value.replace(/{\\"u}/g, '&uuml;');
        value = value.replace(/{\\"A}/g, '&Auml;');
        value = value.replace(/{\\"O}/g, '&Ouml;');
        value = value.replace(/{\\"U}/g, '&Uuml;');
        value = value.replace(/\\ss/g, '&szlig;');
        value = value.replace(/\{(.*?)\}/g, '$1');
        return value;
    }
    var ccfBadge = function(value){
        if (value == "A"){
            var badge = "<img src='https://img.shields.io/badge/CCF-A-red?style=flat-square'>"
        }else if (value == "B"){
            var badge = "<img src='https://img.shields.io/badge/CCF-B-blue?style=flat-square'>"
        }else if (value == "C"){
            var badge = "<img src='https://img.shields.io/badge/CCF-C-green?style=flat-square'>"
        }else{
            var badge = ""
        }
        return badge;
    }
    var authorBold = function(value){
        // first split by end
        var authors = value.split(" and ");
        // for each author, if the author name contains comma, then remove the comma and change the order
        for (var i = 0; i < authors.length; i++){
            var author = authors[i];
            if (author.indexOf(",") > 0){
                var name = author.split(",");
                authors[i] = name[1].trim() + " " + name[0].trim();
            }
        }
        // finally, join the authors and bold the name in myname
        var author = authors.join(", ");
        author = author.replace(myname, "<b>" + myname + "</b>");
        return author;
    }
    function getRemote(remote_url) {
    return $.ajax({
        type: "GET",
        url: remote_url,
        async: false
    }).responseText;
}   bibtex_string = getRemote(bibtex_file);
    parser.setInput(bibtex_string);
    parser.bibtex();
    let entries = Object.values(parser.getEntries());
    let html = "<ul>";
    // sort by year, descending
    entries.sort(function(a, b) {
        return b["YEAR"] - a["YEAR"];
    });
    let prev_year = 0;
    for(let entry of entries) {
        let title = fixValue(entry["TITLE"]);
        let author = fixValue(entry["AUTHOR"]);
        let year = entry["YEAR"];
        if ("JOURNAL" in entry) {
            var venue = fixValue(entry["JOURNAL"]);
        } else if ("BOOKTITLE" in entry) {
            var venue = fixValue(entry["BOOKTITLE"]);
        } else if ("SCHOOL" in entry) {
            var venue = fixValue(entry["SCHOOL"]);
        } else if ("PUBLISHER" in entry) {
            var venue = fixValue(entry["PUBLISHER"]);
        } else {
            var venue = "";
        }
        if ("CCF" in entry) {
            var ccf = ccfBadge(entry["CCF"]);
        } else {
            var ccf = "";
        }
        if("OPENSOURCE" in entry){
            var opensource = "<li>This paper is open-sourced at <a href='" + entry["OPENSOURCE"] + "'>this website</a>.</li>";
        }else{
            var opensource = "";
        }
        html += "<li>";
        html += "<span>" + year + ", " + title + "</span>\n" + ccf;
        html += "<ul>";
        html += "<li>" + authorBold(author) + "</li>";
        html += "<li>" + venue + "</li>";
        html += opensource;
        html += "</ul>";
        html += "</li>";
    }
    html += "</ul>";
    document.getElementById("show_bib").innerHTML = html;
</script>
