## mac OS Big sur -> Calatlina 다운그레이드 가이드



1. https://apps.apple.com/kr/app/macos-catalina/id1466841314?l=en&mt=12 위 링크에 들어가 Mac OS Calalina 를 **다운로드** 받는다 ( 약 8.25 GB )
2. **16기가 이상의 USB**를 준비하고 맥을 정상 부팅 후 **디스크 유틸리티** 를 실행한다.
3. 보기 메뉴에서 **모든 디바이스** 를 선택한 후, USB의 최상위 드라이브를 선택한다. ( 볼륨이 아닌 최상의 드라이브 )
4. **지우기** 옵션을 누른 후, **드라이브명을 지정**하고, **맥OS확장(저널링)** ( mac OS Extend ( Journalerd) ), **GUID 파티션 맵** 을 차례로 선택한 후 **지우기** 를 눌러준다.
5. **터미널을 실행**하고, `sudo /Applications/Install\ macOS\ Catalina.app/Contents/Resources/createinstallmedia --volume /Volumes/드라이브명` 명령어를 입력해준다.
6. 사용자 비밀번호를 입력하고, Y를 입력한다.
7. 사용한 USB의 속도에 따라 시간이 소요된다. ( 이때 중간에 한번이라도 강제로 종료할 시 Error erasing disk error number (-69888, 0) 에러가 발생하여 이때 사용한 USB로는 포멧을 해도 재사용이 불가능하다. 다른 USB를 사용하거나, 포멧 옵션 중 7 패스 방식을 사용하여 포멧하여 사용하여야 한다. )
8. mac을 종료하고, **복구 모드** ( cmd + R )로 재시동한다.
9. 상단 메뉴의 유틸리티 -> 시동 보안 유틸리티 에서 **외부 전원 장치로 부팅 허용** 옵션을 활성화한다.
10. 다시 mac을 종료한 뒤 **듀얼부팅 모드** ( cmd + option )로 재시동한 뒤 **Install Mac OS Catalina** 를 선택한다.
11. 로딩이 끝나면 **디스크 유틸리티** 를 선택해 **Macintosh HD** 를 선택해 **APFS** 형식으로 포멧한다.
12. 디스크 유틸리티를 종료하고, **mac OS 설치** 를 선택해 진행해준다. ( Macintosh HD 에 설치 )
13. 안정적인 버전이 나올때 까지 **Big sur로 업그레이드 하지 않는다.**

