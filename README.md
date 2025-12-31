# k-cure2

# 주제
- Screening Eligibility and Survival among Patients with Lung Cancer: A Korean Nationwide Cohort Study
 
# 배경
- 흡연 유형에 따른 전체/폐암 사망 위험도를 분석하고 전체/폐암에 영향을 끼치는 개인 특성 요인이 무엇인지 분석하는 것을 목적으로 한다.
 
# 주최
- 분당서울대병원 빅데이터센터

# 일정
- 2025.01.15 - 2026.01.14

# 데이터
- 폐암 환자 : 147303명 (건강검진데이터와 연계 가능한 인원)
- 표본1 : 77554명 (Aged 50-80, >=20PY smoking history: 31804명/ Aged 50-80, <20PY smoking history: 12735명/ Aged 50-80, never-smoked: 33015명)
- 표본2: 44539명 (Smk_duration >=20: 39383명/ Smk_duration <20: 5156명)
- 표본3: 32514명 (Aged 50-80, >=20PY smoking history: 31804명/ Aged 40-49, >=20PY smoking history: 710명)
- 표본4: 13682명 (Aged 50-80, <20PY smoking history: 12735명/ Aged 40-49, <20PY smoking history: 947명)
- 표본5: 34984명 (Aged 50-80, Never-smoker: 33015명/ Aged 40-49, Never-smoker: 1969명)
- 표본6: 147299명 (Included in analysis: 89860명/ Excluded from the analysis: 57439명)


# 사용 통계 모델
- Anova(분산 분석)
- Pearson's Chi-squared Test(카이제곱 검정)
- cox proportional hazard regression
- Proportional Subdistribution Hazards Regression(Fine-gray model)

# 분석1
- 분석방법: Anova(분산분석)
- 표본: 표본1(77554명)/ 표본2(44539명)/ 표본3(32514명)/ 표본4(13682명)/ 표본5(34984명)
- 종속변수: grouptype
- 독립변수: AGE, pack_year, BMI
- 목적: grouptype벼로 AGE, pack_year, BMI가 차이가 있는지 검정
- 분석결과: Tables_Dummy_20251125파일에서 table1,table3-1,table3-3,table4-1,table5-1,table6-1,table7-1에서 확인 가능


Pearson's chisq test(변수1: grouptype / 변수2: SEX, Smoking status, INCOME, CCI_SCORE(상병점수), Physical activity, Histological type of lung cancer, Stage(수술부위),수술여부, 방사선치료여부, 전신항암요법치료여부 


# 분석3
- 사용모델: cox proportional hazard regression
- 표본: 30550명(Never-smokers: 18093명/ Smoking quitters before diagnosis: 7742명/ Smoking quitters after diagnosis: 3414명/ Continuous smokers after diagnosis: 1301명)
- 사망원인: All cause mortality(전체), Lung cancer mortality(폐암), Non Lung cancer mortality(비폐암)
- 독립변수: 흡연유형1(Never-smokers/Smoking quitters before diagnosis/Smoking quitters after diagnosis/Continuous smokers after diagnosis), AGE,SEX,BMI,INCOME,CCI_SCORE(상병점수),physical activity, 비소세포암 여부, STAGE(수술부위),수술여부,방사선치료여부,전신항암요법치료여부
- 목적: 표본1(30550명)을 대상으로 (univariable/multivariable)cox proportional hazard regression을 활용하여 사망(ALL cause mortality/Lung cancer mortality/Non Lung cancer mortality)에 영향을 미치는 요인(흡연유형1, 개인특성) 분석
- 분석결과: tables_20250901파일에서 table5에서 확인 가능 

# 분석4
- 사용모델: cox proportional hazard regression
- 표본: 30550명(Never-smokers: 18093명/ Smoking quitters before diagnosis: 7742명/ Smoking quitters after diagnosis: 3414명/ Continuous smokers after diagnosis: 1301명)
- 사망원인: All cause mortality(전체), Lung cancer mortality(폐암), Non Lung cancer mortality(비폐암)
- 독립변수: 흡연유형2(Never-smokers without NTP use/Never-smokers with NTP use after diagnosis/Smoking quitters before diagnosis without NTP use after diagnosis/Smoking quitters before diagnosis with NTP use after diagnosis/Smoking quitters after diagnosis without NTP use/Smoking quitters after diagnosis with NTP use/Continuous smokers after diagnosis without NTP use/Countinous smokers after diagnosis with NTP use), AGE,SEX,BMI,INCOME,CCI_SCORE(상병점수),physical activity, 비소세포암 여부, STAGE(수술부위),수술여부,방사선치료여부,전신항암요법치료여부
- 목적: 표본1(30550명)을 대상으로 (univariable/multivariable)cox proportional hazard regression을 활용하여 사망(ALL cause mortality/Lung cancer mortality/Non Lung cancer mortality)에 영향을 미치는 요인(흡연유형2, 개인특성) 분석
- 분석결과: tables_20250901파일에서 table6에서 확인 가능

# 분석5
- 사용모델: cox proportional hazard regression
- 표본: 30550명(Never-smokers: 18093명/ Smoking quitters before diagnosis: 7742명/ Smoking quitters after diagnosis: 3414명/ Continuous smokers after diagnosis: 1301명)
- 사망원인: All cause mortality(전체), Lung cancer mortality(폐암)
- 독립변수: 흡연유형1(Never-smokers/Smoking quitters before diagnosis/Smoking quitters after diagnosis/Continuous smokers after diagnosis), AGE,SEX, 비소세포암 여부, STAGE(수술부위)
- 목적: 표본1(30550명)을 대상으로 (univariable/multivariable)cox proportional hazard regression을 활용하여 사망(ALL cause mortality/Lung cancer mortality)에 영향을 미치는 요인(흡연유형1, 개인특성) 분석
- 분석결과: tables_20250901파일에서 table8에서 확인 가능

# 분석6
- 사용모델: cox proportional hazard regression
- 표본: 30550명(Never-smokers: 18093명/ Smoking quitters before diagnosis: 7742명/ Smoking quitters after diagnosis: 3414명/ Continuous smokers after diagnosis: 1301명)
- 사망원인: All cause mortality(전체), Lung cancer mortality(폐암)
- 독립변수: 흡연유형2(Never-smokers without NTP use/Never-smokers with NTP use after diagnosis/Smoking quitters before diagnosis without NTP use after diagnosis/Smoking quitters before diagnosis with NTP use after diagnosis/Smoking quitters after diagnosis without NTP use/Smoking quitters after diagnosis with NTP use/Continuous smokers after diagnosis without NTP use/Countinous smokers after diagnosis with NTP use), AGE,SEX,비소세포암 여부, STAGE(수술부위)
- 목적: 표본1(30550명)을 대상으로 (univariable/multivariable)cox proportional hazard regression을 활용하여 사망(ALL cause mortality/Lung cancer mortality)에 영향을 미치는 요인(흡연유형2, 개인특성) 분석
- 분석결과: tables_20250901파일에서 table9에서 확인 가능


# 분석7
- 사용모델: cox proportional hazard regression
- 표본: 12457명 (Smoking quitters before diagnosis: 7742명/ Smoking quitters after diagnosis: 3414명/ Continuous smokers after diagnosis: 1301명)
- 사망원인: All cause mortality(전체), Lung cancer mortality(폐암)
- 독립변수: 흡연유형3(Smoking quitters before diagnosis/Smoking quitters after diagnosis/Continuous smokers after diagnosis), AGE,SEX,비소세포암 여부, STAGE(수술부위)
- 목적: 표본3(12457명)을 대상으로 (univariable/multivariable)cox proportional hazard regression을 활용하여 사망(ALL cause mortality/Lung cancer mortality)에 영향을 미치는 요인(흡연유형3, 개인특성) 분석
- 분석결과: tables_20250901파일에서 table10에서 확인 가능
