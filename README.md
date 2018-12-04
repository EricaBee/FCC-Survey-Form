# FCC-Survey-Form
FreeCodeCamp Responsive Web Design Project #2
<!DOCTYPE html>
<html>
<head>
<style>
@import url(https://fonts.googleapis.com/css?family=Raleway:400,500);

html,
body {
  background-color: #CCCCFF;
  text-align: center;
  font-family: 'Raleway', Helvetica, sans-serif;
  min-width: 320px;
}

header {
  font-size: 2em;
  font-weight: bold;
  margin: 20px;
}

#form-outer {
  background-color: rgb(250, 250, 250);
  margin: 0 auto;
  border-radius: 4px;
  width: 75%;
  max-width: 900px;
  padding: 10px;
  padding-top: 20px;
}

.labels {
  display: inline-block;
  text-align: right;
  width: 40%;
  padding: 5px;
  vertical-align: top;
  margin-top: 10px;
}

.rightTab {
  display: inline-block;
  text-align: left;
  width: 48%;
  vertical-align: middle;
}

.input-field {
  height: 20px;
  width: 280px;
  padding: 5px;
  margin: 10px;
  border: 1px solid #c0c0c0;
  border-radius: 2px;
}

#userAge {
  width: 40px;
}

.userRatings,
input[type="checkbox"] {
  float: left;
  margin-right: 5px;
}

#submit {
  background-color: #9999FF	;
  border-radius: 4px;
  color: white;
  font-size: 1em;
  height: 40px;
  width: 96px;
  margin: 10px;
  border: 0px solid;
}

.dropdown {
  height: 35px;
  width: 140px;
  padding: 5px;
  margin: 10px;  
  margin-top: 15px;
  border: 1px solid #c0c0c0;
  border-radius: 2px;
}

.radio, .checkbox {
  position: relative;
  left: -43px;
  margin-left: 10px;
  display: block;
  padding-bottom: 10px;
}

@media screen and (max-width: 833px) {
  .input-field {
    width: 80%;
  }
  select {
    width: 90%;
  }
}

@media screen and (max-width: 520px) {
  .labels {
    width: 100%;
    text-align: left;
  }
  .rightTab {
    width: 80%;
    float: left;
  }
  .input-field {
    width: 100%;
  }
  select {
    width: 100%;
  }
}
</style>

<h1 id="title">Survey Form</h1>
<div id="form-outer">
  <p id="description">
    Let Erica know how she can improve her Instagram page for her food creations.
  </p>
  <form id="survey-form" method="GET" action="https://crossorigin.me/https://freecodecamp.com">
    <div class="rowTab">
      <div class="labels">
        <label id="name-label" for="name">* Name: </label>
      </div>
      <div class="rightTab">
        <input autofocus type="text" name="name" id="name" class="input-field" placeholder="Enter your name" required>
      </div>
    </div>
    <div class="rowTab">
      <div class="labels">
        <label id="email-label" for="email">* Email: </label>
      </div>
      <div class="rightTab">
        <input type="email" name="email" id="email" class="input-field" required placeholder="Enter your Email">
      </div>
    </div>
     <div class="rowTab">
      <div class="labels">
        <label id="name-label" for="name">* Instagram: </label>
      </div>
      <div class="rightTab">
        <input autofocus type="text" name="name" id="name" class="input-field" placeholder="@instagram handle" required>
      </div>
    </div>
    <div class="rowTab">
      <div class="labels">
        <label id="number-label" for="age">* Age: </label>
      </div>
      <div class="rightTab">
        <input type="number" name="age" id="number" min="1" max="125" class="input-field" placeholder="Age">
      </div>
    </div>
    <div class="rowTab">
      <div class="labels">
        <label for="currentPos">How often do you use Instagram?</label>
      </div>
      <div class="rightTab">
        <select id="dropdown" name="currentPos" class="dropdown">
      <option disabled value>Select an option</option>
      <option  value="never">Never</option>
      <option value="job">1x per month</option>
      <option value="learner">1x per week</option>
      <option value="preferNo">1x per day</option>
      <option value="other">Multiple times per day</option>
    </select>
      </div>
    </div>
    <div class="rowTab">
      <div class="labels">
        <label for="userRating">* How often do you use Instagram to look at food related content?</label>
      </div>
      <div class="rightTab">
        <ul style="list-style: none;">
          <li class="radio"><label>Daily<input name="radio-buttons" value="1"  type="radio" class="userRatings" ></label></li>
          <li class="radio"><label>Weekly<input name="radio-buttons" value="2"  type="radio" class="userRatings" ></label></li>
          <li class="radio"><label>Monthly<input name="radio-buttons" value="3"  type="radio" class="userRatings" ></label></li>
          <li class="radio"><label>Never<input name="radio-buttons" value="4"  type="radio" class="userRatings" ></label></li>
        </ul>
      </div>
    </div>
    <div class="rowTab">
      <div class="labels">
        <label for="most-like">What is your favorite type of content on Instagram? </label>
      </div>
      <div class="rightTab">
        <select id="most-like" name="mostLike" class="dropdown">
      <option disabled selected value>Select an option</option>
      <option value="motivation&positivity">Motivation & Positivity</option>
      <option value="foodInspiration">Food Inspiration</option>
      <option value="community">Community</option>
      <option value="workouts">Workouts</option>
      <option
value="beauty">Beauty</option>
          <option value="travel">Travel</option>
          <option 
                  value="other">Other</option>
    </select>
      </div>
    </div>
    <div class="rowTab">
      <div class="labels">
        <label for="preferences">Things you look for in food instagram pages<br>(Check all that apply): </label>
      </div>
      <div class="rightTab">
        <ul id="preferences" style="list-style: none;">
          <li class="checkbox"><label><input name="prefer" value="1" type="checkbox" class="userRatings">Appeal of Food Photo</label></li>
          <li class="checkbox"><input name="prefer" value="2" type="checkbox" class="userRatings">Recipe Included </li>
          <li class="checkbox"><label><input name="prefer" value="3" type="checkbox" class="userRatings">Vegan</label></li>
          <li class="checkbox"><label><input name="prefer" value="4" type="checkbox" class="userRatings">Vegetarian</label></li>
          <li class="checkbox"><label><input name="prefer" value="5" type="checkbox" class="userRatings">Healthy</label></li>
          <li class="checkbox"><label><input name="prefer" value="6" type="checkbox" class="userRatings">Easy to Make</label></li>
          <li class="checkbox"><label><input name="prefer" value="7" type="checkbox" class="userRatings">To Share With Others</label></li>
          <li class="checkbox"><label><input name="prefer" value="8" type="checkbox" class="userRatings">Decadence</label></li>
          <li class="checkbox"><label><input name="prefer" value="9" type="checkbox" class="userRatings">Lots of Likes</label></li>
        
      </div>
    </div>
    <div class="rowTab">
      <div class="labels">
        <label for="comments">Any Comments or Suggestions?</label>
      </div>
      <div class="rightTab">
        <textarea id="comments" class="input-field" style="height:50px;resize:vertical;" name="comment" placeholder="Enter your comment here..."></textarea>
      </div>
    </div>
    <button id="submit" type="submit">Submit</button>
  </form>
</div>
</html>
