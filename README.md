# wsb-dev
 
I. Adding a Card

	Add the following code template after each card’s </div>. Make sure that the code below is not copied into another alumni card’s <div> otherwise the page will not look as intended.

	Card Code Template
 
      <div class="card"> 
        <a href = “LINK TO PAGE“>
        <img src=“REPLACE WITH IMAGE LINK“ alt=“REPLACE WITH ALT IMAGE NAME>
        <h3 style = "text-align: center" >REPLACE WITH ALUMNI NAME</h3>
        <p>REPLACE WITH ALUMNI DESCRIPTION</p>
        </a>
      </div>


II. Adding Tags to Letter

	After adding formatting and encoding your letter, you can paste the xml directly to the page and add tags to sort through the letters.

	Tag Creation Template

      <button class="tag" onclick="filterTag(‘love’)”>Love</button>
      <button class="tag" onclick="filterTag(‘scenery’)”>Scenery</button>

	   
	  Note: The text in the ‘’ is what to use as your data-tag, the text in between the > and </button> is what will actually show up on the page as your label


	Creating a Letter + Tag Template

	<div class="letter" data-tags=“love scenery”>
         <h2>Letter 3</h2>
         <p>Aliquam et enim sed neque dignissim porttitor.</p>
      </div>


	Note: This snippet uses the tags love and scenery. Make sure that in data-tags the text used is the text written in the ‘’ and not the text that would show on the webpage after the >. You do not need to use commas or hyphens in between each tag, just spaces


	Blank Alumni Page Code with Example Tags

	Note: You can edit the CSS and any other part of this as needed

		
		
<div class="letter">
    <div class="letter-item" data-tags="tag1 tag2">Letter 1</div>
    <div class="letter-item" data-tags="tag2 tag3">Letter 2</div>
    <div class="letter-item" data-tags="tag1 tag3">Letter 3</div>
</div>

<button onclick="filterLetters('tag1')">Tag 1</button>
<button onclick="filterLetters('tag2')">Tag 2</button>
<button onclick="filterLetters('tag3')">Tag 3</button>

<script>
function filterLetters(tag) {
    var letters = document.getElementsByClassName("letter-item");
    for (var i = 0; i < letters.length; i++) {
        var tags = letters[i].dataset.tags.split(" ");
        if (tags.includes(tag)) {
            letters[i].classList.remove("hidden");
        } else {
            letters[i].classList.add("hidden");
        }
    }
}
</script>

<style>
.hidden {
    display: none;
}
</style>


</body>
</html>

	
	



