Introduction
============

Our project looks at contributions to political campaigns by members of
various institutions in the states of New York, Ohio, and Texas. Using
an interactive map, our project compares the party leanings of these
donations in comparison to the regions in which the institutions reside.
We selected a handful of institutions in each state that were diverse in
terms of size, location (urban vs. rural), and regional political
affiliation. The state of New York serves as an overwhelmingly
Democratic state, while Texas serves as a Republican state and Ohio
serves as a swing state.

Why should anyone care about this?
==================================

There is a commonly-held belief that institutions are heavily liberal,
so we hope to explore whether or not this is true by doing a deep dive
into political donations. Futhermore, we thought it would be interesting
to see whether the truth of this assumption depends on the political
environment geographically surrounding a given institution. We were
motivated by many political controversies on our own campus in recent
years, such as the Amherst Uprising, the defunding of the Amherst
Republicans Club, and the publication of the Office of Diversity and
Inclusion’s Common Language Guide.

We quantified the political identity of institutions by exploring which
campaigns and candidates they donate too. We know that since we only
looked at the donation habits of the employees at the college, this is
just an estimate of the true political identity of an instution.

Data Sources
============

### 2016/2017 College Scorecard Data

-   Obtained from:
    <a href="https://collegescorecard.ed.gov/data/" class="uri">https://collegescorecard.ed.gov/data/</a>

### FEC Campaign Financing, Budgeting, and Spending Data

-   Publicly Accessible by anyone at:
    <a href="https://www.fec.gov/data/receipts/individual-contributions/?two_year_transaction_period=2020&amp;min_date=01%2F01%2F2019&amp;max_date=12%2F31%2F2020" class="uri">https://www.fec.gov/data/receipts/individual-contributions/?two_year_transaction_period=2020&amp;min_date=01%2F01%2F2019&amp;max_date=12%2F31%2F2020</a>
-   This dataset is readily downloaded as a csv from the ‘export’
    function on the website.

### Ballotpedia

-   A digital encyclopedia of American politics and elections run by a
    nonpartisan nonprofit organization.
-   Used to manually classify donations from FEC data (above) as
    democratic, republican, nonpartisan, or 3rd party

### 2016 County Level Census Data (from BigQuery)

-   Google’s Big Query provides a public dataset regarding US Census
    information on demographics, populations, etc. in certain years on a
    year by year basis that can be accessed from the link below:
-   <a href="https://console.cloud.google.com/bigquery?project=bigquery-public-data&amp;p=bigquery-public-data&amp;d=census_bureau_acs&amp;t=county_2016_1yr&amp;page=table" class="uri">https://console.cloud.google.com/bigquery?project=bigquery-public-data&amp;p=bigquery-public-data&amp;d=census_bureau_acs&amp;t=county_2016_1yr&amp;page=table</a>

### 2016 State Level Census Data (from BigQuery)

-   Google’s Big Query provides a public dataset regarding US Census
    information on demographics, populations, etc. in certain years on a
    year by year basis that can be accessed from the link below:
-   <a href="https://console.cloud.google.com/bigquery?project=bigquery-public-data&amp;p=bigquery-public-data&amp;d=census_bureau_acs&amp;t=state_2016_1yr&amp;page=table" class="uri">https://console.cloud.google.com/bigquery?project=bigquery-public-data&amp;p=bigquery-public-data&amp;d=census_bureau_acs&amp;t=state_2016_1yr&amp;page=table</a>
-   <a href="https://console.cloud.google.com/bigquery?project=bigquery-public-data&amp;p=bigquery-public-data&amp;d=census_bureau_acs&amp;t=state_2016_1yr&amp;page=table" class="uri">https://console.cloud.google.com/bigquery?project=bigquery-public-data&amp;p=bigquery-public-data&amp;d=census_bureau_acs&amp;t=state_2016_1yr&amp;page=table</a>

### US General Election Presidential Results

-   <a href="https://github.com/tonmcg/US_County_Level_Election_Results_08-16" class="uri">https://github.com/tonmcg/US_County_Level_Election_Results_08-16</a>

### County Names and GEOID’s

-   <a href="https://api.census.gov/data/2016/cbp?get=NAICS2012_TTL,GEO_TTL,EMP,LFO_TTL,GEO_ID,ESTAB&amp;for=county" class="uri">https://api.census.gov/data/2016/cbp?get=NAICS2012_TTL,GEO_TTL,EMP,LFO_TTL,GEO_ID,ESTAB&amp;for=county</a>

Variables
=========

### From the College Scorecard Data, we used:

-   Institution Name
-   City
-   State Abbreviation

### From the FEC’s data on individual contributions, we used

-   Contributor Name
-   Recipient (the group or political committee receiving the donation)
-   State (that the contributor resides in)
-   Employer (Institution the donor belongs to)
-   Occupation (of the donor)

### From Ballotpedia, we used:

-   Organization Name
-   Political Affiliation (democratic, republican, nonpartisan, and 3rd
    party)

### From BigQuery’s ‘census\_bureau\_acs’ ‘county\_2016\_1yr’ dataset:

-   GEOID Code
-   Median Income of the County ($)

### From the ‘county\_2018\_1yr’ dataset, we can collect the same type of information as above, except on a state-wide basis

-   GEOID Code
-   Median Income of the County ($)

### From the US General Election Presidential Results we used:

-   Percentage Democratic Votes
-   Percentage Republican Votes
-   State Abbreviation
-   County Name

### From the County Names and GEOID’s dataset, we used:

-   County Name
-   State Name
-   GEOID Code

Results
=======

Our map serves to show how colleges donated and counties voted. The
interactivity allows for one to click on a county or college and view
specific data. We also perused our data a little farther and found a few
interesting caveats. The following analyses explore who is donating, and
how many donations are coming from each of the 28 instiutions.

![](index_files/figure-markdown_strict/unnamed-chunk-7-1.png)

[Click here to see interactivity for Texas](txmap.html)

![](index_files/figure-markdown_strict/unnamed-chunk-8-1.png)

[Click here to see interactivity for New York](nymap.html)

![](index_files/figure-markdown_strict/unnamed-chunk-9-1.png)

[Click here to see interactivity for Ohio](ohmap.html)

### A look at who’s donating

Professors and Researchers were among the top donors in Ohio.

![](index_files/figure-markdown_strict/unnamed-chunk-10-1.png)

Professors and Legal Assisants were among the top donors in Texas.

![](index_files/figure-markdown_strict/unnamed-chunk-11-1.png)

IT Support Associates, professors, and technical writers were among the
top donors in New York.

![](index_files/figure-markdown_strict/unnamed-chunk-12-1.png)

Institutions and Donations
--------------------------

<table>
<caption>Ohio Institutions</caption>
<thead>
<tr class="header">
<th style="text-align: left;">Name</th>
<th style="text-align: right;">Donations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Bowling Green State University</td>
<td style="text-align: right;">898</td>
</tr>
<tr class="even">
<td style="text-align: left;">Kenyon College</td>
<td style="text-align: right;">1139</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Marietta College</td>
<td style="text-align: right;">12</td>
</tr>
<tr class="even">
<td style="text-align: left;">Oberlin College</td>
<td style="text-align: right;">3312</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Ohio State University</td>
<td style="text-align: right;">24609</td>
</tr>
<tr class="even">
<td style="text-align: left;">Ohio Wesleyan University</td>
<td style="text-align: right;">540</td>
</tr>
<tr class="odd">
<td style="text-align: left;">University of Mount Union</td>
<td style="text-align: right;">95</td>
</tr>
<tr class="even">
<td style="text-align: left;">University of Toledo</td>
<td style="text-align: right;">1247</td>
</tr>
</tbody>
</table>

Ohio made over 1,000 individual donations to ACTBLUE (19560), IT STARTS
TODAY (6780), FRIENDS OF SHERROD BROWN (1165), SWING LEFT (1045), and
DCCC (1035).

<table>
<caption>Texas Institutions</caption>
<thead>
<tr class="header">
<th style="text-align: left;">Name</th>
<th style="text-align: right;">Donations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Baylor University</td>
<td style="text-align: right;">2341</td>
</tr>
<tr class="even">
<td style="text-align: left;">Dallas Baptist University</td>
<td style="text-align: right;">168</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Lamar University</td>
<td style="text-align: right;">373</td>
</tr>
<tr class="even">
<td style="text-align: left;">Southern Methodist University</td>
<td style="text-align: right;">3231</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Texas AM University</td>
<td style="text-align: right;">49</td>
</tr>
<tr class="even">
<td style="text-align: left;">Texas Tech University</td>
<td style="text-align: right;">3624</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Texas Woman’s University</td>
<td style="text-align: right;">222</td>
</tr>
<tr class="even">
<td style="text-align: left;">Trinity University</td>
<td style="text-align: right;">926</td>
</tr>
<tr class="odd">
<td style="text-align: left;">University of Texas at El Paso</td>
<td style="text-align: right;">1043</td>
</tr>
<tr class="even">
<td style="text-align: left;">University of Texas at Rio Grande Valley</td>
<td style="text-align: right;">42</td>
</tr>
</tbody>
</table>

Texas made over 500 individual donations ACTBLUE (9538), BETO FOR TEXAS
(794), and SWING LEFT (779).

<table>
<caption>New York Institutions</caption>
<thead>
<tr class="header">
<th style="text-align: left;">Name</th>
<th style="text-align: right;">Donations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Adelphi University</td>
<td style="text-align: right;">1139</td>
</tr>
<tr class="even">
<td style="text-align: left;">Cornell University</td>
<td style="text-align: right;">28210</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Elmira College</td>
<td style="text-align: right;">108</td>
</tr>
<tr class="even">
<td style="text-align: left;">Hamilton College</td>
<td style="text-align: right;">2027</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Molloy College</td>
<td style="text-align: right;">291</td>
</tr>
<tr class="even">
<td style="text-align: left;">Rensselaer Polytechnic Institute</td>
<td style="text-align: right;">672</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Roberts Wesleyan College</td>
<td style="text-align: right;">10</td>
</tr>
<tr class="even">
<td style="text-align: left;">SUNY Canton</td>
<td style="text-align: right;">63</td>
</tr>
<tr class="odd">
<td style="text-align: left;">SUNY Geneseo</td>
<td style="text-align: right;">1047</td>
</tr>
<tr class="even">
<td style="text-align: left;">United States Military Academy</td>
<td style="text-align: right;">52</td>
</tr>
</tbody>
</table>

New York made over 500 individual donations ACTBLUE (15467), IT STARTS
TODAY (14089), SWING LEFT (710), and DCCC (500).

Analysis
========

Our analyses involved a few subjective decisions. To classify the
political leaning each of the 386 FEC committees, we used the
nonpartisan website ballotpedia. To classify a counties leaning, we
looked at the 2016 election results. We computed the difference in % of
Democratic Votes and % of Republican Votes and this supported the color
scale seen in our maps. To classify the institutions as a Democratic or
Repubican donating majority, we took looked at the difference in %
donations going to Democratic committees - Repubican committees. We
decided that a 50/50 donation cutoff would not be a durable estimate, so
our threshold was greater than 60% donations to one party.

Future Work
-----------

Although our work provides interesting and important insight to the
political leanings of institutions of higher education, our work only
scratches the surface of a very complex investigation. Our study was
limited in that only 8-11 institutions per state were included, and only
3 states were explored. Furthermore, we classify the “political
affiliation” of an institution by the percentage of donations given to
Democratic and/or Republican campaigns. We recognize that this may not
necessary holistically represent the political affiliation of the
institution as a whole, but we believe that it is a good way to classify
institutions (especially since voting records are not public
information). In the future, this project could be extended to more
states and more institutions so that a more complete investigation could
be done. With more time (as we had to manually look up each committee
donation), more institutions could be classified. With a larger amount
of data, statistical analysis of the percentage of donations going to
republican or democratic in comparison to an institution’s region could
be possible, leading to a statistically valid conclusion (rather than
anecdotal).

Conclusion
==========

Our primary goal was to explore whether or not the political affiliation
of the region surrounding an institution had an effect on the political
leanings of that institution. We also wanted to explore the general
claim that institutions of higher education are usually liberal leaning.
Although there are limitations to our study (to be discussed further),
we found that all of the colleges we investigated were Democratic.
Furthermore, we found the political affiliation of the region in which
an institution resides to have no effect on the political affiliation of
the majority of the members of the institution. Since all the
institutions’ donations were majority Democratic, we explored whether
the political affiliation of the region affected the percentage of
Democratic donations–– we found the region’s political affiliation to
have similarly no effect on the percentage of donations that were
Democratic.
