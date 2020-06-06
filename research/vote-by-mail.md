# Voter Registration
In the past absentee voting was used primarily for US citizens traveling overseas and active military. Its use expanded as more voters with accessibility disabilities requested absentee voting access. 

Five states (Washington, Oregon, Colorado, Hawaii, Utah) have become permanent vote by mail states. Each of these states send absentee or vote by mail ballots to every resident of their state. Each state allows citizens to use a state ID to register online, at the Department of Motor Vehicles, or in person. California is temporarily a vote by mail state for the 2020 election and allows citizens to use a proof of residency, state ID, or a social security number for voter registration. 

For the rest of the states, the process for requesting an absentee ballot varies. Most states require the voter to fill out a registration form and return it to their local county election office. Some states have added some online tools to make the registration process easier. The National Conference of State Legislators (NCSL) highlights the states and their online absentee registration options.

16 states have specific absentee registration requirements such as a signature witness or signature notarization. There is a mix of requirements or “excuses” that allow a voter to absentee. New Hampshire has determined that the pandemic is an acceptable reason for requesting absentee voting in the 2020 election. As of April 2020, Texas is going through a lawsuit where the pandemic is requested to be added as a valid excuse. This NCSL table overviews the absentee excuses allowed by the state. 

Once the absentee registration has been received by the elections official, the identity of the voter needs to be matched with a trusted source such as the state voter registration database. This is often completed manually with some training to match signatures. This NCSL list highlights some of the steps and state requirements. 

16 states provide a permanent or semi-permanent absentee registration. This NCSL table highlights the options that provide an ongoing absentee registration. The permanent absentee list can be culled for reasons such as the absentee ballot being returned non-deliverable or the voter’s status changed to inactive or challenged. This NCSL table highlights the 7 states with the reasons. 

34 states have established “no excuse absentee” registration. This NCSL table highlights the no excuse absentee states. 

# Absentee Ballot and Envelope Layout
The Absentee Ballot Layout includes the Ballot Layout and Vote Selections. The Ballot Layout is the template structure and requirements for every ballot election to election. This includes the QR code (this could be a bar code or a number, but for simplicity here we will assume a QR code) encoding the ballot type and version, so the Ballot Scanners can correctly identify the area to scan for the Vote Selections. There is also the Envelope Layout which is the digital description of how the ballot envelope text and markings are designed for the printer. Most importantly it sets aside the signature space. The digital files created from the Absentee Ballot and Envelope Layouts are transmitted to the Printer.

# Voter Registration List
The Voter Registration List provides the names and addresses of the Registered Voters that have requested absentee ballots. The Absentee Ballot is always provided as a paper document to be filled out by hand.

# Printer
The Printer is a commercial vendor that can handle the specific requirements of the Ballot Paper Standards. This includes paper weight, size, font, and ink. The Printer is a critical part of the election process. It can take many weeks to print the ballots and envelopes. If there are errors that require reprinting, it could be weeks or months before the second batch of ballots and envelopes are available. 

# Delivering Absentee Ballots to the Voter
Once the Printer delivers the ballots and envelopes, they need to be combined. There is commercial equipment available that automates this process. Once the envelopes have been loaded either by hand or by equipment, they then need to be delivered to the US Post Office. The US Post Office takes the responsibility for delivery of the sealed envelope. 

The timing of the delivery to the absentee voter varies from 15 to 60 days before the election depending on the state. If there are any problems with the arrival of the absentee ballot before the voting period, then the voter must contact their local county elections office for a replacement absentee ballot. 

# Voter’s Selections
The vote selections on the absentee ballot provide the options by contest. The Voter makes their selections, casting their ballot. 

# Signing the Envelope
Each absentee ballot envelope has a space for the voter’s signature. Some states require additional information as well. When a ballot is returned to the election office by the US Postal Office, the back of the envelope must be signed by the Voter. Envelopes delivered to the election office without a signature are required to be adjudicated. 

# Delivering the Absentee Ballots to the Elections Office
The Absentee Ballot can be returned in most states by the voter either dropping off the ballot in a sealed envelope at a US Post Office, their local mailbox, or at a Voter Drop Box. Utah and Oregon provide online maps of ballot drop boxes. In some states the Voter can drop off their Absentee Ballot at an in-person voting location drop box after providing the required registration information similar to any other in-person voter. The Absentee Ballots sealed in their envelopes are delivered to the Elections Office by the US Post Office as they are available.

There is an additional class of registration that permits a third party to return absentee ballots. For the few states that permitted this activity in the past, it was restricted to a designated family member. Over the past few years, the definition of a designated person to return a ballot has been expanded. This NCSL list shows the states with this type of absentee ballot delivery to the local county elections office, as well as, the restrictions and punishments for violations. 

A majority of states require the absentee ballot to be in the local county elections office by the close of Election Day. A few states allow for a US Post Office postmarked absentee ballot by close of Election Day. 

# Signature Verification
The signature verification process in most states requires the envelope to have an area reserved for the Registered Voter’s signature. The signature is required to be verified to match the Registered Voter Signature on file. The Registered Voter Signature can be provided by a paper voter roll, a local Registered Voter database, a state Registered Voter database, or a regional Registered Voter database. Jurisdictions match the Registered Voter Signature either by utilizing the same commercial scanners used for the ballots, separate commercial scanners specific for the envelopes, or by hand. Envelopes that have signatures that do not match the Registered Voter Signature on file for any reason are set aside to be Adjudicated. 

# Envelope and its Metadata
After the ballot envelope Registered Voter Signature has been verified, the ballot is removed from the envelope. Some states require the envelope be marked by a printer to match the Absentee Ballot and archived. The envelope metadata added to the Absentee Ballot would include the postmark date, time, location. The ballot can be removed by commercial letter openers or by hand.  In Washington state they have two envelopes to separate the ballot envelope from the US Post Office postmarked envelope with the Registered Voter signature. The two envelope system is meant to make it impossible to post-election identify a Voter’s Selections. 

# Ballot Scanning, Ballot Digital File, and its Metadata
Using the Ballot Scanner, the Absentee Ballot is scanned producing a digital file. While the Absentee Ballot is scanned it is also likely marked (printed) with a Voter ID. The QR code, ballot type, version, time, date, Voter ID, scanner ID, and Absentee Ballot filename are recorded as metadata.

# Voter Selections
Using Optical Character Recognition, the Absentee Ballot digital image has the Voter Selections recorded. The Vote Selections are the marked contest options. 

# Cast Vote Record
Combining the Voter ID and the Vote Selections, the Cast Vote Record is recorded in the Elections Database for each Absentee Ballot.

# Tabulation
Using the Cast Vote Records, the total counts of each Vote Selection are tallied. The tally process is generally done by software and double check by a variety of processes. The tabulation is usually pre-checked before the election by feeding a known set of ballots into the tabulator. The Vote Selection totals equal the expected result or else diagnostics and adjustments are required to correct the system. The backup is generally a manual count of the ballots using poll workers.

Note that the tabulation system goes through a series of pre-checks before counting the ballots. These include running test counts using known test ballots to verify counts are accurate and printing a “zero tape” that verifies the tabulators counters are all at zero. 

Risk Limiting Audits are also used in parallel to the tabulation process to double check the tabulation counts are accurate.

# Reporting
Most counties provide unofficial tallies of elections starting immediately after Election Day has closed. Generally these results are shared through an official county elections website, but press releases are not uncommon if there are significant delays in the official results. 

The quantity and quality of the elections reporting varies from county to county and state to state. 

The official tally or result is shared with the state Secretary of State.

# Oversight, Risk Limiting Audits
In parallel the Cast Vote Records are Tallied, Reported, and Risk Limiting Audits are run. 

There are a variety of methods of elections oversight, but generally it involves making a request to the local county elections official. The oversight is simply the ability to view the process of processing and tallying the ballots. Some elections offices provide some form of oversight training.

A more advanced form of oversight is a Risk Limiting Audit (RLA). A RLA involves comparing a statistical sample of the ballots to the tally of the absentee ballots. RLAs are the most efficient and inexpensive when the margin of victory is large. With elections where the margin of victory is small, then larger numbers of ballots need to be sampled and compared to the tally. Multiple RLAs are performed while the tabulation is underway to provide insight to the quality of the election process. The paper archive could become an issue during an RLA as the ballots need to be recovered in the same condition as they were originally stored.

When a RLA finds a discrepancy it is generally due to a faulty scanner sensor or paper ballot feeder skipping ballots. Fixing the problem early and recounting the ballots in question usually solves the problem without impacting the quality of the election. 

RLAs have been widely tested in many states and counties to review their ability to improve both operations and public trust. Colorado has implemented statewide RLAs since 2017. At least Ohio, California, and Washington have provided some RLA options for their counties to optionally participate in. 

# Certification of the Vote
After the final Tally has been completed and all Ballot Adjudications and Risk Limiting Audits have been completed, then the election can be certified complete. The Certified Election can then be transmitted to the State Secretary of State Elections Office. The transmission can be hand delivered by a paper record, by facsimile, or by transmission of a digital file. 

# Same Day Registration
In some states, a potential voter can show up on the day of the election and request same day registration. They would then fill out a ballot that would be marked as a Provisional Ballot. This could be a regular Absentee Ballot marked Provisional or a completely different ballot layout. The process for a damaged Ballot or lost Ballot generally means the Voter fills out a Provisional Ballot as well. 

# Provisional Ballot
Provisional ballots, also called an “affidavit ballot”, are usually used when a voter’s eligibility is in question. There are additional situations where a ballot is spoiled and then a provisional ballot is used in its place. In some cases, the provisional ballot is treated like an absentee ballot with a signed envelope. The provisional ballots are kept separate from the rest of the ballots. Generally, local election officials manually review and confirm the legitimacy of the voter within days after the Election Day.

Idaho, Minnesota, and New Hampshire provide same day registration and do not have provisional ballots. 

NCSL has done extensive research on the various scenarios of provisional ballots. 

# Adjudication
When the Voter’s selections are unclear, the process to resolve the voter intent is called adjudication. In some states this process can also be called a “cure”. The confusion can come from a damaged ballot that cannot be scanned, a ballot with one or more blank selections, no many selections or overvotes, and / or write-ins.

The adjudication process will vary with different election offices. It is common practice to make an effort to count all votes rather than discard or spoil ballots requiring adjudication. Working in pairs, poll workers use guides that provide text and images to describe marks, combination of marks, and other possible ballot damage to ballots. Generally anything not in the guides is resolved by a poll supervisor. The process can involve multiple stages of review, random audits by secondary teams, and even quality control teams to verify the guides are being used properly. If all options have been exhausted to gauge the voter intent, then the ballot is considered spoiled and archived.

It is common practice to remake an understood voter intent damaged ballot with a newly marked blank ballot. This is the same process as is used for emailed or faxed ballots by overseas or active military voters. Again working in pairs, poll workers determine the voter intent, create the newly marked blank ballot, and then run the ballot through the scanner. 

Always both the original and replacement ballots are archived with the rest of the paper ballots.

# Paper Archive, Digital Archive
The Absentee Ballot is saved in a Paper Archive. The Paper Archive must be saved for a required period to allow for recounts and/or other activities to reduce elections fraud. 

After the tally has been completed the paper archive can be counted to verify the ballot counts match the archived ballots.

# Recount
If after an oversight review or a Risk Limited Audit finds a discrepancy, then a partial or full recount is performed. The recount can be tallied by the tabulator or be done manually by hand. 
