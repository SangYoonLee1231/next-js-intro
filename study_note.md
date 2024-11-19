### 2.0 Introduction

- NextJS는 프레임워크이다.

- NextJS는 실행시 app 폴더와 page.tsx 파일을 참조하지만, 동시에 layout.tsx 파일도 확인한다. (layout.tsx 파일이 없으면 자동으로 생성된다)

<br/>

### 2.1 Defining Routes

- NextJS는 파일 시스템을 통해서 url을 표현한다.

- `root segment`: `app` 폴더의 가장 바깥쪽 영역으로 NextJS가 가장 먼저 참고하는 페이지가 있는 영역

- 폴더명이 잠재적으로 하나의 페이지가 될 수 있다.

  - `/about-us` url을 가진 페이지를 생성하려면..  
    `app` 폴더 내에 `about-us` 폴더를 만든 후, 그 안에 `page.tsx` 파일 생성해 UI 코드를 넣으면 된다.

- 폴더는 그저 경로일 뿐, 그 안에 `page.tsx` 파일이 있어야 해당 경로에 실제로 화면을 보여준다.

- 폴더를 중첩하면 중첩 라우팅이 가능하다.

  - `about-us/company/sales` 경로로 화면을 볼려면, `about-us/company/sales/page.tsx` 파일을 만들어 UI 코드를 넣어주면 된다.

<br/>

### 2.2 Not Found Routes

- not found 페이지

  - 잘못된 경로를 처리

- page, layout, not-found은 특별한 이름을 가진 파일

- Navigation Bar 만들기

- usePathname

  - usePathname은 client components에서만 작동

  - 파일 상단에 "use client"를 적어주면 사용 가능 (이유는 다음에 살펴봄)

<br/>

### 2.3 SSR vs CSR

- usePathname은 client components에서만 작동한다.

- next.js가 application을 render하는 방식

  - rendering: next.js가 우리의 react component를 가져와서 브라우저가 이해할 수 있는 html로 변환하는 작업을 말함

- CSR (Client Side Rendering)

  - 클라이언트에서 랜더링을 진행

  - 페이지 로딩 시 자바스크립트를 로드하는 시간이 필요

  - 빈 페이지에서 시작하므로 SEO에 불리

- SSR (Server Side Rendering)

  - 모든 page 안의 모든 component들은 우선 서버에서 렌더링 됨

  - 따라서 클라이언트에는 (서버로부터 받은) 이미 랜더링된 HTML 코드가 존재

- React - CSR | NextJS - SSR

- "use client"를 적어도, 해당 파일이 클라인트에서 랜더링 된다는 의미가 아니다.

<br/>
