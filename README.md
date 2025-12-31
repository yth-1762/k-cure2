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
- logistic regression
- cox proportional hazard regression


# 분석1
- 사용모델: logistic regression 
- 표본: 4715명(Smoking quitters after diagnosis: 3414명/ Continuous smokers after diagnosis: 1301명)
- 종속변수: stop_yn(금연 여부)
- 독립변수: AGE,SEX,BMI,INCOME,CCI_SCORE(상병점수),STAGE(수술부위),수술여부,방사선치료여부,전신항암요법치료여부,폐암진단후전자담배사용여부
- 목적: 진단 후 금연자와 현재 흡연중인 자를 대상으로 univariable, multivariable(univariable에서 p<0.2인 변수) 로지스틱 회귀분석을 활용하여 금연에 영향을 미치는 특성 요인 분석
- 분석결과: tables_20250901파일에서 table3에서 확인 가능


# 분석2
- 사용모델: logistic regression 
- 표본: 4715명(Smoking quitters after diagnosis: 3414명/ Continuous smokers after diagnosis: 1301명)
- 종속변수: ntp_yn(전자담배 흡연여부)
- 독립변수: AGE,SEX,BMI,INCOME,CCI_SCORE(상병점수),STAGE(수술부위),수술여부,방사선치료여부,전신항암요법치료여부,흡연유형
- 목적: 진단 후 금연자와 현재 흡연중인 자를 대상으로 univariable, multivariable(univariable에서 p<0.2인 변수) 로지스틱 회귀분석을 활용하여 전자담배 흡연에 영향을 미치는 특성 요인 분석
- 분석결과: tables_20250901파일에서 table4에서 확인 가능

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
