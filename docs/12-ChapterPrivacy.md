<!--
% - Rayid: "check Initially, assume the organization is on the outer frontier." ... what does this mean?
% - some references appear with n.d. in the compiled markdown
% - Julia: on Research Data Centers, add a line how the new envisioned ADRF would allow more replicability/reproducibility and access toothers but researchers? (industry, non-profit, government) for whom current RDCs are too hard to jump through hoops?
--> 



Privacy and Confidentiality {#chap:privacy}
===========================

**Stefan Bender, Ron Jarmin, Frauke Kreuter, and Julia Lane**


This chapter addresses the issue that sits at the core of any study of
human beings---privacy and confidentiality. In a new field, like the one
covered in this book, it is critical that many researchers have access
to the data so that work can be replicated and built upon---that there
be a scientific basis to data science. Yet the rules that social
scientists have traditionally used for survey data, namely anonymity and
informed consent, no longer apply when data are collected in the wild.
This concluding chapter identifies the issues that must be addressed for
responsible and ethical research to take place.

Introduction
------------

Most applications in the social sciences involve data on units
such as individuals, households, and different types of business,
educational, and government organizations. Indeed, the example running
throughout this book involves data on individuals (such as faculty and
students) and organizations (such as universities and firms). In
circumstances such as these, researchers must ensure that such data are
used responsibly and ethically---that the subjects under study suffer no
harm from their data being accessed, analyzed, and reported. A clear
distinction must be made between analysis done for the public good and
that done for private gain. In practical terms, this requires that the
interests of individual privacy and data confidentiality be
balanced against the social benefits of research access and use.

**Privacy** "encompasses not only the famous 'right to be left alone,' or keeping
one's personal matters and relationships secret, but also the ability to
share information selectively but not publicly" [@house2014big]. A useful way of thinking about privacy is the notion of preserving the appropriate flow of information [@nissenbaum2009]. There is no specific data type or piece of information that is too sensitive to be shared in all circumstances. In some context providing detailed information about one’s health is very appropriate, for example if it helps finding the right treatment for a disease. It is generally important to understand the context and the contextual integrity of the data flow when deciding which data to collect and how to analyze and share them. 

**Confidentiality** is
"preserving authorized restrictions on information access and
disclosure, including means for protecting personal privacy and
proprietary information" [@mccallister2010sp]. Doing so is not
easy---the challenge to the research community is how to balance the
*risk* of providing access with the associated utility
[@duncanstatistical]. To give a simple example, if means and percentages
are presented for a *large* number of people, it will be difficult to
infer an individual's value from such output, even if one knew that a
certain individual or unit contributed to the formation of that mean or
percentage. However, if those means and percentages are presented for
subgroups or in multivariate tables with small cell sizes, the risk for
disclosure increases [@doyle2001confidentiality]. As a result, the
quality of data analysis is typically degraded with the production of
public use data [@duncanstatistical].

<div class="figure" style="text-align: center">
<img src="ChapterPrivacy/figures/fig11-1.png" alt="The privacy--utility tradeoff" width="70%" />
<p class="caption">(\#fig:fig11-1)The privacy--utility tradeoff</p>
</div>

In general, the greater the access to data and their original values,
the greater the risk of reidentification for individual units. We depict
this tradeoff graphically in
Figure \@ref(fig:fig11-1). The
concave curves in this hypothetical example depict the technological
relationship between data utility and privacy for an organization such
as a business firm or a statistical agency. At one extreme, all
information is available to anybody about all units, and therefore high
analytic utility is associated with the data that are not at all
protected. At the other extreme, nobody has access to any data and no
utility is achieved. Initially, assume the organization is on the outer
frontier. Increased external data resources (those not used by the
organization) increase the risk of reidentification. This is represented
by an inward shift of the utility/privacy frontier in
Figure \@ref(fig:fig11-1).
Before the increase in external data, the organization could achieve a
level of data utility $U^*$ and privacy $P_1$. The increase in
externally available data now means that in order to maintain utility at
$U^*$, privacy is reduced to $P_2$. This simple example represents the
challenge to all organizations that release statistical or analytical
products obtained from underlying identifiable data. As more data from external sources becomes available, it becomes more difficult
to maintain privacy.

Previously, national statistical agencies had the capacity
and the mandate to make dissemination decisions: they assessed the risk,
they understood the data user community and the associated utility from
data releases. And they had the wherewithal to address the legal,
technical, and statistical issues associated with protecting
confidentiality [@trewin2007managing].

But in a world of massive amounts of data, many once-settled issues have new
complications, and wholly new issues arise that need to be addressed,
albeit under the same rubrics. The new types of data have much greater
potential utility, often because it is possible to study small cells or
the tails of a distribution in ways not possible with small data. In
fact, in many social science applications, the tails of the distribution
are often the most interesting and hardest-to-reach parts of the
population being studied; consider health care costs for a small number
of ill people [@stanton2006high], or economic activity such as rapid
employment growth by a small number of firms [@decker2015has].

--- 

**BOX**

**Example: The importance of activity in the tails**

Spending on health care services in the United States is highly
concentrated among a small proportion of people with extremely high use.
For the overall civilian population living in the community, the latest
data indicate that more than 20% of all personal health care spending in
2009 (\$275 billion) was on behalf of just 1% of the population
[@healthcarespending].

**BOX**

---

It is important to understand where the risk of privacy breaches comes
from. Let us assume for a moment that we conducted a traditional
small-scale survey with 1,000 respondents. The survey contains
information on political attitudes, spending and saving in a given year,
and income, as well as background variables on income and education. If
name and address are saved together with this data, and someone gets
access to the data, obviously it is easy to identify individuals and
gain access to information that is otherwise not public. If the personal
identifiable information (name and address) are removed from this data
file, the risk is much reduced. If someone has access to the survey data
and sees all the individual values, it might be difficult to assess with
certainty who among the 320 million inhabitants in the USA is associated
with an individual data record. However, the risk is higher if one knows
some of this information (say, income) for a person, and knows that this
person is in the survey. With these two pieces of information, it is
likely possible to uniquely identify the person in the survey data.

Larger amounts of data increase the risk precisely for this reason. Much data is
available for reidentification purposes [@ohm2010broken]. Most
obviously, the risk of reidentification is much greater because the new
types of data have much richer detail and a much larger public community
has access to ways to reidentify individuals. There are many famous
examples of reidentification occurring even when obvious personal
information, such as name and social security number, has been removed
and the data provider thought that the data were consequently
deidentified. In the 1990s, Massachusetts Group Insurance released
"deidentified" data on the hospital visits of state employees;
researcher Latanya Sweeney quickly reidentified the hospital records of
the then Governor William Weld using nothing more than state voter
records about residence and date of birth [@sweeney2001computational].
In 2006, the release of supposedly de-identified web search data by AOL
resulted in two *New York Times* reports being able to reidentify a
customer simply from her browsing habits [@barbaro2006face]. And in
2012, statisticians at the department store, Target, used a young
teenager's shopping patterns to determine that she was pregnant before
her father did [@hill2012target].

But there are also less obvious problems. What is the legal framework
when the ownership of data is unclear? In the past, when data were more
likely to be collected and used within the same entity---for example,
within an agency that collects administrative data or within a
university that collects data for research
purposes---organization-specific procedures were (usually) in place and
sufficient to regulate the usage of these data. Today,
legal ownership is less clear.

Who has the legal authority to make decisions about permission, access,
and dissemination and under what circumstances? The answer is often not
clear. The challenge today is that data sources are
often combined, collected for one purpose, and used for another. Data
providers often have a poor understanding of whether or how their data
will be used.

---

**Example: Knowledge is power**

In a discussion of legal approaches to privacy in the context of big
data, Strandburg [@Strandburg2014] says: "'Big data' has great potential
to benefit society. At the same time, its availability creates
significant potential for mistaken, misguided or malevolent uses of
personal information. The conundrum for the law is to provide space for
big data to fulfill its potential for societal benefit, while protecting
citizens adequately from related individual and social harms. Current
privacy law evolved to address different concerns and must be adapted to
confront big data's challenges."

---

It is critical to address privacy and confidentiality issues if the full
public value of big data is to be realized. This chapter highlights why
the challenges need to be met (i.e., why access to data is crucial),
review the pre-big data past, point out challenges with this approach in
the context of big data, briefly describe the current state of play from
a legal, technical, and statistical perspective, and point to open
questions that need to be addressed in the future.

Why is access important?
------------------------

This book gives detailed examples of the potential of data to
provide insights into a variety of social science
questions---particularly the relationship between investments in R&D and
innovation. But that potential is only realized if researchers have
access to the data [@Lane2007]: not only to perform primary analyses but
also to validate the data generation process (in particular, data
linkage), replicate analyses, and build a knowledge infrastructure
around complex data sets.

**Validating the data generating process**

Research designs requiring a combination of data sources and/or analysis
of the tails of populations challenge the traditional paradigm of
conducting statistical analysis on deidentified or aggregated data. In
order to combine data sets, someone in the chain that transforms raw
data into research outputs needs access to link keys contained in the
data sets to be combined. High-quality link keys uniquely identify the
subjects under study and typically are derived from items such as
individual names, birth dates, social security numbers, and business
names, addresses, and tax ID numbers. From a privacy and confidentiality
perspective, link keys are among the most sensitive information in many data
sets of interest to social scientists. This is why many organizations
replace link keys containing personal identifiable information (PII)^[PII is "any information about an individual maintained by an agency, including (1) any information
that can be used to distinguish or trace an individual’s identity, such as name,
social security number, date
and place of birth, mother’s
maiden name, or biometric
records; and (2) any other
information that is linked
or linkable to an individual, such as medical, educational, financial, and employment information” [254].]
with privacy-protecting identifiers [@schnell2009privacy]. Regardless,
at some point in the process those must be generated out of the original
information, thus access to the latter is important.

**Replication**

John Ioannidis has claimed that most published research findings are
false [@Ioannidis2005]; for example, the unsuccessful replication of
genome-wide association studies, at less than 1%, is staggering
[@Bastian2013]. Inadequate understanding of coverage, incentive, and
quality issues, together with the lack of a comparison group, can result
in biased analysis---famously in the case of using administrative
records on crime to make inference about the role of death penalty
policy in crime reduction [@donohue2006uses; @levitt2006economic].
Similarly, overreliance on, say, Twitter data, in targeting resources
after hurricanes can lead to the misallocation of resources towards
young, Internet-savvy people with cell phones and away from elderly or
impoverished neighborhoods [@shelton2014mapping], just as bad survey
methodology led the *Literary Digest* to incorrectly call the 1936
election [@squire19881936]. The first step to replication is data
access; such access can enable other researchers to ascertain whether
the assumptions of a particular statistical model are met, what relevant
information is included or excluded, and whether valid inferences can be
drawn from the data [@kreuter201412].

**Building knowledge infrastructure**

Creating a community of practice around a data infrastructure can result
in tremendous new insights, as the Sloan Digital Sky Survey and the
Polymath project have shown [@nielsen2012reinventing]. In the social
science arena, the Census Bureau has developed a productive ecosystem
that is predicated on access to approved external experts to build,
conduct research using, and improve key data assets such as the
Longitudinal Business Database [@jarmin2002longitudinal] and
Longitudinal Employer Household Dynamics [@abowd2004integrated], which
have yielded a host of new data products and critical policy-relevant
insights on business dynamics [@haltiwanger2013creates] and labor market
volatility [@brown2008economic], respectively. Without providing robust,
but secure, access to confidential data, researchers at the Census
Bureau would have been unable to undertake the innovations that made
these new products and insights possible.

Providing access
----------------

The approaches to providing access have evolved over time. Statistical
agencies often employ a range of approaches depending on the needs of
heterogeneous data users
[@doyle2001confidentiality; @foster2009resolving]. Dissemination of data
to the public usually occurs in three steps: an evaluation of disclosure
risks, followed by the application of an anonymization technique, and
finally an evaluation of disclosure risks and analytical quality of the
candidate data release(s). The two main approaches have been
*statistical disclosure* control techniques to produce anonymized public
use data sets, and controlled access through a *research data center* [@shlomo2018].

**Statistical disclosure control techniques**

Statistical agencies have made data available in a number of ways:
through tabular data, public use files, licensing agreements and, more
recently, through synthetic data [@reiter2012statistical]. Hundepool et
al. [@hundepool2010handbook] define statistical disclosure control as
follows:

> concepts and methods that ensure the confidentiality of micro and
> aggregated data that are to be published. It is methodology used to
> design statistical outputs in a way that someone with access to that
> output cannot relate a known individual (or other responding unit) to
> an element in the output.

Traditionally, confidentiality protection was accomplished by
releasing only *aggregated tabular data*. This practice worked well in
settings where the primary purpose was enumeration, such as census
taking. However, tabular data are poorly suited to describing the
underlying distributions and covariance across variables that are often
the focus of applied social science research [@duncanstatistical].

To provide researchers access to data that permitted analysis of the
underlying variance--covariance structure of the data, some agencies
have constructed public use micro-data samples. To product
confidentiality in such *public use files*, a number of statistical
disclosure control procedures are typically applied. These include
stripping all identifying (e.g., PII) fields from the data, topcoding
highly skewed variables (e.g., income), and swapping records
[@doyle2001confidentiality; @zayatz2007disclosure]. However, the mosaic
effect---where disparate pieces of information can be combined to
reidentify individuals---dramatically increases the risk of releasing
public use files [@czajka2014minimizing]. In addition, there is more and
more evidence that the statistical disclosure procedure applied to
produce them decreases their utility across many applications
[@burkhauser2010improving].

Some agencies provide access to confidential micro-data through
*licensing* arrangements. A contract specifies the conditions of use and
what safeguards must be in place. In some cases, the agency has the
authority to conduct random inspections. However, this approach has led
to a number of operational challenges, including version control,
identifying and managing risky researcher behavior, and management costs
[@doyle2001confidentiality].

Another approach to providing access to confidential data that has been proposed by a group of theoretical computer scientists Cynthia Dwork, Frank McSherry, Kobbi Nissim, and Adam Smith [@Dworkroth2014]. Here statistics or other reported outputs are injected with noise, and are called “differentially private” if the inclusion or exclusion of the most at-risk person in the population does not change the probability of any output by more than a given factor. The parameter driving this factor (usually referred to as epsilon) quantifies how sensitive the aggregate output is to any one person’s data. If it is low, the output is highly “private” in the sense that it will be very difficult to reconstruct anything based on it. If it is high, reconstruction is easy. For a discussion of the applications to Census data see [@ruggles2019; @abowed2018].



Another approach that has had some resurgence is the use  of *synthetic data* where certain properties of the original data are preserved but the original data are replaced by “synthetic data” so that no individual or  business entity can be found in the released data
[@drechsler2011synthetic]. One of the earlier examples of such work was the IBM Quest system (cite : http://www.vldb.org/conf/1994/P487.PDF) that generated synthetic transaction data. Two more recent examples of synthetic data sets are the SIPP Synthetic-Beta [@abowd2006final] of linked Survey of Income and Program Participation (SIPP) and Social Security Administration earnings
data, and the Synthetic Longitudinal Business Database (SynLBD)
[@kinney2011towards]. Jarmin et al. [@jarmin2014expanding] discuss how
synthetic data sets lack utility in many research settings but are
useful for generating flexible data sets underlying data tools and apps
such as the Census Bureau's OnTheMap.  

It  is important to keep in mind that the utility of synthetic data sets as a general purpose “anonymization” tool is fairly limited. Synthetic data generation typically requires explicitly defining which properties of the original data need to be preserved (such as univariate or bivariate distributions of certain variables), and as such can be of limited use in most social science research.

**Research data centers**

The second approach is establishing research data centers (RDC). RDC present an established operational approach to facilitate access to confidential microdata for research and/or statistical purposes. This approach is based on the theoretical framework of the "Five Safes" which was initially developed by Felix Ritchie at the UK Office of National Statistics in 2003 [@desaietal2016]. The first dimension refers to safe projects. This dimension mainly refers to the whether the intended use of the data conforms with the use specified in legislations or regulations. For example, a legislation may specifically allow users to use the data only for independent scientific research. Safe people, the second dimension of the Five Saves framework, requires data users to be able to use the data in an appropriate way. A certain amount of technical skills or minimum educational levels may be required to access the data. In contrast, safe data refers to the potential to de-identifying individuals or entities in the data. Safe settings relate to the practical controls on how the data are accessed. Different channels may exist which in turn may depend on the de-identifcation risk. In practice, the lower the de-identifcation risk the more restrictive the setting will be. Lastly, safe output refers to the risk of de-identifcation in publications from confidential microdata. Strong input and output controls are in place to ensure that published findings comply with the privacy and confidentiality regulations
[@hayden2012broken]. 


Non-Tabular data
-------------------
In addition to tabular data, a lot of new sources of data consist of text, audio, image, and video content.  The above approaches primarily deal with maintaining the privacy and confidentiality of entities in tabular data but it is equally important to do the same in non-tabular data. Medical records, sensitive crime records, notes and comments in administrative records, camera footage (from police body-cams or security cameras for example) are all examples of data that   is being used for analysis and requires robust techniques to maintain the privacy and confidentiality of individuals.Although the techniques there are not as mature, there is some work in these areas:

Text Anonymization. Typical approaches here range from simply removing Personally identifiable information (PII) through regular expressions and dictionaries (cite:https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/1472-6947-8-32)  to machine learning based approaches that balance the confidentiality of the entities in the data and the utility of the text (cite: https://www.aaai.org/ocs/index.php/IAAI/IAAI-11/paper/viewPaper/3528)
Image and Video Anonymization: The  most common use of anonymization techniques  in image and video data is to redact, blur, or remove faces of individuals in order to protect their identity. This can be extended to other attributes of the person, such as clothing or the rest of the body but the primary focus so far has been on detecting, and then blurring or modifying the faces of individuals in the data. https://www.spiedigitallibrary.org/journals/journal-of-electronic-imaging/volume-26/issue-05/051406/Video-redaction-a-survey-and-comparison-of-enabling-technologies/10.1117/1.JEI.26.5.051406.full?SSO=1 provide a survey of video redaction methods.  Cite: https://arxiv.org/abs/1909.04538 recently presented a method to automatically anonymize faces in images while retaining the original data distribution.

The new challenges
------------------

While there are well-established policies and protocols surrounding
access to and use of survey and administrative data, a major new
challenge is the lack of clear guidelines governing the collection of
data about human activity in a world in which all public, and some
private, actions generate data that can be harvested
[@house2014big; @ohm2010broken; @Strandburg2014]. The twin pillars on
which so much of social science have rested---informed consent and
anonymization---are virtually useless in a big data setting where
multiple data sets can be and are linked together using individual
identifiers by a variety of players beyond social scientists with formal
training and whose work is overseen by institutional review boards. This
rapid expansion in data and their use is very much driven by the
increased utility of the linked information to businesses, policymakers,
and ultimately the taxpayer. In addition, there are no obvious data
stewards and custodians who can be entrusted with preserving the privacy
and confidentiality with regard to both the source data collected from
sensors, social media, and many other sources, and the related analyses
[@lane2013me].

It is clear that informed consent as historically construed is no longer
feasible. As Nissenbaum [@nissenbaum2011contextual] points out,
notification is either comprehensive or comprehensible, but not both.
While ideally human subjects are offered true freedom of choice based on
a sound and sufficient understanding of what the choice entails, in
reality the flow of data is so complex and the interest in the data
usage so diverse that simplicity and clarity in the consent statement
unavoidably result in losses of fidelity, as anyone who has accepted a
Google Maps agreement is likely to understand [@check2015researchers].
In addition, informed consent requires a greater understanding of the
breadth of type of privacy breaches, the nature of harm as diffused over
time, and an improved valuation of privacy in the big data context.
Consumers may value their own privacy in variously flawed ways. They
may, for example, have incomplete information, or an overabundance of
information rendering processing impossible, or use heuristics that
establish and routinize deviations from rational decision-making
[@Acquisti2014].

It is also nearly impossible to truly anonymize data. Big data are often
structured in such a way that essentially everyone in the file is
unique, either because so many variables exist or because they are so
frequent or geographically detailed, that they make it easy to
reidentify individual patterns [@narayanan2008robust]. It is also no
longer possible to rely on sampling or measurement error in external
files as a buffer for data protection, since most data are not in the
hands of statistical agencies.

There are no data stewards controlling access to individual data. Data
are often so interconnected (think social media network data) that one
person's action can disclose information about another person without
that person even knowing that their data are being accessed. The group
of students posting pictures about a beer party is an obvious example,
but, in a research context, if the principal investigator grants access
to the proposal, information could be divulged about colleagues and
students. In other words, volunteered information of a minority of
individuals can unlock the same information about many---a type of
"tyranny of the minority" [@barocas2014bigger].

There are particular issues raised by the new potential to link
information based on a variety of attributes that do not include PII.
Barocas and Nissenbaum write as follows [@barocas2014big]:

> Rather than attempt to deanonymize medical records, for instance, an
> attacker (or commercial actor) might instead infer a rule that relates
> a string of more easily observable or accessible indicators to a
> specific medical condition, rendering large populations vulnerable to
> such inferences even in the absence of PII. Ironically, this is often
> the very thing about big data that generate the most excitement: the
> capacity to detect subtle correlations and draw actionable inferences.
> But it is this same feature that renders the traditional protections
> afforded by anonymity (again, more accurately, pseudonymity) much less
> effective.

In light of these challenges, Barocas and Nissenbaum continue

> the value of anonymity inheres not in namelessness, and not even in
> the extension of the previous value of namelessness to all uniquely
> identifying information, but instead to something we called
> "reachability," the possibility of knocking on your door, hauling you
> out of bed, calling your phone number, threatening you with sanction,
> holding you accountable---with or without access to identifying
> information.

It is clear that the concepts used in the larger discussion of privacy
and big data require updating. How we understand and assess harms from
privacy violations needs updating. And we must rethink established
approaches to managing privacy in the big data context. The next section
discusses the framework for doing so.

Legal and ethical framework
---------------------------

The Fourth Amendment to the US Constitution, which constrains the
government's power to "search" the citizenry's "persons, houses, papers,
and effects" is usually cited as the legal framework for privacy and
confidentiality issues. In the US a "sectoral" approach to privacy
regulation, for example, the Family Education Rights and Privacy Act and
the Health Insurance Portability and Accountability Act, is also used in
situations where different economic areas have separate privacy laws
[@Ohm2014]. In addition, current legal restrictions and guidance on data
collection in the industrial setting include the Fair Information
Practice Principles dating from 1973 and underlying the Fair Credit
Reporting Act from 1970 and the Privacy Act from 1974 [@Strandburg2014].
Federal agencies often have statutory oversight, such as Title 13 of the
US Code for the Census Bureau, the Confidential Information Protection
and Statistical Efficiency Act for federal statistical agencies, and
Title 26 of the US Code for the Internal Revenue Service.

Yet the generation of big data often takes place in the open, or through
commercial transactions with a business, and hence is not covered by
these frameworks. There are major questions as to what is reasonably
private and what constitutes unwarranted intrusion [@Strandburg2014].
There is a lack of clarity on who owns the new types of data---whether
it is the person who is the subject of the information, the person or
organization who collects these data (the data custodian), the person
who compiles, analyzes, or otherwise adds value to the information, the
person who purchases an interest in the data, or society at large. The
lack of clarity is exacerbated because some laws treat data as property
and some treat it as information [@Cecil2003].

The ethics of the use of big data are also not clear, because analysis
may result in being discriminated against unfairly, being limited in
one's life choices, being trapped inside stereotypes, being unable to
delineate personal boundaries, or being wrongly judged, embarrassed, or
harassed. There is an entire research agenda to be pursued that examines
the ways that big data may threaten interests and values, distinguishes
the origins and nature of threats to individual and social integrity,
and identifies different solutions [@boyd2012critical]. The approach
should be to describe what norms and expectations are likely to be
violated if a person agrees to provide data, rather than to describe
what will be done during the research.

What is clear is that most data are housed no longer in statistical
agencies, with well-defined rules of conduct, but in businesses or
administrative agencies. In addition, since digital data can be alive
forever, ownership could be claimed by yet-to-be-born relatives whose
personal privacy could be threatened by release of information about
blood relations.

The new European Data Protection Regulation (GDPR), which is in effect since May, 2018, was designed to address some of the challenges.  In addition to ensuring lawful data collection practices, GDPR pushes for purpose limitation and data minimisation. This principle requires organisations to clearly state for what purpose personal data is collected, to collect the data only for the time needed to complete the purpose, and to collect only those personal data that is needed to achieve the specified processing purposes. In the U.S. the California Consumer Privacy Act (CCPA) is in effect since January 2020, and here too companies have now have time limits to process customer data. 

However, GDPR and other regulations of this type, still rely on traditional regulatory tools for managing privacy, which is notice, and consent. Both have failed to provide a viable market mechanism allowing a form of self-regulation governing industry data collection. Going forward, a more nuanced assessment of tradeoffs in the big data context, moving
away from individualized assessments of the costs of privacy violations,
is needed [@Strandburg2014]. 

Ohm advocates for a new conceptualization of legal policy regarding privacy in the big data context that uses five guiding principles for reform: first, that rules take into account the
varying levels of inherent risk to individuals across different data
sets; second, that traditional definitions of PII need to be rethought;
third, that regulation has a role in creating and policing walls between
data sets; fourth, that those analyzing big data must be reminded, with
a frequency in proportion to the sensitivity of the data, that they are
dealing with people; and finally, that the ethics of big data research
must be an open topic for continual reassessment [@Ohm2014].

Summary
-------

The excitement about how big data can change the social science research
paradigm should be tempered by a recognition that existing ways of
protecting privacy confidentiality are no longer viable [@karr2014analytical].
There is a great deal of research that can be used to inform the
development of such a structure, but it has been siloed into
disconnected research areas, such as statistics, cybersecurity, and
cryptography, as well as a variety of different practical applications,
including the successful development of remote access secure data
enclaves. We must piece together the knowledge from these various fields
to develop ways in which vast new sets of data on human beings can be
collected, integrated, and analyzed while protecting them [@lane2014].

It is possible that the confidentiality risks of disseminating data may
be so high that traditional access models will no longer hold; that the
data access model of the future will be to take the analysis to the data
rather than the data to the analyst or the analyst to the data. One
potential approach is to create an integrated system including (a)
unrestricted access to highly redacted data, most likely some version of
synthetic data, followed by (b) means for approved researchers to access
the confidential data via remote access solutions, combined with (c)
verification servers that allows users to assess the quality of their
inferences with the redacted data so as to be more efficient with their
use (if necessary) of the remote data access. Such verification servers
might be a web-accessible system based on a confidential database with
an associated public micro-data release, which helps to analyze the
confidential database [@karr2014analytical]. Such approaches are
starting to be developed, both in the USA and in Europe
[@Elias2014; @jones2006administrative].

There is also some evidence that people do not require complete
protection, and will gladly share even private information provided that
certain social norms are met [@Wilbanks2014; @Pentland2014]. There is a
research agenda around identifying those norms as well; characterizing
the interests and wishes of actors (the information senders and
recipients or providers and users); the nature of the attributes
(especially types of information about the providers, including how
these might be transformed or linked); and identifying transmission
principles (the constraints underlying the information flows).

However, it is likely that it is no longer possible for a lone social
scientist to address these challenges. One-off access agreements to
individuals are conducive to neither the production of high-quality
science nor the high-quality protection of data [@schermann2014big]. The
curation, protection, and dissemination of data on human subjects cannot
be an artisan activity but should be seen as a major research
infrastructure investment, like investments in the physical and life
sciences [@bird2011computing; @abazajian2009seventh; @human2010catalog].
In practice, this means that linkages become professionalized and
replicable, research is fostered within research data centers that
protect privacy in a systematic manner, knowledge is shared about the
process of privacy protections disseminated in a professional fashion,
and there is ongoing documentation about the value of evidence-based
research. It is thus that the risk--utility tradeoff depicted in
Figure \@ref(fig:fig11-1) can
be shifted in a manner that serves the public good.

Resources
---------

The American Statistical Association's Privacy and Confidentiality
website provides a useful source of information
[@AmericanStatisticalAssociation].

An overview of federal activities is provided by the Confidentiality and
Data Access Committee of the Federal Committee on Statistics and
Methodology [@ConfidentialityandDataAccessCommittee].

The World Bank and International Household Survey Network provide a good
overview of data dissemination "best practices"
[@InternationalHouseholdSurveyNetwork].

There is a *Journal of Privacy and Confidentiality* based at Carnegie
Mellon University [@JPC], and also a journal called *Transactions in
Data Privacy* [@TransactionsonDataPrivacy].

The United Nations Economic Commission on Europe hosts workshops and
conferences and produces occasional reports
[@UnitedNationsEconomicCommissionforEurope].

Collection of lectures from the semester on privacy at the Simons Institute for the Theory of Computing https://simons.berkeley.edu/programs/privacy2019 (available on youtube https://www.youtube.com/user/SimonsInstitute/




