---
layout: default
title: Phylogeny subsets
weight: 4
---

Phylogeny subsets
=================

This tool provides a simple way to produce distributions of trees with subsets
of taxa. The upper limit for the tool is 2,500 species. If larger subsets ar
required you can [download full trees](http://litoria.eeb.yale.edu/archives/).

The tool first trims to a subset, and then samples trees from a chosen
pseudo-posterior distribution. *Note that any further analyses should only
be conducted with a large sample of trees.*

**Instructions**

1. Select species from the list. Then copy and paste or drag and drop
them into the box to the right. Alternatively, download the [taxonomy file](http://litoria.eeb.yale.edu/bird-tree/BLIOCPhyloMasterTax.csv)
and paste species names from the "Scientific" column.  
2. Choose a tree distribution (see paper for details).  
3. Select the number of trees to download (defaults to minimum of 100)  
4. Click "Get Trees" to download a zipped set of randomly selected
trees with metadata including accession numbers and citations to original  
sources.  

<div class="container">
<div class="row">
<div class="speciesContainer col-md-3">
  {% include species.html %}
</div>

<textarea  class="selectedContainer col-md-3" id="selected" placeholder="Paste species names here (one binomial per line)."></textarea></div>
</div>



Please provide your email address: <input type="text" name="email" id="email" size="25">

Source of trees: <select name="treeset" id="treeset">
   <option selected="selected" value="4">Ericson All Species: a set of 10000 trees with 9993 OTUs each </option>
   <option value="2">Ericson Sequenced Species: a set of 10000 trees with 6670 OTUs each </option>
   <option value="3">Hackett All Species: a set of 10000 trees with 9993 OTUs each </option>
   <option value="5">Hackett Sequenced Species: a set of 10000 trees with 6670 OTUs each </option>
   <option value="6">Stage2 Parrot</option>
   <option value="7">Stage2 FP Trees Ericson</option>
   <option value="8">Stage2 FP Trees Hackett</option>
   <option value="13">Stage2 MayrAll Ericson</option>
   <option value="14">Stage2 MayrParSho Ericson</option>
   <option value="15">Stage2 MayrAll Hackett</option>
   <option value="16">Stage2 MayrParSho Hackett</option>
</select>

Select number of trees to create (minimum 100, maximum 10,000): <input id="treenum" type="text" size="2" value="100">
<button class="btn" id="gettrees">Get Trees</button> <span><img id="loading" src="/images/loading.gif" onload="$(this).toggle(false)" style="display: none;"><span><span id="status"></span>
