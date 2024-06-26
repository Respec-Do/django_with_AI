<h1>🚩 Onelab AI Project</h1>

---

<h3>✨ AI 프로젝트 소개</h3>

- 게시글 내용 추천 시스템

  > 이번 AI 프로젝트에서 제가 구현한 기능은 게시글 내용을 추천해주는 시스템입니다.

<h3>✨ 목차</h3>

- 기획배경 및 기대효과
- 화면
- 데이터 수집(Data Crowling)
- Cosine_Similarity 이용하여 유사도 분석
- Django로 구현
- 서버 배포 및 화면 시연
- Trouble-Shooting
- 느낀점
- 개선 사항

---

<h3>✨기획배경 및 기대효과</h3>

<h4>👉기획배경</h4>

1. 콘텐츠 창작의 어려움
   - 블로그, 소셜 미디어, 온라인 커뮤니티 등에서 콘텐츠를 작성하고 싶어하는 많은 사람들은 종종 주제나 방향을 잡는 데 어려움을 겪습니다.
   - 글의 구조나 내용에 대한 명확한 아이디어가 부족해 시작조차 어려운 상황을 해결할 필요가 있습니다.
   - 다양한 아이디어와 창의적인 방향을 제시함으로써, 사용자의 창의력을 자극하고 더 풍부하고 다양한 콘텐츠를 작성할 수 있도록 돕습니다.
1. 시간과 노력 절감
   - 콘텐츠 작성에는 많은 시간이 소요될 수 있습니다.
   - 제목과 범주를 기반으로 한 추천 서비스는 사용자가 글을 작성하는 시간을 크게 절감시키고, 더 효율적으로 작업할 수 있도록 도와줍니다.

<h4>👉기대효과</h4>

1. 콘텐츠 품질 향상
   - 추천된 아이디어와 구조를 기반으로 사용자는 더 높은 품질의 글을 작성할 수 있습니다.
   - 이는 전체적인 콘텐츠의 수준을 향상 시키며, 사용자들에게 더 유익하고 흥미로운 정보를 제공할 수 있습니다.
1. 콘텐츠 작성의 용이성 증대
   - 콘텐츠 작성 난이도의 허들을 낮춤으로써, 주기적인 콘텐츠 생성에 긍정적인 영향을 미칠 뿐만 아니라 더욱 양질의 내용을 추천하는 플랫폼을 기대할 수 있습니다.
1. 사용자의 편의성 및 만족도 향상
   - 직관적이고 사용하기 쉬운 인터페이스와 자동화된 추천 시스템으로 번거로운 과정없이 간편하게 콘텐츠를 생성할 수 있어 사용자의 만족도 향상을 기대할 수 있습니다.

---
  
<h3>✨ 화면</h3>

- 제목과 게시글의 유형으로 내용을 자동으로 추천해주는 시스템을 구현했습니다.
- <details><summary> AI 적용할 화면 확인</summary>
    <br>
    <img width="960" alt="슬라이드0001" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/ec8ebefc-c21b-44a0-9f9b-2c6922763cf9">  
  </details>

---

<h3>✨ 데이터 수집(Data Crowling)</h3>

- <details><summary> 수집해야할 데이터 종류</summary>
    <br>
    <img width="400" alt="community_category" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/4dfdacfc-1585-4743-b101-d77f632e8cb0">  
  </details>
- BeautifulSoup을 이용하여 데이터를 수집했습니다.
- 게시글의 유형별로 데이터를 수집하기 위해 다음 사이트를 참고하여 수집했습니다.
- 데이터를 수집하기 위한 코드는 Jupyter Notebook 환경에서 진행하였습니다.

<h4>✨ 자료 요청</h4>

- 위에 해당하는 내용은 데이터를 직접 작성하여 csv파일로 만들었습니다.
- <details><summary> 코드 확인</summary>
    <br>
    <img width="960" alt="file_request_code" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/fe05e43a-e561-4b10-aa6c-f0a8206cd59d">
    <img width="960" alt="file_request_code2" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/eeec7bb2-42d1-46e9-9ff7-6e8f80a47dc6">
  </details>

<h4>✨ 질문</h4>

- https://www.a-ha.io/
- <details><summary> a-ha 페이지</summary>
    <br>
    <img width="960" alt="a-ha_page" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/c05a3592-1146-4d5a-82ac-e2bdf07d114b">
  </details>
- <details><summary> 코드 확인</summary>
    <br>
    <img width="960" alt="question_code2" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/d06dfcf2-1f7c-4d4a-9c93-692dfbc2ee17">
    <img width="960" alt="question_code1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/6b042a46-ea8a-4405-896a-216f16772bd3">
  </details>

<h4>✨ 기타</h4>

- https://news.naver.com/
- <details><summary> 네이버 뉴스 페이지</summary>
    <br>
    <img width="960" alt="naver_news" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/59c852c9-e175-4d6a-a128-e635b451c5be">
  </details>
- <details><summary> 코드 확인</summary>
    <br>
    <img width="960" alt="etc_code" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/a851a9d2-2a6e-4f95-a26c-ff5bf4b9338d">
    <img width="960" alt="etc_code1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/d8f4a62e-6c78-434e-831f-de5b424c9c66">
    <img width="960" alt="etc_code2" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/e13469d3-26bf-42d8-ad5a-c3c481c4e7cf">
  </details>

---

<h3>✨ Cosine_Similarity 이용하여 유사도 분석</h3>

- Jupyter Notebook에서 앞서 만든 데이터에서 제목과 내용, 그리고 글의 범주를 이용하여 유사도 분석을 진행했습니다.
- 제목, 내용 그리고 범주를 우선 하나의 긴 문자열로 연결했습니다.
- 긴 문자열로 만들어진 새로운 데이터프레임을 만들고 그 데이터프레임을 CountVectorizer에 fit_transform하여 벡터화를 해주었습니다.
- 벡터화 된 metrix를 Sklearn의 Cosine_Similarity에 넣고 유사도를 나타내었습니다.
- 이때 나타난 유사도는 metrix형태이기에 list로 바꾼 다음 유사도가 높은 순서대로 다시 바꿔주었습니다.
- enumerate를 이용하여 key값을 인덱스로 나타나게 하였습니다.
- 이 인덱스를 토대로 get_title_from_index라는 함수를 만들어 제목을 가져오게 했습니다.
- <details><summary> 코드 확인</summary>
  
    <br>
    
    - 먼저 만든 3개의 데이터를 하나로 합치고 제목과 내용과 범주를 가져왔습니다.
    
    <br>
    <img width="960" alt="cs1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/37969b69-b471-4e5a-ab35-269f2445e34a">
    <br>
    
    - 합쳐진 데이터가 한 줄로 나타나는 것을 확인했습니다.
    
    <br>
    <img width="960" alt="cs2" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/116e546e-297a-406a-a1f6-2913c93b4cf5">
    <br>
    
    - Sklearn의 CountVectorizer와 Cosine_Similarity를 이용하여 CountVector로 만들어준 다음,<br>
      Cosine_Similarity에 넣어서 확인해 주었습니다.
    - 유사도 결과가 잘 나타나는 것을 확인하였습니다.
    
    <br>
    <img width="960" alt="cs3" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/bd5b9d5d-a4ac-48ea-88d0-915265262b01">
    <br>
    
    - 인덱스로 제목을 가져오는 함수와 제목으로 인덱스를 가져오는 함수를 만들어 각각 확인해 주었습니다.
    - 이 때, 네이버 뉴스에서 수집한 데이터 중 하나를 확인하여 제목과 인덱스 번호를 확인하였고,<br>
      그 제목과 유사한 내용을 가져오는 지 확인했습니다.
    
    <br>
    <img width="960" alt="cs4" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/67b25334-c58c-4e75-902d-000cbc2aee1c">
    <br>
    
    - 유사한 제목을 가져오는 것을 확인할 수 있었습니다.
    - 위의 로직을 이용하여 Django에 넣어 주었습니다.
  </details>

---

<h3>✨ Django로 구현</h3>

- 제목과 범주만 입력한 다음 자동완성 버튼을 누르면 데이터 베이스 내의 모든 커뮤니티 게시글을 확인하고<br>
  유사도 검사를 진행한 다음, 가장 유사도가 높은 제목의 내용을 화면상으로 나타내는 것이 목표입니다.
- 위 목표를 위해 수정할 파일들은 다음과 같습니다.
  
1. HTML, CSS
1. JS
1. View


<h4>✨ HTML, CSS</h4>

- 화면상에서 자동완성 버튼을 눌렀을 때, View를 통해 가장 유사도가 높은 3개의 내용을 추천하는 Div 태그를 새로 만들었습니다.
- 비동기 방식으로 내용을 불러오는 동안 Loading 하는 이미지도 포함하였습니다.
- 내용을 수정하지 않으면 저장하기 버튼을 비활성화해서 내용을 수정하게끔 했습니다.
- CSS 파일은 따로 표기하지 않았습니다.
- <details><summary> 화면 확인</summary>
    <br>
    <img width="600" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/cf5feeb7-f4a6-4b2a-9e25-383797c16b8b">
    <br>
  
    - 표기한 부분에 제목을 입력하고 해당되는 범주를 고른 다음 오른쪽의 ai 자동추천 버튼을 누릅니다.

    <br>
    <img width="600" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/fee5aefc-a1ec-41e2-b9b2-d60aecb6e4ac">
    <br>
    
    - 유사도가 가장 높은 내용 중 상위 3개의 내용을 표현합니다.
    - 이 중 하나를 선택합니다.

    <br>
    <img width="600" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/e34ec4ae-a084-4ef7-a8c3-539ed7d0c2b2">
    <br>
    
    - 선택한 내용이 게시글 작성 부분으로 들어갑니다.
    - 이 때, 내용을 수정하지 않으면 저장되지 않도록 저장버튼을 비활성화합니다.
  </details>
- <details><summary> 코드 확인</summary>
    <br>
    <img width="600" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/49600bc6-da17-489b-b752-7ec9cfef8474">
    <img width="600" alt="html2" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/35a37548-b074-4dd0-adac-999c431227df">
  </details>

<h4>✨ JS</h4>

- 내용 추천 버튼을 눌렀을 때 view로 보내기 위해 비동기 방식을 이용하여 JavaScript를 구성했습니다. 

  > 상세 설명은 주석을 통해 확인하실 수 있습니다.

- <details><summary> 코드 확인</summary>
    <br>
    <img width="800" alt="jscode11" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/3b14cfb1-e4bc-42bc-9716-720d2e7962be">
    <img width="800" alt="jscode12" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/985a9fb4-96a2-4eb9-8839-d9e99682b4a9">
    <img width="800" alt="jscode13" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/9ae6dd37-23b8-41f9-b43c-c202a60eabcf">
  </details>


<h4>✨ Django</h4>

- JavaScript로 비동기통신 방식을 이용하기 위해 view 와 url을 작성하였습니다.
- 앞선 JupyterNotebook으로 작성한 코드를 View에 모듈화하였습니다.

**✨상세 설명**

- AIView
  - Post 방식으로 json 형태로 통신된 데이터를 data에 담아줍니다.
  - 제목과 범주를 title과 radio_active 라는 변수에 할당합니다.
  - radio_active는 수치형이기에 translate_status 함수를 통해 범주이름으로 변경합니다.
  - 제목과 범주를 하나의 문자열로 만들어주고 get_similar_communities 함수를 호출합니다.
  - <details><summary> 코드 보기</summary>
      <br>
      <img width="800" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/f341703e-905a-450c-9c10-416fa3a28638">
    </details>

    
- get_similar_communities
  - community.objects.all을 통해 커뮤니티의 모든 내용을 가져옵니다.
  - 가져온 community를 make_dataframe 함수를 통해 df라는 데이터프레임으로 만들어줍니다.
  - Sklearn의 CountVectorizer()를 호출합니다.
  - df 데이터프레임에 make_dataframe 함수를 통해 미리 만들어진 combined_features 를<br>
    CountVectorizer에 담아 Count_Matrix로 만들어줍니다.
  - 앞서만든 하나의 문자열 (제목과 범주) 또한 CountVectorizer에 담아 title_vector_matrix로 만들어줍니다.
  - Sklearn의 Cosine_Similarity를 호출하여 데이터프레임으로 만들어진 Count_Matrix와 title_vector_matrix간의 유사도를 구합니다.
  - 구해진 유사도를 enumerate를 통해 index를 나타나게 하고, list에 담아 similar_community라는 변수에 할당합니다.
  - 할당된 similar_community를 다시 유사도가 높은 순서로 정렬하여 similar_community_sorted라는 변수에 할당합니다.
  - 유사도가 가장 높은 3개를 추출합니다.
  - 이때, 기존의 데이터프레임에 유사도가 가장 높은 상위 3개의 인덱스를 참조하여 similar_content라는 리스트에 append하여 return 해줍니다.
  - <details><summary> 코드 보기</summary>
      <br>
      <img width="800" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/8a40cacb-6fc9-498a-b436-e901c9ddd475">
    </details>


- AIView
  - 다시 AIView로 돌아와서 get_similar_communities 함수로 return 된 similar_content를 similar_communities라는 변수에 할당해줍니다.
  - JsonResponse를 통해 similar_communities를 return하고 비동기통신을 종료합니다.
  - <details><summary> 코드 보기</summary>
      <br>
      <img width="800" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/009b8d77-f6ec-4f35-94e1-0b10ed6dcc9f">
    </details>

- make_dataframe
  - 불러온 community의 데이터 중 제목과 내용 그리고 범주를 list로 묶은 다음 데이터프레임으로 만듭니다.
  - post_status가 수치형이기 때문에 translate_status 함수로 문자로 변환해줍니다.
  - combined_features 라는 새로운 feature로 concatenate 라는 함수를 통해 하나의 문자열로 만들어줍니다.
  - 그 데이터프레임을 return으로 반환합니다.
  - <details><summary> 코드 보기</summary>
      <br>
      <img width="800" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/b8d2379d-2572-4247-bc75-cd53fcfaebe9">
    </details>

- translate_status & concatenate
  - 수치형인 범주값을 문자로 변환해주는 함수와 하나의 문자열로 만들어주는 함수입니다.
  - <details><summary> 코드 보기</summary>
      <br>
      <img width="800" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/233658ce-adeb-4059-8b2e-55c526552835">
    </details>

---

<h3>✨ 서버 배포 및 화면 시연</h3>

- 로컬에서 구현한 기능이 정상적으로 작동이 되는 것을 확인하고 이를 ubuntu를 이용하여 서버에 배포하였습니다.

---

<h1>✨ Trouble-Shooting ✨</h1>

<h2>👉 JavaScript와 View 간의 비동기 통신에서 생긴 Trouble</h2>

1. await fetch() 를 이용하여 url을 통해 view로 넘어갈 때 url을 찾지 못하는 Not Found 에러
1. CSRF-Token을 찾지 못하여 Not Certificated Token 에러
1. View로 넘어왔지만 같이 넘어온 데이터가 None 인 에러
1. Django에서 비동기 방식으로 데이터를 불러오는 중 발생한 문제

   > 아래에서 하나씩 상세히 설명하겠습니다.

<br>
<h3>✨해결 과정</h3>

<h3>1. await fetch() 를 이용하여 url을 통해 view로 넘어갈 때 url을 찾지 못하는 Not Found 에러</h3>

- 문제 : url 경로를 설정했음에도 불구하고 Not Found 에러가 발생했습니다.
- 시도 : 경로를 다시 추적하니, Main url 파일에 새롭게 만든 ai urls를 추가하지 않아 찾지 못하는 것을 파악하고 추가하였습니다.
- 해결 : 정상적으로 url 경로를 찾는 것을 확인하였습니다.

<h3>2. CSRF-Token을 찾지 못하여 Not Certificated Token 에러</h3>

- 문제 : url 경로를 통해 View로 넘어가는 것을 확인하려 했으나 개발자 도구에서 Token과 관련된 에러가 나타났습니다.
- 문제 파악 : HTML 상 form 태그 안에 CSRF-Token이 있었으나, 비동기 통신 방식으로 통신을 시도할 때 CSRF-Token이 포함되지 않음을 확인했습니다.
- 시도 : Javascript에서 CSRF-Token을 가져오는 함수를 만들고 함수를 통해 csrftoken 이라는 변수에 할당하여 headers에 담아주었습니다.
- 해결 : 더이상 개발자 도구에서 Token과 관련된 에러가 나타나지 않음을 확인하고 정상적으로 CSRF-Token이 같이 전송되는 것을 알 수 있었습니다.
- <details><summary> 코드 보기</summary>
    <br>
    <img width="800" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/c1fdb71c-52c4-4b26-b5c7-64e23991511f">
    <img width="800" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/e27b21e2-2a27-4a1f-88a2-3c9686b99ae8">
  </details>

<h3>3. View로 넘어왔지만 같이 넘어온 데이터가 None 인 에러</h3>

- 문제 : View를 통해 받아온 데이터가 None으로 나타났습니다.
- 문제 파악 : 
  - print()를 통해 하나씩 확인한 결과, Javascript에서 비동기 통신으로 받아온 데이터가 None으로 나타남을 알게 되었습니다.
  - 다시 Javascript로 넘어가서 문제를 확인했을 때, 데이터를 <code>body: JSON.stringify</code>의 형태로 담아서 전달했는데<br>
    View에서는 request.post로 데이터를 받아오고 있던 것이었습니다.
- 시도 : View에서 <code>data =  json.loads(requests.body)</code>로 바꿔주었습니다.
- 해결 : 정상적으로 데이터가 넘어오는 것을 확인할 수 있었습니다.

<h3>4. Django에서 비동기 방식으로 데이터를 불러오는 중 발생한 문제</h3>

- 문제 : 수정 작업이 된 화면을 검토하는 과정에서 비동기 방식으로 데이터를 불러올 때 화면이 비어있는 상태로 남아있는 문제가 발생했습니다.
- 문제 파악 : 이는 사용자 입장에서 버튼을 눌렀을 때 로딩 중인 것인지 혹은 에러가 발생해서 멈춘 것인지 확인할 방법이 없다는 것을 깨달았습니다.
- 시도 : 로딩을 의미하는 GIF 그림을 화면 상에 표기하는 로직을 추가하였습니다.
- 해결 : 위 로직을 추가하여 사용자 환경을 개선하였습니다.
- <details><summary> 추가한 그림 보기</summary>
    <br>
    <img width="150" alt="html1" src="https://github.com/Respec-Do/django_with_AI/assets/105579519/f070e52f-837e-4361-be71-e3a25359c2d7">
  </details>


<h2>👉 서버 배포에서 생긴 Trouble</h2>

<h3>✨해결 과정</h3>

<h3>1. 서버에서 collectstatic 진행 중 서버가 멈추는 현상이 발생했습니다.</h3>

  - 시도 : AWS에서 서버 재시작 후 'collectstatic' 다시 시도했으나, 서버가 여전히 멈췄습니다.
  - 해결책 : Pycharm terminal에서 'collectstatic' 실행 후 GIT에 push하고 원격에서 pull을 진행했습니다.

<h3>2. Merge 과정에서 충돌이 발생했습니다.</h3>

  - 문제 : pull 진행 시 병합 충돌이 발생했습니다.
  - 시도 : 'cd'와 'vim'으로 충돌 파일 수정하고, 다시 pull 진행했으나 여전히 충돌이 발생했습니다.
  - 해결책 : 충돌 파일을 삭제 후 pull을 진행했습니다.
    
<h3>3. Rebase 문제 해결</h3>

  - 문제 : 충돌 파일을 삭제 후 pull을 진행했으나 fatal-merge 에러가 발생했습니다.
  - 검색 : GIT에서는 현재 merge를 진행중인 공간을 rebase라고 명명하는 것을 알게 되었습니다. 따라서 rebase를 삭제하고 다시 진행하기로 했습니다.
  - 해결책 : <code>'rm -fr .git/rebase-merge</code> 명령어로 rebase 삭제 후 pull을 진행했습니다.
    
<h3>4. 삭제한 파일에서 문제 발견</h3>

  - 문제 : rebase 삭제 후 pull을 진행했을 때 삭제한 파일이 pull 되지 않는 것을 알게 되었습니다.
  - 검색 : GIT에는 로컬 브랜치와 원격 브랜치를 강제로 동기화하는 방법을 찾았습니다.
  - 해결책 : <code>git fetch origin</code> <code>git reset --hard origin/master</code> 로 강제 동기화를 진행후 pull을 진행했습니다.
    
<h3>5. CSS 파일 문제</h3>

  - 문제 : CSS 파일이 적용이 안되었음을 확인했습니다. <code>display : 'none'</code>로 설정된 div가 화면상으로 표시가 되고 있었습니다.
  - 해결책 : 수정된 CSS 파일을 삭제하고 'collectstatic'을 다시 실행후 gunicorn과 nginx를 재시작해주어 해결하였습니다.
    
<h3>6. 최종 결과</h3>

  - 성공 : 모든 기능이 정상 작동하고, JS 파일과 CSS 파일이 올바르게 반영되는 것을 확인하였습니다.

---

<h3>✨ 느낀 점</h3>

- 이번 프로젝트를 통해 Django와 AI를 결합한 웹 애플리케이션을 개발하는 귀중한 경험을 할 수 있었습니다.
- 데이터 수집부터 유사도 분석, 그리고 실제 서버 배포까지 전 과정을 직접 경험하며, 다양한 시행착오를 겪으면서 많은 것을 배웠습니다.
- Cosine Similarity를 이용한 유사도 분석을 통해 사용자가 원하는 내용을 자동으로 추천하는 기능을 성공적으로 구현할 수 있었습니다.
- 특히 Trouble-Shooting 과정에서 여러 에러들을 하나씩 확인하고 수정하면서, 문제 해결 능력과 디버깅 역량을 크게 향상시켰습니다.
- 또한, 비동기 통신을 활용하여 사용자 경험을 향상시키는 방법을 익히고, 비동기 통신의 중요성과 이를 효과적으로 구현하는 방법에 대한 깊은 이해를 얻을 수 있었습니다.

<h3>✨ 개선 사항</h3>

- 이번 AI 프로젝트를 통해 많은 것을 배웠지만, 더 나은 시스템을 만들기 위해서 몇가지 개선 사항이 필요하다고 생각했습니다.
- 아래는 제가 생각한 몇 가지 사항들입니다.

<h4>1. 다양한 데이터 수집</h4>

- 현재 데이터를 한정된 사이트에서 수집을 하게 되어, 유사도 분석 및 추천 시스템의 정확도가 특정 단어에 대해서만 높게 나타납니다.
- 따라서 다양한 커뮤니티 및 기타 사이트 등에서 데이터를 가져와서 더 풍부한 데이터 셋을 구성하게 된다면 정확도를 더욱 높이고,<br>
  사용자로 하여금 더 도움이 되는 내용을 추천해 줄 수 있을 것으로 예상합니다.

<h4>2. 추천 시스템의 성능 향상</h4>

- 현재 Cosine Similarity를 이용한 유사도 검사를 사용하고 있습니다.
- 하지만 추가적으로 탐색한 결과, 자연어 처리 기법을 도입하게 된다면 더 정교한 추천을 제공할 수 있을 것으로 기대할 수 있습니다.

<h4>3. 사용자 피드백 시스템 도입</h4>

- 추천된 게시글 내용에 대해 사용자가 피드백을 제공할 수 있는 시스템을 도입하면, 추천 시스템을 개선할 수 있습니다.
- 사용자의 피드백을 가중치로 두어 유사도 검사를 진행한다면, 사용자 만족도를 높일 수 있을 것으로 예상합니다.
