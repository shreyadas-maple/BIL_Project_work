# Tau CSV, Columns could be used
EPVS volumetric measures: EPVS_Caudate_Putamen,EPVS_bg,EPVS_bg_large_box,wm.lh.frontal.lobe,wm.lh.cingulate.lobe,wm.lh.occiptal.lobe,wm.lh.temporal.lobe,wm.lh.parietal.lobe,wm.lh.insula.lobe,wm.lh.CSO,wm.rh.frontal.lobe,wm.rh.cingulate.lobe,wm.rh.occiptal.lobe,wm.rh.temporal.lobe,wm.rh.parietal.lobe,wm.rh.insula.lobe,wm.rh.CSO,total_FS_space
Corresponding regional volumetric measures for EPVS: EPVS_Caudate_Putamen_vol,EPVS_bg_vol,EPVS_bg_large_box_vol,wm.lh.frontal.lobe_vol,wm.lh.cingulate.lobe_vol,wm.lh.occiptal.lobe_vol,wm.lh.temporal.lobe_vol,wm.lh.parietal.lobe_vol,wm.lh.insula.lobe_vol,wm.lh.CSO_vol,wm.rh.frontal.lobe_vol,wm.rh.cingulate.lobe_vol,wm.rh.occiptal.lobe_vol,wm.rh.temporal.lobe_vol,wm.rh.parietal.lobe_vol,wm.rh.insula.lobe_vol,wm.rh.CSO_vol
DTI ALPS D5mm: alps_L_D5mm,alps_R_D5mm,alps_D5mm
DTI ALPS D10mm: alps_L_D10mm,alps_R_D10mm,alps_D10mm
PET TAU: TRACER_TAU_tx must be FTP
META_TEMPORAL_SUVR_TAU, values equal or above (≥1.37) this threshold indicate elevated tau accumulation
T1(EPVS availablity): T1 (1=YES)
DTI (ALPS availablilty): DTI (1=YES)
Age: AGE_Actual
Gender: PTGENDER
Cognitive Measures: CDRSB,ADAS11,ADAS13,ADASQ4,MMSE,MOCA,mPACCdigit,mPACCtrailsB; Typically I like to include MMSE in the models
Diagnostic GRP: DX
ICV: ICV or ICV_bl (Either works for cross-sectional models)
PET->MRI Delta T: PET_Years,PET_Days
Others (Might be helpful): Site,PTEDUCAT,PTETHCAT,PTRACCAT,APOE4

# AB CSV, Columns could be used
Most of them are the same as Tau
PET AB: 
AMYLOID_STATUS: 1 is postive and 0 is negative
CENTILOIDS_AB_tx: 
cutoff1: ≥30 Centiloids is positive
cutoff2: ≥37 Centiloids is positive
The others should be the same as Tau CSV

General Suggestions for building the models
1, ALL volumetric EPVS measures must be normalized by ICV
OR
2, ALL volumetric EPVS measures must be normalized by corresponding regional structural volumes
OR
3, Volumetric EPVS measures + ICV
OR
4, Volumetric EPVS measures + corresponding regional structural volumes
AND
ALL imaging features entering the models must be biologically or anatomically indepedent each other