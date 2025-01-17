# korea-covid-19-remaining-vaccine-macro
잔여백신 지도 API로 남은 백신 수를 확인하고, 잔여백신이 있는 경우 잔여백신 예약 페이지로 이동합니다.

## 카카오 잔여백신 예약
### 이용방법
1. [https://accounts.kakao.com/login](https://accounts.kakao.com/login?continue=https%3A%2F%2Faccounts.kakao.com%2Fweblogin%2Faccount%2Finfo) 에 접근하여 카카오 로그인을 합니다.
2. https://vaccine.kakao.com/api/v1/user 에 접근하여 본인의 정보가 정상적으로 표시되는지 확인합니다.  
정상적으로 표시되지 않는 경우 카카오톡에서 잔여백신 알림 신청을 해줍니다.
3. https://vaccine-map.kakao.com/map2?v=1 에서 지도를 움직여서 잔여백신을 검색할 지역을 설정하고, 개발자도구를 열어 해당 위치의 x, y값을 기록해둡니다. 자세한 방법은 [#2](https://github.com/SJang1/korea-covid-19-remaining-vaccine-macro/discussions/2) 에 있습니다.
4. [Release](https://github.com/SJang1/korea-covid-19-remaining-vaccine-macro/releases) 페이지에서 .exe 파일을 다운받고 실행합니다.
5. 백신이 발생하면 해당 병원 잔여백신 예약 페이지로 이동되며, 바로 당일예약이 됩니다.

### 주의사항
- 잔여백신 예약 성공의 타이밍이 매번 다릅니다. 어떤 경우는 잔여백신이 발생한 직후에는 예약이 실패하기도 합니다. 따라서, 타이밍이 다르게 `time.sleep(시간)`을 다르게 설정 후, 두 개 이상의 프로세스를 실행하기를 권장합니다.
- 예약 시도 후에는 자동 예약 프로그램은 정지됩니다.
- 예약 시도가 반드시 성공 한다는 보장이 없습니다.
- 예약 시도 후에는 다시 시도 할 경우 이용 방법의 5번째 항목에 있는 터미널에서 실행하는 부분부터 다시 시작하셔야 합니다.
- 코드를 수정하지 않는다고 하면 크롬브라우저가 설치되어 있어야 하며, 모든 이용방법은 크롬 브라우저를 이용하셔야 합니다.

## 네이버 잔여백신 예약
### 주의사항
- 네이버 서버의 문제로, 잔여백신이 발생할 때마다 잔여백신 지도 API가 작동을 하지 않습니다.

## Disclaimer
- 본 프로그램은 매크로를 이용한 백신 예약을 유도하는 내용이 아니며, 해당 프로그램을 사용함으로서 생기는 책임은 모두 이용자 본인에게 있습니다.
