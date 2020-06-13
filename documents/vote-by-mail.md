<!-----
Copy and paste the converted output.

NEW: Check the "Suppress top comment" option to remove this info from the output.

Conversion time: 5.459 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β26
* Sat Jun 13 2020 11:20:55 GMT-0700 (PDT)
* Source doc: White Paper: Vote by Mail
* Tables are currently converted to HTML tables.
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!


WARNING:
You have 13 H1 headings. You may want to use the "H1 -> H2" option to demote all headings by one level.

----->

# White Paper: Vote by Mail

**_Absentee Voting Solutions for 2020 and Beyond_**

*   Sean Roberts, Chief Technologist at Lincoln Network
*   Alexiaa Jordan, Policy Analyst for Innovation, Cyber, and National Security Policy at Lincoln Network

---

# Foreword 

The Lincoln Network’s mission is to connect Silicon Valley and other technology hubs with national policymakers to create a freer and more secure future. We believe in a world of free markets and free people, and that fostering a robust but responsible innovation ecosystem is crucial to creating a better, freer, and more abundant future. Our cyber and national security team focuses on identifying ways that technology and innovation can address major challenges facing the United States and the world. 

In 2020, one of the most significant challenges facing the nation is to hold a democratic election during a pandemic, at a time of heightened international competition including growing cybersecurity threats.

This working paper is the beginning of Lincoln Network’s long-term, inter collaborative project to galvanize collaboration between engineering and policy circles to address our, very dire, election security issues. Our big idea is to create a better job and products market whereby states and innovators come together to choose the best inventions for their state and increase our countries collective security. This big idea starts with writing a quantitative, straight-forward paper on election security issues. Thus far, this paper has been shared narrowly with various engineers to think about ideas such as how to make e-poll books safer to improve baseline network security or how geo-fencing could be easily used to improve voter experience and decentralization in-person voting amidst COVID-19. We will be sharing this paper with various policy circles to begin the process of open-source collaboration. This is a living document and there are issues we plan on covering in future revisions. As our collaboration increases, we look forward to shaping this paper to further fill missed considerations.




# Executive Summary

Defending American elections from cybersecurity threats and potential foreign interference has been a bipartisan, national priority since 2016. National policymakers, led by the Department of Homeland Security and Election Assistance Commission, have promoted a nonpartisan and intergovernmental effort to improve the security and resiliency of state and local election systems. Congress and the Trump Administration have authorized and provided more than $1 billion in new funding to states to modernize and secure election infrastructure. 

A focus of this national project has been to protect state and local governments and election infrastructure from potential cybersecurity threats. But few envisioned our current challenge—holding a national election during a pandemic. 

The COVID-19 pandemic has led to more than 100,000 deaths across the United States and widespread economic devastation. The pandemic also disrupted American democracy: delaying at least 16 state primary elections since March.[^1] Washington, DC and several states holding primary elections in early June experienced problems including long wait times as voters had fewer options to vote in person and many did not receive absentee ballots.[^2] 

But the November election must move forward. National, state, and local policymakers are currently making plans for holding the election on November 3rd while assuming that the pandemic persists. State election directors and local election administrators are quickly adjusting plans to prepare to hold the election at a time when public health may require social distancing and other precautions.

In 2018, 1 in 4 American voters cast their ballots by mail.[^3] Many states are considering ways to expand absentee voting or Voting-by-Mail (VBM). American voters have historically had the opportunity to use absentee voting to cast their ballot if they are unable to vote in person on election day due to specific circumstances. More than 30 states have offered no excuse “voting-by-mail” as an option for all voters. During the pandemic, 46 states are offering absentee balloting for all voters. Recent primary elections revealed the risks and challenges of in-person voting during the pandemic, since many poll workers stayed home and voters were forced to wait in long lines. To many, voting by mail is a practical and safe alternative.

But Voting-by-Mail has become the focus of a divisive national political debate by American leaders. President Trump has strongly condemned plans to expand voting-by-mail, warning that doing so will lead to fraud. Senate Democrats have proposed legislation that would require states to offer expanded absentee balloting and voting-by-mail options to all voters. 

This report provides a technical and policy analysis of absentee voting and Voting-by-Mail. Its purpose is to inform the current national debate with an accurate understanding of how voting-by-mail works and a fair analysis of the benefits and risks of voting by mail. The paper includes three sections:

1.	Technical and Policy Overview of Absentee Voting

2.	Discussion of Key Benefits of and Concerns About Absentee Voting  

3.	Technical and Policy Recommendations to Improve Voting Integrity and Absentee Voting

Widespread absentee balloting provides important benefis, including voter convenience, increasing participation, yielding government savings and protecting individual and public health during the pandemic. But absentee voting also comes with real risks, including administrative and voter problems, increasing fraud and ballot harvesting, and creating inequality for individuals with disabilities. Since widespread voting by mail is expected in November, policymakers should take prudent precautions to address these problems. 

This white paper proposes several solutions to improve the integrity of the voting process while expanding access to absentee balloting. This includes establishing and enforcing rules to prevent ballot harvesting, increasing voter confidence in absentee balloting by providing electronic receipts, strengthening oversight of voter registration rolls, and maintaining and improving in-person voting, including to ensure equal access to independent voting for persons with disabilities. Recognizing that states and local election administrators may need additional resources to make these changes, we recommend that state and local governments quickly use available funding to improve election systems and report to Congress on any additional needs.

The decentralized election system of the United States includes and affects more than 3100 counties, 116,000 polling places, 900,000 polling workers, and 150 million registered voters. [^4] Modifying these complex systems during a global pandemic and national election will require a fact-based discussion about pros and cons and a collaborative approach to make changes. This technical and policy analysis is intended to inform this important discussion.  


[TOC]



# 


# I. Technical and Policy Overview of Absentee Voting 

If the COVID-19 pandemic continues in November, public health concerns may require continued social distancing and prohibitions on large gatherings in certain communities. For many voters, going to the polls during the pandemic may be impractical due to individual and public health concerns. Evidence from 2020 primary elections held during the pandemic suggests that fewer poll workers and polling locations are causing longer than usual wait times to vote.[^5]

As the United States prepares for the November 2020 election, many states are exploring options for expanding voting-by-mail and early voting to accommodate voters during the pandemic. One option is to allow early voting, which gives voters the choice to cast their ballot in person at a polling station ahead of election day. Another option is to expand voting-by-mail and absentee balloting.

This section presents an overview and technical analysis of absentee voting and voting by mail. We provide background information on state-by-state absentee ballot and voting-by-mail options. A technical analysis of each step of the absentee voting process and system presents a detailed examination of the system to inform an analysis of strengths and weaknesses and recommendations for improving election integrity.   


## What is Absentee Voting and Voting by Mail?

Many people are using the terms Absentee Voting and Voting by Mail interchangeably. While they are related, each term means something different.  

Absentee voting is the option available to voters in all states and territories to cast a ballot if they cannot vote in person on election day. In general, voters can request an absentee ballot before a certain date and, therefore, can cast their ballot by mail ahead of the election. Common reasons for using absentee ballots include living abroad, planned travel on election day, and serving as an active military member.  Each state has their own rules to define the valid reason(s) for being an absentee voter. Some states allow for permanent absentee designation, while a few others have assigned the entire state population as absentee voters. The important fact is that some voters have valid reasons for not being able to vote in person and most states allow for that voting option.

Voting by Mail is the act of casting a ballot through the mail, rather than by voting in person. Unlike absentee ballot, voting by mail does not require a reason that the voter will be absent or unable to vote in person. There are many other ways of absentee ballots being returned such as a voter dropping the ballot off at an US Post Office, dropping the ballot off at a county voting center, at the voter’s polling place, at a county voting drop box, or in some jurisdictions at the Central Elections Office. Any of these methods could be considered valid depending on the regulations and laws of the city, county, and state. 

For this discussion, we will define Absentee Voting as the act of not voting in person. And vote by mail as using the US Post Office to return an absentee ballot. Some locations use these terms interchangeably or define all not in-person voting as vote by mail due to their specific implementation. 


## Background Information on Absentee Voting 

In the past, absentee voting was used primarily for US citizens traveling overseas and in the active military. The term absentee means literally being absent from your local polling place. Historically, the first use of voting in absentia was for military voters during the Civil War [^6] Throughout the 20th century, most Americans voted in-person at a local polling station[^7], which afforded the benefit of maintaining a secret ballot and prevented vote-buying, coercion, and other problems which became common in the late 1800s.[^8] 

But over the past fifty years, American policies for voting have shifted away from the secret ballot. Writing in 2003, American Enterprise Institute scholars John C. Fortier and Norman J. Orstein discussed this trend: “[T]he country has moved in the direction of convenience voting and away from the traditional polling place and its safeguards. Many election officials have focused their efforts on reducing barriers to voting and as the complications and costs of maintaining numerous election-day polling places for longer hours have risen, have been attracted by the lower administrative costs of absentee voting, vote-by-mail and early voting.”

Expanding absentee voting has become increasingly common over the past decade. In 2014, the bipartisan Presidential Commission on Election Administration reviewed American election systems and presented key recommendations. A top recommendation was to improve access to the polls: “In order to limit congestion on Election Day and to respond to the demand for greater opportunities to vote beyond the traditional Election Day polling place, states that have not already done so should expand alternative ways of voting, such as mail balloting and in-person early voting.”[^9]

  

Many states have heeded this recommendation and other calls for expanded access to the ballot through absentee voting. All states and territories allow absentee voting upon request. But now 33 states and Washington D.C. allow no-excuse (no reason required) absentee voter registration.[^10] Five states (Washington, Oregon, Colorado, Hawaii, Utah) have become permanent vote by mail states. Permanent vote by mail states Each of these states send absentee or vote by mail ballots to every resident of their state without requiring new yearly absentee ballot requests.

The Open Source Election Technology Institute recently reviewed the status of absentee voting and voting-by-mail options across the United States. OSET Institute found that “46 out of 50 states currently offer some form of by-mail voting that is available to _all _voters.”[^11] See Table 1. Moreover, OSET Institute found that the 46 states are nearly evenly divided in political leadership (since “24 states have Democratic governors” and “22 have Republican governors”).[^12]

**Table 1--Current Absentee and Vote-by-Mail Options During the Pandemic, According to OSET Institute**

 


<table>
  <tr>
   <td>States that allow “all by-mail” voting
   </td>
   <td>CO, HI, OR, UT, WA
   </td>
  </tr>
  <tr>
   <td>States that are “heavily” by mail voting 
   </td>
   <td>CA, MT
   </td>
  </tr>
  <tr>
   <td>States that provided “no excuse” by mail voting pre-pandemic
   </td>
   <td>AZ, FL, GA, IA, ID, IL, KS, MD, ME, MI, MN, NC, ND, NE, NJ, NM, NV, OH, OK, PA, RI, SD, VA, VT, WI, WY
   </td>
  </tr>
  <tr>
   <td>States requiring an “excuse” for absentee voting, but relaxed restrictions to include the pandemic as a reason for voting absentee
   </td>
   <td>AL, AR, CT, DE, IN, KY, LA, MA, NH, NY, SC, WV 
<p>
 
   </td>
  </tr>
</table>


 

Source: OSET Institute, May 27, 2020[^13]


##  \
**A Step-by-Step Technical Analysis of the Absentee Voting System **

The general process and components of absentee voting are outlined below. This outlines how the functions of absentee voting works. While the terms and implementations will vary, this will describe the working parts of absentee voting.

1. Voters Register Their Request To Vote Absentee

33 states and Washington D.C. allow no-excuse (no reason required) absentee voter registration.[^14] Five states (Washington, Oregon, Colorado, Hawaii, Utah) have become permanent vote by mail states. Permanent vote by mail states send absentee ballots to every resident of their state without requiring new yearly absentee ballot requests. Each state allows citizens to use a state ID to register online, at the Department of Motor Vehicles, or in person. California is temporarily a vote by mail state for the 2020 election[^15] and allows citizens to use a proof of residency, state ID, or a social security number for voter registration.[^16] 

For the rest of the states, the process for requesting an absentee ballot varies. Most states require the voter to fill out a registration form and return it to their local county election office. 12 states have added online forms for absentee registration to make the process easier. [^17]

16 states have specific absentee registration requirements such as a signature witness or signature notarization.[^18] There is a mix of requirements or “excuses” that allow a voter to absentee. New Hampshire has determined that the pandemic is an acceptable reason for requesting absentee voting in the 2020 election. Conversely, lack of immunity from COVID-19 is not a valid absentee registration excuse in Texas. The Texas Democratic Party had sued the Secretary of State and the Travis County Clerk demanding the additional excuse and lost in the Texas Supreme Court on 20 May 2020.[^19] 

In some states, a potential voter can show up on the day of the election and request same day registration. While this is not a voting absentee, how the ballot is handled and processed is the same as an absentee ballot, so we mention it here. The voter in this case would fill out a ballot that would be marked as a provisional ballot. This could be a regular absentee ballot marked provisional or a completely different ballot layout. 

As a rule, provisional ballots, also called an “affidavit ballot”, are used when a voter’s eligibility is in question. There are additional situations where a ballot is spoiled and then a provisional ballot is used in its place. In some cases, the provisional ballot is treated like an absentee ballot with a signed envelope. The provisional ballots are kept separate from the rest of the ballots. Generally, local election officials manually review and confirm the legitimacy of the voter within days after the Election Day to determine if their provisional ballot is to be counted. There is a notable exception in Idaho, Minnesota, and New Hampshire where they provide same day registration and do not provide provisional ballots.[^20][ ](https://www.ncsl.org/research/elections-and-campaigns/provisional-ballots.aspx)



2. The Elections Office Maintains The Absentee Voter Rolls

Once the absentee registration has been received by the elections official, the identity of the voter needs to be matched with a trusted source such as the state voter registration database. As part of the process of verifying the voter’s identity, the submitted registration signature must be matched. This is often completed manually with some training to match signatures. Additionally, 30 states utilize the nonprofit Electronic Registration Information Center (ERIC) database which combines member states voter data.[^21] ERIC provides data on voters that moved, died, eligible but not registered, and in-state duplicates.  to ensure more accurate voter rolls.

Once registered to vote absentee, it is not permanent in a majority of states. 16 states provide a permanent or semi-permanent absentee registration.[^22] Even with the states that have permanent absentee registration, the voter roll can be culled for reasons such as the absentee ballot being returned non-deliverable or the voter’s status changed to inactive or challenged. 7 states allow for permanent absentee voters to be removed. [^23] Reasons vary from in California missing four consecutive statewide elections to in the District of Columbia having any mail from the election office as undeliverable. 



3. The Election Office Prints and Mails the Absentee Ballots

The absentee ballot consists of a standard layout that generally remains the same year over year and the contest options. The Ballot Layout is the template structure and requirements for every ballot election to election. This includes a computer readable code encoding the ballot type and version, so the ballot scanners can correctly identify the area to scan for the contest options area. There is also the envelope layout which is the digital description of how the ballot envelope text and markings are designed for the printer. Most importantly the envelope layout sets aside the signature space. Once updated for the current election contest, the digital files are transmitted to a commercial industrial printer.

The printer is a critical part of the election process. Generally, each printer that does business with a state has certification requirements similar to the election system vendors that manage the in-person voting process and tabulation of votes.

Ideally the printer is a commercial vendor that can handle the specific requirements of the ballot paper standards, the security of the ballots, stuffing and addressing of the envelopes, and the secure delivery of the stuffed envelopes to the US Post Office. For example, the largest full service ballot printer in the US, Runbeck Election Services, will deliver close to 50 million stuffed ballot envelopes through the US Post Office in 2020. [^24] Using a full service printer eliminates some of the complication of the process as they are generally using automation to optimize time and waste

However, some states do not require the full range of services from their printer and ask the local election office to provide the envelope stuffing and delivery to the US Post Office. In this case, once the printer delivers the ballots and envelopes, they need to be combined. There is commercial equipment available that automates this process. Once the envelopes have been loaded either by hand or by equipment, they then need to be delivered to the US Post Office. Once delivered to the US Post Office, they take the responsibility for delivery of the sealed envelope to the voter. 

The timing of the ballot printing needs to be accurate in order to get to the voter within a time window. The timing of the delivery to the absentee voter varies from 15 to 60 days before the election depending on the state.[^25] Additionally, it can take many weeks to print the ballots and envelopes. If there are errors that require reprinting, it could be weeks or months before the second batch of ballots and envelopes are available. If there are any problems with the arrival of the absentee ballot before the voting period, then the voter must contact their local county elections office for a replacement absentee ballot. 



4. The Voter Fills Out the Ballot, Signs the Envelope. and Returns the Ballot

The absentee ballot provides the options by contest. The voter makes their selections and stuffs the ballot into the envelope. Putting the stuffed ballot envelope in the mail, drop box, or dropped off at the election office is casting their ballot. This is similar to casting your ballot in-person where you are dropping a completed ballot into a ballot drop box at a polling place.

Each absentee ballot envelope has a space for the voter’s signature. Some states require additional information as well. 8 states require a witness signature and 3 states require a notarization. Arkansas requires a copy of the voter ID while Alabama requires both a copy of the voter ID and notarization or two witnesses.[^26] When a ballot is returned to the election office by the US Postal Office, the back of the envelope must be signed by the voter. Envelopes delivered to the election office without a signature are required to be adjudicated. 

The absentee ballot can be returned in most states by the voter either dropping off the ballot in a sealed envelope at a US Post Office, their local mailbox, or at a voter drop box. Utah and Oregon provide online maps of ballot drop boxes. In some states the voter can drop off their absentee ballot at an in-person voting location drop box after providing the required registration information similar to any other in-person voter. The absentee ballots sealed in their envelopes are delivered to the elections office by the US Post Office as they are available.

There is an additional group that is permitted to deliver sealed absentee ballots envelopes to the election office. For the few states that permitted this activity in the past, it was restricted to a designated family member. Over the past few years, the definition of a designated person to return a ballot has been expanded. 27 states and Washington DC permit a designated agent to deliver a sealed absentee ballot envelope to an election office. [^27] It is generally considered a felony for violating rules around illegal ballot collection. This practice is commonly called ballot harvesting.

A majority of states require the absentee ballot to be in the local county elections office by the close of Election Day. A few states allow for a US Post Office postmarked absentee ballot by close of Election Day. 



5. The Election Office Matches the Signature and Scans the Ballot

15 states do not allow the processing of ballot envelopes before election day. A few allow signature verification upon receipt. While most states have some variation of days before the election to begin signature verification. [^28]

The signature verification process in most states requires the envelope to have an area reserved for the registered voter’s signature. In a majority of states, the signature is required to be verified to match the registered voter signature on file. The registered voter signature can be provided by a paper voter roll, a local registered voter database, a state registered voter database, or a regional registered voter database such as ERIC. Jurisdictions match the registered voter signature either by utilizing the same commercial scanners used for the ballots, separate commercial scanners specific for the envelopes, or by hand. Envelopes that have signatures that do not match the registered voter signature on file for any reason are set aside to be adjudicated. 

After the ballot envelope registered voter signature has been verified, the ballot is removed from the envelope. Some states require the envelope be marked by a printer to match the absentee ballot and archived. The envelope marking added to the absentee ballot would include the postmark date, time, location. The ballot can be removed by commercial letter openers or by hand.  In Washington state they have two envelopes to separate the ballot envelope from the US Post Office postmarked envelope with the registered voter signature. The two envelope system is meant to make it impossible to post-election identify a voter’s selections. 

Using a ballot scanner, the absentee ballot is scanned producing a digital file. While the absentee ballot is scanned it is also likely marked (printed) with a voter ID. The voter ID is generally not connected with the voter rather it is a generic number. The ballot type, time, date, voter ID, and scanner ID are recorded along with the digital file.



6. The Ballots Get Counted

The Election Administration Voting Survey (EAVS) tracks the use of 6 types of voting equipment in addition to the hand-counting of ballots. Nationally, jurisdictions reported using 334,422 pieces of equipment in the 2018 general elections. Most jurisdictions and states used more than one type of equipment. The most commonly used equipment types were scanners (used in 96.3 percent of states) and BMDs (79.6 percent). Hand counting of ballots was used in 44.4 percent of states.[^29] 

When scanners are used, they utilize Optical Character Recognition (OCR) to find the voter’s selections in the absentee ballot digital image. Combining the voter ID and the voter’s selections, the cast vote record is recorded in the elections database for each absentee ballot. The cast vote record is the official countable (tabulatable) record from the available contest options. [^30] Using the cast vote records, the total counts of the voters’ selections are tallied. The tally process is generally performed by software. 

Even with the automation provided by the scanners and software tabulation, the tabulation process is time consuming. Handing stacks of paper ballots and dealing with paper jams is a constant issue. Absentee ballot processing delays the results of providing a count of the election results on election day. Due to the issues of dealing with absentee ballots, 17 states begin some form of tabulating absentee ballots before election day. [^31]

The tabulation process is double checked by a variety of processes.One of the tabulation checks is a pre-check for accuracy and quality before the election by feeding a known set of ballots into the tabulator. The vote selection totals equal the expected result or else diagnostics and adjustments are required to correct the system. Another check involves printing a “zero tape” that verifies the tabulator's counters are all at zero. In the case of software failure, the backup is generally a manual count of the ballots using poll workers.



7. Continuous Oversight to Avoid Fraud

In parallel, as the cast vote records are tallied, there is continuous oversight to avoid fraud. 

There are a variety of methods of elections oversight, but generally it involves making a request to the local county elections official. The oversight is simply the ability to view the process of processing and tallying the ballots. Some elections offices provide some form of oversight training.

In the past, a few polling places were audited during each election to verify the voting process and poll worker practices were in line with expectations. This practice has generally been abandoned as the sample size and selection makes the results close to useless.

A more advanced form of auditing is a Risk Limiting Audit (RLA). A RLA involves comparing a statistical sample of the ballots to the tally of the absentee ballots. RLAs are the most efficient and inexpensive when the margin of victory is large. With elections where the margin of victory is small, then larger numbers of ballots need to be sampled and compared to the tally. Multiple RLAs are performed while the tabulation is underway to provide insight to the quality of the election process. The paper archive could become an issue during an RLA as the ballots need to be recovered in the same condition as they were originally stored.

When a RLA finds a discrepancy it is generally due to a faulty scanner sensor or paper ballot feeder skipping ballots. Fixing the problem early and recounting the ballots in question usually solves the problem without impacting the quality of the election. 

RLAs have been widely tested in many states and counties to review their ability to improve both operations and public trust. Colorado has implemented statewide RLAs since 2017. At least Ohio, California, and Washington have provided some RLA options for their counties to optionally participate in. 

Another form of oversight is adjudication. When the voter’s selections on ballot are unclear, the process to resolve the voter intent is called adjudication. In some states this process can also be called a “cure”. The confusion can come from a damaged ballot that cannot be scanned, a ballot with one or more blank selections, too many selections or overvotes, and / or write-ins.

The adjudication process will vary with different election offices. It is common practice to make an effort to count all votes rather than discard or spoil ballots requiring adjudication. Working in pairs, poll workers use guides that provide text and images to describe marks, combination of marks, and other possible ballot damage to ballots. Generally anything not in the guides is resolved by a poll supervisor. The process can involve multiple stages of review, random audits by secondary teams, and even quality control teams to verify the guides are being used properly. If all options have been exhausted to gauge the voter intent, then the ballot is considered spoiled and archived.

It is common practice to remake an understood voter intent damaged ballot with a newly marked blank ballot. This is the same process as is used for emailed or faxed ballots by overseas or active military voters. Again working in pairs, poll workers determine the voter intent, create the newly marked blank ballot, and then run the ballot through the scanner. .

The absentee ballot is saved in a paper archive. The paper archive must be saved for a required period to allow for recounts and/or other activities to reduce elections fraud. Always both the original and replacement ballots are archived with the rest of the paper ballots

After the tally has been completed, the paper archive can be counted to verify the ballot counts match the archived ballots. If after an oversight review or a RLA finds a discrepancy, then a partial or full recount is performed. The recount can be tallied by the tabulator or be done manually by hand. 



8. When Everything Has Been Double Checked, the Election is Reported

Most counties provide unofficial tallies of elections starting immediately after election day has closed. Generally these results are shared through an official county elections website, but press releases are not uncommon if there are significant delays in the official results. It is becoming more common that larger election offices work with marketing firms to manage expectations and likely delays in reporting due to absentee ballot tabulation.

The quantity and quality of the elections reporting varies from county to county and state to state. For example, Los Angeles provides absentee ballot results on election day through their LA vote website.[^32] Graphical and text results for over the last decade with various demographic breakdowns are provided. Other counties simply provide a web page with the tabulation results updated every few days. 

After the final Tally has been completed and all ballot adjudications and RLAs have been completed, then the election can be certified complete. The certified election can then be transmitted to the Secretary of State Elections Office. The transmission can be hand delivered by a paper record, by facsimile, or by transmission of a digital file. 


# II. **Discussion of Key Benefits of and Concerns About Absentee Voting **

The ongoing expansion of vote-by-mail options demonstrates the growing recognition that absentee balloting is an important aspect of modern American voting.There are over 8,000 state and local election officials who are dedicated to administering elections without incident, and the implementation of these options demonstrates broad bipartisan support. But a contentious partisan debate at the highest levels of national politics persists about the benefits and risks of voting by mail. 

The Lincoln Network reviewed relevant literature and available evidence about the pros and cons of absentee voting. We reviewed formal commentary and research pieces from political and apolitical organizations, security professionals, elected officials, pieces of legislation, and most importantly, election officials. We are surveying election practitioners and spectators to categorize and quantify all concerns, hopes, and suggested security improvements in regards to expanding absentee voting. The following discussion presents the benefits of and concerns about voting by mail.


# Benefits of Absentee Voting 


## Voter Convenience

Absentee balloting provides voters with more convenience and flexibility during the process. Voting by absentee ballot allows voters to research candidates and issues on the ballot in their own time. It also eliminates the challenges many working class voters face with getting to the polls in person--such as polling hours that conflict with  working hours, traffic, and long lines. 

Surveys in several predominantly vote by mail states have shown that people appreciate this convenience. For example, 87 percent of Oregon’s voters approve of the state’s vote-by-mail system. .[^33] [^34] In 2013, Colorado’s Governor implemented wider vote by mail access and expanded the timelines for ID-voter registration measures. In 2016, [The Pew Charitable Trusts](http://www.pewtrusts.org/en/research-and-analysis/issue-briefs/2016/03/colorado-voting-reforms-early-results) ran a research project 2016 to see how the process went; It showed voters were 95% satisfied with their mail-in voting experience--right on par with 96% of in-person voters.[^35] 


## Saving Money

Mailing ballots is less complicated and less expensive compared to the massive logistical undertaking of finding, staffing, equipping, testing, sanitizing and maintaining hundreds of voting locations across the state. Especially in the midst of the COVID-10 pandemic, several election officials compared it to staffing a small army.[^36]

Colorado found costs decreased an average of 40% in five election administration categories across 46 of Colorado’s 64 counties (those with available cost data) after it implemented all-mail ballot elections.[^37] Counties spent an average of $9.56 per vote in 2014, down from $15.96 in 2008, and all but three counties spent less per vote in 2014 than in 2008.[^38] 

Arizona, Florida, and Oregon tout similar cost efficiencies with expansion to their absentee voting. Without the need of polling places or voting centers there is a cost and time savings. Staff does not need to train volunteers every voting cycle, and outdated equipment is less of an issue. In regards to shifting of postage costs, some states include a prepaid envelope in the absentee ballot, some states require citizens to pay for postage (USPS is required to prioritize all ballots even if with insufficient postage), and in most state voters can submit their ballots through private mail service if they choose. 


## Increasing Voter Turnout

Due to the convenience of mailed ballots, absentee voting has increased voter turnout. Importantly, turnout increases are across the political spectrum and, therefore, do not appear to benefit a particular political party. 

In 2013, Cambridge University and Yale University published a research paper analyzing the effects of voter turnout in Washington state with expanded mail-in ballot reforms. They found these reforms increased voter participation by about 2-4% and increased turnout among more historically lower-participating voters.[^39] The amount of newly participating voters were equal across parties.

In Colorado, voter turnout increased from 51.7% to 54.7% after the absentee ballot measures were extended. Another study of Utah’s 2016 general election (where 21 counties administered voting entirely by mail while eight counties administered traditional polling place-based voting) showed that the voting by mail increased turnout by 4-9 points.[^40] Utah’s young voters (who are historically less likely to vote than older voters) showed the greatest demographic increase in surveyed vote by mail counties.

In 2020, Stanford University’s Democracy and Polarization Lab found similar positive results in their statistical study. Their research shows that universal vote by mail produces a 5% increase in the share of ballots that are mailed in and that voters appreciate the chance to mail in their ballot.[^41] They also note that increased mail-in ballot access raises voter turnout but not in a way that helps either party. Stanford researchers estimated that voting by mail leads to a 0.1% increase of registered Democrats.[^42] 


## Protecting Public Health by Allowing Social Distancing During the Pandemic 

During the pandemic, absentee voting allows voters to safely cast their ballot from home without needing to go to a physical polling station. Increasing the number of voters who cast absentee ballots will also improve safety for other voters who choose to vote in person by reducing the number of people at the polling station. This will also reduce the number of poll workers who are required on election day. (According to the Election Assistance Commission, “24 percent of poll workers were 71 or older and another 32 percent were between the ages of 61 and 70,” in 2016.[^43] Individual health risks may prevent many older Americans from volunteering or working at the polls during the pandemic.) If the COVID-19 pandemic persists in November and public health authorities recommend social distancing at that time, absentee ballots will provide significant benefits by minimizing the number of voters who must cast ballots in person on November 3rd.


# 


# Concerns About Absentee Voting 

 


## Voter Rolls, Administrative Errors, and Voter Ballot Mistakes

Administrative errors are any clerical or logistic human errors that could happen during the printing, mailing, and receiving portion of the voting process. Voter ballot mistakes are mistakes citizens make when filling out their ballot. 

The 2014 Presidential Commission on Election Administration reported that administrative error and voter ballot mistakes are key drawbacks of absentee balloting: 


    “No-excuse absentee voting and vote-by-mail, moreover, often lead to errors in balloting on the part of the election authority or the voter. Ballots can be lost in the mail (either in delivery or return), they can be mailed out or received too late for timely voting, and voters occasionally make mistakes in complying with various signature and other requirements that make an absentee ballot legal.”[^44]

 

Inaccurate voter rolls is a common flaw. There are two federal guidelines that give states a framework on how to operate their voter rolls. The National Voter Registration Act and the Help America Vote Act. The National Voter Registration Act tells states to update their voter rolls at a minimum, based on the registration of cars in their state. It also forbids states to update their voter roll 90 days before an election. The Help America Vote Act mandated basic computerized voter roll maintenance. Both of these federal laws outline basic ways for states to keep their voter rolls, many states go above and beyond, and are encouraged to do so as long as they are fair.

Each state has its own laws on how it updates its voter rolls. Most states cross-check between the United States Postal Service and National Change of Address database, conducts a confirmation of address mailings, and cross references their DMV databases.

The updating of these rolls is difficult because millions of citizens move, die, marry, or become ineligible to vote every year. Since people generally do not update their election officials when life changes happen, 1 out of 8 registered voter data is inaccurate.[^45] This worries critics because if ballots are sent based on inaccurate voter rolls, it leaves open the potential for ballots to be completed by an unintended, unregistered, or unlawful party.

Incorrect, damaged, and unclear ballots are common voter ballot mistakes. Citizens voting at home might incorrectly complete their ballots, whereas in-person voting equipment and personnel generally allow people to correct it. Literacy should also be considered when creating ballots. Election materials are often written at a college level and this can also be an issue for some voters that contribute to voter ballot mistakes. [^46]

Logistic concerns arise from election officials’  seemingly minute administrative processes that can have a big impact on voting. For example, in April 2020, Georgia’s Secretary of State had to revise ballot instructions and resend those instructions to voters due to a miscommunication about whether there is supposed to be one or two envelopes in their mail-in ballot.[^47] Washington, DC election officials reported that confirmation of absentee ballot requests ended up in spam folders because emails from the Board of Election were not recognized. 


## Ballot Harvesting and Voter Fraud

A common concern about widespread absentee balloting and voting-by-mail is that it will enable ballot harvesting and increase voter fraud.

Ballot harvesting is when absentee ballots are taken by a third party and completed fraudulently or with coercion, and then submitted to election officials. This term also covers a substantial gray area, including cases where different third parties “help” people complete their ballots. There are many legitimate cases where friends or family might legitimately return a ballot on someone’s behalf, but it can also include abusive spouses or shady political groups.[^48] According to the Washington Post, ballot harvesting is common. “Political operatives from both sides routinely do it. Democrats used it with particular success in California in 2018 and Republicans used it in North Carolina”[^49] 

Ballot harvesting is indeed a bipartisan problem. The House Committee on Administration’s Ranking Member Rodney Davis (R-IL) issued a report in May 2020 examining “the political weaponization of ballot harvesting” during the 2018 election.[^50] The most notable example during the 2018 election cycle was in North Carolina, where the 9th Congressional district election was overturned.[^51] A consultant working on behalf of the Republican candidate used ballot harvesting to manipulate the outcome of the election.[^52] The State Board of Elections required a new election be held.[^53] 

Congressman Davis’s report alleged widespread ballot harvesting used in California during the 2018 election, which allegedly benefitted Democratic candidates.[^54]  The report describes how changes in state law encouraged unlimited ballot harvesting and encouraged more voters to vote by mail.[^55] The House Committee on Administration minority report explains the result of these changes: 


    “This also gave rise to paid political operatives, known as “ballot brokers,” recruiting and pressuring voters to vote by mail. These ballot brokers identify specific locations, such as large apartment complexes or nursing homes, where voters have traditionally voted for their party and built relationships with the residents. Operatives encourage, and even assist, these unsuspecting voters in requesting a mail- in ballot; weeks later when the ballot arrives in the mail the same ballot brokers are there to assist the voter in filling out and delivering their ballot. This behavior can result in undue influence in the voting process and destroys the secret ballot, a long-held essential principle of American elections intended to protect voters.”[^56] 

Congressman Davis asserts that unlimited ballot harvesting in California “led to the defeat of seven Republican [Congressional] candidates in the California 2018 midterm election.”

The conservative Heritage Foundation asserts that fraud is widespread--publishing a database that cites 1,285 proven instances of voter fraud in the United States.[^57] However, the Heritage Foundation has diluted their argument by including counts of incidents since the 1970s and examples that are not incidents of fraud, but rather other examples of things that can go wrong in the voting process. Other organizations that contend that fraud is rare and state that Heritage’s database exaggerates the problem. The Brennan Center for Justice reviewed Heritage’s  database and concluded: “nothing in the database to confirm claims of rampant voter fraud.”[^58] 

However, we were able to easily find recent examples of voter fraud. The following are several other notable examples of ballot harvesting and ballot tampering from recent elections: 



*   In Houston, TX, a local campaign official worked with known forgers to group 50 absentee ballots at a time, cast the vote for her candidate, and then forge the envelope signature. The campaign official would enter nursing homes, gather residents' absentee ballots, and then fill them out. Their knowledge of how the election system worked allowed them to cast votes illegally through ballot harvesting. This case was only brought to light due to the extraordinary efforts of a local elections activist  Colleen Vera, who noticed election crimes were being committed. If not for her two year investigation, this would have never been prosecuted. [^59] It should also be noted that Texas does not require an ID to request an absentee ballot, so this type of election crime could be more common than we would hope for.


*   Over multiple election cycles, a Philadelphia elections official illegally cast votes effectively stuffing the ballot box. [^60] In 2020, a West Virginia mail carrier was charged with tampering with absentee ballot requests.[^61] While these cases are not examples of ballot harvesting, it highlights the risk of manipulation.
The laws and regulations mitigating ballot harvesting vary state by state. 27 states allow voters to specify anyone to submit their vote, 12 states specify a limited number of possible representatives (household members, caregivers, etc.), and in 14 states the matter is hazy.[^62] [^63] Some states also regulate the number of people and types of relationships a given person can represent, in order to prevent vote harvesting.[^64] There are also efforts to nationalize the ability for any “any person to return a voted and sealed absentee ballot” with no “limit on how many voted and sealed absentee ballots any designated person can return.” [^65]

Historically, it has been standard practice to verify sealed absentee ballots are delivered to the local election office by trustworthy actors. The practice “of allowing candidates or party workers to pick up and deliver absentee ballots should be eliminated.”[^66] Only a voter, elections official, US Postal worker, or an acknowledged family member should handle absentee ballots. It has been correctly noted that there is an exception for tribal lands where friends and neighbors rely on each other to deliver the US mail.[^67] When the quality of the absentee ballots becomes suspect, we have to resort to more extreme efforts on signature matching and physical security to safeguard the integrity of the vote. 

Poor quality registration rolls causing inactive voters to receive ballots through the US Post Office make it easier for bad actors to have access to absentee ballots. One troubling result can be the accumulation of undeliverable absentee ballots at local US Post Offices and apartment complexes. For example, in Clark County, Nevada, for the local 2020 primary election, thousands of absentee ballots were sent to voters that were no longer at the election registration list addresses.[^68] As a result the misplaced ballots were generally available to anyone that would be interested in breaking the election laws.

Bad actors do not have to get direct access to absentee ballots to commit election crimes. The early twentieth century is full of stories of corrupt elections through voter coercion. It is the reason for ballot secrecy laws**. **Disinterested voters or paid voters can and do hand over their ballots to dishonest third parties.[^69] Voters can be threatened or persuaded to hand their ballot over.[^70] Voter coercion will likely continue  to be a problem and policymakers should take the necessary steps to combat it.

TI 


## Major Changes Take Time to Implement

Election officials warn states that changing voting procedures need to put extra effort into communications and operations. This includes massive messaging, logistical accommodations, an increased focus on ensuring that expanded absentee voting solutions are fool-proof. Experienced election veterans warn against making too many changes due to lack of time. Major expansions of vote by mail systems require at least two-years to prepare, vet, and execute.[^71]

The technology, oversight, and time required to drastically change and shore up a new election procedure should not be understated. California’s experience during the 2020 primary provides a warning about the challenges of transitioning to a new election system. In Los Angeles County, a $300 million project to modernize voting by creating voting centers and expanding vote-by-mail options. While this promising effort has the potential to increase participation and voter convenience, California’s March primary resulted in very long lines in Los Angeles since many voters chose to follow past tradition by voting in person on election day.[^72] Breaking traditional behavior while ineffectively relaying those changes due to COVID opens up opportunities to confuse turnout. 

Systemwide transitions before November (such as enabling universal absentee balloting) may face major challenges. During the 2020 primary season, several states experienced significant problems with expanded voting-by-mail options. For example, Washington DC took the unusual action to allow email voting due to complaints that voters did not receive the absentee ballots ahead of its June primary.[^73] 

Several legal challenges raise questions about whether widespread absentee voting can or will be executed by November. The Republican National Committee and several state GOP party committees have initiated legal challenges to prevent expanded absentee balloting or other measures to modify voting rules.[^74] The uncertain outcome of these legal challenges will add to election officials’ difficulty quickly transitioning to vote-by-mail systems before November even if the lawsuits prove unsuccessful.


## Inaccessibility for Persons with Disabilities 

The 2014 Presidential Commission on Election Administration reported that administrative error and mistakes are a key drawback of absentee balloting: “absentee ballots are usually paper ballots, and are therefore not accessible to many persons with disabilities, such as those with visual or dexterity challenges.[^75] 

The National Federation of the Blind stresses the rights of blind Americans under the Americans with Disabilities Act and the Help America Vote Act:[^76]


    “The number of states and local jurisdictions that are considering converting to all vote-by-mail is increasing because it is cheaper than conventional poll-based voting systems and is more convenient for voters. As with any paper ballot system, an accessible way for blind, low-vision, or other print-disabled voters to privately and independently mark their ballots must be provided, as required by the Americans with Disabilities Act (ADA).”

The National Disability Rights Network supports the expansion of voting-by-mail options but urges that the disabled community’s rights be maintained: “election administrators to enhance their options for remote voting while maintaining in-person voting systems to the greatest extent possible.”[^77]


## Delay in Election Results

Most current absentee provisions allow voters to submit their ballots by mail as long as they are postmarked by election day. If states dramatically increase their amount of vote by mail ballots under these provisions, critics worry election results will be excessively delayed. 

If a large number of people mail and postmark their ballots on election day Tuesday, November 3rd, 2020 (instead of taking advantage of early voting) depending on its destination, it will arrive a few days after that. Then, election officials must count those ballots for an non uniform amount of time, finalizing election results days following the election

Arizona election officials made a statement on the contrary saying in-person, Election Day voting does not speed up ballot tabulation. Provisional ballots and conditional provisional ballots can take days to process and can require additional voter outreach. Vote by mail elections would actually reduce their time after election day by doing a lot of this work on the front end.[^78]

Given each state has different timelines and protocols, delays may or may not occur. Delays in election results for the sake of accuracy are normal in American elections, but suspected delays will have to be communicated across the board to preserve faith in the system. 


# Weighing the Benefits and Concerns 

Expanding absentee balloting and voting-by-mail offers tradeoffs for voters and the United States. On the one hand, increasing access to absentee ballots offers more convenience for voters, reduces costs for states and local governments administering elections, and increases voter turnout. Importantly, absentee voting provides a safe option during the pandmeic when individual and public health concerns may require social distancing and prevent in-person for certain voters. 

However, increasing absentee voting also has significant risks--including practical challenges of administering voting-by-mail and problems quickly transitioning to a new system in the short time period before November. A major risk is the potential for voter coercion, increased fraud and ballot harvesting. (The latter is a bipartisan problem, though the extent of its practice is unknown.) Absentee voting also creates challenges for individuals with disabilities, who are legally entitled to the opportunity to privately and independently cast their ballot. 

Policymakers and state and local election officials must recognize these benefits and risks, and ensure that expanded absentee voting addresses potential problems. The COVID-19 pandemic has created challenges and a public health response that is unprecedented in modern American life. Looking to November, planning to provide expanded absentee balloting and vote-by-mail options is a sensible way to prepare to hold the election during the pandemic. Moreover, 46 states currently offer universal voting-by-mail for the 2020 election. 

The question is not whether or not widespread voting-by-mail will occur during the 2020 election. But instead whether widespread absentee balloting will occur in a manner that addresses the known risks, including minimizing administrative and voter problems and preventing fraud and ballot harvesting. The following section offers solutions and recommendations for policymakers to address these challenges. 


# 


# III Solutions

 



1. Address Security Concerns of Vote-By-Mail Expansion

**National and state policymakers should protect the integrity of the democratic process by expanding access to voting-by-mail while establishing protections to address administrative problems, enhance laws to prevent ballot harvesting and fraud**

_ _

State and local election officials responsible for administering the nation’s elections should move forward with providing expanded access to absentee balloting and voting-by-mail to provide all voters with a safe and convenient way to vote during the pandemic. Available evidence suggests that expanding access to absentee voting is popular, convenient, and will increase voter turnout without favoring either political party. However, state and local policymakers should take steps to address potential problems with expanding absentee voting. 

_ _

Increasing the number of absentee and vote by mail ballots will create more manual work. It is likely that many of the election offices do not have automation available to process absentee ballots or their envelopes. More oversight by the political parties and the general public is likely, which will cause more delays. Large numbers of ballots requiring adjudication such as mis-marked absentee ballots and provisional ballots will cause delays. Election offices will need to radically staff up to meet the increased demand. Additionally, every election office should plan for likely failure scenarios like broken scanners due to higher volumes and new staff not fully understanding processes. 

Even if an election office has little to no changes in their 2020 election plans, communication with the voting public is critical. Election officials should work with public relations and marketing firm in order to communicate with the media and voters. The public needs to understand what to expect from their ballots and the coming election.

 

All voting territories should establish laws to prevent ballot harvesting by adding stricter language about ballot returning methods. At the moment, thirty-seven states and Washington, D.C. have language that allow absentee ballots to be returned by a designated person. There are thirteen states who don’t address this issue at all (Delaware, Hawaii, Idaho, Mississippi, New York, Oklahoma, Rhode Island, Tennessee, Utah, Vermont, Washington, Wisconsin and Wyoming.)[^79] [^80]We recommend the Board of Elections / Secretary of State for the final 13 states adopt language that could reduce the legal opportunity for ballot harvesting. That language should provide voters with the option to return the ballot themselves, allow for US Post Office or private mail couriers to pick up and deliver the ballot, restrict the number of designated people allowed to return one’s ballot, and make clear the penalties for anyone who fraudulently collects and returns ballots from another person. 

These measures should be tailored by the state to ensure accessibility and can be implemented before the November 2020 elections. As states consider this option, their choices should be widely communicated early and often to ensure voter suppression does not happen. 

_ _



2. Implement Ballot Tracking Measures 

**States and local governments should improve voter confidence in absentee balloting by providing voters a way to track their absentee ballot and a receipt to prove that an absentee ballot was received and counted**

 

This potential solution is broadly consistent with the following recommendation of the bipartisan Presidential Commission on Election Administration in 2014: 

 


    _“Therefore, while endorsing the expansion of no-excuse absentee voting, the Commission also encourages the increased use of safeguards. One such safeguard is online tracking of absentee ballots. County election websites should enable voters to verify that their absentee ballot request was received, that their ballot was mailed out, and then later that it was received and counted (and if not counted, the reason why). Barcoding technology has empowered jurisdictions to automate this process and to empower voters to check that their votes have not been “lost in the system.” Moreover, jurisdictions that recognize a problem with the absentee ballot or application of a voter should follow up with that voter if sufficient time exists to cure any technical defects that might prevent the voter’s vote from being counted.”**[1]**_

 

In addition to tracking the absentee ballot, states could consider implementing technology that would allow voters to know their vote has been counted. Designing ballots in a manner that provides voters with an electronic receipt (such as a “QR code”) may be an option. This process, combined with other checks-and-balances, such as the creation of a state election integrity ombudsman that would work alongside the post-election audit team, could establish a proper system. A few states provide an online tool to verify their vote was recorded. Using a QR code would be broadly useful for states that concerned the privacy of the voter’s selections could be compromised. 

_ _



3. Keep In-Person Voting Open

**State and local governments should maintain and improve in-person voting options and ensure that all voters, particularly individuals with disabilities, can vote independently and privately while addressing the practical challenges of in-person voting during the COVID-19 pandemic**

 

For states that have expanded or are expanding their absentee voting options, most are still keeping in-person voting as an option during COVID-19. Many bipartisan voting rights groups have argued that not offering in-person voting infringes on the right to vote as it takes away voting options for those that need assistance or have un-permanent mailing addresses. 

 

Recent federal measures support this as well, the Natural Disaster and Emergency Ballot Act sponsored by Senator’s Klobuchar & Wyden note that states need to reduce in-person voting risks such as no lickable envelopes, staff to sanitize equipment, and enforced social distancing protocols. In Travis County, Texas moving voting polls to retail voting spaces that were already open was very successful and could be used amidst our current public health crisis. Additionally, simply adding curbside voting to existing voting centers and expanding the use of ballot drop boxes will augment and improve the quantity of available options.

 

To deal with the social-distancing aspect of in-person voting, an improvement would be to fix the voter center congestion problem. Given most people work during the day and many states have same-day registration, crowding at popular sites may become a health issue. Early voting is still happening with postponed primaries but that should not be the only distancing precaution. In the Los Angeles March 2020 primary, only about 15.3 percentage of voters participated in early voting.

 

An improvement would be to use geo-fencing to let voters use a mobile poll registration application to check in automatically when they arrive at a voting center. This automatic activity will alert the poll registration system to the increased voting demand and likely resulting wait times. The same monitoring data can be shared with a variety of services supporting wait time web sites and mobile mapping applications like Waze, Google Maps, and Apple Maps. Either the mapping or the mobile poll registration application would then be able to direct the voter to a less congested voting center. 

 

Additionally, providing the voter with a mobile sample ballot application would allow the voter’s selections to be documented before arriving at the polls. Using a QR code to encode the data, the voter could then use a scanner in the voting booth to load the voter’s selections into the ballot. The voter then would only need to review their ballot and accept to cast their ballot.



4. Reconsider Allocating Additional Funds

**States and local governments should use previously authorized and appropriated federal funding (and other available federal resources) to administer and secure the 2020 election. National policymakers should ease burdens on state and local governments and improve oversight and transparency to clarify what additional resources are needed to modernize and secure U.S. election systems moving forward.**

**_ _**

Since 2018, the U.S. Congress has provided $1.2 billion in funding to support state and local election administration through the Help America Vote Act. (See Table 02.) The U.S. Election Assistance Commission awards this funding to states.

 

 

**Table 02 — HAVA Funding Since FY2018 **[^81]** **[^82]** **[^83]

 


<table>
  <tr>
   <td>FY2018
   </td>
   <td>$380,000,000
   </td>
  </tr>
  <tr>
   <td>FY2020
   </td>
   <td>$425,000,000
   </td>
  </tr>
  <tr>
   <td>2020 CARES Act
   </td>
   <td>$400,000,000
   </td>
  </tr>
  <tr>
   <td><strong>Total </strong>
   </td>
   <td><strong>$1,205,000,000</strong>
   </td>
  </tr>
</table>


 

As of September 2019 of the 2018 HAVA funds distributed, the states collectively reported spending roughly 24 percent or $91.2 million.[^84] It is projected that 75 percent or $285 million will be spent by the November 2020 elections.

Through HAVA, the EAC has released an additional $825 million in allocations for all the states for FY 2020 and CARES Act funding. This money allows states to use those funds to 1) update voter equipment to record digital voter intent 2) replace voter equipment with a voter-verified paper record such as mail-in ballots 3) implement post-election audits systems such as RLAs that provide high confidence. 

 

These funds can also be used to address COVID related expenses including increased absentee ballot printing (not including the normal amount a state would have printed), increased labor costs, equipment to process absentee ballots, laptops for election workers, space leasing for new polling locations, communique on new election tech to the public, not including Get Out The Vote (GOTV) work.

 

Some national lawmakers[^85] and several nonpartisan organizations have recommended additional funding to support modernizing state and local election infrastructure, improving cybersecurity and administering the election during the pandemic.[^86]  However, it is unclear that additional funding is needed at this time, particularly since many states have not yet spent all of the federal dollars provided since 2018. 

The current system of reporting spending on hundreds of millions of dollars through a single, annual report is unacceptable when customizable web forms are easily available. A simple, digital reporting system would make it easier on all parties involved. 

For example, when additional funds are requested either through the US Congress, Secretary of State, Governor, or election office, a more specific request and reporting system can be tailor made. Even more importantly, it would make a better case for why more funds are needed. It would have the added benefit of increasing oversight. 

State and local governments should be able to promptly report to Congress on what funds have been spent at least annual quarter by quarter, how unobligated funding will be used, and identify any remaining gaps in funding that are needed to administer the election during 2020. Absent convincing evidence that all existing funding has been spent and that new dollars are needed, Congress should not appropriate new HAVA funding for 2020. 

 

In addition to available HAVA funding, state and local governments should use other available resources to secure and administer the election. For example, states and local governments could use some of the billions in unspent homeland security grants awarded by DHS and the Federal Emergency Management Agency since 2015.[^87]  (Cybersecurity is listed as one of the FEMA’s “[core capabilities](https://www.fema.gov/media-library-data/1575301594630-07bf5dcfaef6482c8597643cc967d44d/CCDS_Protection_508.pdf)” for homeland security and FEMA’s grant manual [allows](https://www.fema.gov/media-library-data/1555010612902-389f8b3351d06d759b01df2a8a851284/FEMA_PreparednessGrantsManual_Final_508.pdf)  cybersecurity costs a way to spend these grant dollars.) 



5. Maintain Trustworthy Voter Rolls

**_States Should Reduce the Chances of Ballot Harvesting and Wrongly Mailed Ballots by Updating Their Voter Rolls_**

States that implement user-friendly registration systems can yield cleaner voter rolls. Cleaner voting rolls means ballots get mailed to the correct voter. Critics of expanded absentee voting are worried about outdated voter rolls because states who expand their absentee voting run the risk of mailing ballots to citizens who have died, moved, or otherwise become ineligible to vote.  An increase of blank ballots in circulation opens the door for nefarious behavior by political operatives. 

The work that the [Election Registration Information Center (ERIC)](https://ericstates.org/) does in 31 states to share voter rolls across states and other sources of voter data should be spread to the rest of the country. 

Additionally, some believe the federal government should help in these efforts by making the Department of Homeland Security and other databases available to states.[^88] [^89] With the quality of the voter registration data vastly improved, then the risks involved with no excuse absentee voter registration and online absentee ballot requests will be greatly minimized. [^90]



6. Inclusive Voter Identification Measures

**States Should Support and Widely Broadcast, Inclusive Voter Identification Measures**

With in-person voting, most polling spaces ask for ID before voters go to the polls. As expanded absentee access takes hold, not requiring ID can increase potential for voter fraud.[^91] 

Oregon’s positive experience with expanding vote by mail has been coupled with investments in technology to better match signatures to address impersonation concerns.[^92] Currently, 17 states compare ballot submissions with their voter registration record, States could consider various forms of privatized information that are aligned with the information present in voter rolls, to ensure identity,[^93] 19 states cross reference ballot signatures with voter registration signatures, 5 states require copies of identification cards or notarized applications, and 4 states (plus DC) have their own verification methods.[^94] [^95]

With this security consideration, states need to ensure inclusive Voter ID rules to prevent voter suppression. For example, North Dakota and Wyoming enacted voting rules that said post-office addresses, even if that’s the only address a voter has, is not sufficient. Thousands of Native American citizens only have post office addresses on their government-issued tribal IDs, and live hundreds of miles from a handful of North Dakota Department of Transportation offices.[^96] [^97]

While there are debates on ensuring inclusive rules, in general, identity verification measures are widely supported on a bipartisan basis.[^98] [^99] As an example, improving voter identification measures include modernizing signature verifications. As a biometric indicator, signature verification is a popular way for states to confirm voter identity. However, the burden is on the majority of the election officials to manually match signatures by eyesight.[^100] Some states like Oregon have invested in technology to better match signatures to address impersonation concerns.[^101] States have previously reported moving slowly on investing in signature technology[^102]  but should reconsider given the new availability of election security funds. 



7. Avoid Major Changes Before November 2020

**Collaborate Within Existing Framework of the Federal, State, And County Election Community**

Respecting the current emergency, we recommend against making large emergency changes to our complex election system. The March 2020 H.R. 6379 and May 2020 H.R. 6800 bills risked making voting by mail the law of the land with poor security and fraud oversight.[^103] [^104] Additionally, the risk of damaging complex systems with major changes is very real with many examples. 

Efforts to nationalize our election system, bypassing the existing elections framework, is inviting lawsuits that could tie up the mandates and funds for years.[^105] Many states believe in the current design of election system federalism, in which each state self determines the best course of action. In the agreed Senate version of the bill HR 748, Congress correctly decided to support the Elections Assistance Commission (EAC) and the community of election officials they work with, enabling them to develop timely solutions within the existing framework of elections laws and regulations.[^106]


# Conclusion

History shows us that we can hold an election during even the most difficult times. The United States held elections in 1864 during the height of the Civil War and in 1944 when the Greatest Generation was fighting World War II. It may be our responsibility to hold a presidential election during a pandemic. The time to prepare is now.

The summer of 2020 is a crucial time for augmentations to the November 2020 elections. Planning, funding, and purchasing changes to the complex elections systems require lead time to be successful. As of the spring, the state of absentee voting in the United States is generally healthy. In order to keep the overall election systems healthy, we need to make improvements that do no harm. 


# Next Steps 

We want to better serve the election community by collaborating with engineers, voters, security professionals, and election officials on future research topics. Lincoln Network will start by socializing this paper through events.

We will also be sharing this paper with various policy circles to begin the process of open source collaboration. This is a living document and there are issues we plan on covering in future revisions. As our collaboration increases, we look forward to shaping this paper to further fill missed considerations. 

Absentee balloting and voting-by-mail is just one of the many challenges facing state and local election directors and state and national policymakers overseeing election administration. In the course of this research, we reviewed the following issues that warrant additional research, analysis, and collaboration among technologists and the policy community


## Apply Layered Cyber Deterrence to Election Ecosystem 

Layered cybersecurity deterrence includes regularly assessing vulnerabilities in the election ecosystem and improving synchronized security capabilities.

Denying adversaries the benefits of their operations lies in resilience planning and risk mitigation.[^107] Since our election ecosystem functions off of software and hardware provided by the private sector, attacker-targeted technologies such as voting machines, electronic poll books, voter registration systems, campaign databases and election administration systems require more coordinated protection and diversification.[^108]

Comprehensive security improvements will cost more than $1 billion,[^109] which will require additional resources. Seven years ago, the 2013 [Presidential Commission on Elections Administration reported that by the end of the decade, voting machines purchased in 1993 would reach their end of life.](http://www.supportthevoter.gov/)[^110] Many of the 10,000 election jurisdictions nationwide still use 1990s technology to run voting equipment, tally votes, and report counts.[^111]  [^112] [^113] To start, states should continue to use and push for Homeland Security grants to improve equipment. 

To move towards cyber defences, the federal government should work with states to test existing election security infrastructure, networks, and contingency plans, to honestly assess their points of vulnerability that could severely disrupt voting. 

 Federal and state governments should prioritize the hiring of cybersecurity and network professionals to advise and build plans forward. Federally, the National Institute of Standards and Technology, DHS - CISA, and FBI’s National Cyber Investigative Joint Task Force should create a synchronized cybersecurity framework that offers direct guidance and on-the-ground assistance to election officials on how to best secure their systems.[^114] [^115]

 

More suggestions on how all levels of government can coordinate layered cyber deterrence are forthcoming. But first we need to have a clear-eyed view of our points of vulnerability and simultaneously support new technology that may make our infrastructure safer to use. 


## Improving the Quality of Electronic Pollbook Networks

Since 2018, just 26.2 percent of jurisdictions nationwide reported using e-poll books.[^116] Improved and increased use of e-poll books would support voter identification confirmation and ensure updates across jurisdictions. It would require external consulting, threat assessments, network updates, and agreement on voter identification methods to ensure all election jurisdictions start out with good online safety habits and regularly submit to vulnerability checks. 

To make e-poll books safer, states need to improve their baseline network security. During California’s 2020 primary, their network's ability to handle the load of electronic registration traffic became overwhelmed. Centralized processes like e-poll books are great tools, but become vulnerable to these types of single points of failure. So states have to improve network operations to avoid failure similar to those experienced in California.

Every network needs full-time attention from knowledgeable engineering staff. Anything less leads to failures during an election. Actions such as implementing load and fault testing carrier networks with their egress points (where the network traffic comes through.), verifying backup for any network connected device, and understanding how and when networks and devices fail are all good measures. In the short term, current or donated labor can work alongside consultants to design and implement solutions for the 2020 general.  

There are additional measures to be explored such as planning for DoS attacks, monitoring for unauthorized traffic, and decrypting traffic for inspection. We will deep dive into how to develop and maintain these networking best practices and more. 


## New Election System Projects

There are new ideas around election systems. The most recent is the ElectionGuard pilot in Fulton, Wisconsin which has the capability of encrypting the vote while allowing the voter to verify their vote was counted. This was the first and successful test of a new collaboration between multiple companies to build an election system. 

While this specific pilot did not include vote by mail, one of the ElectionGuard partners VotingWorks is building a vote by mail system. VotingWorks plans at least one pilot for November 2020.  

Another example of new ideas is the Los Angeles Voting System for All People (VSAP) built by the county. VSAP vote by mail has been in service for a few election cycles already. They have spent an extraordinary amount of time focusing on the quality of the voting experience. 

Other interesting projects such as improving state election system certification to support new election system projects, monitoring social media weather patterns and nonpartisan fact checking services are being developed right now, but these will not be ready for use until next year at the earliest. We will explore the capabilities and viability of these new election system projects. 


## Only with Increased Prosecution of Election Crimes will Confidence in Absentee Voting become the Norm

States  should consider mandating RLAs--as of now, 80 percent of states require audits.[^117] All states should have a mechanism for conducting recounts to ensure that ballots were counted correctly. Legislatively, all states can and should support post-election collaboration between audit conductors and non-partisan research institutions to gather intelligence on how their states' election process went after November 2020. This research is actually very rare and will support our nation as a whole and the state's ability to execute better plans in the future.

The US Election Assistance Commission has concluded that past studies of elections crimes were “limited in scope and some have been riddled with bias.” [^118] Additionally, it appears that the states and local authorities have assigned a low priority to election crime prosecution. The state and local prosecutors often apply a low priority to pursuing election fraud. Additionally, evidence is difficult to obtain to the level required for prosecution.[^119]

There are a limited number of federal prosecutors as compared to the state prosecutors. In the period of 2002 through 2005, there were 180 federal investigations of election fraud resulting in the conviction of 52 people.[^120] Additionally the federal government sees elections as a state right and responsibility. The Federal Justice Department sees its role as prosecution rather than intervention in the elections process. They are not seeking to be preventative and take pains to avoid becoming part of the state’s responsibility of holding the elections themselves. Activities such as seizing ballots as evidence impact the confidence and outcomes of elections in progress. Some activities are prohibited by federal law such as sending armed men to the vicinity of open polling places. 18 U.S.C. § 592. [^121] 

Unfortunately, a possible reason for the lack of clarity about the extent to which voter fraud and ballot harvesting is a problem is the lack of confirmed incidents. In fact, the Brennan Center has highlighted the lack of “incident rates” as proof that election crimes are not occurring.[^122] It appears to be a self fulfilling prophecy, that the lack of prosecutions, mean voting fraud is considered a low priority. [^123] [^124] [^125] Even with high penalties such as $10,000 fine and 5 years in federal prison, ballot harvesting appears to be a low risk election crime as it is rarely prosecuted.[^126]


<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
     "16 States Have Postponed Primaries During the Pandemic ...." Accessed June 11, 2020. [https://www.nytimes.com/article/2020-campaign-primary-calendar-coronavirus.html](https://www.nytimes.com/article/2020-campaign-primary-calendar-coronavirus.html).

[^2]:
     “Primary Election Snafus Show Challenges For November Vote,” Accessed June 11, 2020, [https://www.npr.org/2020/06/03/869042005/primary-election-snafus-show-challenges-for-november-vote](https://www.npr.org/2020/06/03/869042005/primary-election-snafus-show-challenges-for-november-vote) 

[^3]:
    "The EAVS! - Election Assistance Commission." Page 20 Accessed May 26, 2020. [https://www.eac.gov/sites/default/files/eac_assets/1/6/2018_EAVS_Report.pdf](https://www.eac.gov/sites/default/files/eac_assets/1/6/2018_EAVS_Report.pdf)

[^4]:
     "EAVS Deep Dive: Poll Workers and Polling Places | U.S. ...." Accessed May 26, 2020. [https://www.eac.gov/documents/2017/11/15/eavs-deep-dive-poll-workers-and-polling-places](https://www.eac.gov/documents/2017/11/15/eavs-deep-dive-poll-workers-and-polling-places) 

[^5]:
     “Primary Election Snafus Show Challenges For November Vote,” Accessed June 11, 2020, [https://www.npr.org/2020/06/03/869042005/primary-election-snafus-show-challenges-for-november-vote](https://www.npr.org/2020/06/03/869042005/primary-election-snafus-show-challenges-for-november-vote)

[^6]:
     “Voting Outside the Polling Place: Absentee, All-Mail and other Voting at Home Options,”  Access June 02, 2020, [https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx](https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx)

[^7]:
     ibid

[^8]:
     “The Absentee Ballot and the Secret Ballot: Challenges for Election Reform,” Accessed June 11, 2020, [https://repository.law.umich.edu/cgi/viewcontent.cgi?article=1415&context=mjlr](https://repository.law.umich.edu/cgi/viewcontent.cgi?article=1415&context=mjlr) 

[^9]:
     The American Voting Experience: Report and Recommendations of the Presidential Commission on Election Administration, January 2014”, Accessed on June 11, 2020 [http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf](http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf)

[^10]:
     “ISSUE BRIEFING: Election Emergencies & COVID-19,” Accessed on June 02, 2020, [https://www.nass.org/resources/issue-briefing-election-emergencies-covid-19](https://www.nass.org/resources/issue-briefing-election-emergencies-covid-19)  

[^11]:
     “The Bipartisan Truth About By-Mail Voting,” Accessed June 11, 2020, [https://trustthevote.org/wp-content/uploads/2020/05/27May20_BipartisanTruthAboutByMailVoting_v3.pdf](https://trustthevote.org/wp-content/uploads/2020/05/27May20_BipartisanTruthAboutByMailVoting_v3.pdf) 

[^12]:
     ibid

[^13]:
     ibid

[^14]:
     “ISSUE BRIEFING: Election Emergencies & COVID-19,” Accessed on June 02, 2020, [https://www.nass.org/resources/issue-briefing-election-emergencies-covid-19](https://www.nass.org/resources/issue-briefing-election-emergencies-covid-19) 

[^15]:
     "Voting Outside the Polling Place: Absentee, All-Mail and ... - NCSL." Accessed May 18, 2020. [https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx](https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx).

[^16]:
     "Frequently Asked Questions | California Secretary of State." Accessed May 18, 2020. [https://www.sos.ca.gov/elections/frequently-asked-questions/](https://www.sos.ca.gov/elections/frequently-asked-questions/).

[^17]:
     "VOPP: Table 6: States With Web-Based and Online Absentee ...." Accessed May 18, 2020. [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-6-states-with-web-based-and-online-absentee-ballot-applications.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-6-states-with-web-based-and-online-absentee-ballot-applications.aspx).

[^18]:
     "VOPP: Table 5: Applying for an Absentee Ballot, Including ...." Accessed May 18, 2020. [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-5-applying-for-an-absentee-ballot-including-third-party-registration-drives.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-5-applying-for-an-absentee-ballot-including-third-party-registration-drives.aspx).

[^19]:
     In The Supreme Court Of Texas, No. 20-0394, In Re State Of Texas, On Petition For Mandamus, Accessed on June 09, 2020, [https://www.txcourts.gov/media/1446711/200394.pdf](https://www.txcourts.gov/media/1446711/200394.pdf)

[^20]:
     "Provisional Ballots - NCSL." Accessed May 26, 2020. [https://www.ncsl.org/research/elections-and-campaigns/provisional-ballots.aspx](https://www.ncsl.org/research/elections-and-campaigns/provisional-ballots.aspx).

[^21]:
     “Electronic Registration Information Center (ERIC),”  Accessed June 09, 2020, [https://ericstates.org/](https://ericstates.org/)

[^22]:
     VOPP: Table 3: States With Permanent Absentee Voting for All Voters, Voters With Permanent Disabilities and/or Senior Voters,” Accessed June 09, 2020, [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-3-states-with-permanent-absentee-voting-for-all-voters-voters-with-permanent-disabilities-and-or-senior-voters.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-3-states-with-permanent-absentee-voting-for-all-voters-voters-with-permanent-disabilities-and-or-senior-voters.aspx)

[^23]:
     “VOPP: Table 4: State Laws on Removing Voters From Permanent Absentee Lists,” Access June 09, 2020, [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-4-state-laws-on-removing-voters-from-permanent-absentee-lists.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-4-state-laws-on-removing-voters-from-permanent-absentee-lists.aspx)

[^24]:
     “Ballot Printers Increase Capacity To Prepare For Mail Voting Surge,” Accessed June 09, 2020, [https://www.npr.org/2020/05/03/848347895/ballot-printers-increase-capacity-to-prepare-for-mail-voting-surge](https://www.npr.org/2020/05/03/848347895/ballot-printers-increase-capacity-to-prepare-for-mail-voting-surge)

[^25]:
     "VOPP: Table 7: When States Mail Out Absentee Ballots - Ncsl." Accessed May 18, 2020. [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-7-when-states-mail-out-absentee-ballots.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-7-when-states-mail-out-absentee-ballots.aspx)

[^26]:
     “Voting Outside the Polling Place: Absentee, All-Mail and other Voting at Home Options,”  Accessed June 09, 2020, [https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx](https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx#verify)

[^27]:
     Ibid

[^28]:
     “VOPP Table 16: When Absentee/Mail Ballot Processing and Counting Can Begin,” Accessed June 10, 2020, [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-16-when-absentee-mail-ballot-processing-and-counting-can-begin.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-16-when-absentee-mail-ballot-processing-and-counting-can-begin.aspx) 

[^29]:
     "The EAVS! - Election Assistance Commission." Page 20 Accessed May 26, 2020. [https://www.eac.gov/sites/default/files/eac_assets/1/6/2018_EAVS_Report.pdf](https://www.eac.gov/sites/default/files/eac_assets/1/6/2018_EAVS_Report.pdf).

[^30]:
     “Election Terminology Glossary - Draft,”, Accessed June 09, 2020, [https://pages.nist.gov/ElectionGlossary/](https://pages.nist.gov/ElectionGlossary/)

[^31]:
     “VOPP Table 16: When Absentee/Mail Ballot Processing and Counting Can Begin,”  Accessed June 10, 2020, [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-16-when-absentee-mail-ballot-processing-and-counting-can-begin.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-16-when-absentee-mail-ballot-processing-and-counting-can-begin.aspx)

[^32]:
     “Los Angeles county RR/CC Election Results June 02, 2020 special elections,” Accessed June 10, 2020, [https://lavote.net/home/voting-elections/current-elections/election-results/live-results](https://lavote.net/home/voting-elections/current-elections/election-results/live-results) 

[^33]:
     "EXPANDING AND IMPROVING OPPORTUNITIES ... - GovInfo." Accessed May 18, 2020. [https://www.govinfo.gov/content/pkg/CHRG-110hhrg40618/html/CHRG-110hhrg40618.htm](https://www.govinfo.gov/content/pkg/CHRG-110hhrg40618/html/CHRG-110hhrg40618.htm) 

[^34]:
     "Oregon Public Broadcasting 2016 - Vote at Home." Accessed May 26, 2020. [https://www.voteathome.org/wp-content/uploads/2018/12/Oregon-Public-Brodcasting-Statewide-Survey-October-2016-2.pdf](https://www.voteathome.org/wp-content/uploads/2018/12/Oregon-Public-Brodcasting-Statewide-Survey-October-2016-2.pdf) 

[^35]:
     "Colorado Voting Reforms: Early Results | The Pew Charitable ...." Accessed May 18, 2020. [https://www.pewtrusts.org/en/research-and-analysis/issue-briefs/2016/03/colorado-voting-reforms-early-results](https://www.pewtrusts.org/en/research-and-analysis/issue-briefs/2016/03/colorado-voting-reforms-early-results) 

[^36]:
     "View the EVIC blog - Early Voting Information Center - Reed ...." Accessed May 18, 2020. [https://evic.reed.edu/blog/](https://evic.reed.edu/blog/) 

[^37]:
     "Colorado Voting Reforms: Early Results | The Pew Charitable ...." Accessed May 18, 2020. [https://www.pewtrusts.org/en/research-and-analysis/issue-briefs/2016/03/colorado-voting-reforms-early-results](https://www.pewtrusts.org/en/research-and-analysis/issue-briefs/2016/03/colorado-voting-reforms-early-results) 

[^38]:
     "Colorado Election Reforms Improve Voter Experience | The ...." Accessed May 18, 2020. [https://www.pewtrusts.org/research-and-analysis/articles/2016/03/23/colorado-election-reforms-improve-voter-experience](https://www.pewtrusts.org/research-and-analysis/articles/2016/03/23/colorado-election-reforms-improve-voter-experience) 

[^39]:
     "Identifying the Effect of All-Mail Elections on Turnout ...." Accessed May 18, 2020. [https://www.cambridge.org/core/journals/political-science-research-and-methods/article/identifying-the-effect-of-allmail-elections-on-turnout-staggered-reform-in-the-evergreen-state/3725E51B9B7F331D77DC9B49130D7F7D](https://www.cambridge.org/core/journals/political-science-research-and-methods/article/identifying-the-effect-of-allmail-elections-on-turnout-staggered-reform-in-the-evergreen-state/3725E51B9B7F331D77DC9B49130D7F7D) 

[^40]:
     "Utah 2016: Evidence for the positive turnout effects of “Vote At ...." Accessed May 18, 2020. [https://kwtri4b8r0ep8ho61118ipob-wpengine.netdna-ssl.com/wp-content/uploads/2018/06/Utah-2016-Voter-File-Analysis-Pantheon-Analytics.pdf](https://kwtri4b8r0ep8ho61118ipob-wpengine.netdna-ssl.com/wp-content/uploads/2018/06/Utah-2016-Voter-File-Analysis-Pantheon-Analytics.pdf) 

[^41]:
     "The Effect of All-mail Elections on Voter Turnout - PRISCILLA ...." Accessed May 18, 2020. [https://journals.sagepub.com/doi/10.1177/1532673X00028001004](https://journals.sagepub.com/doi/10.1177/1532673X00028001004) 

[^42]:
     "the neutral partisan effects of vote-by-mail - siepr - Stanford ...." Accessed May 18, 2020. [https://siepr.stanford.edu/sites/default/files/publications/20-015.pdf](https://siepr.stanford.edu/sites/default/files/publications/20-015.pdf) 

[^43]:
     https://www.eac.gov/documents/2017/11/15/eavs-deep-dive-poll-workers-and-polling-places

[^44]:
     The American Voting Experience: Report and Recommendations of the Presidential Commission on Election Administration, January 2014”, Accessed on June 11, 2020 [http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf](http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf)

[^45]:
     "Electronic Registration Information Center ...." Accessed May 18, 2020. [https://ericstates.org/](https://ericstates.org/).

[^46]:
     "Voting Outside the Polling Place: Absentee, All-Mail ... - NCSL." Accessed May 26, 2020. [https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx](https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx).

[^47]:
     "Georgia absentee voting instructions to be corrected - AJC.com." Accessed May 26, 2020. [https://www.ajc.com/news/state--regional-govt--politics/georgia-absentee-voting-instructions-corrected/kzkuKmLufxIRcwIW0oEzCN/](https://www.ajc.com/news/state--regional-govt--politics/georgia-absentee-voting-instructions-corrected/kzkuKmLufxIRcwIW0oEzCN/).

[^48]:
     "True Confessions of Texas Vote Harvesters ...." Accessed May 26, 2020. [https://www.realclearinvestigations.com/articles/2019/02/19/true_confessions_of_texas_vote_harvesters.html](https://www.realclearinvestigations.com/articles/2019/02/19/true_confessions_of_texas_vote_harvesters.html).

[^49]:
     “What is ballot 'harvesting,' and why is Trump so against it,” Accessed June 11, 2020, [https://www.washingtonpost.com/politics/2020/05/26/what-is-ballot-harvesting-why-is-trump-so-against-it/](https://www.washingtonpost.com/politics/2020/05/26/what-is-ballot-harvesting-why-is-trump-so-against-it/) 

[^50]:
     “Report: Political Weaponization of Ballot Harvesting in California, US House of Representatives Committee on House Administration,” Accessed June 11, 2020,  [https://republicans-cha.house.gov/sites/republicans.cha.house.gov/files/documents/CA%20Ballot%20Harvesting%20Report%20FINAL.pdf](https://republicans-cha.house.gov/sites/republicans.cha.house.gov/files/documents/CA%20Ballot%20Harvesting%20Report%20FINAL.pdf) 

[^51]:
     “Committee Republicans’ Report Highlights How Ballot Harvesting is Ripe for Voter Fraud & Abuse,” Accessed 11 June 2020, [https://republicans-cha.house.gov/sites/republicans.cha.house.gov/files/documents/California%20Report%20Summary.pdf](https://republicans-cha.house.gov/sites/republicans.cha.house.gov/files/documents/California%20Report%20Summary.pdf) 

[^52]:
     Ibid

[^53]:
     Ibid

[^54]:
     Ibid

[^55]:
     Ibid

[^56]:
     Ibid

[^57]:
     “Database Swells to 1,285 Proven Cases of Voter Fraud in America,”  Accessed May 12, 2020, [https://www.heritage.org/election-integrity/commentary/database-swells-1285-proven-cases-voter-fraud-america](https://www.heritage.org/election-integrity/commentary/database-swells-1285-proven-cases-voter-fraud-america) 

[^58]:
     “Heritage Fraud Database: An Assessment,” 11 June 2020, [https://www.brennancenter.org/sites/default/files/2019-07/Report_HeritageAnalysis_Final.pdf](https://www.brennancenter.org/sites/default/files/2019-07/Report_HeritageAnalysis_Final.pdf) 

[^59]:

     “Alleged Ballot Harvesting in Harris County Prompts Investigation Request by Secretary of State,” Accessed on June 01, 2020, [https://thetexan.news/alleged-ballot-harvesting-in-harris-county-prompts-investigation-request-by-secretary-of-state/](https://thetexan.news/alleged-ballot-harvesting-in-harris-county-prompts-investigation-request-by-secretary-of-state/) 

[^60]:

     “U.S. Attorney William M. McSwain Announces Charges and Guilty Plea of Former Philadelphia Judge of Elections Who Committed Election Fraud,” June 01, 2020, [https://www.justice.gov/usao-edpa/pr/us-attorney-william-m-mcswain-announces-charges-and-guilty-plea-former-philadelphia](https://www.justice.gov/usao-edpa/pr/us-attorney-william-m-mcswain-announces-charges-and-guilty-plea-former-philadelphia) 

[^61]:
     “West Virginia mail carrier charged with attempted absentee ballot application fraud,” Accessed June 01, 2020, [https://www.whsv.com/content/news/Pendleton-County-mail-carrier-charged-with-altering-absentee-ballot-requests-570777221.html](https://www.whsv.com/content/news/Pendleton-County-mail-carrier-charged-with-altering-absentee-ballot-requests-570777221.html) 

[^62]:
     "Time to Prepare for Voting by Mail | Mercatus Center." Accessed May 26, 2020. [https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail](https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail).

[^63]:
     "Voting Outside the Polling Place: Absentee, All-Mail ... - NCSL." Accessed May 26, 2020. [https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx](https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx).

[^64]:
     "Time to Prepare for Voting by Mail | Mercatus Center." Accessed May 26, 2020. [https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail](https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail).

[^65]:
     “116TH Congress 2D Session H.R. 6800,” Accessed May 27, 2020, [https://www.congress.gov/116/bills/hr6800/BILLS-116hr6800ih.pdf](https://www.congress.gov/116/bills/hr6800/BILLS-116hr6800ih.pdf) 

[^66]:
     “Building Confidence in US Elections Report of the Commission on Federal Election Reform, September 2005,” Accessed on 29 May 2020, [https://www.legislationline.org/download/id/1472/file/3b50795b2d0374cbef5c29766256.pdf](https://www.legislationline.org/download/id/1472/file/3b50795b2d0374cbef5c29766256.pdf)

[^67]:
     Dirty Tricks: Eight Falsehoods that Could Undermine the 2020 Electio,n Accessed June 01, 2020, [https://www.brennancenter.org/our-work/research-reports/dirty-tricks-eight-falsehoods-could-undermine-2020-election](https://www.brennancenter.org/our-work/research-reports/dirty-tricks-eight-falsehoods-could-undermine-2020-election)

[^68]:
     “Nevada's vote-by-mail primary stirs fraud concerns, as unclaimed ballots pile up: 'Something stinks here,' Accessed on May 27, 2020, [https://www.foxnews.com/politics/nevadas-vote-by-mail-primary-fraud-concerns](https://www.foxnews.com/politics/nevadas-vote-by-mail-primary-fraud-concerns)

[^69]:
     State of Connecticut, Laws concerning corrupt practices at elections, caucuses and primaries, 1915,” Accessed May 29 2020, [https://www.loc.gov/item/17006245/](https://www.loc.gov/item/17006245/)

[^70]:
     “What is Vote Buying?,” Accessed on May 27, 2020, [http://www.gsdrc.org/docs/open/po14.pdf](http://www.gsdrc.org/docs/open/po14.pdf)

[^71]:
     "Masks required at DC voting sites as officials push voting by mail." Accessed May 18, 2020. [https://wtop.com/dc/2020/04/masks-required-at-dc-voting-sites-as-officials-push-voting-by-mail/](https://wtop.com/dc/2020/04/masks-required-at-dc-voting-sites-as-officials-push-voting-by-mail/).

[^72]:
     “Lessons from California’s Primary: The Shift to Voting Centers Caused System-wide Challenges,” Accessed June 11, 2020, 
    [https://lincolnpolicy.org/2020/learning-lessons-from-californias-primary-for-november/](https://lincolnpolicy.org/2020/learning-lessons-from-californias-primary-for-november/) 

[^73]:
     “D.C. Lets Voters Submit Ballots by Email After Mail Problems,” Accessed June 11, 2020, [https://www.wsj.com/articles/d-c-letsvoters-submit-ballots-by-email-after-mail-problems-11591211518](https://www.wsj.com/articles/d-c-letsvoters-submit-ballots-by-email-after-mail-problems-11591211518) 

[^74]:
     “As Trump attacks voting by mail, GOP builds 2020 strategy around limiting its expansion,” Accessed June 11, 2020, [https://www.washingtonpost.com/politics/as-trump-attacks-voting-by-mail-gop-builds-2020-strategy-around-limiting-its-expansion/2020/05/31/a17ccfa0-a00d-11ea-b5c9-570a91917d8d_story.htm](https://www.washingtonpost.com/politics/as-trump-attacks-voting-by-mail-gop-builds-2020-strategy-around-limiting-its-expansion/2020/05/31/a17ccfa0-a00d-11ea-b5c9-570a91917d8d_story.htm) l

[^75]:
    “The American Voting Experience: Report and Recommendations of the Presidential Commission on Election Administration, January 2014”, Accessed on June 11, 2020 [http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf](http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf)

[^76]:
     “Voting, Accessibility, and the Law: The Help America Vote Act,” Accessed June 11, 2020, 
    [https://www.nfb.org/programs-services/center-excellence-nonvisual-access/national-center-nonvisual-election-3](https://www.nfb.org/programs-services/center-excellence-nonvisual-access/national-center-nonvisual-election-3) 

[^77]:
     “Statement on Elections Accessibility during the COVID-19 Pandemic” Accessed June 11, 2020, [https://www.ndrn.org/resource/statement-on-elections-accessibility-during-the-covid-19-pandemic/](https://www.ndrn.org/resource/statement-on-elections-accessibility-during-the-covid-19-pandemic/) 

[^78]:
     "All-mail election for 2020 wouldn't ruin its integrity, officials say." Accessed May 18, 2020. [https://www.azcentral.com/story/opinion/op-ed/2020/04/08/arizona-all-mail-election-2020-wouldnt-ruin-its-integrity/2957970001/](https://www.azcentral.com/story/opinion/op-ed/2020/04/08/arizona-all-mail-election-2020-wouldnt-ruin-its-integrity/2957970001/).

[^79]:
     "Voting Outside the Polling Place: Absentee, All-Mail ... - NCSL." Accessed June 9, 2020. [https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx](https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx).

[^80]:
     "VOPP: Table 10: Who Can Collect and Return an Absentee ...." Accessed June 9, 2020. [https://www.ncsl.org/research/elections-and-campaigns/vopp-table-10-who-can-collect-and-return-an-absentee-ballot-other-than-the-voter.aspx](https://www.ncsl.org/research/elections-and-campaigns/vopp-table-10-who-can-collect-and-return-an-absentee-ballot-other-than-the-voter.aspx).

[^81]:
     “2018 HAVA Funds,” Accessed June 11, 2020, [https://www.eac.gov/payments-and-grants/2018-hava-funds](https://www.eac.gov/payments-and-grants/2018-hava-funds)

[^82]:
     “2020 HAVA Funds,” Accessed June 11, 2020, [https://www.eac.gov/payments-and-grants/2020-hava-funds](https://www.eac.gov/payments-and-grants/2020-hava-funds)

[^83]:
     “2020 CARES Act Grants,” Accessed June 11, 2020, [https://www.eac.gov/payments-and-grants/2020-cares-act-grants](https://www.eac.gov/payments-and-grants/2020-cares-act-grants)

[^84]:
     “Serving America’s Election Officials and Voters: 2019 EAC Annual Report,” Accessed June 11, 2020, [https://www.eac.gov/sites/default/files/eac_assets/1/6/EACAnnualReport_2019.pdf](https://www.eac.gov/sites/default/files/eac_assets/1/6/EACAnnualReport_2019.pdf)

[^85]:
     “Natural Disaster and Emergency Ballot Act (NDEBA) of 2020,” Accessed on June 11, 2020, [https://www.klobuchar.senate.gov/public/_cache/files/0/0/00bfcd4c-8bff-4e40-8082-9c509e6bf168/C874798F600EED86B58DED75D3FE5875.naturaldisasterandeba.pdf](https://www.klobuchar.senate.gov/public/_cache/files/0/0/00bfcd4c-8bff-4e40-8082-9c509e6bf168/C874798F600EED86B58DED75D3FE5875.naturaldisasterandeba.pdf)

[^86]:
     "Defending Elections - Brennan Center for Justice." Accessed June 9, 2020. [https://www.brennancenter.org/sites/default/files/2019-08/Report_Defending_Elections.pdf](https://www.brennancenter.org/sites/default/files/2019-08/Report_Defending_Elections.pdf)

[^87]:
     "States and Cities Could Use Billions of Unspent DHS Grants ...." Accessed June 9, 2020. [https://www.lawfareblog.com/states-and-cities-could-use-billions-unspent-dhs-grants-protect2020](https://www.lawfareblog.com/states-and-cities-could-use-billions-unspent-dhs-grants-protect2020)

[^88]:
     "How We Can Safeguard Our Election Process - The Daily Signal." Accessed May 26, 2020. [https://www.dailysignal.com/2019/08/19/how-we-can-safeguard-our-election-process/](https://www.dailysignal.com/2019/08/19/how-we-can-safeguard-our-election-process/).

[^89]:
     "More Proof That Voter Fraud Is Real, and Bipartisan | The Heritage Foundation" Accessed May 26, 2020. [https://www.heritage.org/election-integrity/commentary](https://www.heritage.org/election-integrity/commentary/more-proof-voter-fraud-real-and-bipartisan).

[^90]:
     “ Defending Democracy Program The 2020 U.S. Elections:Readying for the Challenges
    “ Accessed May 19, 2020, [https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2020/04/MSFT_ES_Whitepaper_FINAL.pdf](https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2020/04/MSFT_ES_Whitepaper_FINAL.pdf) 

[^91]:
     "Be wary of voting by mail initiatives | TheHill." Accessed May 26, 2020. [https://thehill.com/opinion/civil-rights/493131-be-wary-of-voting-by-mail-initiatives](https://thehill.com/opinion/civil-rights/493131-be-wary-of-voting-by-mail-initiatives).

[^92]:
     "Time to Prepare for Voting by Mail | Mercatus Center." Accessed May 26, 2020. [https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail](https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail).

[^93]:
     "Voting Outside the Polling Place: Absentee, All-Mail and other Voting at Home Options
    - NCSL." Accessed May 26, 2020. [https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx](https://www.ncsl.org/research/elections-and-campaigns/absentee-and-early-voting.aspx).

[^94]:
     Ibid

[^95]:
     Ibid

[^96]:
     "ALEC-Backed Legislators Behind Suppressing Vote | PR Watch." Accessed May 26, 2020. [https://www.prwatch.org/news](https://www.prwatch.org/news/2018/10/13411/alec-backed-legislators-behind-suppressing-vote).

[^97]:
     "Discriminatory North Dakota Voter ID Law Still In Effect ...." Accessed May 26, 2020. [https://www.narf.org/spirit-lake-voter-id/](https://www.narf.org/spirit-lake-voter-id/).

[^98]:
     "Potential for Fraud Is Why Mail-In Elections Should Be Dead ...." Accessed May 26, 2020. [https://www.heritage.org/election-integrity/commentary](https://www.heritage.org/election-integrity/commentary/potential-fraud-why-mail-elections-should-be-dead-letter).

[^99]:
     "The False Narrative of Vote-by-Mail Fraud | Brennan Center ...." Accessed May 26, 2020. [https://www.brennancenter.org/our-work/analysis-opinion/false-narrative-vote-mail-fraud](https://www.brennancenter.org/our-work/analysis-opinion/false-narrative-vote-mail-fraud).

[^100]:
     "Signature Verification Guide." Accessed May 26, 2020. [http://www.sos.state.co.us/pubs/elections/docs/SIgVerificationSinglePageSept2018.pdf](http://www.sos.state.co.us/pubs/elections/docs/SIgVerificationSinglePageSept2018.pdf).

[^101]:
     "Time to Prepare for Voting by Mail | Mercatus Center." Accessed May 26, 2020. [https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail](https://www.mercatus.org/publications/covid-19-policy-brief-series/time-prepare-voting-mail).

[^102]:
     "Observations on Voting Equipment Use and Replacement - GAO." Accessed May 26, 2020. [https://www.gao.gov/assets/700/691201.pdf](https://www.gao.gov/assets/700/691201.pdf).

[^103]:
     “H.R. 6379 - Take Responsibility for Workers and Families Act - [Rep. Lowey, Nita M](https://www.congress.gov/member/nita-lowey/L000480?q=%7B%22search%22%3A%5B%22hr6379%22%5D%7D&r=1)” [https://www.congress.gov/](https://www.congress.gov/bill/116th-congress/house-bill/6379?q=%7B%22search%22%3A%5B%22hr6379%22%5D%7D&s=1&r=1)

[^104]:
     “ H.R.6800 - The Heroes Act - [Rep. Lowey, Nita M](https://www.congress.gov/member/nita-lowey/L000480?q=%7B%22search%22%3A%5B%22hr6379%22%5D%7D&r=1)”
    [https://www.congress.gov/](https://www.congress.gov/bill/116th-congress/house-bill/6800?q=%7B%22search%22%3A%5B%22heros+act%22%5D%7D&s=2&r=1)

[^105]:
     "Nancy Pelosi Is Trying To Use The Coronavirus Package To Get Ahead On Election Day
    " Accessed May 26, 2020. [https://www.rnla.org/dhillon_pelosi](https://www.rnla.org/dhillon_pelosi).

[^106]:
     "CARES Act - Senate Appropriations." Accessed May 26, 2020. [https://www.appropriations.senate.gov/imo/media/doc/FINAL%20FINAL%20CARES%20ACT.pdf](https://www.appropriations.senate.gov/imo/media/doc/FINAL%20FINAL%20CARES%20ACT.pdf).

[^107]:
     "How to Get Ahead of Election 2020 Security Threats ...." Accessed May 26, 2020. [https://statetechmagazine.com/](https://statetechmagazine.com/article/2020/03/how-get-ahead-election-2020-security-threats).

[^108]:
     "Strategic Election Security Solutions in Action - FireEye." Accessed May 26, 2020. [https://www.fireeye.com/](https://www.fireeye.com/content/dam/fireeye-www/solutions/pdfs/cs-strategic-election-security-solution.pdf).

[^109]:
     "What Does Election Security Cost? | Brennan Center for Justice." Accessed May 26, 2020. [https://www.brennancenter.org/our-work/analysis-opinion/what-does-election-security-cost](https://www.brennancenter.org/our-work/analysis-opinion/what-does-election-security-cost).

[^110]:
      “The American Voting Experience: Report and Recommendations of the Presidential Commission on Election Administration, January 2014”, Accessed on June 11, 2020 [http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf](http://web.mit.edu/supportthevoter/www/files/2014/01/Amer-Voting-Exper-final-draft-01-09-14-508.pdf)  

[^111]:
     "Learn More | TrustTheVote." Accessed June 10, 2020. [https://trustthevote.org/learnmore/](https://trustthevote.org/learnmore/).

[^112]:
     "FY 2021 Budget in Brief - Homeland Security." Accessed May 26, 2020. [https://www.dhs.gov/sites/default/files/publications/fy_2021_dhs_bib_web_version.pdf](https://www.dhs.gov/sites/default/files/publications/fy_2021_dhs_bib_web_version.pdf).

[^113]:
     "New Election Systems Use Vulnerable Software”  AP News. Accessed May 26, 2020. [https://apnews.com/e5e070c31f3c497fa9e6875f426ccde1](https://apnews.com/e5e070c31f3c497fa9e6875f426ccde1).

[^114]:
     "Defending America's Election Infrastructure - Brennan Center" Page 2.  Accessed May 26, 2020. [https://www.brennancenter.org/](https://www.brennancenter.org/sites/default/files/2020-04/Defending%20Americas%20Election%20Infrastructure%20October%202019_3.pdf).

[^115]:
     "Congressional Testimony: Voting Technology Vulnerabilities." Accessed May 26, 2020. [https://www.brennancenter.org/](https://www.brennancenter.org/our-work/research-reports/congressional-testimony-voting-technology-vulnerabilities).

[^116]:
     "Electronic Poll Books | e-Poll Books - NCSL." Accessed June 11, 2020. [https://www.ncsl.org/research/elections-and-campaigns/electronic-pollbooks.aspx](https://www.ncsl.org/research/elections-and-campaigns/electronic-pollbooks.aspx).

[^117]:
     "Fiscal Year 2018 Annual Report - Election Assistance ...." page iii Accessed May 26, 2020. [https://www.eac.gov/](https://www.eac.gov/sites/default/files/eac_assets/1/6/EACannualreport_2018.pdf).

[^118]:
     “US EAC, Election Crimes: An Initial Review and REcommendations for Future Study, December 2006,” Accessed May 29, 2020, [https://www.eac.gov/sites/default/files/document_library/files/2006_Election_Crimes_Report_1.pdf](https://www.eac.gov/sites/default/files/document_library/files/2006_Election_Crimes_Report_1.pdf)

[^119]:
     “Building Confidence in US Elections, Report of the Commision on Federal Election Reform,”  Accessed May 18 2020, “[https://www.legislationline.org/download/id/1472/file/3b50795b2d0374cbef5c29766256.pdf](https://www.legislationline.org/download/id/1472/file/3b50795b2d0374cbef5c29766256.pdf) 

[^120]:
     “Department Of Justice To Hold Ballot Access And Voting Integrity Symposium,” Accessed on 29, 2020, [https://www.justice.gov/archive/opa/pr/2005/August/05_ag_404.htm](https://www.justice.gov/archive/opa/pr/2005/August/05_ag_404.htm)

[^121]:
     “Federal Prosecution of Election Offenses Eighth Edition December 2017,”  Accessed May 29, 2020, [https://www.justice.gov/criminal/file/1029066/download](https://www.justice.gov/criminal/file/1029066/download)

[^122]:
     “Dirty Tricks: Eight Falsehoods that Could Undermine the 2020 Election,” June 01, 2020, [https://www.brennancenter.org/our-work/research-reports/dirty-tricks-eight-falsehoods-could-undermine-2020-election](https://www.brennancenter.org/our-work/research-reports/dirty-tricks-eight-falsehoods-could-undermine-2020-election) 

[^123]:
     “In 5-Year Effort, Scant Evidence of Voter Fraud,” June 01, 2020, [https://www.nytimes.com/2007/04/12/washington/12fraud.html](https://www.nytimes.com/2007/04/12/washington/12fraud.html) 

[^124]:
     “Probing illegal vote claims is low priority for agency,” June 01, 2020, [https://www.arkansasonline.com/news/2018/jan/22/probing-illegal-vote-claims-is-low-prio/](https://www.arkansasonline.com/news/2018/jan/22/probing-illegal-vote-claims-is-low-prio/) 

[^125]:
     Voter fraud is not a persistent problem, Accessed June 01, 2020, [https://votingwars.news21.com/voter-fraud-is-not-a-persistent-problem/](https://votingwars.news21.com/voter-fraud-is-not-a-persistent-problem/) 

[^126]:
     “The False Narrative of Vote-by-Mail Fraud” Accessed June 11, 2020, [https://www.brennancenter.org/our-work/analysis-opinion/false-narrative-vote-mail-fraud](https://www.brennancenter.org/our-work/analysis-opinion/false-narrative-vote-mail-fraud)
