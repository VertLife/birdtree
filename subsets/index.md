---
layout: default
title: Phylogeny subsets
weight: 4
---

Phylogeny subsets
=================

This tool provides a simple way to produce distributions of trees with subsets
of taxa. The upper limit for the tool is 2,500 species. If larger subsets ar
required you can [download full trees](http://birdtree.org/archives/).

The tool first trims to a subset, and then samples trees from a chosen
pseudo-posterior distribution. *Note that any further analyses should only
be conducted with a large sample of trees.*

**Instructions**

1. Select species from the list. Then copy and paste or drag and drop
them into the box to the right. Alternatively, download the [taxonomy file](http://birdtree.org/bird-tree/BLIOCPhyloMasterTax.csv)
and paste species names from the "Scientific" column.  
2. Choose a tree distribution (see paper for details).  
3. Select the number of trees to download (defaults to minimum of 100)  
4. Click "Get Trees" to download a zipped set of randomly selected
trees with metadata including accession numbers and citations to original  
sources.  

<td valign="TOP">
    <div class="topright">
      <div class="selectInstructions DATE">
      <p>
    This website accompanies the following study:
     <br><br>
    The global diversity of birds in space and time<br>
    W. Jetz,  G. H. Thomas, J. B. Joy, K. Hartmann, A. O. Mooers<br>
    Nature, 491: 444-448<br><br>
    doi:10.1038/nature11631,<br>
    URL: <a href="http://www.nature.com/nature/journal/v491/n7424/full/nature11631.html">http://www.nature.com/nature/journal/v491/n7424/full/nature11631.html</a><br><br><br><br><br><br><br><br><br>
      <font size="5"><strong>Phylogeny subsets</strong></font>
        <br>
        This tool provides a simple way to produce distributions of trees with subsets of taxa. The upper limit for the tool is 2,500 species (above which server-based subsetting becomes prohibitively slow). If larger subsets are required you can <a href="archives/">download full trees</a> by following the links on the left.
        <br><br>
        The tool first trims to a subset, and then samples trees from a chosen pseudo-posterior distribution. <i>Note that any further analyses should only be conducted with a large sample of trees.</i>

          <br><br>
          <b>Instructions</b>
          <br>
          1. Select species from the list. Then copy and paste or drag and drop them into the box to the right. Alternatively, download the <a href="BLIOCPhyloMasterTax.csv"> taxonomy file</a> and paste species names from the "Scientific" column.
          <br>
          2. Choose a tree distribution (see paper for details).
          <br>
          3. Select the number of trees to download (defaults to minimum of 100)
          <br>
          4. Click "Get Trees" to download a zipped set of randomly selected trees with metadata including accession numbers and citations to original sources.

          <br><br><br>



      </p></div>

      <div class="speciesContainer">
        {% include species.html %}
      </div>

      <textarea class="selected" placeholder="Paste species names here (one binomial per line)."></textarea>


    </div>
    <div class="bottomright">
            <label for="email">Please provide your email address:</label><input type="text" name="email" id="email" size="25">
      <br>
      <label for="treeset">Source of trees:</label>
      <select name="treeset" id="treeset">
         <option selected="selected" value="4">Ericson All Species: a set of 10000 trees with 9993 OTUs each </option>
         <option value="2">Ericson Sequenced Species: a set of 10000 trees with 6670 OTUs each </option>
         <option value="3">Hackett All Species: a set of 10000 trees with 9993 OTUs each </option>
         <option value="5">Hackett Sequenced Species: a set of 10000 trees with 6670 OTUs each </option>
      </select>
      <br>
      <label for="treenum">Select number of trees to create (minimum 100, maximum 10,000)</label>
      <input id="treenum" type="text" size="2" value="100">
      <button id="gettrees">Get Trees</button>
      <img id="loading" src="/{{site.root}}/images/loading.gif" onload="$(this).toggle(false)" style="display: none;">
      <div id="status"></div>
    </div>
