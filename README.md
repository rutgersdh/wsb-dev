# wsb-dev
 
I. Adding a Card

	Add the following code template after each card’s </div>. Make sure that the code below is not copied into another alumni card’s <div> otherwise the page will not look as intended.

	Card Code Template
 ```
      <div class="card"> 
        <a href = “LINK TO PAGE“>
        <img src=“REPLACE WITH IMAGE LINK“ alt=“REPLACE WITH ALT IMAGE NAME>
        <h3 style = "text-align: center" >REPLACE WITH ALUMNI NAME</h3>
        <p>REPLACE WITH ALUMNI DESCRIPTION</p>
        </a>
      </div>
```

II. Adding Tags to Letter

	After adding formatting and encoding your letter, you can paste the xml directly to the page and add tags to sort through the letters.

	Tag Creation Template
```
      <button class="tag" onclick="filterTag(‘love’)”>Love</button>
      <button class="tag" onclick="filterTag(‘scenery’)”>Scenery</button>
```
	   
	  Note: The text in the ‘’ is what to use as your data-tag, the text in between the > and </button> is what will actually show up on the page as your label


	Creating a Letter + Tag Template
```
	<div class="letter" data-tags=“love scenery”>
         <h2>Letter 3</h2>
         <p>Aliquam et enim sed neque dignissim porttitor.</p>
      </div>
```

	Note: This snippet uses the tags love and scenery. Make sure that in data-tags the text used is the text written in the ‘’ and not the text that would show on the webpage after the >. You do not need to use commas or hyphens in between each tag, just spaces


	Blank Alumni Page Code with Example Tags

	Note: You can edit the CSS and any other part of this as needed

```		
<?xml version="1.0" encoding="UTF-8"?><html xmlns="http://www.w3.org/1999/xhtml">
    <head>
       <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
   <style>

h1 {
  font-family: "Arial", "Lucida Console", "Courier New";
}

h2 {
  font-family: "Arial", "Lucida Console", "Courier New";
}

h4 {
  font-family: "Arial", "Lucida Console", "Courier New";
}

p {
  font-family: "Times New Roman", Times, serif;
  line-height: 1.25;
  font-size:18px;
}


      .tag {
         cursor: pointer;
         color: blue;
         text-decoration: underline;
      }
      .hidden {
         display: none;
      }

                     
                      .tooltip {
                     display:inline-block;
                     position:relative;
                     border-bottom:1px dotted #666;
                     text-align:left;
                     }
                     
                     .tooltip .top {
                     min-width:200px; 
                     top:-20px;
                     left:50%;
                     transform:translate(-50%, -100%);
                     padding:10px 20px;
                     color:#444444;
                     background-color:#EEEEEE;
                     font-weight:normal;
                     font-size:13px;
                     border-radius:8px;
                     position:absolute;
                     z-index:99999999;
                     box-sizing:border-box;
                     box-shadow:0 1px 8px rgba(0,0,0,0.5);
                     display:none;
                     }
                     
                     .tooltip:hover .top {
                     display:block;
                     }
                     
                     .tooltip .top i {
                     position:absolute;
                     top:100%;
                     left:50%;
                     margin-left:-12px;
                     width:24px;
                     height:12px;
                     overflow:hidden;
                     }
                     
                     .tooltip .top i::after {
                     content:'';
                     position:absolute;
                     width:12px;
                     height:12px;
                     left:50%;
                     transform:translate(-50%,-50%) rotate(45deg);
                     background-color:#EEEEEE;
                     box-shadow:0 1px 8px rgba(0,0,0,0.5);
                     }
                     
                 </style>
   </style>
</head>
<body>
   <div style = "text-align: center">
   <h1> Alumni Name </h1>
<p> edited by [Name]</p>
   <p>Mss: https://doi.org/doi:10.7282/T3DF6TXM </p>
   <div id="tags">
      <p >Tags:</p>
      <button class="tag" onclick="filterTag('all')">All</button>
      <button class="tag" onclick="filterTag('isolation')">Isolation</button>
      <button class="tag" onclick="filterTag('personal')">Personal Relationships</button>
      <button class="tag" onclick="filterTag('combat')">Combat</button>
      <button class="tag" onclick="filterTag('women')">Women</button>
      <button class="tag" onclick="filterTag('scenery')">Scenery</button>
   </div>
   <div id="letters">
      <div class="letter" data-tags="all isolation">
         <hr />
         <h2> Letter 1</h2>
         <p> Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit...</p>
      </div>
      <div class="letter" data-tags="all combat scenery">
         <h2>Letter 2</h2>
         <p>Nulla facilisi. Ut pretium ante id velit malesuada, ac convallis magna suscipit.</p>
      </div>
      <div class="letter" data-tags="all women personal">
         <h2>Letter 3</h2>
         <p>Aliquam et enim sed neque dignissim porttitor.</p>
      </div>
   </div>
</div>
   <script>
      function filterTag(tag) {
         // Hide all letters
         var letters = document.getElementsByClassName("letter");
         for (var i = 0; i < letters.length; i++) {
            letters[i].classList.add("hidden");
         }
         // Show letters with selected tag
         var selectedLetters = document.querySelectorAll('[data-tags~="' + tag + '"]');
         for (var i = 0; i < selectedLetters.length; i++) {
            selectedLetters[i].classList.remove("hidden");
         }
      }
   </script>

</body>
</html>
```
	
	



