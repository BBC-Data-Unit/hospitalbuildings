# NHS crisis: Patient care hit by disrepair in buildings

![Beams and props holding up parts of the ceiling at a Norfolk hospital](https://ichef.bbci.co.uk/news/976/cpsprodpb/2DE4/production/_125684711_16079512-877c-4545-bb73-f8328783cc10.png.webp)

In February 2024 The Shared Data Unit (SDU) [looked at the scale of the backlog of repairs affecting hospitals, and the human impact of those](https://www.bbc.co.uk/news/uk-england-68214879): thousands of potentially-harmful incidents including critically-ill patients being moved when rainfall came through the ceiling.

A [custom website](https://hospitalbuildings.github.io/site2/index.html) was created for partners to find out the story in their area, including custom visualisation. 

## Methodology

We analysed data from the last five years of the NHS’s [Estates Returns Information Collection (ERIC)](https://digital.nhs.uk/data-and-information/publications/statistical/estates-returns-information-collection) to look at the cost of the backlog of repairs facing hospitals in the NHS. These repairs are grouped into four risk areas: “low”, “moderate”, “significant”, and “high risk”. To ensure that comparisons were accurate, historical costs were adjusted for inflation using the Construction output price indices on all construction (new work and repair and maintenance).

In some cases trusts have merged to create new trusts. Where possible we have used old trusts’ figures to provide historical context to the new trust’s repair costs, using [NHS data on successor organisations](https://digital.nhs.uk/services/organisation-data-service/export-data-files/csv-downloads/miscellaneous).

Data on clinical incidents was taken from the same dataset. These are defined as those leading to “services being delayed, cancelled or otherwise interfered with owing to problems or failures related to the estates and infrastructure failure.” Incidents include problems with electrical, water or ventilation systems, internal fabric and fixtures, roofs and structures, or lifts and hoists.

Before 2021 this was only provided at trust level, so we have limited our analysis to the two latest years during which data has been provided at site level. In the most recent data hospitals also provide (where incidents have been recorded) data on the first, second, and third most clinically impactful incident type, and so we have included this too.

Further information on the methodology can be found in a [dedicated methodology document](https://docs.google.com/document/d/1wVUgjH1YpWRKX2Tthkbf0i0XoI9p6giUbI-emnzhDsE/edit?usp=sharing)

## Data

* NHS Digital: [Estates Returns Information Collection (ERIC)](https://digital.nhs.uk/data-and-information/publications/statistical/estates-returns-information-collection)
* [NHS data on successor organisations](https://digital.nhs.uk/services/organisation-data-service/export-data-files/csv-downloads/miscellaneous)
* ONS: [Construction output price indices](https://www.ons.gov.uk/businessindustryandtrade/constructionindustry/datasets/interimconstructionoutputpriceindices)
* [Hospital FOI responses](https://docs.google.com/spreadsheets/d/1VWCysIpaq0H3xh8XxbEMo73EmeIJbdzfcaCg-koqJw0/edit?usp=sharing)

## Scripts

As well as the Python notebook to gather, combine and clean the data on hospital buildings, R notebooks were used to create a bespoke analysis for 112 separate trusts, and publish that as a webpage with a page detailing the picture at each trust. The code for those notebooks is available in this repo in [the scripts folder](https://github.com/BBC-Data-Unit/hospitalbuildings/tree/main/scripts) and at the links below.

* [Python notebook that fetches, combines, cleans and analyses the ERIC data on repairs backlogs](https://github.com/BBC-Data-Unit/hospitalbuildings/blob/main/scripts/hospitalBuildingsAnalysisREPAIRS.ipynb)
* [Python notebook that fetches, combines, cleans and analyses the ERIC incident data](https://github.com/BBC-Data-Unit/hospitalbuildings/blob/main/scripts/hospitalBuildingsAnalysisINCIDENTS.ipynb)
* [R notebook that generates the homepage for the story website](https://github.com/BBC-Data-Unit/hospitalbuildings/blob/main/scripts/index.Rmd)
* [R notebook that generates a 'template' page for each hospital trust](https://github.com/BBC-Data-Unit/hospitalbuildings/blob/main/scripts/01templateBYTRUST.Rmd)
* [R notebook that 'renders' that template into 120 different markdown files - one for each hospital trust](https://github.com/BBC-Data-Unit/hospitalbuildings/blob/main/scripts/02render.Rmd)
* [R notebook that renders those 112 markdown files as HTML versions](https://github.com/BBC-Data-Unit/hospitalbuildings/blob/main/scripts/03renderhtml.Rmd)
* [R notebook that cleans those HTML files and adds extra elements such as navigation, charts, etc.](https://github.com/BBC-Data-Unit/hospitalbuildings/blob/main/scripts/04cleaning.Rmd)

## Partner usage

* Alton Herald: [Tens of millions of pounds needed to repair crumbling buildings at Southern Health](https://www.altonherald.com/news/tens-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-southern-health-667125)
* Andover Advertiser: [Floods and sewage leaks among incidents reported by HHFT](https://www.andoveradvertiser.co.uk/news/24131780.floods-sewage-leaks-among-incidents-reported-hhft/)
* BBC London: [Leaks and extreme temperatures affecting patient care in London](https://www.bbc.co.uk/news/uk-england-london-68350346)
* BBC London: [Hospitals: A look inside St Mary's Hospital in Paddington](https://www.bbc.co.uk/news/av/uk-england-london-68364140)
* BBC North East: [Hospitals hit by power cuts as repair bills soar](https://www.bbc.co.uk/news/articles/ce7lkwxd894o)
* BBC North East: [Hospital bosses not doing jobs, says councillor](https://www.bbc.co.uk/news/articles/cq5xn9y0ddko)
* BBC Oxford: [Oxford University Hospitals facing large urgent repair backlog](https://www.bbc.co.uk/news/uk-england-oxfordshire-68359066)
* Bedford Independent: [Bedford Hospital Trust sees high-risk repairs bill rise by 161%](https://www.bedfordindependent.co.uk/bedford-hospital-trust-sees-high-risk-repairs-bill-rise-by-161/)
* Bedford Today: [More than £100m needed to repair crumbling buildings at Bedfordshire Hospitals Trust](https://www.bedfordtoday.co.uk/health/more-than-ps100m-needed-to-repair-crumbling-buildings-at-bedfordshire-hospitals-trust-4528134)
* Bicester Advertiser: [Oxfordshire hospitals require £240m of repairs - new figures](https://www.bicesteradvertiser.net/news/24132995.oxfordshire-hospitals-require-240m-repairs---new-figures/)
* Birmingham World: [Tens of millions of pounds needed to repair crumbling buildings at Birmingham Women's and Children's Hospital](https://www.birminghamworld.uk/your-birmingham/birmingham/tens-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-birmingham-womens-and-childrens-hospital-4526309)
* BNN Breaking: [Wycombe Hospital's Scaffolding Saga: A Visible Symptom of the NHS Maintenance Crisis](https://bnnbreaking.com/breaking-news/health/wycombe-hospitals-scaffolding-saga-a-visible-symptom-of-the-nhs-maintenance-crisis)
* BNN Breaking: [Crumbling Legacy: London's NHS Hospitals Face a High-Risk Repair Crisis](https://bnnbreaking.com/politics/crumbling-legacy-londons-nhs-hospitals-face-a-high-risk-repair-crisis)
* BNN Breaking: [Southampton Hospital Faces £130M Repair Crisis: Doctors Slam NHS Infrastructure Neglect](https://bnnbreaking.com/breaking-news/health/southampton-hospital-faces-130m-repair-crisis-doctors-slam-nhs-infrastructure-neglect)
* Bolton News: [Royal Bolton Hospital's bid for new build rejected](https://www.theboltonnews.co.uk/news/24136608.royal-bolton-hospitals-bid-new-build-rejected/)
* Bracknell News: [Hospitals in Berkshire require millions of pounds in repairs](https://www.bracknellnews.co.uk/news/24142134.hospitals-berkshire-require-millions-pounds-repairs/)
* Bracknell News: [Reading hospital heating breakdown led to care delays](https://bracknellnews.co.uk/news/24180821.reading-hospital-heating-breakdown-led-care-delays/)
* Brighton Argus: [Millions of pounds needed to fix crumbling Sussex hospital buildings](https://www.theargus.co.uk/news/24151881.millions-pounds-needed-fix-crumbling-sussex-hospital-buildings/)
* Bristol World: [Tens of millions of pounds needed to repair crumbling buildings at the North Bristol Trust](https://www.bristolworld.com/your-bristol/south-gloucestershire/tens-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-the-north-bristol-trust-4526277)
* Bucks Free Press: [Bucks NHS Trust faces £100 million repairs backlog](https://www.bucksfreepress.co.uk/awards/bhsc-awards-2021/news/24131107.bucks-nhs-trust-faces-100-million-repairs-backlog/)
* The Bucks Herald: [Buckinghamshire NHS Trust faces £100 million high-risk repairs backlog](https://www.bucksherald.co.uk/health/buckinghamshire-nhs-trust-faces-ps100-million-high-risk-repairs-backlog-4526934)
* The Bucks Herald: [Shadow health secretary labels 'sticky plaster politics' as key reason for NHS building issues in Bucks and beyond](https://www.bucksherald.co.uk/news/politics/shadow-health-secretary-labels-sticky-plaster-politics-as-key-reason-for-nhs-building-issues-in-bucks-and-beyond-4529524)
* Cambridge Independent: [Cambridge University Hospitals Trust faces £125m repair backlog bill](https://www.cambridgeindependent.co.uk/news/cambridge-university-hospitals-trust-faces-125m-repair-back-9354159/)
* Crediton Courier: [Ageing hospital buildings push up Royal Devon and Exeter Trust’s repair bill](https://www.creditoncourier.co.uk/news/health/ageing-hospital-buildings-push-up-royal-devon-and-exeter-trusts-repair-bill-668121)
* Devon Live: [Devon hospital trust's massive repair bill revealed](https://www.devonlive.com/news/devon-news/devon-hospital-trusts-massive-repair-9121391)
* Essex Live: [The £101m of repairs needed to fix the hospitals falling apart across Essex](https://www.essexlive.news/news/essex-news/101m-repairs-needed-fix-hospitals-9143880)
* Falmouth Packet: [Royal Cornwall Hospital millions need to repair buildings](https://www.falmouthpacket.co.uk/news/24149188.royal-cornwall-hospital-millions-need-repair-buildings/)
* Greatest Hits Radio: [Bucks NHS faces £100m repairs backlog](https://planetradio.co.uk/greatest-hits/beds-bucks-herts/news/bucks-nhs-faces-pound100m-repairs-backlog/)
* Greatest Hits Radio: [Over £55million needed to repair hospitals across Peterborough, Stamford and Rutland](https://planetradio.co.uk/greatest-hits/cambridgeshire/news/millions-needed-to-repair-peterborough-hospitals/)
* Greatest Hits Radio: [Oxford University Hospitals NHS Foundation Trust among those facing the most repairs](https://planetradio.co.uk/greatest-hits/oxfordshire/news/oxford-university-hospitals-nhs-foundation-trust-among-those-facing-the-most-repairs/)
* Harrow Online: [New figures reveal ‘significant challenge’ of ageing infrastructure at Northwick Park Hospital](https://harrowonline.org/2024/02/22/new-figures-reveal-significant-challenge-of-ageing-infrastructure-at-northwick-park-hospital/)
* Herts Advertiser: [West Hertfordshire: Almost £70m needed for hospital repairs](https://www.hertsad.co.uk/news/24139462.west-hertfordshire-almost-70m-needed-hospital-repairs/)
* Hertfordshire Comet: [Hertfordshire: Millions needed for repairs at NHS buildings](https://www.thecomet.net/news/24143678.hertfordshire-millions-needed-repairs-nhs-buildings/)
* Hucknall Dispatch: [Hundreds of millions of pounds needed to repair crumbling buildings at Nottingham University Hospitals Trust](https://www.hucknalldispatch.co.uk/news/people/hundreds-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-nottingham-university-hospitals-trust-4529252)
* Hucknall Dispatch: [More than £10 million needed to repair crumbling buildings at Nottinghamshire Healthcare Trust](https://www.hucknalldispatch.co.uk/news/people/more-than-ps10-million-needed-to-repair-crumbling-buildings-at-nottinghamshire-healthcare-trust-4537696)
* Hull Daily Mail: [Hull hospitals hit by water leak and broken lifts as repair bill reaches £84m](https://www.hulldailymail.co.uk/news/hull-east-yorkshire-news/hull-hospitals-face-water-leaks-9117770)
* Lincolnshire World: [Tens of millions of pounds needed to repair crumbling buildings at United Lincolnshire Hospitals Trust](https://www.lincolnshireworld.com/lincolnshire/grantham/tens-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-united-lincolnshire-hospitals-trust-4526244)
* Lincs Online: [Outdated hospital buildings and failing equipment serving Lincolnshire patients – report](https://www.lincsonline.co.uk/spalding/news/the-outdated-hospital-buildings-and-failing-equipment-servin-9353722/)
* Liverpool World: [Tens of millions of pounds needed to repair crumbling buildings at Liverpool University Hospitals Trust](https://www.liverpoolworld.uk/your-merseyside/liverpool/tens-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-liverpool-university-hospitals-trust-4526268)
* Liverpool World: [More than £1 million needed to repair crumbling buildings at Alder Hey Children's Hospital](https://www.liverpoolworld.uk/your-merseyside/liverpool/more-than-ps1-million-needed-to-repair-crumbling-buildings-at-alder-hey-childrens-hospital-4526305)
* London Evening Standard: [£3bn needed to fix London’s crumbling hospitals amid safety warning](https://www.standard.co.uk/news/health/london-hospitals-repair-patient-safety-b1138171.html)
* London World: [Millions of pounds needed to repair crumbling buildings at Moorfields Eye Hospital Trust](https://www.londonworld.com/your-london/islington/millions-of-pounds-needed-to-repair-crumbling-buildings-at-moorfields-eye-hospital-trust-4526275)
* Luton Today: [More than £100m needed to repair crumbling buildings at Bedfordshire Hospitals Trust](https://www.lutontoday.co.uk/health/more-than-ps100m-needed-to-repair-crumbling-buildings-at-bedfordshire-hospitals-trust-4528134)
* Manchester Evening News: [Find out here how much is needed to fix your local hospital as region faces £500m bill](https://www.manchestereveningnews.co.uk/news/greater-manchester-news/find-out-here-how-much-28686505)
* Mansfield and Ashfield Chad: [Sherwood Forest Hospitals Trust bucks trend with all buildings in full working order](https://www.chad.co.uk/health/sherwood-forest-hospitals-trust-bucks-trend-with-all-buildings-in-full-working-order-4529040)
* Medriva: [Urgent Repair Backlogs and the State of Hospital Infrastructure in England: A Close Look at St. Mary's Hospital in Paddington](https://medriva.com/breaking-news/urgent-repair-backlogs-and-the-state-of-hospital-infrastructure-in-england-a-close-look-at-st-marys-hospital-in-paddington/)
* Medriva: [Urgent Backlog of Repairs at Oxford University Hospitals: A Call for Investment in Healthcare Infrastructure](https://medriva.com/health/healthcare/urgent-backlog-of-repairs-at-oxford-university-hospitals-a-call-for-investment-in-healthcare-infrastructure/)
* Milton Keynes Citizen: [Tens of millions of pounds needed to repair crumbling buildings at Milton Keynes University Hospital](https://www.miltonkeynes.co.uk/news/people/tens-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-milton-keynes-university-hospital-4529101)
* MyLondon: [Hillingdon Hospital in desperate need of improvements 'still waiting on funding'](https://mylondon.news/news/west-london-news/hillingdon-hospital-desperate-need-improvements-28737913)
* Newcastle World: [Tens of millions of pounds needed to repair crumbling buildings at the South Tyneside and Sunderland Trust](https://www.newcastleworld.com/your-newcastle/south-tyneside/tens-of-millions-of-pounds-needed-to-repair-crumbling-buildings-at-the-south-tyneside-and-sunderland-trust-4526267)
* Nottingham Post: [Nottingham hospitals in 'dreadful state' as repairs backlog rises to nearly £440m](https://www.nottinghampost.com/news/nottingham-news/nottingham-hospitals-dreadful-state-repairs-9114146)
* Nottinghamshire Live: [Nottingham hospitals in 'dreadful state' as repairs backlog rises to nearly £440m](https://www.nottinghampost.com/news/nottingham-news/nottingham-hospitals-dreadful-state-repairs-9114146)
* Radio Exe: [‘Unforgivable’ backlog of South Devon hospital repairs](https://www.radioexe.co.uk/news-and-features/local-news/unforgivable-backlog-of-south-devon-hospital-repairs/)
* Reading Today: [Heating failure at Reading hospital causes disruption](https://rdg.today/heating-failure-at-reading-hospital-causes-disruption/)
* Signal1 Radio: [UHNM repairs backlog hits £34.7m](https://planetradio.co.uk/signal1/local/news/uhnm-repairs-backlog-hits-pound347m/)
* Southern Daily Echo: [Southampton hospital buildings need repairs costing £128m](https://www.dailyecho.co.uk/news/24136356.southampton-hospital-buildings-need-repairs-costing-128m/)
* Suffolk News: [Large repair bill for West Suffolk NHS Foundation Trust due to ‘ageing estate and RAAC’ at West Suffolk Hospital site in Bury St Edmunds](https://www.suffolknews.co.uk/bury-st-edmunds/news/amp/safety-is-our-priority-hospital-s-trust-has-one-of-bigges-9353322/)
* TFM (Planet Radio): [Nearly 40 million pounds needed for hospital repair work at James Cook in Middlesbrough](https://planetradio.co.uk/tfm/local/news/nearly-40-million-pounds-needed-james-cook-hospital-middlesbrough-repair-work/)
* Westmoreland Gazette: [Furness General Hospital needs £19.7 million in repairs](https://www.thewestmorlandgazette.co.uk/news/24135397.furness-general-hospital-needs-19-7-million-repairs/)
* Wigan Today: [Tens of millions of pounds needed to repair Wigan hospital buildings despite being top ranked for maintenance](https://www.wigantoday.net/health/tens-of-millions-of-pounds-needed-to-repair-wigan-hospital-buildings-despite-being-top-ranked-for-maintenance-4545328)
* Yahoo! News UK: [£240 MILLION needed to carry out necessary repairs to Oxford hospitals](https://uk.news.yahoo.com/240-million-needed-carry-necessary-123000215.html)
* Yahoo! News UK: [£34 million needed to restore crumbling buildings at York hospital trust](https://uk.news.yahoo.com/34-million-needed-restore-crumbling-040000194.html)
* Yahoo! News UK: [£30 million needed to restore 'crumbling' buildings at Warrington and Halton Hospital](https://uk.news.yahoo.com/30-million-needed-restore-crumbling-050000106.html)
* Yahoo! News UK: [Almost £15m needed to repair buildings at Lancs hospital trust](https://uk.news.yahoo.com/almost-15m-needed-repair-buildings-050000823.html)

In addition, the story was covered across BBC television and radio, including packages by Hugh Pym for BBC Breakfast and Alix Hattenstone for Radio 4’s Today Programme. Questions were put to the health secretary Victoria Atkins on both programmes. BBC South West's 6.30 news programme carried the story, as did news bulletins on Radio 2, Radio 4 and Radio 5. Pieces were broadcast across 16 local radio outlets in total: Yorkshire, Scotland, Ulster, Northampton, Suffolk, Oxford, Three Counties, Surrey, Wiltshire, Nottingham, Lincolnshire, Cumbria, Cambridgeshire, London, Shropshire and Berkshire. On the Sunday following publication the matter was [discussed on Politics North](https://www.bbc.co.uk/news/articles/cq5xn9y0ddko).

![Victoria Atkins](https://raw.githubusercontent.com/BBC-Data-Unit/hospitalbuildings/main/victoriaatkins.jpeg)

Data from the project was also used by the BBC England Data Unit during the 2024 general election in its article [NHS: Your concerns, questions and stories](https://www.bbc.co.uk/news/extra/uzeufqrb78/nhs_your_voice_your_vote)

