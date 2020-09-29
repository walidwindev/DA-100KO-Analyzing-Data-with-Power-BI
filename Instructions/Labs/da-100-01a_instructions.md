

### 랩 01A

시작하기

# 개요

**랩을 완료하는 데 예상되는 시간은 15분입니다.**

이 랩에서는 강의실 가상 머신에 연결하고 환경을 설정합니다. 이 랩을 시작하기 전에 계정과 암호를 받아야 합니다. 제공된 계정을 사용하여 랩을 완료하는 것이 중요합니다.

이 랩의 학습 내용은 다음과 같습니다.

* Power BI 서비스에 로그인

* 작업 영역 만들기

* Power BI Desktop 열기

# 연습 1: 시작

이 연습에서는 교실 가상 머신에 연결하고 환경을 설정합니다.

### 작업 1: 계정 세부 정보 기록

이 작업에서는 **MySettings.txt** 파일을 열고, 계정 세부 정보를 기록합니다.

*강사가 계정을 제공했으며 이 계정을 사용하여 모든 랩을 완료하는 것이 중요합니다. 계정이 제공되지 않은 경우 https://powerbi.microsoft.com/ko-kr/documentation/powerbi-admin-signing-up-for-power-bi-with-a-new-office-365-trial로 이동하여 이 랩을 계속하기 전에 계정을 만드는 단계를 따릅니다.*

1. 파일 탐색기를 열려면 작업 표시줄에서 파일 탐색기 프로그램 바로 가기를 클릭합니다.

    ![그림 7](Linked_image_Files/PowerBI_Lab01A_image1.png)

2. 파일 탐색기에서 **D:\DA100\Setup** 폴더로 이동합니다.

3. **MySettings.txt** 파일을 열려면 파일을 두 번 클릭합니다.

4. **MySettings.txt** 파일에서 레이블 옆에 계정 이름과 암호를 입력합니다.

    ![그림 9](Linked_image_Files/PowerBI_Lab01A_image2.png)

5.  **MySettings.txt** 파일을 저장하려면, **파일** 메뉴에서 **저장**(또는**Ctrl+S**를 누르기)을 선택합니다.

6.  **MySettings.txt**파일을 열어 둡니다. 

7. 파일 탐색기를 열어 둡니다.

### 작업 2: Power BI 서비스에 로그인

이 작업에서는 Power BI 서비스에 로그인합니다.

1. 작업 표시줄에서 Edge를 열려면 Microsoft Edge 프로그램 바로 가기를 클릭합니다.

    ![그림 1](Linked_image_Files/PowerBI_Lab01A_image3.png)

9. Edge에서 **http://powerbi.com**으로 이동합니다.

    *팁: Microsoft Edge 즐겨찾기 모음에서 Power BI Service 즐겨찾기를 사용할 수도 있습니다*.

10.  **로그인** 오른쪽 상단 모서리에 위치)을 클릭합니다.

    ![그림 5](Linked_image_Files/PowerBI_Lab01A_image4.png)

11. **MySettings.txt** 파일에서 계정 세부 정보를 입력합니다.

12. 암호를 업데이트하라는 메시지가 표시되면 제공된 암호를 다시 입력한 다음 새 암호를 입력하고 확인합니다. 새 암호로 **MySettings.txt** 파일을 업데이트해야 합니다.

13. 로그인 프로세스를 완료합니다.

14. Edge에서 로그인 상태를 유지하라는 메시지가 표시되면 **예**를 클릭합니다.

15. Power BI 서비스의 오른쪽 상단 모서리에 있는 'AuNew Look'Au가 활성화되지 않은 경우 슬라이더 컨트롤을 클릭하여 켭니다.

    ![그림 13](Linked_image_Files/PowerBI_Lab01A_image5.png)

16. Microsoft Edge 창을 열어 둡니다.

  


### 작업 3: 작업 영역 만들기

이 작업에서는 작업 영역을 만듭니다. 또한 계정을 Power BI Pro로 업그레이드합니다.

*이 과정에서 개발하는 모든 콘텐츠가 이 작업 영역에 추가됩니다.*

1. 작업 영역을 만들려면 **탐색** 창(왼쪽에 위치)에서 **작업 영역**을 클릭한 다음 **작업 영역 만들기**를 클릭합니다.

    ![그림 14](Linked_image_Files/PowerBI_Lab01A_image6.png)

18. 계정을 Power BI Pro로 업그레이드하라는 메시지가 표시되면 **무료 체험**을 클릭합니다.

    ![그림 17](Linked_image_Files/PowerBI_Lab01A_image7.png)

    *작업 영역을 만들고 작업하려면 Power BI Pro 라이선스가 필요합니다. 콘텐츠를 공유할 때도 필요합니다. 평가판을 통해 최대 60일 동안 Pro 기능으로 작업할 수 있습니다.*

19. 60일 무료 프로 평가판을 시작하라는 메시지가 표시되면 **평가판 시작**을 클릭합니다.

    ![그림 18](Linked_image_Files/PowerBI_Lab01A_image8.png)

20. 평가판이 연장된 경우 **닫기**를 클릭합니다.

21. 이 작업의 첫 번째 단계를 반복하여 작업 영역을 만듭니다.

22. **작업 영역 만들기** 창(오른쪽에 위치)에서 **작업 영역 이름** 상자에 작업 영역의 이름을 입력합니다.

    *영역 이름은 리소스 그룹 내에서 고유해야 합니다. 작업 영역의 이름을 **영업 분석**으로 지정하고 이니셜도 추가합니다. 예를 들어 이름은 **판매 분석 AB**일 수 있습니다*.

23. 작업 영역을 만들려면 창 하단에 **저장**을 클릭합니다.

    ![그림 21](Linked_image_Files/PowerBI_Lab01A_image9.png)

24. **탐색** 창에서 작업 영역이 열려 있음을 알 수 있습니다. 

    ![그림 22](Linked_image_Files/PowerBI_Lab01A_image10.png)

25. **랩 03D**의 작업 영역에 콘텐츠를 게시합니다.

  


### 작업 4: Power BI Desktop 열기

이 작업에서는 Power BI Desktop을 열고 계정을 사용하여 로그인합니다.

26. Power BI Desktop을 열려면 작업 표시줄에서 Microsoft Power BI Desktop 바로 가기를 클릭합니다.

    ![그림 2](Linked_image_Files/PowerBI_Lab01A_image11.png)

27. 메시지가 표시되면 **로그인**을 클릭합니다.

    ![그림 25](Linked_image_Files/PowerBI_Lab01A_image12.png)

28. **MySettings.txt** 계정 세부 정보를 사용하여 로그인 프로세스를 완료합니다.

29. Power BI Desktop의 오른쪽 상단 모서리에서 계정이 표시되는지 확인합니다.

    ![그림 27](Linked_image_Files/PowerBI_Lab01A_image13.png)

30. Power BI Desktop을 열어 둡니다.

    ***Lab 02A**에서 데이터 모델 개발을 시작합니다*.

  


### 작업 5: 랩 데이터베이스 업데이트

이 작업에서는 PowerShell 스크립트를 실행하여 **AdventureWorksDW2020** 데이터베이스의 데이터를 업데이트합니다.

1. 파일 탐색기에서 **D:\DA100\Setup** 폴더 내부의 **UpdateDatabase-1-UpdateAccount.ps1** 파일을 마우스 오른쪽 단추로 클릭한 다음 **PowerShell으로 실행**을 선택합니다.

    ![그림 28](Linked_image_Files/PowerBI_Lab01A_image14.png)

32. **Windows PowerShell** 창에서 계정을 입력하라는 메시지가 표시되면 **MySettings.txt**파일에서 계정 이름에 붙여 넣습니다.

    *팁: **Windows PowerShell** 창에 붙여 넣으려면, **계정** 프롬프트에서 마우스 오른쪽 단추를 클릭합니다.*

    ![그림 29](Linked_image_Files/PowerBI_Lab01A_image15.png)

33. 데이터베이스를 업데이트하려면 **Enter** 키를 누릅니다.

34. 계속하려면 아무 키나 누르라는 메시지가 표시되면, **Enter** 키를 다시 누릅니다.

    ***AdventureWorksDW2020** 데이터베이스가 계정 세부 정보를 사용하도록 업데이트되었습니다. 이제 영업 직원인 마이클 브라이스(Michael Blythe)가 되었다고 가정하며, 세 가지 영업권역 지역의 판매로 판매 실적을 측정합니다. 미국 북동부, 미국 중부, 미국 남동부*.

    *이러한 사실은 **랩 03B**에서 행 수준 보안을 구현할 때 연관됩니다*.
