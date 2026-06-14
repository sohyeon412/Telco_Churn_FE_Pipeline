# 머신러닝 특성 공학 파이프라인 — Telco Customer Churn

빅데이터분석 01분반 | 컴퓨터공학과 | 2204774 | 박소현

고객 이탈(Churn) 예측을 위한 전체 ML 파이프라인. EDA → 결측치/인코딩/스케일링 비교 →
파생변수 → 변수선택 → 다중 모델 학습·평가 → 실험 비교 → 가산점(Pipeline, GridSearchCV,
SHAP, Feature Importance 고도화, AutoML)까지 한 노트북에 구현했고, 마지막 셀이 한국어 PDF
보고서를 자동 생성한다.

## 실행 방법 (Colab 권장 — 내 컴퓨터 저장공간 불필요)

1. `Telco_Churn_FE_Pipeline.ipynb`를 Google Colab에서 연다.
   - GitHub에 올렸다면: Colab → File → Open notebook → GitHub 탭 → 저장소/노트북 선택.
   - 또는 [https://colab.research.google.com](https://colab.research.google.com) 에서 직접 업로드.
2. 상단 메뉴 `런타임(Runtime) → 모두 실행(Run all)`.
3. 데이터는 코드가 인터넷에서 자동 다운로드하므로 별도 업로드가 필요 없다.
4. 마지막 셀이 `Telco_Churn_보고서_2204774_박소현.pdf`를 생성하고 자동 다운로드한다.

## 제출물

- 소스코드: 이 GitHub 저장소 주소 (`Telco_Churn_FE_Pipeline.ipynb`)
- 보고서: 노트북 실행으로 생성되는 PDF 파일

## 데이터셋

Telco Customer Churn (약 7,043행, 21컬럼). 노트북이 공개 미러 URL에서 자동 로드한다.

## 평가/가산점 매핑

- EDA: 결측치·이상치·분포·상관·타겟분포 + Histogram/Boxplot/Heatmap/Barplot
- Feature Engineering: 결측치 3종 + 인코딩 2종 + 스케일링 3종 비교, 파생변수 5종
- 실험 비교: Base / Exp-1 / Exp-2 / Exp-3 × 4모델, 전 지표(Acc/Prec/Rec/F1/ROC-AUC)
- 변수선택: SelectFromModel 제거 전/후 비교
- 가산점: sklearn Pipeline, GridSearchCV, SHAP, Permutation Importance, AutoML 스타일 리더보드
- 재현성: `random_state=42` 고정, 결과·그래프 기반 PDF 자동 생성
