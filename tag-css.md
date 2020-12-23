# Markdown Tag with CSS

## Tags overview

### Navigation (NAV)

<span class="tt nav">
  <p class="area">NAV</p>
  <p class="element">ELEMENT</p>
  <p class="desc">STATUS</p>
</span>

---
### Process (WAIT)

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

<span class="tt ok">
  <p class="area">IS</p>
  <p class="desc">desc</p>
</span>

<span class="tt error">
  <p class="area">IS</p>
  <p class="desc">desc</p>
</span>

---
### Test Result (SHOULD)

<span class="tt should">
  <p class="area">should</p>
  <p class="desc">desc</p>
</span>


# Examples

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

--- 

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
