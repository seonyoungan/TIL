# SE_Chapter01

Status: 소프트웨어공학

### 1. **소프트웨어 개념과 특징**

1. 소프트웨어 개념과 특징
    - 개념: 프로그램+프로그램 개발 운용, 보수에 필요한 관련 정보 일체를 일컫음
            SW개발 산출물: 코드 + 개발과정에서 산출되는 문서들
    - 분류
        - 응용 소프트웨어: 회사 또는 기관의 내부 시스템
        - 시스템 소프트웨어: 운영체제, 컴파일러 등
        - 주문형 소프트웨어: 특정고객이나 기업 만족시키기 위해 제작된 소프트웨어
        - 패키지 소프트웨어: 패키지화 하여 상업적으로 판매하는 소프트웨어
        - 임베디드 소프트웨어: 다른 시스템에 내장된 소프트웨어
2. **소프트웨어의 특징** 
    - **Invisibility**: 생산물의 구조가 코드 안에 숨어있으며 작업 과정, 결과물 평가 어려움
    - **Complexity**: 규칙적이고 정형적인 구조가 없음
    - **Conformity**: 쉽게 변경이 가능
3. (하드웨어와 비교) 소프트웨어의 특징
    - (제조가 아닌) **개발**
    - (마모가 아닌) **품질저하**
4. 소프트웨어 시스템
    - 소프트웨어는 독립적으로 존재하는 것이 아님→하드웨어 기반으로 여러 시스템과 관계가 있음

### 2. 소프트웨어 공학의 필요성

1. 소프트웨어의 위기:  Nato, 1968, Germany
    - 하드웨어: 시스템비용 감소추세
    - 소프트웨어: 유지보수비용 증가→낮추기위한 학문의 등장(SE)
2. 소프트웨어의 위기 이유
    - **당초 예산 초과 running over budget**
    - **기간 초과 running overtime**
    - **품질 부족 관련**
       - 비현실적 veryinefficient
       - 낮은 품질 low quality
       - 요구사항 미충족not meet requirements
3. 그외
    - **고비용**
        - **소프트웨어의 주된 비용→인건비**
        - LOC(Line Of Code)계산법: 소프트웨어 규모 추정하는 데에 가장 널리 사용
```markdown
M/M: 노력측정단위로, 1명의 1개월동안 업무량을 나타냄
Productivity: 1인당 월평균 생산 코드라인수
LOC 계산법(상세)
낙관치: 라인 수 가장 **적게** 생각할 때의 예상 라인 수**(가중치 1)**
비관치: 라인 수 가장 **많이** 생각할 때의 예상 라인 수**(가중치 1)**
중간치: 라인 수 **보통**이라고 생각할 때 예상 라인 수**(가중치 4)**
추정LOC: (낙 + (4 * 중) + 비) / 6

M/M: (참여 인원/월) * 개발 기간 = LOC / 1인 평균 라인 수
개발 비용: (M/M) * 1인 평균 인건비
개발 기간: (M/M) / 참여 인원
생산성: LOC / (M/M)
 ```
    - **개발 지연과 낮은 신뢰도**
        - 계획에 벗어난 컴퓨터 개발 프로젝트 또는 예상대로 작동하지 않는 사례
    - **유지보수와 재작업**
        - 소프트웨어에 **유지보수**가 필요한 이유
            - 시스템에 남아있는 오류(부품 마모 또는 교체 필요 때문에 유지보수 하는 것이 아님)
            - 잦은 소프트웨어의 변경(환경 변경, 업그레이드 등)
        - 소프트웨어에 **재작업**이 필요한 이유
            - 의도한 바를 왜곡 없이 코드에 반영하기 어려움
            - 의뢰자의 아이디어는 초기 작업에 가까움
        

### 3. 소프트웨어 공학의 정의와 다루는 문제

1. 정의(IEEE): SW의 Life Cycle에 대한 체계적 접근 방법
2. SE가 다루는 근본적 문제: 사용자의 요구를 만족 시키기 위한 소프트웨어를 체계적으로 개발하는 것
3. 과학과 엔지니어링의 차이
    - 과학: 진리탐구 / 엔지니어링: 문제해결
4. SE의 도전과제
    - **규모**: Industrial strength software =/= Student programs. 그러므로 다른 접근 방법이 필요
    - **품질과 생산성**
        - 품질: 소프트웨어의 품질은 정의하기 어려움
            - ISO Standard[ISO9126]은 6개의 태도를 가짐: 기능성 / 신뢰성 / 사용용이성 / 효율성 / 유지보수성 / 이식성
                - 신뢰성(relibility)
                    - 방법1: Transaction Reliablity
                    - 방법2: Defece Desity(버그밀도) = `특정 라인당 발생한 오류의 갯수 / 실제 프로젝트의 라인 수`
        - 생산성: 엔지니어링 프로젝트는 비용, 일정이라는 제약이 존재함 → 생산성↑ 비용↓ 시간 ↓
    
5. **일관성과 재현성**
    - 일관성: 누가 만들더라도 이 방법을 쓰면 높은 품질 + 생산성 고취 가능할 것
    - 재현성: 여러번 반복해도 성공할 수 있도록 할 것(ISO9001, CMM을 따름)

6. **변경성**
    - 유지보수를 피할 순 없으므로 공학 측면의 변화 대응법 필요
    - 생산성 + 품질만 생각하면 프로그램의 가치는 없음 (→ 프로그램은 무조건 변하기 때문)
    - 산업에 강한 SE: Consistently, high qulity, problems, change, scale

### 4. 소프트웨어 공학의 접근

1. 소프트웨어 공학의 접근 방법
    - Q&P / People / Process / Technology (체계적, 일관성, 재현성 중시)
    - SE 개발 프로세스: NEEDS → IDEA →(PROCESS)→ SOFTWARE
    - 비즈니스 요구파악 → 타당성 검토→요구사항 정형화 →설계→구현→테스팅→설치
    - 품질보증: 개발작업이 적절히 수행되었는지 확인하는 작업
    - 프로젝트 관리: 개발과 품질보증 작업의 관리 감독 / 노력예측 / 일정과 리스트, 행정 등
2. 단계적 개발 프로세스
    - SE는 페이즈를 나눠서 관리함
    - 왜? 소프트웨어의 문제를 나눠 여러 개발 단계에서 다른 관점으로 다루기 위함
          개발하는 동안 정해진 시점에 품질과 진행 체크 가능
    

### 5. 소프트웨어 공학의 지식체계

1. SWEBOK (IEEE, 2004)
    - 소프트웨어 요구→설계→구축→테스트→유지보수
      →형상관리→프로젝트 관리→프로세스→도구와 방법→품질→기타 관련 지식
