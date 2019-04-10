기본구축과정(strapi서버:1337, 개발서버:4000)

1. github에서 strapi폴더 다운(구축성공한버전)
2. 다운받은 strapi폴더 들어가서 우클릭으로 "터미널에서 열기"
3. 그 경로로 vscode 실행
   [code .]
4. 상단에 터미널 메뉴 눌러서 새 터미널 열어
   dev버전에서 기본 플러그인 설치하고 사용 할수있게 하는 명령어 터미널에 입력
   [sudo npm run setup:build]
   - 혹시 Error: EACCES: permission denied 뜨면 [npm config set unsafe-perm=true] 입력
5. 지금있는 strapi폴더 밖의 경로로 이동하는 명령어 터미널에 입력
   [cd ..]
6. strapi –dev버전 생성 명령어 터미널에 입력(ex// project_name)
   [strapi new project_name –dev]
7. 설치 완료 후 생성된 project_name 폴더로 경로 이동하는 명령어 터미널에 입력
   [cd project_name]
8. strapi 서버여는 명령어 터미널에 입력(strapi서버:1337)
   [strapi start]
9. admin계정 생성
   - 아이디가 아닌 이메일로 로그인
10. 기본 플러그인 생성해주는 명령어 터미널에 입력
    [strapi generate:plugin plugin_name]
11. project_name 폴더안의 admin폴더로 이동하는 명령어 터미널에 입력
    [cd admin]
12. 플러그인에 개발에 필요한 파일들 생성하는 명령어 터미널에 입력
    [npm run setup]
13. admin폴더에서 project_name 폴더로 이동하는 명령어 터미널에 입력
    [cd ..]
14. 플러그인과 프로젝트 연동하는 명령어 터미널에 입력
    [npm run setup ---plugins]
15. strapi 서버여는 명령어 터미널에 입력
    [strapi start]
16. strapi 서버 좌측 plugins메뉴에 생성한 플러그인(ex// plugin_name) 확인
17. vscode 터미널 분할 후 admin폴더 이동하는 명령어 터미널에 입력
    [cd admin]
18. 플러그인 개발 서버 여는 명령어 터미널에 입력(개발서버:4000)
    [npm start]
19. 개발 서버 구동 확인
20. 확인 위해 플러그인 내용 조금 바꿔서 저장(플러그인 내용 수정하면 4000서버에만 수정)
    project_name/plugins/plugin_name/admin/src/containers/ExamplePage/index.js
21. 개발 서버에 변경사항 확인(plugins메뉴-project_name)
22. project_name폴더로 이동하는 명령어 터미널에 입력
    [cd ..]
23. 플러그인 수정내용 strapi 서버(strapi서버:1337) 연동하는 명령어 터미널에 입력
    [npm run setup ---plugins]
24. strapi 서버 닫았다가 열어 플러그인 내용 수정된 부분 연동확인(plugins메뉴-project_name)
