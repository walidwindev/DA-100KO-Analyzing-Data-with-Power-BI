---
lab:
    title: '행 수준 보안 적용'
    module: '모듈 13 - 행 수준 보안'
---


# **행 수준 보안 적용**

**이 랩을 완료하는 데 걸리는 예상 완료 시간은 45분입니다.**

이 랩에서는 **Salesperson** 테이블과 **Sales** 테이블 간에 다대다 관계를 만듭니다. 또한 영업 사원이 할당된 지역의 판매 데이터만 분석할 수 있도록 행 수준 보안을 적용합니다.

이 랩에서는 다음 작업을 수행하는 방법을 알아봅니다.

- 다 대 다 관계 구성

- 행 수준 보안 적용

### **랩 스토리**

이 랩은 데이터를 준비하여 보고서와 대시보드로 게시하는 전체 스토리로 제작된 랩 시리즈에 포함되어 있는 여러 랩 중 하나입니다. 랩은 원하는 순서로 완료하면 됩니다. 그러나 여러 랩을 진행하려는 경우 처음 10개 랩은 다음 순서로 수행하는 것이 좋습니다.

1. Power BI Desktop에서 데이터 준비

2. Power BI Desktop에서 데이터 로드

3. Power BI Desktop에서 데이터 모델링, 1부

4. Power BI Desktop에서 데이터 모델링, 2부

5. Power BI Desktop에서 DAX 계산 만들기, 1부

6. Power BI Desktop에서 DAX 계산 만들기, 2부

7. Power BI Desktop에서 보고서 디자인, 1부

8. Power BI Desktop에서 보고서 디자인, 2부

9. Power BI 대시보드 만들기

10. Power BI Desktop에서 데이터 분석 수행

11. Power BI 페이지를 매긴 보고서 만들기

12. **행 수준 보안 적용**

## **연습 1: 행 수준 보안 적용**

이 연습에서는 영업 직원이 할당된 지역에 대한 판매량만 볼 수 있도록 행 수준 보안을 적용합니다.

### **작업 1: 시작**

이 작업에서는 랩용 환경을 설정합니다.

*중요: 이전 랩을 정상적으로 완료했으며 작업을 계속 이어서 하는 경우 이 작업을 완료하지 말고 다음 작업부터 계속 진행하세요.*

1. Power BI Desktop을 열려면 작업 표시줄에서 Microsoft Power BI Desktop 바로 가기를 클릭합니다.

	![그림 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)

1. 시작 창을 닫으려면 창 왼쪽 위의 **X**를 클릭합니다.

	![그림 7](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image2.png)

1. 시작 Power BI Desktop 파일을 열려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **보고서 열기**를 선택합니다.

	![그림 6](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image3.png)

1. **보고서 찾아보기**를 클릭합니다.

	![그림 5](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image4.png)

1. **열기** 창에서 **D:\DA100\Labs\12-row-level-security\Starter** 폴더로 이동합니다.

1. **판매 분석** 파일을 선택합니다.

1. **열기**를 클릭합니다.

	![그림 4](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image5.png)

1. 정보 창이 열릴 수도 있는데 모두 닫으면 됩니다.

1. 파일 복사본을 만들려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **다른 이름으로 저장**을 선택합니다.

	![그림 3](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image6.png)

1. 변경 내용을 적용하라는 메시지가 표시되면 **적용**을 클릭합니다.

	![그림 15](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image7.png)

1. **다른 이름으로 저장** 창에서 **D:\DA100\MySolution** 폴더로 이동합니다.

1. **저장**을 클릭합니다.

	![그림 2](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image8.png)

### **작업 2: 행 수준 보안 적용**

이 작업에서는 영업 직원이 할당된 지역에 대한 판매량만 볼 수 있도록 행 수준 보안을 적용합니다.

1. 데이터 뷰로 전환합니다.

	![그림 5701](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image20.png)

2. **필드** 창에서 **Salesperson (Performance)** 테이블을 선택합니다.

3. 데이터를 검토하면 Michael Blythe(EmployeeKey 281)의 UPN 값이 **michael-blythe@adventureworks.com**임을 확인할 수 있습니다.

	*Michael Blythe는 판매 지역 세 곳에 할당되어 있습니다: 미국 북동부, 미국 중부, 미국 남동부.*

4. 보고서 뷰로 전환합니다.

5. **보안** 그룹 내부의 **모델링** 리본 탭에서 **역할 관리**를 클릭합니다.

	![그림 5700](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image21.png)

6. **역할 관리** 창에서 **만들기**를 클릭합니다.

	![그림 5702](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image22.png)

7. 상자에서 선택한 텍스트를 역할 이름으로 바꿉니다. **Salespeople**, 그 다음 **입력**을 누릅니다.

	![그림 5703](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image23.png)

8. 필터를 할당하려면 **Salesperson (Performance)** 테이블에서 줄임표(...) 문자를 클릭한 다음 **필터 추가 | [UPN]** 를 선택합니다.

	![그림 5704](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image24.png)

9. **Table Filter DAX Expression** 상자에서 **"값"** 을 **USERPRINCIPALNAME()** 으로 바꿔 식을 수정합니다.

	![그림 11](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image25.png)

	*USERPRINCIPALNAME()은 인증된 사용자 이름을 반환하는 DAX(데이터 분석 식) 함수입니다. 즉, **Salesperson (Performance)** 테이블은 모델을 쿼리하는 사용자의 UPN(사용자 계정 이름)으로 필터링합니다.*

10. **저장**을 클릭합니다.

	![그림 5706](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image26.png)

11. 보안 역할을 테스트하려면 **보안** 그룹 내부의 **모델링** 리본 탭에서 **View As**를 클릭합니다.

	![그림 5708](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image27.png)

12. **역할로 보기** 창에서 **다른 사용자** 항목을 선택한 다음 해당 상자에 **michael-blythe@adventureworks.com**을 입력합니다.

13. **Salespeople** 역할을 확인합니다.

	![그림 5709](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image28.png)

	*이 구성을 적용하면 **Salespeople** 역할이 사용되며, 사용자가 Michael Blyth의 이름으로 가장됩니다.*

14. **확인**을 클릭합니다.

	![그림 5710](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image29.png)

15. 테스트 보안 컨텍스트를 설명하는 보고서 페이지 위의 노란색 배너를 확인합니다.

	![그림 13](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image30.png)

16. 테이블 시각적 개체에서 판매원 **Michael Blythe**만 나열되는 것을 확인합니다.

	![그림 5713](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image31.png)

17. 테스트를 중지하려면 노란색 배너 오른쪽에서 **보기 중지**를 클릭합니다.

	![그림 5712](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image32.png)

	*Power BI Desktop 파일이 Power BI 서비스에 게시되면 보안 주체를 **Salespeople** 역할에 매핑하는 게시 후 작업을 완료해야 합니다. 이 랩에서는 해당 작업을 수행하지 않습니다.*

18. 역할을 삭제하려면 **모델링** 리본 탭의 **보안** 그룹 내에서 **역할 관리**를 클릭합니다.

	![그림 16](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image33.png)

19. **역할 관리** 창에서 **삭제**를 클릭합니다.

	![그림 17](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image34.png)

20. 삭제를 확인하라는 메시지가 표시되면, **예, 삭제합니다**.를 클릭합니다.

21. **저장**을 클릭합니다.

	![그림 18](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image35.png)

### **작업 2: 완료**

이 작업에서는 랩을 완료합니다.

1. Power BI Desktop 파일을 저장합니다.
