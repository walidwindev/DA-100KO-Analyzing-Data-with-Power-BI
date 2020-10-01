

### 랩 03A

Power BI Desktop으로 데이터 로드

# 개요

**랩을 완료하는 데 예상되는 시간은 45분입니다.**

이 랩에서는 이전 랩에서 만든 각 쿼리에 대한 변환 적용을 시작합니다. 그런 다음 쿼리를 적용하여 각 쿼리를 데이터 모델에 테이블로 로드합니다.

이 랩의 학습 내용은 다음과 같습니다.

* 다양한 변환 적용하기

* 쿼리를 적용하여 데이터 모델에

# 연습 1: 데이터 로드

이 연습에서는 이전 랩에서 만든 각 쿼리에 변환을 적용합니다.

*이전 랩을 성공적으로 완료했다고 확신하지 못하는 경우 **D:\DA100\Lab02A\Solution** 폴더에 있는 이전 랩의 솔루션 파일을 열어 볼 수 있습니다*.

### 작업 1: 영업 직원 쿼리 구성

이 작업에서는 **영업 직원** 쿼리를 구성합니다.

1. **파워 쿼리 편집기** 창의 **쿼리** 창에서 **DimEmployee** 쿼리를 선택합니다.

    ![그림 1](Linked_image_Files/PowerBI_Lab03A_image1.png)

2. 쿼리 이름을 변경하려면 **쿼리 설정** 창(오른쪽에 위치)의 **이름** 상자에서 텍스트를 **Salesperson**으로 대체한 다음 **Enter** 키를 누릅니다.

    *쿼리 이름은 모델 테이블 이름을 결정합니다. 간결하면서도 친근한 이름을 정의하는 것이 좋습니다*.

3. **쿼리** 창에서 쿼리 이름이 업데이트되었는지 확인합니다.

    ![그림 87](Linked_image_Files/PowerBI_Lab03A_image2.png)

    *이제 쿼리 행을 필터링하여 영업 직원인 직원만 검색합니다*.

4. 특정 열을 찾으려면 **열 관리** 그룹 내부의 **홈** 리본 탭에서 **열 선택** 아래쪽 화살표를 클릭한 다음 **열로 이동**을 선택합니다.

    ![그림 88](Linked_image_Files/PowerBI_Lab03A_image3.png)

    *팁: 이 기술은 쿼리에 많은 열이 포함된 경우에 유용합니다. 일반적으로 가로로 스크롤하여 열을 찾을 수 있습니다*.

5. **열로 이동** 창에서 열 이름으로 목록을 정렬하려면 **AZ** 정렬 단추를 클릭한 다음 **이름**을 선택합니다.

    ![그림 94](Linked_image_Files/PowerBI_Lab03A_image4.png)

6. **SalesPersonFlag** 열을 선택하고 **확인**을 클릭합니다.

7. 쿼리를 필터링하려면 **SalesPersonFlag** 열 헤더에서 아래쪽 화살표를 클릭한 다음 **FALSE**를 선택 해제합니다.

    ![그림 95](Linked_image_Files/PowerBI_Lab03A_image5.png)

8. **확인**을 클릭합니다.

    ![그림 96](Linked_image_Files/PowerBI_Lab03A_image6.png)

9. **쿼리 설정** 창의 **적용된 단계** 목록에서 **필터링된 행** 단계가 추가됩니다.

    ![그림 98](Linked_image_Files/PowerBI_Lab03A_image7.png)

    *변환을 생성할 때마다 추가 단계 논리가 생성됩니다. 단계를 편집하거나 삭제할 수 있습니다. 또한 변환 단계에서 쿼리 결과를 미리 볼 단계를 선택할 수도 있습니다*.

10. 열을 제거하려면 **열 관리** 그룹 내부의 **홈** 리본 탭에서 **열 선택** 아이콘을 클릭합니다.

    ![그림 99](Linked_image_Files/PowerBI_Lab03A_image8.png)

11. **열 선택** 창에서 모든 열을 선택 취소하려면 **(모든 열 선택)** 항목을 선택 취소합니다.

    ![그림 102](Linked_image_Files/PowerBI_Lab03A_image9.png)

12. 열을 포함하려면 다음 여섯 개의 열을 확인합니다.

    * EmployeeKey

    * EmployeeNationalIDAlternateKey

    * FirstName

    * LastName

    * Title

    * EmailAddress

13. **확인**을 클릭합니다.

    ![그림 104](Linked_image_Files/PowerBI_Lab03A_image10.png)

14. **적용된 단계** 목록에서 다른 쿼리 단계가 추가됩니다.

    ![그림 112](Linked_image_Files/PowerBI_Lab03A_image11.png)

15. 단일 이름 열을 만들려면 먼저 **FirstName** 열 헤더를 선택합니다.

16. **Ctrl** 키를 누르면서 **LastName** 열을 선택합니다.

    ![그림 116](Linked_image_Files/PowerBI_Lab03A_image12.png)

17. 선택한 열 헤더 중 하나를 마우스 오른쪽 단추로 클릭한 다음 컨텍스트 메뉴에서 **열 병합**을 선택합니다.

    ![그림 117](Linked_image_Files/PowerBI_Lab03A_image13.png)

    *상당수의 일반적인 변환은 열 헤더를 마우스 오른쪽 단추로 클릭한 다음 컨텍스트 메뉴에서 변환을 선택하여 적용할 수 있습니다. 하지만 리본에서 모든 변환 및 더 많은 것을 사용할 수 있습니다*.

18. **열 병합** 창의 **구분 기호** 드롭다운 목록에서 **공간을**선택합니다.

19. **새 열 이름** 상자에서 텍스트를 **Salesperson**으로 바꿉니다.

    ![그림 119](Linked_image_Files/PowerBI_Lab03A_image14.png)

20. **확인**을 클릭합니다.

    ![그림 5636](Linked_image_Files/PowerBI_Lab03A_image15.png)

21. **EmployeeNationalIDAlternateKey** 열의 이름을 변경하려면 **EmployeeNationalIDAlternateKey** 열 헤더를 두 번 클릭합니다.

22. 텍스트를 **EmployeeID**로 바꾼다음 **Enter** 키를 누릅니다.

    *열 이름을 변경하라는 지시가 있을 때 설명된 대로 정확하게 이름을 바꾸는 것이 중요합니다*.

23. 이전 단계를 사용하여 **EmailAddress** 열의 이름을 **UPN**으로 변경합니다.

    *UPN은 사용자 계정 이름의 약어입니다. 이 열의 값은 **랩 05A**에서 행 수준 보안을 구성할 때 사용됩니다*.

24. 왼쪽 아래 상태 표시줄에서 쿼리에 열이 5개, 행이 18개 있는지 확인합니다.

    ![그림 5638](Linked_image_Files/PowerBI_Lab03A_image16.png)

    *쿼리가 올바른 결과를 생성하지 않으면 나중에 랩을 완료할 수 없게 되므로 더 진행하지 않는 것이 중요합니다. 그렇지 않은 경우 이 작업의 단계를 다시 참조하여 문제를 해결하세요*.

### 작업 2: SalespersonRegion 쿼리 구성

이 작업에서는 **SalespersonRegion** 쿼리를 구성합니다.

1. **쿼리** 창에서 **DimEmployeeSalesTerritory** 쿼리를 선택합니다.

    ![그림 5639](Linked_image_Files/PowerBI_Lab03A_image17.png)

26. **쿼리 설정** 창에서 쿼리 이름을 **SalespersonRegion**으로 바꿉니다.

27. 마지막 두 열을 제거하려면 먼저 **DimEmployee** 열 헤더를 선택합니다.

28. **Ctrl** 키를 누르면서 **DimSalesTerritory**열 헤더를 선택합니다.

29. 선택한 열 헤더 중 하나를 마우스 오른쪽 단추로 클릭한 다음 컨텍스트 메뉴에서 **열 제거**를 선택합니다.

    ![그림 5640](Linked_image_Files/PowerBI_Lab03A_image18.png)

30. 상태 표시줄에서 쿼리에 두 개의 열과 39개의 행이 있는지 확인합니다.

    ![그림 5641](Linked_image_Files/PowerBI_Lab03A_image19.png)

### 작업 3: 제품 쿼리 구성

이 작업에서는 **제품** 쿼리를 구성합니다.

*랩에 자세한 지침이 이미 제공된 경우 랩 단계에서는 이제 더 간결한 지침이 제공됩니다. 자세한 지침이 필요한 경우 다른 작업을 다시 참조할 수 있습니다*.

1. **DimProduct** 쿼리를 선택합니다.

    ![그림 5643](Linked_image_Files/PowerBI_Lab03A_image20.png)

2. 쿼리 이름을 **제품**로 바꿉니다.

3. **FinishedGoodsFlag** 열을 찾은 다음 열을 필터링하여 완제품인 제품을 검색합니다(예: TRUE).

4. 다음을 제외한 모든 열을 제거합니다.

    * ProductKey

    * EnglishProductName

    * StandardCost

    * Color

    * DimProductSubcategory

5. **DimProductSubcategory** 열은 관련 테이블을 나타냅니다(**값** 링크가 포함됨).

6. 열 이름 오른쪽에 있는 **DimProductSubcategory** 열 헤더에서 확장 단추를 클릭합니다.

    ![그림 5644](Linked_image_Files/PowerBI_Lab03A_image21.png)

7. 모든 열을 선택 취소하려면 **(모든 열 선택)** 을 선택 취소합니다.

8. **EnglishProductSubcategoryName** 및 **DimProductCategory** 열을 선택하세요.

    ![그림 5646](Linked_image_Files/PowerBI_Lab03A_image22.png)

    *이 두 열을 선택하면 **DimProductSubcategory** 테이블에 결합하도록 변환이 적용된 다음 열을 포함하게 됩니다. **DimProductCategory** 열은 실제로는 별개의 관련 테이블입니다*.

9. **원래 열 이름을 접두사로 사용** 확인란을 선택 취소합니다.

![그림 5647](Linked_image_Files/PowerBI_Lab03A_image23.png)

    *쿼리 열 이름은 항상 고유해야 합니다. 이 확인란을 선택하면 각 열의 이름에 확장된 열 이름이 접두사로 추가됩니다(이 경우 **DimProductSubcategory**). 선택한 열이 **제품** 쿼리의 열과 충돌하지 않는 것으로 알려져 있으므로 옵션이 선택 해제됩니다*.

10. **확인**을 클릭합니다.

    ![그림 5648](Linked_image_Files/PowerBI_Lab03A_image24.png)

11. 변환 결과 두 개의 열이 생성되고 **DimProductCategory** 열이 제거되었습니다.

12. **DimProductCategory**를 확장한 다음 **EnglishProductCategoryName** 열만 도입합니다.

13. 다음 네 개의 열의 이름을 변경합니다.

    * **EnglishProductName**을 **Product**

    * **StandardCost**를 **Standard Cost**로(공백 포함)

    * **EnglishProductSubcategoryName**를 **Subcategory**로

    * **EnglishProductCategoryName**를**Category**

14. 상태 표시줄에서 쿼리에 열이 6개, 행이 397개 있는지 확인합니다.

    ![그림 5651](Linked_image_Files/PowerBI_Lab03A_image25.png)

### 작업 4: 재판매인 쿼리 구성

이 작업에서는 **재판매인** 쿼리를 구성합니다.

1. **DimReseller** 쿼리를 선택합니다.

    ![그림 5653](Linked_image_Files/PowerBI_Lab03A_image26.png)

2. 쿼리 이름을 **재판매인**으로 변경합니다.

3. 다음을 제외한 모든 열을 제거합니다.

    * ResellerKey

    * BusinessType

    * RellerName

    * DimGeography

4. **DimGeography** 열을 확장하여 다음 세 개의 열만 포함합니다.

    * City

    * StateProvinceName

    * EnglishCountryRegionName

![그림 5656](Linked_image_Files/PowerBI_Lab03A_image27.png)

5. **비즈니스 유형** 열 헤더에서 아래쪽 화살표를 클릭한 다음 항목과 웨어하우스의 잘못된 맞춤법을 검토합니다.

    ![그림 2](Linked_image_Files/PowerBI_Lab03A_image28.png)

  
​ 

6. **비즈니스 유형** 열 헤더를 마우스 오른쪽 단추로 클릭한 다음 **값 바꾸기**를 선택합니다.

    ![그림 4](Linked_image_Files/PowerBI_Lab03A_image29.png)

7. **값 바꾸기** 창에서 다음 값을 구성합니다.

    * **찾을 값** 상자에서 **Ware House**를 입력합니다

    * **바꿀 항목** 상자에서 **Warehouse**를 입력합니다

    ![그림 5](Linked_image_Files/PowerBI_Lab03A_image30.png)

8. **확인**을 클릭합니다.

    ![그림 6](Linked_image_Files/PowerBI_Lab03A_image31.png)

9. 다음 네 개의 열의 이름을 변경합니다.

    * **BusinessType**을 **비즈니스 유형**으로 (공백 포함)

    * **ResellerName**을 **재판매인**으로

    * **StateProvinceName**을 **주-도**로

    * **EnglishCountryRegionName**을 **국가-지역**으로

10. 상태 표시줄에서 쿼리에 6개의 열과 701개의 행이 있는지 확인합니다.

    ![그림 5657](Linked_image_Files/PowerBI_Lab03A_image32.png)

### 작업 5: 지역 쿼리 구성

이 작업에서는 **지역** 쿼리를 구성합니다.

1. **DimSalesTerritory** 쿼리를 선택합니다.

    ![그림 5659](Linked_image_Files/PowerBI_Lab03A_image33.png)

2. 쿼리 이름을 **지역**으로 바꿉니다.

3. 값 0(영)을 제거하려면 **SalesTerritoryAlternateKey** 열에 필터를 적용합니다.

    ![그림 5660](Linked_image_Files/PowerBI_Lab03A_image34.png)

4. 다음을 제외한 모든 열을 제거합니다.

    * SalesTerritoryKey

    * SalesTerritoryRegion

    * SalesTerritoryCountry

    * SalesTerritoryGroup

5. 다음 세 개의 열의 이름을 변경합니다.

    * **SalesTerritoryRegion**을 **지역**으로

    * **SalesTerritoryCountry**를  **국가**

    * **SalesTerritoryGroup**을 **그룹**으로

6. 상태 표시줄에서 쿼리에 열이 4개, 행이 10개 있는지 확인합니다.

    ![그림 5661](Linked_image_Files/PowerBI_Lab03A_image35.png)

### 작업 6: 판매 쿼리 구성

이 작업에서는 **판매** 쿼리를 구성합니다.

1.  **FactResellerSales** 쿼리를 선택합니다.

    ![그림 5663](Linked_image_Files/PowerBI_Lab03A_image36.png)

2. 쿼리 이름을 **판매**로 바꿉니다.

3. 다음을 제외한 모든 열을 제거합니다.

    * SalesOrderNumber

    * OrderDate

    * ProductKey

    * ResellerKey

    * EmployeeKey

    * SalesTerritoryKey

    * OrderQuantity

    * 단가

    * TotalProductCost

    * SalesAmount

    * DimProduct

    ***랩 02A**에서 **FactResellerSales** 행의 일부가 **TotalProductCost** 값을 누락했다는 것을 기억하세요. **DimProduct** 열이 포함되어 제품 표준 비용을 검색하여 누락된 값을 수정합니다*.

4. **DimProduct** 열을 확장한 다음 **StandardCost** 열을 포함합니다.

5. 사용자 지정 열을 만들려면 **일반** 그룹 내의 **열 추가** 리본 탭에서 **사용자 지정 열**을 클릭합니다.

    ![그림 5664](Linked_image_Files/PowerBI_Lab03A_image37.png)

6. **새 열 이름** 상자의 **사용자 지정 열** 창에서 텍스트를 **비용**으로 바꿉니다.

    ![그림 5665](Linked_image_Files/PowerBI_Lab03A_image38.png)

7. **사용자 지정 열 수식** 상자에서 다음 식을 등호 뒤에 입력합니다.

8. 편의를 위해 **D:\DA100\Lab03A\Assets\Snippets.txt** 파일에서 식을 복사할 수 있습니다.

    **파워 쿼리**

    ```
    if [TotalProductCost] = null then [OrderQuantity] * [StandardCost] else [TotalProductCost]
    ```

    *이 식은 **TotalProductCost** 값이 누락되었는지 테스트합니다. 누락된 경우 **OrderQuantity** 값을 **StandardCost** 값으로 곱하여 값을 생성하며 그렇지 않으면 기존 **TotalProductCost** 값을 사용합니다*.

9. **확인**을 클릭합니다.

    ![그림 5666](Linked_image_Files/PowerBI_Lab03A_image39.png)

10. 다음 두 개의 열을 제거합니다.

    * TotalProductCost

    * StandardCost

11. 다음 세 개의 열의 이름을 변경합니다.

    * **OrderQuantity**을  **수량**대한 주문 수량

    * **UnitPrice**를 **단가**로

    * **SalesAmount**를 **Sales**로

12. 열 데이터 형식을 수정하려면 열 이름 왼쪽에 있는 **수량** 열 헤더에서 **1.2** 아이콘을 클릭한 다음 **정수**를 선택합니다.

    ![그림 5667](Linked_image_Files/PowerBI_Lab03A_image40.png)

    *올바른 데이터 형식을 구성하는 것이 중요합니다. 열에 숫자 값이 포함 된다면 수학적 연산을 수행할 것으로 예상될 경우 올바른 형식을 선택하는 것도 중요합니다.*

13. 다음 세 개의 열 데이터 형식을 **고정 10진수**로 수정합니다.

    * 단가

    * 영업

    * 비용

    ![그림 5668](Linked_image_Files/PowerBI_Lab03A_image41.png)

    *고정 10진수 데이터 유형은 완전한 정밀도로 값을 저장하므로 10진수만큼 더 많은 저장 공간이 필요합니다. 재무 값 또는 비율(예: 환율)에 고정 10진수 유형을 사용하는 것이 중요합니다*.

14. 상태 표시줄에서 쿼리에 열이 10개, 행이 999개 이상 있는지 확인합니다.

    ![그림 5669](Linked_image_Files/PowerBI_Lab03A_image42.png)

    *최대 1,000개의 행이 각 쿼리에 대한 미리 보기 데이터로 로드됩니다*.

### 작업 7: 대상 쿼리 구성

이 작업에서는 **대상** 쿼리를 구성합니다.

1. **ResellerSalesTargets** 쿼리를 선택합니다.

    ![그림 5672](Linked_image_Files/PowerBI_Lab03A_image43.png)

2. 쿼리 이름을 **대상**으로 변경합니다.

3. 12개월 열(**M01**-**M12**)을 피벗 해제하려면 먼저 **연도** 및 **EmployeeID** 열 헤더를 다중 선택합니다.

    ![그림 5673](Linked_image_Files/PowerBI_Lab03A_image44.png)

4. 선택한 열 헤더 중 하나를 마우스 오른쪽 단추로 클릭한 다음 컨텍스트 메뉴에서 **다른 열 피벗 해제**를 선택합니다.

    ![그림 5674](Linked_image_Files/PowerBI_Lab03A_image45.png)

5. 열 이름이 이제 **특성** 열에 나타나고 값이 **값** 열에 나타납니다.

6. **값** 열에 필터를 적용하여 하이픈(-) 값을 제거합니다.

7. 다음 두 열의 이름을 변경합니다.

    * **특성**을 **MonthNumber**으로(두 단어 간 공간 없음. 추후 제거됨)

    * **값**을 **대상**으로

    *이제 변환을 적용하여 날짜 열을 생성합니다. 날짜는 **연도** 및 **MonthNumber** 열에서 파생됩니다. **예제에서 열 생성** 기능을 사용하여 열을 만듭니다*.

8. **MonthNumber** 열 값을 준비하려면 **MonthNumber** 열 헤더를 마우스 오른쪽 단추로 클릭한 다음 **값 바꾸기**를 선택합니다.

    ![그림 5676](Linked_image_Files/PowerBI_Lab03A_image46.png)

9. **값 바꾸기** 창의 **찾을 값** 상자에서 **M**을 입력합니다.

    ![그림 5677](Linked_image_Files/PowerBI_Lab03A_image47.png)

10. **확인**을 클릭합니다.

11. **MonthNumber** 열 데이터 형식을 **정수**로 수정합니다.

    ![그림 5678](Linked_image_Files/PowerBI_Lab03A_image48.png)

12. **일반** 그룹 내부의 **열 추가** 리본 탭에서 **예제에서 열 생성** 아이콘을 클릭합니다.

    ![그림 5675](Linked_image_Files/PowerBI_Lab03A_image49.png)

13. 첫 번째 행은 **2017**년, 월 번호 **7**입니다.

14. **Column1** 열의 첫 번째 표 셀에서 **7/1/2017**을 입력한 다음 **Enter**를 누릅니다.

    *가상 머신은 미국 지역 설정을 사용하므로 이 날짜는 실제로 2017년 7월 1일입니다*.

15. 모눈 셀이 예측값으로 업데이트됩니다.

    이 기능은 두 열의 값을 결합하고 있음을 정확하게 예측했습니다.

16. 또한 쿼리 표 위에 표시되는 수식도 확인합니다.

    ![그림 5679](Linked_image_Files/PowerBI_Lab03A_image50.png)

17. 새 열의 이름을 바꾸려면 **병합된** 열 헤더를 두 번 클릭합니다.

18. **TargetMonth**로 열 이름을 변경합니다.

    ![그림 5680](Linked_image_Files/PowerBI_Lab03A_image51.png)

19. **확인**을 클릭합니다.

    ![그림 5681](Linked_image_Files/PowerBI_Lab03A_image52.png)

20. 다음 열을 제거합니다.

    * 연도

    * MonthNumber

21. 다음 열 데이터 형식을 수정합니다.

    * **Target**을 고정 10진수로

    * **TargetMonth**을 날짜로

22. **Target** 값을 1000으로 곱하려면 **Target** 열 헤더를 선택한 다음 **숫자 열** 그룹 내부의 **변환** 리본 탭에서 **표준**을 클릭한 다음 **곱하기**를 선택합니다.

    ![그림 5682](Linked_image_Files/PowerBI_Lab03A_image53.png)

23. **곱하기** 창에서 **값** 상자에 **1000**을 입력합니다.

    ![그림 5683](Linked_image_Files/PowerBI_Lab03A_image54.png)

24. **확인**을 클릭합니다.

    ![그림 5684](Linked_image_Files/PowerBI_Lab03A_image55.png)

25. 상태 표시줄에서 쿼리에 세 개의 열과 809개의 행이 있는지 확인합니다.

    ![그림 5685](Linked_image_Files/PowerBI_Lab03A_image56.png)

### 작업 8: ColorFormats 쿼리 구성

이 작업에서는 **ColorFormats** 쿼리를 구성합니다.

1. **ColorFormats** 쿼리를 선택합니다.  
	![그림 5687](Linked_image_Files/PowerBI_Lab03A_image57.png)

2. 첫 번째 행에는 열 이름이 포함되어 있습니다.

3. **변환** 그룹 내의 **홈** 리본 탭에서 **첫 행을 머리글로 사용**을 클릭합니다.  
    ![그림 5688](Linked_image_Files/PowerBI_Lab03A_image58.png)

4. 상태 표시줄에서 쿼리에 세 개의 열과 10개의 행이 있는지 확인합니다.  
	![그림 5689](Linked_image_Files/PowerBI_Lab03A_image59.png)

### 작업 9: 제품 쿼리 업데이트

이 작업에서는 **ColorFormats** 쿼리를 병합하여 **제품** 쿼리를 업데이트합니다.

1. **제품** 쿼리를 선택합니다.  
	![그림 5690](Linked_image_Files/PowerBI_Lab03A_image60.png)

1. **결합** 그룹 내의 **홈** 리본 탭에서 **ColorFormats** 쿼리를 병합하려면 **쿼리 병합**을 클릭합니다.  
	![그림 5654](Linked_image_Files/PowerBI_Lab03A_image61.png)  
	*쿼리 병합을 통해 다른 데이터 원본(SQL Server 및 CSV 파일)에서 데이터를 통합할 수 있습니다*.

1. **제품** 쿼리 표의 **병합** 창에서 **색상** 열 헤더를 선택합니다.  
	![그림 5655](Linked_image_Files/PowerBI_Lab03A_image62.png)

1. **제품** 쿼리 표 아래의 드롭다운 목록에서 **ColorFormats** 쿼리를 선택합니다.

1. **ColorFormats** 쿼리 표에서 **색상** 열 헤더를 선택합니다.

1. **개인 정보 수준** 창이 열리면 해당 드롭다운 목록에서 두 데이터 원본 각각에 대해 **조직**을 선택합니다.  
	![그림 5691](Linked_image_Files/PowerBI_Lab03A_image63.png)  
	*데이터 원본에 대해 개인 정보 수준을 구성하여 원본 간에 데이터를 공유할 수 있는지 확인할 수 있습니다. 각 데이터 원본을 **조직**으로 설정하면 필요한 경우 데이터를 공유할 수 있습니다. 개인 데이터 원본은 다른 데이터 원본과 공유할 수 없습니다. 이는 개인 데이터를 공유할 수 없다는 의미가 아니며 파워 쿼리 엔진은 소스 간에 데이터를 공유할 수 없다는 의미입니다.*

1. **저장**을 클릭합니다.  
	![그림 5692](Linked_image_Files/PowerBI_Lab03A_image64.png)

1. **병합** 창에서 **확인**을 클릭합니다.  
	![그림 5693](Linked_image_Files/PowerBI_Lab03A_image65.png)

1. 다음 두 개의 열을 포함하도록 **ColorFormats** 열을 확장합니다.
    * 배경색 형식  
    * 글꼴 색상 형식

	![그림 5694](Linked_image_Files/PowerBI_Lab03A_image66.png)

1. 상태 표시줄에서 쿼리에 이제 8개의 열과 397개의 행이 있는지 확인합니다.  
	![그림 5695](Linked_image_Files/PowerBI_Lab03A_image67.png)

### 작업 10: ColorFormats 쿼리 업데이트

이 작업에서는 **ColorFormats**를 업데이트하여 로드를 비활성화합니다.

1. **ColorFormats** 쿼리를 선택합니다.  
	![그림 321](Linked_image_Files/PowerBI_Lab03A_image68.png)

2. **쿼리 설정** 창에서 **모든 속성** 링크를 클릭합니다.  
	![그림 322](Linked_image_Files/PowerBI_Lab03A_image69.png)

3. **쿼리 속성** 창에서 **보고하기 위해 로드 실행** 확인란을 선택 취소합니다.  
	![그림 323](Linked_image_Files/PowerBI_Lab03A_image70.png)  
	*로드를 비활성화하면 데이터 모델에 테이블로 로드되지 않습니다. 쿼리가 데이터 모델에 사용 가능한 제품 쿼리와 병합되었기 때문에 이 작업이 수행됩니다.*

4. **확인**을 클릭합니다.  
	![그림 324](Linked_image_Files/PowerBI_Lab03A_image71.png)

### 완료

이 작업에서는 랩을 완료합니다.

1. 다음과 같이 올바르게 명명된 8개의 쿼리가 있는지 확인합니다.

    * Salesperson

    * SalespersonRegion

    * Product

    * Reseller

    * Region

    * 영업

    * Target

    * ColorFormats(데이터 모델에 로드되지 않음)

2. 데이터 모델을 로드하려면 **파일** backstage 보기에서 **닫기 및 적용**을 선택합니다.  
	![그림 326](Linked_image_Files/PowerBI_Lab03A_image72.png)  
	*이제 모든 로드 지원 쿼리가 데이터 모델에 로드됩니다*.

3. **필드** 창(오른쪽에 위치)에서 데이터 모델에 로드된 7개의 테이블을 확인합니다.  
	![그림 3](Linked_image_Files/PowerBI_Lab03A_image73.png)

4. Power BI Desktop 파일을 저장합니다.

5. Power BI Desktop을 열어 둡니다.  
	*다음 랩에서는 데이터 모델 테이블 및 관계를 구성합니다.*
