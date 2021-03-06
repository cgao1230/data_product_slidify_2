---
title       : BMI calculator
subtitle    : my first shiny app        
author      : Cheng Gao 
job         : Graduate student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, shiny,interactive,bootstrap,quiz]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## What is BMI?

* BMI is short for Body Mass Index. It is a meausre of relative weight based on an individual'smass and height.
* It has formula (in metric) $$ BMI=mass(kg)/(height(m)^2) $$
or the formula can be expressed in standard measure $$ BMI=mass(lbs)/(height(inch)^2) $$
*Just for your reference 1 feet = 12 inches

--- 

## Categories of BMI
A frequent use of the BMI is to assess how much an individual's body weight departs from what is normal or desirable for a person of his or her height. There are variety of standards for categories of BMI. In this BMI calculator app, we use,
* less than 18.5: underweight
* greater than 18.5 and less than 24.9: normal
* greater than 24.9 and less than 30.0: overweight
* greater than 30.0: obesity

---

## What does BMI calculator provide?
* allows users to input her or his weight and height
* allows users to choose weight unit and height unit
* verifies users' inputs
* gives BMI value
* gives BMI category

--- 

## What does it work?
<div class="row-fluid">
  <div class="span4">
    <form class="well">
      <label for="weight">Weight</label>
      <input id="weight" type="number" value="1"/>
      <label class="control-label" for="wt_unit">Weight unit</label>
      <select id="wt_unit"><option value="lbs" selected>lbs</option>
<option value="kgs">kgs</option></select>
      <script type="application/json" data-for="wt_unit" data-nonempty="">{}</script>
      <label for="height">Height</label>
      <input id="height" type="number" value="1"/>
      <label class="control-label" for="ht_unit">Height unit</label>
      <select id="ht_unit"><option value="inches" selected>inches</option>
<option value="m">m</option></select>
      <script type="application/json" data-for="ht_unit" data-nonempty="">{}</script>
    </form>
  </div>
  <div class="span8">
    <h4>You can enter weight and height under the correct measure.</h4>
    <h4>Here is the link for the interactive shiny app. https://chenggao.shinyapps.io                        /Data_product/.</h4>
  </div>
</div>

If you enter weight 200 lbs and height 72 inches, you will get BMI 

```r
200 * 703/(72 * 72)
```

```
## [1] 27.12
```

and the BMI category is overweight based on the previous standard.













