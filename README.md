# 기능 구현 목록(과제 조건 기준 정리)
## 개발 환경 및 조건
- [X] HTML/CSS/Javascript(프레임워크/라이브러리가 적용되지 않은 순수 자바스크립트) 사용
- [X] 반드시 ES6 문법 사용 (Chrome 최신버전에서 테스트 예정으로 transpiler 필요 없음)
- [X] 1280*720(px) 화면 구성 (해당 사이즈를 벗어나지 않도록 유의)

## 기본 구조
```
todolist calendar
├─ .vscode
│  └─ settings.json
├─ css
│  └─ style.css
├─ edittodo.html
├─ index.html
├─ newtodo.html
├─ README.md
└─ readtodo.html

```
- [X] 프로젝트 루트에 index.html 파일 생성
- [X] 프로젝트 루트에 README.md 파일 생성(folder structure 작성 필수)
- [X] 그 외 자유롭게 구성

## 기본 기능
- [X] 현재 월부터 3개월간 캘린더 화면 구성
  - [X] 10월
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/3eaec7c8-2a4d-4658-8c7f-020ff662fae0)
  - [X] 11월
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/f9215fe2-cfea-4361-b4f5-7cc6cb8a3b48)
  - [X] 12월
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/83cd068e-a97b-46a6-8e69-f563359cf53f)



- [X] 첫 페이지에는 현재 월에 대한 캘린더만 구성하며, 상/하 또는 좌/우 버튼을 추가하여 버튼 클릭 시 이전/다음달 캘린더 화면 노출
- ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/5e1577ec-6b89-4d9e-beb0-4b9d44582eb1)
- [X] 특정 날짜를 클릭 시 특정 시간에 할 일 등록/수정/삭제 기능.
  - [X] 등록
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/02863b4a-7e08-4ba3-b31c-c8147f0a5584)
  - [X] 수정
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/928f4277-2ada-4dfb-b95c-aa35479b31d2)
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/7bcef6a5-4ef7-4e1e-b61c-90e7e95a4db5)
  - [X] 삭제
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/e0e9a6a2-27ad-47e6-a042-d88ecb2d137e)
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/23151115-125d-426f-9e1b-6222650a84bc)
  - ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/6d8a6603-3767-4c00-9c05-1da9fc3542ed)


- [X] 할 일은 타이틀, 날짜/시간, 설명으로 구성
- ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/a3ebfb25-2e22-4303-928d-63c7bb51143b)
- [X] 할 일을 등록하면 캘린더 해당 날짜에 표시 되어야 함.
- ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/d3e13e09-5dab-4123-b6b9-6c28219a2342)
- [X] 페이지 reload시 기존 등록한 할 일이 그대로 표시 되어야 함. (localStorage 활용)
- ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/3389a692-0ac6-4b48-b762-23151803384a)

추가 기능 (가산점)
- [X] 키보드 이벤트로 화면 이동/할 일 등록, 수정, 삭제 기능 수행 가능(초기 디폴트 포커스는 현재 날짜이며, 상하좌우 방향키로 포커스 이동/enter키로 클릭/backspace로 (팝업)닫기 등 수행)
- ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/4c72da6e-e994-4068-a721-aebd9767a307)  
- ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/9ba4a331-a07c-42b0-9856-8d06a53366fa)
- [X] 그 외 자유롭게 추가하고 싶은 기능 (단, 추가한 기능에 대해 README.md에 작성해야 함) : 3개월이 아닌 실제 달력 구현
- ![image](https://github.com/vHaYoungv/todolist-calendar/assets/134265313/73e0ace9-2c7a-41cd-966b-9f506a48eff9)


과제 제출
- [ ] 프로젝트 폴더를 압축하여 서비스개발_성명.zip 파일로 메일 제출(제출처 : lghvhr@lghv.net)
- [ ] 제출 소스는 index.html 파일을 크롬 브라우저 상에서 실행하여 결과를 확인하는 것이 가능해야 함.

<br>
<br>
<br>


# 기능 구현 목록(기능별로 정리)
## 기본 기능
### 캘린더 화면 구성
- [X] 년, 월 선택 
- [X] 선택한 년, 월에 맞는 달력 표시
- [X] <, > 버튼 누를 때 월 감소, 증가
- [X] 해당 일자에 To do 등록
- [X] 해당 일자에 To do가 있으면, 달력에 제목 표시
- [X] 표시된 To do를 누르면 상세 페이지로 이동 
- [X] 상세 페이지에서 수정을 누르면 localStorage에서 Todo 수정 
- [X] 상세 페이지에서 삭제를 누르면 localStorage에서 Todo 삭제

### To do 기능
- [X] 날짜 클릭 하면 할 일 등록 화면 불러오기
- [X] 할 일 등록 화면 구성
- [X] To do 객체 ex: {id: 1, date:'2023-11-01', time: 15, detail: '자바스크립트 공부하기'}
  - [X] 타이틀 : todo_title
  - [X] 날짜, 시간 : todo_date, todo_time
  - [X] 설명 : todo_detail
- [X] reload 시에도 데이터 유지 
  - [X] localStorage 활용
  

## 추가 기능
### 실제 달력 구현 (3개월이 아닌)
- [x] 윤년 계산
- [X] Year와 Month에 따른 첫 날짜의 요일 설정 
- [X] Month에 따른 끝 날짜 설정(28,29,30,31)
- [X] 그 외의 칸들은 공백으로 설정 
  

### 키보드 이벤트
  - [X] 초기 디폴트 포커스: 현재 날짜 설정
  - [X] 상하좌우 방향키로 포커스 이동
  - [X] enter키로 현재 포커스의 새 to do 생성
  - [X] backspace로 이전 페이지로 이동 

