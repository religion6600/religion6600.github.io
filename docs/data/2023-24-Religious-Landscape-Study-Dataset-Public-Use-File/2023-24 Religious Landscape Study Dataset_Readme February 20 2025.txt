PEW RESEARCH CENTER
2023-24 Religious Landscape Study (RLS) 
Dates: July 17, 2023 - March 4, 2024
Modes: Web, Paper, Inbound Phone
Sample: ABS, managed by NORC for Pew Research Center 
Languages: English, Spanish
N=36,908

***************************************************************************************************************************

NOTES 

Pew Research Center's 2023-24 Religious Landscape Study (RLS) is a national cross-sectional survey of U.S. adults. The study was made possible by The Pew Charitable Trusts, which received support from the Lilly Endowment Inc., Templeton Religion Trust, The Arthur Vining Davis Foundations and the M.J. Murdock Charitable Trust. 

The public use file (PUF) is available to all users at www.pewresearch.org. We also intend to make the PUF available to all users via ICPSR at a future date. Also at a future date, we intend to make a restricted use file (RUF) accessible via ICPSR with a data use agreement. Questions about the survey and the data files can be sent to info@pewresearch.org. 

Both the PUF and the RUF include all 36,908 respondents. The variables in the datasets roughly follow the order of the paper questionnaire. The PUF excludes the following sensitive variables, which will be available only in the RUF.
	DENOMREC2
	FAMILY
	PROTFAM
	CURREL2
	BRANCH
	FRMREL2
	SPREL
	SPREL2
	SPBORNFINAL
	KIDS4ANDUNDERREC
	KIDS5TO12REC
	KIDS13TO17REC
	BIRTHHALFDECADE
	RESPONDENT_BIRTHREGION
	MOTHER_BIRTHREGION
	FATHER_BIRTHREGION
	YEARSINUSREC
	CITIZEN
	ORIENTMOD
	REGION
	STATE
	MSA
	WEIGHT_MSA

There are 6 documents accompanying these datasets (provided as both SPSS and CSV files) and Readme file: 
1) English paper questionnaire
2) Spanish paper questionnaire
3) Web/phone questionnaire (including both English and Spanish specifications)
4) One codebook detailing the values and labels for variables included in the public-use and restricted-use datasets 
5) One detailed methodology statement outlining the methodology for the survey
6) One document explaining how the RLS categorizes religion


The datasets contain the following backcoded variables, based on open-ended responses. To protect the confidentiality of respondents, the original variables and open-end responses are not released. 
-	DENOMREC2, FAMILY, RELTRAD, PROTFAM, BRANCH are variables describing the respondent's current religious affiliation, based on RELIG-QA4p and BRANCH in the web/phone questionnaire and Q.22-24 and Q.28 in the paper questionnaire
-	CURREL is a recoded version of RELTRAD that collapses Protestants into a single category. CURREL2 is a recode of CURREL with additional detail for Protestants (from PROTFAM) and the religiously unaffiliated (from DENOMREC2)
-	CONGRACE, LEADRACE and CHCONGRACE describe the racial/ethnic composition of the respondent's congregation and childhood congregation
-	FRMREL and FRMREL2 describe the religion in which the respondent was raised, based on CHRELIG-CHA3 in the web/phone questionnaire and questions 66-67 in the paper questionnaire
-	SPREL and SPREL2 describe the religious affiliation of the respondent's spouse or partner, based on SPRELIG-SPA3 in the web/phone questionnaire and questions 79-80 in the paper questionnaire
-	HISP and RACECMB describe the respondent's race and ethnicity
-	RESPONDENT_BIRTHREGION, MOTHER_BIRTHREGION and FATHER_BIRTHREGION describe the place of birth for the respondent and the respondent's parents

The datasets include the following filters: 
-	PAR2CHILDa is based on those who said in PAR2CHILD that children are better off if one parent stays home to focus on the family
-	BORNFINAL is based on those who are Christian in RELTRAD
-	BRANCH is based on those who are Jewish in RELTRAD
-	CONGRACE and LEADRACE are based on those who said in ATTNDPERRLS that they attend religious services at least a few times a year
-	GOD2 is based on those who said "yes" or "no" in GOD
-	HUMNTR_A and HUMNTR_B are based on those who said "yes" in GOD
-	CHBORNFINAL is based on those who were raised Christian in FRMREL
-	CHCONGRACE is based on those who said in CHATTEND that as a child they attended religious services at least a few times a year
-	SPREL, SPREL2, RELMATCH, SPRELIMP, SPRELTALK, and SPRELSIM are based on those who are married or living with a partner in MARITAL
-	SPBORNFINAL is based on those whose spouse/partner is Christian in SPREL
-	MARWHENREC is based on those who are married in MARITAL
-	KIDS4ANDUNDERREC, KIDS5TO12REC, KIDS13TO17REC, KIDACT_A, KIDACT_B, and KIDACT_C are based on those who said in CHILDREN that they are the parent/guardian of a child living in their household
-	PARTYLN is based on those who said "independent," "something else" or did not answer PARTY
-	YEARSINUSREC is based on those who were born outside the U.S. (RESPONDENT_BIRTHREGION=2-10)
-	HH3REC is based on those who said in HH1REC that they live in a multi-person household
-	WEIGHT_MSA is based on those who live in one of 34 large metro areas indicated in MSA

The datasets were cleaned and recoded as indicated below:
-	RELCON_a-e are set to "Respondent is __ by religion" if the respondent identifies in RELTRAD with the religion in question
-	KIDS4ANDUNDERREC, KIDS5TO12REC, and KIDS13TO17REC are dummy variables (rather than counts) indicating whether the respondent has children in each age range
-	CITIZEN is set to "1" for all respondents who were born in the U.S. or Puerto Rico
-	REG is set to "2" for all respondents who said "no" or "not sure" in REG, as well as for those who did not answer REG and those who are not citizens in CITIZEN
-	MARWHENREC is a coarsened version of the respondent's year of marriage
-	RELMATCH is an indicator of whether CURREL matches SPREL (for analysis of religious intermarriage)
-	HH1REC and HH3REC are capped at 3
-	FERTREC is capped at 4
-	EDUCREC is a coarsened version of the respondent's educational attainment
-	BIRTHDECADE and BIRTHHALFDECADE are coarsened versions of the respondent's year of birth
-	YEARLOCREC is a coarsened version of the number of years the respondent has lived in their community
-	RESPONDENT_BIRTHREGION, MOTHER_BIRTHREGION, and FATHER_BIRTHREGION are coarsened versions of country of birth for the respondent and the respondent's parents
-	YEARSINUSREC is a coarsened version of the number of years the respondent has lived in the U.S.



***************************************************************************************************************************
WEIGHTS 

WEIGHT is the full sample adult raked weight. REPWT_001 to REPWT_500 are the replicate weights. WEIGHT or the replicate weights should be used for conducting analysis of national- and state-level data. 

Analysis of metro areas should be conducted using WEIGHT_MSA.

Refer to the code below for instructions on setting up the survey design with the full sample adult raked weight and replicate weights using Stata.

*Syntax for designating the survey design in Stata

svyset [pweight=weight], bsrweight(repwt_001-repwt_500) vce(bootstrap)

***************************************************************************************************************************
Releases from this survey (at the time of data publication):

Feb. 26, 2025. "Decline of Christianity in the U.S. Has Slowed, May Have Leveled Off"
https://www.pewresearch.org/religion/2025/02/26/decline-of-christianity-in-the-us-has-slowed-may-have-leveled-off/

Refer also to https://www.pewresearch.org/religious-landscape-study/

