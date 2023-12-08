## Ubuntu로 가상 서버 만들기 (Mac 버전)
- ubuntu,UTM 
- cockpit   
- cloudpanel  
----
1.ubuntu,UTM 설치  
<https://king-ja.tistory.com/93>

***M1,M2 다 지원가능***
***UTM( Uncomplicated Terminal Master): ubuntu 운영체제 위에서 실행되는 가상화(VM)관리도구***     

나머지는 올려둔 사이트 대로 하면 된다.    
그럼 설정 완료!  
2. update&upgrade

시스템의 보안강화와 안정성과 성능을 유지&향상을 위해 해준다.

    $sudo apt-get update
    $sudo apt-get upgrade

### update와upgrade의 차이점?
update:이전 정보를 최신화 하는것  
upgrade:성능,품질등을 한단계 끌어올리는것    

update시 오류가 떴었는데 이렇게 해결하였다


1. Apt 설정 파일 열기

   ```bash
   sudo nano /etc/apt/sources.list
   ```

3. CD/DVD-ROM 관련 줄 주석 처리
   `sources.list` 파일을 열면 다음과 같은 줄이 있을 것입니다.

   ```
   deb file:/cdrom jammy release
   ```

   이 줄을 주석 처리하려면 줄 앞에 `#`을 추가합니다.

   ```
   # deb file:/cdrom jammy release
   ```

   


4. 변경 사항 저장
   수정을 완료하고 저장하려면 `Ctrl + O`를 누르고 Enter를 누른 다음, 파일을 닫으려면 `Ctrl + X`를 누릅니다.

5. 다시 업데이트 명령 실행
   마지막으로 패키지 목록을 업데이트하려면 다음 명령어를 실행합니다.

   ```bash
   sudo apt update
   ```

3.cockpit install

### Cockpit이란?
리눅스 서버를 웹 기반으로 관리하기 위한 사용자 친화적인 웹 인터페이스이다.
