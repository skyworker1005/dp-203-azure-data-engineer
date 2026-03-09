
`Allfiles/labs/` 아래 폴더들을 기준으로 정리한 분석입니다.

---

# Allfiles/labs 폴더별 분석

이 저장소는 **Microsoft DP-203 Azure Data Engineer** 과정용이며, 랩은 **Azure Synapse Analytics**와 **Azure Databricks** 두 흐름으로 나뉩니다.  
지침서는 `Instructions/Labs/`의 `NN-제목.md`에 있고, 실습 자원은 `Allfiles/labs/NN/`에 있습니다.

---

## 1. Azure Synapse Analytics 기초 (01~04)

| 폴더 | 제목 | 주요 내용 | 실습 자원 |
|------|------|-----------|-----------|
| **01** | Explore Azure Synapse Analytics | Synapse 워크스페이스, 리소스 프로비저닝, 포털 탐색 | `setup.ps1`, `setup.sql`, `setup.json`, `data/`, `adventureworks/`, `files/`, `iot/` |
| **02** | Query files using a serverless SQL pool | 서버리스 SQL 풀로 파일(데이터 레이크) 쿼리 | `setup.ps1`, `setup.json`, `data/` |
| **03** | Transform data using a serverless SQL pool | 서버리스 SQL로 데이터 변환 (CETAS 등) | `setup.ps1`, `setup.json`, `data/` |
| **04** | Analyze data in a lake database | 레이크 데이터베이스 생성·분석 | `setup.ps1`, `setup.json`, `data/` (salesorder, product, customer CSV) |

---

## 2. Synapse Spark & Delta Lake (05~07)

| 폴더 | 제목 | 주요 내용 | 실습 자원 |
|------|------|-----------|-----------|
| **05** | Analyze data in a data lake with Spark | Spark로 레이크 파일 분석 | `setup.ps1`, `setup.json`, `data/` (2019~2021.csv) |
| **06** | Transform data using Spark in Synapse | Spark 노트북으로 데이터 변환 | `setup.ps1`, `setup.json`, `data/`, `notebooks/Spark Transform.ipynb` |
| **07** | Use Delta Lake in Azure Synapse Analytics | Synapse에서 Delta Lake 사용 | `setup.ps1`, `setup.json`, `data/products.csv` |

---

## 3. 데이터 웨어하우스 (08~09)

| 폴더 | 제목 | 주요 내용 | 실습 자원 |
|------|------|-----------|-----------|
| **08** | Explore a relational data warehouse | 전용 SQL 풀(데이터 웨어하우스) 탐색 | `setup.ps1`, `setup.sql`, `setup.json`, `data/` (Dim*/Fact* .fmt), `Solution.sql` |
| **09** | Load Data into a Relational Data Warehouse | 웨어하우스로 데이터 로드 (Polybase/COPY 등) | `setup.ps1`, `setup.sql`, `setup.json`, `data/` (동일 스키마 + Customer.csv 등) |

---

## 4. Synapse 파이프라인 (10~11)

| 폴더 | 제목 | 주요 내용 | 실습 자원 |
|------|------|-----------|-----------|
| **10** | Build a data pipeline in Azure Synapse Analytics | Synapse 파이프라인으로 파이프라인 구축 | `setup.ps1`, `setup.sql`, `setup.json`, `data/Product.csv` |
| **11** | Use an Apache Spark notebook in a pipeline | 파이프라인에서 Spark 노트북 실행 | `setup.ps1`, `setup.json`, `data/`, `notebooks/Spark Transform.ipynb` |

---

## 5. Synapse Link & 통합 (14~15, 22)

| 폴더 | 제목 | 주요 내용 | 실습 자원 |
|------|------|-----------|-----------|
| **14** | Use Azure Synapse Link for Azure Cosmos DB | Cosmos DB → Synapse 링크 | `setup.ps1`, `setup.json` |
| **15** | Use Azure Synapse Link for SQL | SQL DB → Synapse 링크 | `setup.ps1`, `setup.json` |
| **22** | Use Microsoft Purview with Azure Synapse Analytics | Purview와 Synapse 연동 (거버넌스) | `setup.ps1`, `setup.sql`, `setup.json`, `data/products.csv` |

---

## 6. 스트리밍 (17~19)

| 폴더 | 제목 | 주요 내용 | 실습 자원 |
|------|------|-----------|-----------|
| **17** | Get started with Azure Stream Analytics | Stream Analytics 입문 | `setup.ps1`, `setup.json`, `setup.txt` |
| **18** | Ingest realtime data with Stream Analytics and Synapse | Stream Analytics → Synapse 실시간 수집 | `setup.ps1`, `setup.sql`, `setup.json`, `setup.txt` |
| **19** | Create a realtime report with Stream Analytics and Power BI | Stream Analytics + Power BI 실시간 리포트 | `setup.ps1`, `setup.json`, `setup.txt` |

---

## 7. Azure Databricks (23~27) — Databricks 전용

| 폴더 | 제목 | 주요 내용 | 실습 자원 |
|------|------|-----------|-----------|
| **23** | Explore Azure Databricks | Databricks 워크스페이스 프로비저닝, 클러스터 생성, 노트북/DBFS 체험 | `setup.ps1` (Storage + Databricks 리소스), `adventureworks/products.csv` |
| **24** | Use Spark in Azure Databricks | Spark DataFrame, 스키마, 필터/집계, Spark SQL, 시각화(matplotlib, seaborn) | `setup.ps1`, `Databricks-Spark.ipynb` (.dbc), `data/` (2019~2021.csv) |
| **25** | Use Delta Lake in Azure Databricks | Delta 테이블 생성·업데이트, Time Travel, External/Managed 테이블, Structured Streaming → Delta | `setup.ps1`, `Delta-Lake.ipynb` (.dbc), `data/` (products.csv, devices1/2.json) |
| **26** | Use a SQL Warehouse in Azure Databricks | SQL Warehouse, 스키마/테이블 생성, SQL Editor로 쿼리 | `setup.ps1`, `data/products.csv` (지침서 기준으로 테이블 생성) |
| **27** | Automate an Azure Databricks Notebook with Azure Data Factory | ADF에서 Databricks 노트북 오케스트레이션, Linked Service, 파이프라인에서 노트북 실행 | `setup.ps1`, `Process-Data.ipynb` (widget `folder`, GitHub에서 CSV 다운로드 후 DBFS 저장, 경로 반환) |

---

## 공통 패턴

- **설정**: 대부분 `setup.ps1`로 Azure 리소스 프로비저닝, 필요 시 `setup.sql`(스키마/초기 데이터), `setup.json`(ARM 등).
- **데이터**: 랩별 `data/` 또는 `adventureworks/` 등에 CSV/JSON/.fmt 샘플 데이터.
- **Databricks 랩(23~27)**: `setup.ps1`에 `Microsoft.Databricks` 등 리소스 프로바이더 등록, 워크스페이스 생성. 24·25·27은 노트북(.ipynb/.dbc)으로 실습.

---

## 요약

- **01~22**: 주로 **Azure Synapse**(서버리스 SQL, Spark, 전용 풀, 파이프라인, Synapse Link, Purview, Stream Analytics) 실습.
- **23~27**: **Azure Databricks** 전용 — 워크스페이스·클러스터(23), Spark(24), Delta Lake(25), SQL Warehouse(26), Data Factory 연동(27).

실습 순서는 강의 커리큘럼에 맞추면 되고, Databricks만 따로 보려면 **23 → 24 → 25 → 26 → 27** 순서가 자연스럽습니다.