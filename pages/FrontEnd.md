- CSS
  heading:: true
	- How to have responsive gaps in grid layout
	  heading:: true
		-
		-
		- ```css
		  .container {
		    display: grid;
		    grid-template-columns: 1fr 1fr;
		    grid-column-gap: 10%;
		    grid-row-gap: 11.1%;
		    padding-bottom: 10%;
		    background-color: black;
		  }
		  
		  .pic {
		    padding-bottom: 100%;
		    background-size: contain;
		    background-repeat: no-repeat;
		    background-image: url(https://via.placeholder.com/512);
		  }
		  ```
		- ```html
		  <div class="container">
		    <div class="pic"></div>
		    <div class="pic"></div>
		    <div class="pic"></div>
		    <div class="pic"></div>
		  </div>
		  ```
		- This question Grid gap percentage without height explains why the problem occurs. It helped me to find the following solution: Instead of setting grid-gap, set grid-column-gap and grid-row-gap separately, with grid-row-gap equal to grid-column-gap / (1 - grid-column-gap). Set padding-bottom of the container equal to grid-column-gap. For example: if grid-column-gap is 0.1 (10%), then grid-row-gap is 0.1 / (1 - 0.1) or 0.1111 (11.1%) This works for any percentage value of grid-column-gap.
		-
- Library
  heading:: true
- React
  heading:: true
- Javascript