- build.sh 로 빌드하려면 ...
1) source build.sh
   -->build 폴더 생성 및 자동으로 build 폴더로 이동
2) cmake --build .
   -->build 안에 있는 CMakeFiles 대로 설치

끝

만약 이 중에 오류가 발생한다면, 
If one of the dependencies can't be found by CMake, use the "-DCMAKE_PREFIX_PATH=" option to tell CMake where to find them. For example, if CMake can't find GLEW :
```
cmake -DCMAKE_PREFIX_PATH="/path/to/glew/glew-2.1.0/build/" ..
```



- 구글 드라이브 대용량 데이터 wget으로 다운받는법

wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=파일ID' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=파일ID" -O 파일명 && rm -rf /tmp/cookies.txt

출처: https://redstarhong.tistory.com/105 [홍석쓰 블로그]

예시:
wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=1heFZLbm1GEMOEjvBB5Z3nvVREwYSPuGe' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=1heFZLbm1GEMOEjvBB5Z3nvVREwYSPuGe" -O snapshot_18.pth.tar && rm -rf /tmp/cookies.txt



**주의** 위를 바로 복사하는 게 아니라, 직접 타이핑하거나, Readme 파일 수정 탭(fork한 뒤)에가서 복사해야 실행됨.

*파일ID는 첨부한 사진의 붉은 부분(2번 있으므로 둘다 입력), 파일명은 이전 디렉토리 없이 파일명만*


![google_big_data](https://user-images.githubusercontent.com/54311546/104596424-4e718b00-56b7-11eb-8a4d-e3108647b320.png)

- 쉘 스크립트 bash 실행 에러 : syntax error : unexpected end of file
문법적으로 오류가 없는데, 이 오류가 뜬다면 Windows OS에서 작성한 스크립트 파일을 Unix(Linux/Mac OS)에서 실행하는 데 문제가 발생한 것이다.
따라서, dos2unix ./run.sh 명령어를 실행시켜주면 된다.
