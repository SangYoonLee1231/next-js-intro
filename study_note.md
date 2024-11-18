### 2.0

- NextJS는 프레임워크이다.

- NextJS는 실행시 app 폴더와 page.tsx 파일을 참조하지만, 동시에 layout.tsx 파일도 확인한다. (layout.tsx 파일이 없으면 자동으로 생성된다)

<br/>

### 2.1

- NextJS는 파일 시스템을 통해서 url을 표현한다.

- `root segment`: `app` 폴더의 가장 바깥쪽 영역으로 NextJS가 가장 먼저 참고하는 페이지가 있는 영역

- 폴더명이 잠재적으로 하나의 페이지가 될 수 있다.

  - `/about-us` url을 가진 페이지를 생성하려면..  
    `app` 폴더 내에 `about-us` 폴더를 만든 후, 그 안에 `page.tsx` 파일 생성해 UI 코드를 넣으면 된다.

- 폴더는 그저 경로일 뿐, 그 안에 `page.tsx` 파일이 있어야 해당 경로에 실제로 화면을 보여준다.

- 폴더를 중첩하면 중첩 라우팅이 가능하다.

  - `about-us/company/sales` 경로로 화면을 볼려면, `about-us/company/sales/page.tsx` 파일을 만들어 UI 코드를 넣어주면 된다.

<br/>
