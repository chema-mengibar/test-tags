# Test tags

## Context

When creating an application it is always convenient to test the possible actions of the user and to be able to be sure that our application works correctly in all the variants.

This testing process starts mainly with the definition of the different cases or scenarios, the corresponding steps that a user would perform and the description of how the application is expected to react. 
If the behaviour of the application was not as expected during the execution of the tests
The current behaviour is also described, so that we can compare how it really is and how it should be.

This description is the means of communication between developer and tester, as it helps them:
- define what the application should and should not do
- reproduce the scenarios several times and check that they work correctly
- get an overview of the status of the application and identify faults


## About this framework

Test-tag decomposes and groups the elements found in an application and establishes a tag for each element that allows it to be quickly identified.

These tags are in turn made up of 3 parts:
1. type
2. subject
3. predicate

The tags are in short a syntax minimalization that allows to write sentences / test cases in an abbreviated way.

## Areas

According to the elements that we find when visualizing a web in the browser, it is possible to create groups according to their characteristics and relationship with the user.

![google-example](./assets/img/Brownie-GoogleSearch.png)

The main areas are:

### Navigation

Browser-specific navigation elements.

- Browser Back
- Reload
- Url + Manipulation
- Browser scroll
- History
  
<img src="./assets/img/areas-nav-filled.jpg" width="400px">

### Context

Entities saved in the browser or the application, not always directly visible.

- Cookies
- User
- Session
- Basket
  
<img src="./assets/img/areas-context-filled.jpg" width="400px">


### User interaction

It groups all the elements with which the user can interact.

- click, hover
- scroll
- keyboard / mobile
  - enter
- links / buttons
- inputfelder
- clickable elementen:
  - images
  
<img src="./assets/img/areas-ui-filled.jpg" width="400px">


### Visual elements

All the relevant visual elements (not clickable)

- Text
- Icons
- Grouped elements
- ...
  
<img src="./assets/img/areas-visual-filled.jpg" width="400px">


## Tags overview

### Navigation (NAV)

<span class="tt nav">
  <p class="area">NAV</p>
  <p class="element">ELEMENT</p>
  <p class="desc">STATUS</p>
</span>

---
### Process (WAIT)

Describe a waiting process for tester/user
- redirects
- loading

<span class="tt wait">
  <p class="area">wait</p>
  <p class="desc">status</p>
</span>

---
### Context (CTX)

<span class="tt ctx">
  <p class="area">ctx</p>
  <p class="element">element</p>
  <p class="desc">status</p>
</span>

---
### User Interaction (UI)

<span class="tt ui">
  <p class="area">ui</p>
  <p class="element">element</p>
  <p class="desc">action</p>
</span>

---
### Visual Elements (VIS)

<span class="tt vis">
  <p class="area">vis</p>
  <p class="element">element</p>
  <p class="desc">status</p>
</span>

---
### Test Result (IS: error, ok )

Describes the result status of the test

<span class="tt ok">
  <p class="area">IS</p>
  <p class="desc">desc</p>
</span>

<span class="tt error">
  <p class="area">IS</p>
  <p class="desc">desc</p>
</span>

---
### Test Result ( SHOULD )

Describes the expected status of the test
<span class="tt should">
  <p class="area">should</p>
  <p class="desc">desc</p>
</span>


<style>

.tt{
  display:inline-block;
  border-radius: 4px;
  padding: 2px 5px;
  background-color: grey;
  font-size:10px;
  line-height:12px;
}

.tt.wait{
  background-color: #cccccc;
  color: black;
}

.tt.nav{
  background-color: #eb8934;
  color: black;
}

.tt.ctx{
  background-color: #bfafa1;
  color: black;
}

.tt.ui{
  background-color: #1687d9;
  color: white;
}

.tt.vis{
  background-color: #f7e23e;
  color: black;
}

.tt.ok{
  background-color: #15b345;
  color: black;
}

.tt.error{
  background-color: #f00707;
  color: white;
}

.tt.should{
  background-color: #000000;
  color: white;
}

.tt p{
  display: inline;
}

.tt p.area, .tt p.element{
  text-transform: uppercase;
}

.tt p.desc, .tt p.element{
  font-style: italic;
}

.tt p:not(:last-child)::after{
  display: inline;
  content:'|';
  margin: 0 2px;
}

</style>


# Usage Examples

**Test case:**  
Redirect action in Google logo in the the "search-results" Page.

**Test tags:**

<span class="tt nav">
  <p class="area">NAV</p>
  <p class="element">url-bar</p>
  <p class="desc">insert "google.com"</p>
</span>
<span class="tt ui">
  <p class="area">UI</p>
  <p class="element">search-field</p>
  <p class="desc">search "brownie"</p>
</span>
<span class="tt wait">
  <p class="area">wait</p>
  <p class="desc">search results page</p>
</span>
<span class="tt ui">
  <p class="area">ui</p>
  <p class="element">google-logo</p>
  <p class="desc">click</p>
</span>
<span class="tt error">
  <p class="area">IS</p>
  <p class="desc">remain in search page</p>
</span>
<span class="tt should">
  <p class="area">should</p>
  <p class="desc">redirect to start page</p>
</span>

# Integration in your project

This method is only a convention with a reduced syntax. Adapt this syntax according to the tool you have available for your project.

- Wikis
- Readme
- Reports

## Conventions

### Tag colors palette
Define your custom palette if needed.  
Respects basic colours such as red and green and their association and meaning of success or error.

### Elements Ids
It is important to assign unique identifiers to the elements.
Define a convention for the name of the ids, which you may be able to apply to other parts of the project such as automated tests.


## List of elements

Define the main list of elements of your application and make it accessible to all stakeholders, so that they can easily copy and paste it to create test cases more quickly and uniformly.
It is impossible to create a list of absolutely all the elements of the project. It is important to define which ones are relevant for quality assurance.

## Inspiration an To-dos
:)


