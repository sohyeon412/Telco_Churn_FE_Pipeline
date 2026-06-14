# 머신러닝 특성 공학 파이프라인 — Telco Customer Churn

빅데이터분석 01분반 | 컴퓨터공학과 | 2204774 | 박소현

고객 이탈(Churn) 예측을 위한 전체 ML 파이프라인. EDA → 결측치/인코딩/스케일링 비교 →
파생변수 → 변수선택 → 다중 모델 학습·평가 → 실험 비교 → 가산점(Pipeline, GridSearchCV,
SHAP, Feature Importance 고도화, AutoML)까지 한 노트북에 구현했고, 마지막 셀이 한국어 PDF
보고서를 자동 생성한다.

## 데이터셋

Telco Customer Churn (약 7,043행, 21컬럼). 노트북이 공개 미러 URL에서 자동 로드한다.

## 평가/가산점 매핑

- EDA: 결측치·이상치·분포·상관·타겟분포 + Histogram/Boxplot/Heatmap/Barplot
- Feature Engineering: 결측치 3종 + 인코딩 2종 + 스케일링 3종 비교, 파생변수 5종
- 실험 비교: Base / Exp-1 / Exp-2 / Exp-3 × 4모델, 전 지표(Acc/Prec/Rec/F1/ROC-AUC)
- 변수선택: SelectFromModel 제거 전/후 비교
- 가산점: sklearn Pipeline, GridSearchCV, SHAP, Permutation Importance, AutoML 스타일 리더보드
- 재현성: `random_state=42` 고정, 결과·그래프 기반 PDF 자동 생성
