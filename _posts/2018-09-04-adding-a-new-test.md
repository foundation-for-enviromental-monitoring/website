---
title: Adding a new test to the suite
date: 2018-09-04
author: Samuel Rajkumar
layout: posts
---
[Bubble Nut Wash](http://bubblenutwash.com/) is a social enterprise based out of Bangalore. They make environment-friendly detergents and home-care cleaning products from [soapnuts](https://en.wikipedia.org/wiki/Sapindus). The enterprise intends to use water test kits developed by ffem to compare parameters of after-wash waste water using synthetic detergents vis-á-vis soapnut-based detergents. When Manas, the cofounder, asked if our kit could test for Hydrogen Peroxide, I was tempted to say no. I am glad I did not, because what followed turned out to be a textbook example of how to add a new parameter to the [ffem water test kit]({{ site.url }}/water/).

<a href="http://bubblenutwash.com"><img src="{{ site.url }}/assets/images/bubblenutwash_logo.png" alt="Bubble Nut Wash"></a>

Perhaps I am still stuck in the past where we used to think of every new parameter as a new feature, while what we have now is a system where adding a new parameter should be analogous to writing a blog post on, say, WordPress. Quite distinct from adding a feature to WordPress. Of course, the first question to ask before one writes a blog post is if the content lends itself to being addressed in such a format. In our case, we needed to find if a suitable colorimetric test exists for Hydrogen Peroxide, one that would lend itself to be used by our method.

Enter [A colorimetric method for rapid and selective quantification of mixtures comprising peroxodisulfate, peroxomonosulfate and hydrogen peroxide](http://www.rsc.org/suppdata/c7/re/c7re00050b/c7re00050b1.pdf) by Benjamin. J. Deadman, Klaus Hellgardt and King Kuok (Mimi) Hiia. This paper lists a number of methods to measure Hydrogen Peroxide. Of interest to us is "TiOSO<sub>4</sub> Redox Colorimetry Test for Hydrogen Peroxide Concentration" which is a colorimetric way of measuring Hydrogen Peroxide, and looks to be well suited for our method, as this image from the paper shows. The vials show reagent mixed with standard solutions of H<sub>2</sub>O<sub>2</sub>, starting with 0 on the left and 1M on the extreme right, with intermediate concentrations in between.

<img src="{{ site.url }}/assets/images/h2o2_test_colour.jpg" alt="h202 test colours">

Preparing the reagent is well documented in the paper, and so it was a matter of a few hours before we got a good answer if the test is good enough with the ffem method of smartphone based colorimetry. Below is a calibration screen for the Hydrogen Peroxide test.

<img src="{{ site.url }}/assets/images/h2o2_calibration.png" alt="h2o2 calibration colours">

The calibration screen above shows progressive colour values from 0 M to 1 M. With ffem tests, we treat RGB colours as points in 3D space, and the difference between 2 calibration points is the [Euclidean distance](https://en.wikipedia.org/wiki/Euclidean_distance). The value that is of most value to us is 'd', representing the Euclidean distance between two succeeding calibration points. The larger the 'd', the better the test. Typically, 'd' values of 20 represent a good enough test. The 'd' values here of 0, 134, 30, 121, and 25 signify that this is indeed a good test.

Tests with lab mixed samples give excellent results.

<table>
  <tr>
    <th>H<sub>2</sub>O<sub>2</sub> Standards (M)</th>
    <th>ffem results (M)</th>
  </tr>
  <tr>
    <td>0.0</td>
    <td>0.0</td>
  </tr>
  <tr>
    <td>0.05</td>
    <td>0.06</td>
  </tr>
  <tr>
    <td>0.10</td>
    <td>0.13</td>
  </tr>
  <tr>
    <td>0.5</td>
    <td>0.5</td>
  </tr>
  <tr>
    <td>1.0</td>
    <td>1.0</td>
  </tr>
</table>

Having delivered this test to Bubble Nut Wash, we hope this will come in handy saving our city from its menace of [frothing and burning lakes](https://www.theguardian.com/cities/2017/mar/01/burning-lakes-experts-fear-bangalore-uninhabitable-2025).
