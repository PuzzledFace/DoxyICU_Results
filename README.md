
<!-- README.md is generated from README.Rmd. Please edit that file -->

# DoxyICU Results

This repo provides the raw data and analysis code to support the paper
<em>Doxycycline for the prevention of progression of COVID-19 to severe
disease requiring intensive care unit (ICU) admission: a randomized,
controlled, open-label, parallel group trial (DOXPREVENT.ICU)</em> by
Dhar et al, submitted to the Lancet on 26 December 2021.

The raw data are contained in `data 2021-12 Dec-24.Rds`, the analysis
code in `analysis.Rmd` and the results in `analysis.html`.

# Data description

<table class="table table-striped table-hover table-condensed" style="margin-left: auto; margin-right: auto;">
<thead>
<tr>
<th style="text-align:left;">
variable
</th>
<th style="text-align:left;">
class
</th>
<th style="text-align:left;">
Label
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
UUID
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Unique database ID
</td>
</tr>
<tr>
<td style="text-align:left;">
PatNo
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Patient number. 4 characters left-padded with zeroes. Numbered from 1
within site
</td>
</tr>
<tr>
<td style="text-align:left;">
SiteID
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Site ID. 3 characters left-padded with zeroes.
</td>
</tr>
<tr>
<td style="text-align:left;">
Treatment
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Randomised treatment: `Standard of Care`, `Doxycycline`
</td>
</tr>
<tr>
<td style="text-align:left;">
ICDate
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date of informed consent
</td>
</tr>
<tr>
<td style="text-align:left;">
Sex
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Patient sex: ‘Male’=1, ‘Female’=2 or NA
</td>
</tr>
<tr>
<td style="text-align:left;">
Age
</td>
<td style="text-align:left;">
integer
</td>
<td style="text-align:left;">
Patient age at baseline in completed years
</td>
</tr>
<tr>
<td style="text-align:left;">
Ethnicity
</td>
<td style="text-align:left;">
integer
</td>
<td style="text-align:left;">
Patient ethnicity: ‘White’=1, ‘Black Caribbean’=2, ‘Black African’=3
‘Indian’=4, ‘Pakistani’=5, ‘Bangladeshi’=6, ‘Chinese’=7, ‘Other’=8
</td>
</tr>
<tr>
<td style="text-align:left;">
Temperature
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Patient temperature at baseline in Celsius
</td>
</tr>
<tr>
<td style="text-align:left;">
TemperatureLocation
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Location at which temperature was measured: ‘On forehead’=1, ‘Orally’=2
</td>
</tr>
<tr>
<td style="text-align:left;">
OnsetDate
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date of symptom onset
</td>
</tr>
<tr>
<td style="text-align:left;">
AdmissionDate
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date of hospital admission
</td>
</tr>
<tr>
<td style="text-align:left;">
FinalStatus
</td>
<td style="text-align:left;">
integer
</td>
<td style="text-align:left;">
Final status: ‘Completed 14 days of treatment and discharged’=1,
‘Discharged before completing 14 days of treatment’=2, ‘Discontinued
treatment because of treatment-related adverse events’=3, ‘Discontinued
treatment for reasons unrelated to treatment’=4, ‘Lost to follow-up’=5,
‘Consent withdrawn’=6, ‘Other’=7, ‘Died’=8
</td>
</tr>
<tr>
<td style="text-align:left;">
ICUAdmissionNeeded
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Did the patient need admission to ICU? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
ICUAdmissionSuccess
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Was the patient actually admitted to ICU? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
ICUAdmissionNeededDate
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date on which the patient’s need for ICU admission was determined
</td>
</tr>
<tr>
<td style="text-align:left;">
ICUNonAdmissionReason
</td>
<td style="text-align:left;">
integer
</td>
<td style="text-align:left;">
Why was the patient NOT admitted to ICU? ‘Lack of beds’=1, ‘Patient
unsuitable’=2, ‘Patient declined’=3, ‘Other’=4
</td>
</tr>
<tr>
<td style="text-align:left;">
ICUDischargeDate
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date of ICU discharge
</td>
</tr>
<tr>
<td style="text-align:left;">
HospitalDischargeDate
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date of hospital discharge
</td>
</tr>
<tr>
<td style="text-align:left;">
Alive
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Was the patient alive on the date of last follow-up? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
DateOfDeath
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date of death
</td>
</tr>
<tr>
<td style="text-align:left;">
RelatedDeath
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Was the death related to COVID-19? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
FollowUpDate
</td>
<td style="text-align:left;">
Date
</td>
<td style="text-align:left;">
Date of last follow-up
</td>
</tr>
<tr>
<td style="text-align:left;">
PCRTest
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: Positive PCR test for SARS-CoV-2? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
Hypersensitivity
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: Known hypersensitivity to doxycycline? ‘Yes’=1,
‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
MyastheniaGravis
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: Myasthenia gravis? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
Pregnancy
</td>
<td style="text-align:left;">
integer
</td>
<td style="text-align:left;">
Inclusion/exclusion: Pregnancy? ‘Yes’=1, ‘No’=0 ‘Not applocable’=2
</td>
</tr>
<tr>
<td style="text-align:left;">
Cirrhosis
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: Cirrhosis? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
Dyspnea
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: New continuous cough or dyspnea? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
Diarrhoea
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: Diarrhoea? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
Anosmia
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: Has the patient recently lost their sense of smell?
‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
Pneumonia
</td>
<td style="text-align:left;">
integer
</td>
<td style="text-align:left;">
Inclusion/exclusion: Evidence of pneumonia on x-ray? ‘Yes’=1, ‘No’=0
’X-ray not done\`=2
</td>
</tr>
<tr>
<td style="text-align:left;">
Rash
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Inclusion/exclusion: Does the patient have ‘COVID rash’ or ‘COVID
fingers and toes’? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtDoxycycline
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with doxycycline? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtAntibiotics
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with other antibiotics? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtAnalgesics
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with analgesics? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtDiabetes
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment for diabetes? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtHeartFailure
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment for heart failure? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtAntiHypertensives
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with anti-hypertensives? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtAntiDepressants
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with anti-depressants? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtCancer
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment for cancer? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtImmunosuppressant
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with immunosuppressants? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtSteroids
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with steroids? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtAntiCoagulantsProphylactic
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline prophylactic treatment with anti-coagulants? ‘Yes’=1,
‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtAntiCoagulantsTherapeutic
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline therapeutic treatment with anti-coagulants? ‘Yes’=1,
‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtFavipiravir
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with favipiravir? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtHydroxychloroquine
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with hydroxychloroquine? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtRemdesivir
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with remdesivir? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtTocilizumab
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with tocilizumab? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtIvermectin
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Post-baseline treatment with vermectin? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
TrtOther
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Other relevant post-baseline treatment?Discontinuation due to
</td>
</tr>
<tr>
<td style="text-align:left;">
TreatmentDuration
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Treatment duration: 14 values from ‘1 day’ to ‘14 days’, ‘&gt;14 days’
</td>
</tr>
<tr>
<td style="text-align:left;">
TreatmentDiscontinuationReason
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Reason for dsiscontinuation of treatment: ‘Patient improved, was
discharged or the patient/physician chose not to give the full 14 day
course of treatment’=‘1’, ‘Patient experienced unacceptable
treatment-related side effects’=‘2’, ‘Other reasons’=‘3’
</td>
</tr>
<tr>
<td style="text-align:left;">
AENausea
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to nausea? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AECramps
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to cramps? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AEDiarrhoea
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to diarrhoea? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AETinnitus
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to tinnitus? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AEGenitalSoreness
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to genital soreness? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AERash
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to rash? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AEHeadache
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to headache? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AEVision
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to vision effects? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AEPalpitation
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to palpitations? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
AEOther
</td>
<td style="text-align:left;">
logical
</td>
<td style="text-align:left;">
Discontinuation due to other reasons? ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumILD
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: ILD ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumCOPD
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: COPD ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumBronchiectasis
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: bronchiectasis ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumAsthma
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: asthma ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumOtherLung
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: other lung condition ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumDiabetes
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: diabetes ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumHeartDisease
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: heart disease ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumHypertension
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: hypertension ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumCancer
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: cancer ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumOther
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Risk factor for stratification: other ‘Yes’=1, ‘No’=0
</td>
</tr>
<tr>
<td style="text-align:left;">
StratumCode
</td>
<td style="text-align:left;">
numeric
</td>
<td style="text-align:left;">
Derived stratum code: 1, 2 or 3
</td>
</tr>
<tr>
<td style="text-align:left;">
Stratum
</td>
<td style="text-align:left;">
character
</td>
<td style="text-align:left;">
Derived stratum text: NONE \[0\], LUNG \[1\], OTHER \[2\]
</td>
</tr>
</tbody>
</table>
