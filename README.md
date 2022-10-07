# 러빗 Loveeat

> 요리 커뮤니티 겸 밀키트 쇼핑몰 웹 프로젝트

![loveeat_cover](https://user-images.githubusercontent.com/68595933/111944919-0a1dc380-8b1c-11eb-8d24-55fb487d2f99.PNG)

## 시작

- 커뮤니티 겸 쇼핑몰 웹 프로젝트입니다.
- 팀 프로젝트로, 전체 웹 사이트 중 서브 게시판1(레시피 후기)을 작업했습니다.
- [데모 사이트 바로가기][데모]

---

## 개발

### 기간

- 20.10.20. ~ 20.11.17.

### 목표

- JSP Model2로 주요 기능을 구현합니다.
- Spring(STS4)을 사용합니다.

### 사용

- HTML5/CSS3
- JavaScript ES6
- Java 8
- Spring(STS4)
- jQuery 3.5
- Bootstrap 3
- AJAX
- JSON
- MySQL 5.6
- Tomcat 8.5
- Cafe24

### 파트

+ 박은주(파트장1)
  - 웹디자인 총괄
  - 메인 페이지
  - 인증(관리자 계정)
  - 메인 게시판(CRUD)
  - 웹 호스팅
+ 김민성(파트장2)
  - 메인 페이지
  - 메인 게시판(필터링/검색창)
  - 서브 게시판2(자취생 노하우)
+ 문진우
  - 인증
  - 메인 게시판(필터링/검색창)
+ 박동찬
  - 인증
  - 스토어(주문하기/결제하기)
+ 박미란
  - 스토어(장바구니, 주문조회/고객정보)
+ 안효성
  - 서브 게시판4(공지/QNA)
+ 이신예
  - 서브 게시판1(레시피 후기)
+ 황예지
  - 서브 게시판3(스토어 후기)

---
## 기능

### 1. 메인 페이지

![main](https://user-images.githubusercontent.com/68595933/190130574-7aa6db24-a9d4-4110-a9c1-06eda8a4ec14.png)
![your_select](https://user-images.githubusercontent.com/68595933/190130211-3f338d38-3e84-4d32-b2d6-fa2dfd796e9f.png)
![modal](https://user-images.githubusercontent.com/68595933/190130414-28192588-3649-437b-9e0f-285d5874c3d2.png)

- 1.1. 필터링/검색창 
  - 헤더의 검색창은 '오늘 뭐 먹지?(메인 게시판)'의 해시태그 및 검색창과 연동됩니다.
  - YOUR SELECT는 '오늘은 뭘로 요리하지?(모달창)'를 불러옵니다.
  - 모달창에서 해시태그 선택을 완료하면 해당 재료가 들어가는 레시피만 필터링해 보여줍니다.

![contents](https://user-images.githubusercontent.com/68595933/190130867-4c2c9161-6853-4d23-bba7-7fab7fba2833.png)
![today's_recipe](https://user-images.githubusercontent.com/68595933/190131239-ae7fd551-f5cd-44c0-affe-681f86699a94.png)

- 1.2. 컨텐츠 영역
  - LOVE.EAT의 하위 이미지를 클릭하면 해당 페이지로 이동합니다.
  - TODAY'S RECIPE는 오늘뭐먹지 페이지에서 가장 조회수가 높은 게시글들을 출력합니다.

---

### 2. 인증

![login](https://user-images.githubusercontent.com/68595933/190131563-473f50de-e902-4a55-827d-efd444a5d763.png)
![encryption](https://user-images.githubusercontent.com/68595933/190131665-35fc41c4-e94f-4bab-9033-4d8c7f767b23.png)

- 2.1. 로그인/로그아웃
  - SNS 계정(네이버, 카카오, 구글)으로도 로그인/로그아웃 가능합니다.
  - 비밀번호를 암호화해 서버에 저장합니다.

![sign_up](https://user-images.githubusercontent.com/68595933/190132045-1aaacb29-1fe4-4945-9081-f69963bf5f53.png)
![withdrawal](https://user-images.githubusercontent.com/68595933/190132187-4126cbe0-eafc-43f5-8bb9-80d6f2da4278.png)

- 2.2. 회원가입/회원탈퇴
  - 회원가입 페이지에서 이메일 인증 후 가입합니다.
  - 회원탈퇴 페이지에서 비밀번호 입력 후 탈퇴합니다.

![forgot_id](https://user-images.githubusercontent.com/68595933/190135580-42293015-b4a0-467a-b7f5-cecfdd3a2a9d.png)
![forgot_pw](https://user-images.githubusercontent.com/68595933/190135998-f59abbdd-1713-4ef7-91c6-0a425fad0e7f.png)

- 2.3. 이메일 인증
  - 회원가입시 이메일 인증이 필요합니다.
  - 가입시 입력한 이메일 주소를 통해 기존 ID나 임시 비밀번호를 받을 수 있습니다.

![edit_nickname](https://user-images.githubusercontent.com/68595933/190136754-927a7767-dac5-45d8-9170-231b2d3b1d80.png)
![edit_password](https://user-images.githubusercontent.com/68595933/190136790-19e89d44-df32-4412-8f26-a9f4f428c41f.png)

- 2.4. 회원정보
  - 닉네임, 이메일, 비밀번호를 수정합니다.

![manage_board](https://user-images.githubusercontent.com/68595933/190137694-a27980b0-33e6-4a2a-86b9-2a6dffcc01a2.png)
![manage_member](https://user-images.githubusercontent.com/68595933/190137833-ce154730-d897-413c-8dd7-b524f0061cd8.png)
![manager_menu](https://user-images.githubusercontent.com/68595933/190137963-b2b6429c-4ed1-4401-97c6-31a0010ec4da.png)

- 2.5. 관리자 계정
  - 게시판 관리(읽기/검색/삭제) 가능합니다.
  - 회원 관리(읽기/검색/삭제) 가능합니다.
  - 배송 관리(배송상태 변경) 가능합니다.

---

### 3. 오늘뭐먹지(메인 게시판)

![search](https://user-images.githubusercontent.com/68595933/190153348-d5b04baf-6616-47d5-a131-145ec8c176ea.png)
![hashtag](https://user-images.githubusercontent.com/68595933/190153388-70656be5-5da0-48fb-80c3-ab82a5dfc387.png)

- 3.1. 필터링/검색창
  - (1)제목, (2)내용, (3)제목과 내용, (4)작성자로 검색합니다.
  - 검색창 하단에 사용률이 높은 해시태그들을 노출합니다.
  - 해시태그를 클릭하면 1.1과 마찬가지로 해당 재료가 들어가는 레시피(게시글)만 필터링해 보여줍니다.
  - 레시피는 한 페이지에 9개(3*3)씩 출력되며 페이징 버튼을 통해 다른 페이지로 이동합니다.

![recipe_view](https://user-images.githubusercontent.com/68595933/190154481-5a0dcac1-94b8-4b08-b041-6731af94a92c.png)
![recipe_write](https://user-images.githubusercontent.com/68595933/190154647-d14f3503-4422-4ba7-b3f8-c1199df1f4fb.png)

- 3.2. 게시판 CRUD
  - 레시피 등록/읽기/수정/삭제 가능합니다.
  - 내가 쓴 레시피만 수정/삭제 버튼을 보여줍니다.
  - 레시피에 썸네일 지정 및 이미지 첨부 가능합니다.

![comment](https://user-images.githubusercontent.com/68595933/190156574-b1177f35-113f-4191-8109-af52f74ceb08.png)

- 3.3. 댓글 CRUD
  - 댓글 등록/읽기/수정/삭제 가능합니다.
  - 내가 쓴 댓글만 수정/삭제 버튼을 보여줍니다.
  - 별점(0~5개) 부여 가능합니다. 단, 별점은 댓글 입력 후 따로 수정할 수 없습니다.

---

### 4. 레시피 후기(서브 게시판)

![recipe_review_main](https://user-images.githubusercontent.com/68595933/190326513-40faa999-bdeb-4bcd-ac3e-8d3e5cca1f7f.png)

- 4.1. 검색창
  - (1)제목, (2)내용, (3)제목과 내용, (4)작성자로 검색합니다.
  - 레시피 후기(게시글)는 한 페이지에 9개(3*3)씩 출력되며 페이징 버튼을 통해 다른 페이지로 이동합니다.

```java
// Recipe_reviewController.java

// 레시피_리뷰 목록
	@RequestMapping(value = "/list", method = RequestMethod.GET)
	public void getList(Recipe_reviewVO vo, Model model) throws Exception {
		List<Recipe_reviewVO> list = null;
		list = service.list();
		model.addAttribute("list", list);
		// 랜덤 썸네일 이미지 출력용 랜덤함수
		Random random = new Random();
		int randomNum = random.nextInt(4)+1;
		model.addAttribute("random", randomNum);
	}  

	// 레시피_리뷰 목록 + 페이징 + 검색
	@RequestMapping(value = "/listPageSearch", method = RequestMethod.GET)
	public void getListPageSearch (Model model,
			@RequestParam("num") int num,
			@RequestParam(value = "searchType", required = false, defaultValue = "r_r_subject") String searchType,
			@RequestParam(value = "keyword", required = false, defaultValue = "") String keyword) throws Exception {
		
		Recipe_reviewPage page = new Recipe_reviewPage();
		page.setNum(num);
		page.setCount(service.searchCount(searchType, keyword));
		page.setSearchType(searchType);
		page.setKeyword(keyword);
		
		List<Recipe_reviewVO> list = null;
		list = service.listPageSearch(page.getDisplayPost(), page.getPostNum(), searchType, keyword);
		
		model.addAttribute("list", list);
		model.addAttribute("page", page);
		model.addAttribute("select", num);
		
		// 랜덤 썸네일 이미지 출력용 랜덤함수
		Random random = new Random();
		int randomNum = random.nextInt(4)+1;
		model.addAttribute("random", randomNum);
	}
```
```java
// Recipe_reviewPage.java

  // 현재 페이지 번호
	private int num;

	// 레시피_리뷰 총 수
	private int count;

	// 한 페이지에 출력할 레시피_리뷰 수
	private final int postNum = 9;

	// 하단 페이징 번호 [레시피_리뷰 총합 ÷ 한 페이지에 출력할 개수]의 올림
	private int pageNum;

	// 출력할 레시피_리뷰
	private int displayPost;

	// 한번에 표시할 페이징 번호 개수
	private final int pageNumCnt = 10;

	// 표시되는 페이지 번호 중 마지막 번호
	private int endPageNum;

	// 표시되는 페이지 번호 중 첫번째 번호
	private int startPageNum;

	// 페이지 넘기기(이전/다음) 표시 여부
	private boolean prev;
	private boolean next;
	
	public void setNum(int num) {
		this.num = num;
	}

	public void setCount(int count) {
		this.count = count;
	  dataCalc();
	}
  
	public int getCount() {
		return count;
	}

	public int getPostNum() {
		return postNum;
	}

	public int getPageNum() {
		return pageNum;
	}

	public int getDisplayPost() {
		return displayPost;
	}

	public int getPageNumCnt() {
		return pageNumCnt;
	}

	public int getEndPageNum() {
		return endPageNum;
	}

	public int getStartPageNum() {
		return startPageNum;
	}

	public boolean getPrev() {
		return prev;
	} 

	public boolean getNext() {
		return next;
	}
	
	private void dataCalc() {
		 
		// 마지막 번호
		endPageNum = (int)(Math.ceil((double)num / (double)pageNumCnt) * pageNumCnt);
		 
		// 시작 번호
		startPageNum = endPageNum - (pageNumCnt - 1);
		 
		// 마지막 번호 재계산
		int endPageNum_tmp = (int)(Math.ceil((double)count / (double)pageNumCnt));
		 
		if (endPageNum > endPageNum_tmp) {
			endPageNum = endPageNum_tmp;
		}
		 
		prev = startPageNum != 1;
		next = endPageNum * pageNumCnt < count;
		 
		displayPost = (num - 1) * postNum;
    
	}

	public String getSearchTypeKeyword() {
		 
		if(searchType.equals("") || keyword.equals("")) {
			return ""; 
		} else {
			return "&searchType=" + searchType + "&keyword=" + keyword; 
		}
    
	}

	private String searchType;
	private String keyword; 

	public void setSearchType(String searchType) {
		this.searchType = searchType;  
	}

	public String getSearchType() {
		return searchType;
	} 

	public void setKeyword(String keyword) {
		this.keyword = keyword;  
	} 

	public String getKeyword() {
		return keyword;
	}
```
```java
// Recipe_reviewVO.java

	private int r_r_bno;
	private String r_r_id;
	private String r_r_nickname;
	private String r_r_subject;
	private String r_r_content;
	private String r_r_file;
	private String r_r_thumbnail;
	private Timestamp r_r_date;
	private int r_r_hit;
	
	public Recipe_reviewVO(int r_r_bno, String r_r_id, String r_r_nickname, String r_r_subject, String r_r_content,
			String r_r_file, String r_r_thumbnail, Timestamp r_r_date, int r_r_hit) {
		super();
		this.r_r_bno = r_r_bno;
		this.r_r_id = r_r_id;
		this.r_r_nickname = r_r_nickname;
		this.r_r_subject = r_r_subject;
		this.r_r_content = r_r_content;
		this.r_r_file = r_r_file;
		this.r_r_thumbnail = r_r_thumbnail;
		this.r_r_date = r_r_date;
		this.r_r_hit = r_r_hit;
	}

	public Recipe_reviewVO() {}
	
	public int getR_r_bno() {
		return r_r_bno;
	}

	public void setR_r_bno(int r_r_bno) {
		this.r_r_bno = r_r_bno;
	}

	public String getR_r_id() {
		return r_r_id;
	}

	public void setR_r_id(String r_r_id) {
		this.r_r_id = r_r_id;
	}

	public String getR_r_nickname() {
		return r_r_nickname;
	}

	public void setR_r_nickname(String r_r_nickname) {
		this.r_r_nickname = r_r_nickname;
	}

	public String getR_r_subject() {
		return r_r_subject;
	}

	public void setR_r_subject(String r_r_subject) {
		this.r_r_subject = r_r_subject;
	}

	public String getR_r_content() {
		return r_r_content;
	}

	public void setR_r_content(String r_r_content) {
		this.r_r_content = r_r_content;
	}

	public String getR_r_file() {
		return r_r_file;
	}

	public String setR_r_file(String r_r_file) {
		return this.r_r_file = r_r_file;
	}

	public String getR_r_thumbnail() {
		return r_r_thumbnail;
	}

	public String setR_r_thumbnail(String r_r_thumbnail) {
		return this.r_r_thumbnail = r_r_thumbnail;
	}

	public Timestamp getR_r_date() {
		return r_r_date;
	}

	public void setR_r_date(Timestamp r_r_date) {
		this.r_r_date = r_r_date;
	}

	public int getR_r_hit() {
		return r_r_hit;
	}

	public void setR_r_hit(int r_r_hit) {
		this.r_r_hit = r_r_hit;
	}
	
	@Override
	public String toString() {
		return "Recipe_reviewVO [r_r_bno=" + r_r_bno + ", r_r_id=" + r_r_id + ", r_r_nickname=" + r_r_nickname
				+ ", r_r_subject=" + r_r_subject + ", r_r_content=" + r_r_content + ", r_r_file=" + r_r_file
				+ ", r_r_thumbnail=" + r_r_thumbnail + ", r_r_hit=" + r_r_hit + "]";
	}
```
```java
// Recipe_reviewDAO.java

	// DB서버의 시간정보를 가져오기
    String getTime();
	
	// 레시피_리뷰 번호
    int cntBno(Recipe_reviewVO vo) throws Exception;
	
	// 레시피_리뷰 목록
    List<Recipe_reviewVO> list() throws Exception;
	
	// 레시피_리뷰 작성
    void write(Recipe_reviewVO vo) throws Exception;
	
	// 레시피_리뷰 조회
    Recipe_reviewVO view(int r_r_bno) throws Exception;
	
	// 레시피_리뷰 조회수
    void hit(int r_r_bno) throws Exception;
	
	// 레시피_리뷰 수정
    void modify(Recipe_reviewVO vo) throws Exception;
	
	// 레시피_리뷰 삭제
    void delete(int r_r_bno) throws Exception;
	
	// 레시피_리뷰 총 수
    int count() throws Exception;
	
	// 레시피_리뷰 목록 + 페이징 + 검색
    List<Recipe_reviewVO> listPageSearch(int displayPost, int postNum, String searchType, String keyword) throws Exception;
	
	// 레시피_리뷰 총 수 + 검색 적용
    int searchCount(String searchType, String keyword) throws Exception;
    
// Recipe_reviewDAOImpl.java

	// 시간정보추가
	@Override
	public String getTime() {
		System.out.println("DAO : DB접근 sqlSession객체를 주입!");
		System.out.println("DAO : TEST에서 해당메서드 호출!!! ");
		System.out.println("DAO : memberMapper.xml 이동");
		System.out.println("DAO : Select구문을 실행하는 메서드를 실행해서 SQL구문 실행");
		// "com.itwillbs.mapper.MemberMapper.getTime";
		String result = sql.selectOne(namespace + ".getTime");
		System.out.println("DAO : SQL 구문 실행완료! 값 리턴 후 테스트로 이동");
		return result;
	}
	
	// 레시피_리뷰 번호 
	@Override
	public int cntBno(Recipe_reviewVO vo) throws Exception {
		return sql.selectOne(namespace + ".cntBno", vo);
	}
	
	// 레시피_리뷰 목록
	@Override
	public List<Recipe_reviewVO> list() throws Exception {
		return sql.selectList(namespace + ".list");
	}
	
	// 레시피_리뷰 작성
	@Override
	public void write(Recipe_reviewVO vo) throws Exception {
		sql.insert(namespace + ".write", vo);
	}
	
	// 레시피_리뷰 조회
	@Override
	public Recipe_reviewVO view(int r_r_bno) throws Exception {
		return sql.selectOne(namespace + ".view", r_r_bno);
	}
	
	// 레시피_리뷰 수정
	@Override
	public void modify(Recipe_reviewVO vo) throws Exception {
		sql.update(namespace + ".modify", vo);
	}
	
	// 레시피_리뷰 조회수
	@Override
	public void hit(int r_r_bno) throws Exception {			
		sql.update(namespace + ".hit", r_r_bno);
	}
	
	// 레시피_리뷰 삭제
	public void delete(int r_r_bno) throws Exception {
		sql.delete(namespace + ".delete", r_r_bno);
	}
	
	// 레시피_리뷰 총 수
	@Override
	public int count() throws Exception {
		return sql.selectOne(namespace + ".count"); 
	}
	
	// 레시피_리뷰 목록 + 페이징 + 검색
	@Override
	public List<Recipe_reviewVO> listPageSearch(int displayPost, int postNum, String searchType, String keyword) throws Exception {
		HashMap<String, Object> data = new HashMap<String, Object>();
		data.put("displayPost", displayPost);
		data.put("postNum", postNum);
		data.put("searchType", searchType);
		data.put("keyword", keyword);
		return sql.selectList(namespace + ".listPageSearch", data);
	}
	
	// 레시피_리뷰 총 수 + 검색 적용
	@Override
	public int searchCount(String searchType, String keyword) throws Exception {
		HashMap data = new HashMap();
		data.put("searchType", searchType);
		data.put("keyword", keyword);
		return sql.selectOne(namespace + ".searchCount", data); 
	}
```

![recipe_review_thumbnail](https://user-images.githubusercontent.com/68595933/190326564-9f707112-dc27-44a6-b487-8840a6b64fcd.png)
![recipe_review_view](https://user-images.githubusercontent.com/68595933/190326405-c321a692-2718-4167-ba36-77050db2a052.png)
![recipe_review_write](https://user-images.githubusercontent.com/68595933/190139479-b737df28-d225-45ae-b765-99eb5619add3.png)

- 4.2. 게시판 CRUD
  - 후기 등록/읽기/수정/삭제 가능합니다.
  - 내가 쓴 후기만 수정/삭제 버튼을 보여줍니다.
  - 리뷰에 썸네일 지정 및 이미지 첨부 가능합니다.
  
```java
// Recipe_reviewController.java
  
  // 레시피_리뷰 작성
	@RequestMapping(value = "/write", method = RequestMethod.GET)
	public String getWrite(Recipe_reviewVO vo, HttpSession session, RedirectAttributes rttr, Model model) throws Exception {
		// 로그인 한 아이디만 글 쓸 수 있도록 처리 
		String id = (String)session.getAttribute("id");
		UserVO user = null;
		user = userService.readMember(id);
		model.addAttribute("user", user);
		return "/Recipe_review/write";
	}
	@RequestMapping(value = "/write", method = RequestMethod.POST)
	public String postWrite(Recipe_reviewVO vo, RedirectAttributes rttr, HttpSession session) throws Exception {
		String pathImg=vo.getR_r_content();
		if(pathImg.indexOf("src=")!=-1) { // content영역에  "src=" 가 포함되어 있을 경우
			String[] result = pathImg.split("upload/");
			String resultTwo = result[1];
			String[] resultTwoPath = resultTwo.split("\" title");
			// 여기에서 r_content 안의 img를 split이나 substring으로 꺼내서
			// vo.setR_file(r_file) 안에 넣어주면 vo에 들어감. 
			vo.setR_r_file(resultTwoPath[0]);
			// 썸네일은 thumbnail.파일명 으로 저장되게 해뒀으므로
			String thumbName = "thumbnail."+resultTwoPath[0];
			vo.setR_r_thumbnail(thumbName);
		} else {// 컨텐츠에 이미지가 없을 경우 미리 지정해 둔 이미지를 썸네일로 사용
			String defaultImg = "defaultImg.jpg";
			vo.setR_r_file(defaultImg);
			vo.setR_r_thumbnail(defaultImg);
		}
		service.write(vo);
		rttr.addFlashAttribute("msg","성공");
		return "redirect:/Recipe_review/listPageSearch?num=1";
	}
	
	// 레시피_리뷰 조회
	@RequestMapping(value = "/view", method = RequestMethod.GET)
	public void getView(@RequestParam("r_r_bno") int r_r_bno, Model model) throws Exception {
		Recipe_reviewVO vo = service.view(r_r_bno);
		model.addAttribute("view", vo);
	}
	
	// 레시피_리뷰 수정
	@RequestMapping(value = "/modify", method = RequestMethod.GET)
	public String getModify(@RequestParam("r_r_bno") int r_r_bno, Model model) throws Exception {
		Recipe_reviewVO vo = service.view(r_r_bno);
		model.addAttribute("view", vo);
		return "/Recipe_review/modify";
	}
	@RequestMapping(value = "/modify", method = RequestMethod.POST)
	public String postModify(Recipe_reviewVO vo) throws Exception {
		String pathImg=vo.getR_r_content();
		if(pathImg.indexOf("src=")!=-1) { // content영역에  "src=" 가 포함되어 있을 경우
			String[] result = pathImg.split("upload/");
			String resultTwo = result[1];
			String[] resultTwoPath = resultTwo.split("\" title");
			// 여기에서 r_content 안의 img를 split이나 substring으로 꺼내서
			// vo.setR_file(r_file) 안에 넣어주면 vo에 들어감. 
			vo.setR_r_file(resultTwoPath[0]);
			// 썸네일은 thumbnail.파일명 으로 저장되게 해뒀으므로
			String thumbName = "thumbnail."+resultTwoPath[0];
			vo.setR_r_thumbnail(thumbName);
		} else {// 컨텐츠에 이미지가 없을 경우 미리 지정해 둔 이미지를 썸네일로 사용
			String defaultImg = "defaultImg.jpg";
			vo.setR_r_file(defaultImg);
			vo.setR_r_thumbnail(defaultImg);
		}
		service.modify(vo);
		return "redirect:/Recipe_review/view?r_r_bno=" + vo.getR_r_bno();
	}
	
	// 레시피_리뷰 삭제
	@RequestMapping(value = "/delete", method = RequestMethod.GET)
	public String getDelete(@RequestParam("r_r_bno") int r_r_bno) throws Exception {
		service.delete(r_r_bno);  
		return "redirect:/Recipe_review/listPageSearch?num=1";
	}
```
```java
// Recipe_reviewService.java

	// 레시피_리뷰 번호
    int cntBno(Recipe_reviewVO vo) throws Exception;
	
	// 레시피_리뷰 목록
    List<Recipe_reviewVO> list() throws Exception;
	
	// 레시피_리뷰 작성
    void write(Recipe_reviewVO vo) throws Exception;
	
	// 레시피_리뷰 조회
    Recipe_reviewVO view(int r_r_bno) throws Exception;
	
	// 레시피_리뷰 수정
    void modify(Recipe_reviewVO vo) throws Exception;
	
	// 레시피_리뷰 삭제
    void delete(int r_r_bno) throws Exception;
	
	// 레시피_리뷰 총 수
    int count() throws Exception;

	// 레시피_리뷰 목록 + 페이징 + 검색
    List<Recipe_reviewVO> listPageSearch(int displayPost, int postNum, String searchType, String keyword) throws Exception;

	// 레시피_리뷰 총 수 + 검색 적용
    int searchCount(String searchType, String keyword) throws Exception;
    
// Recipe_reviewServiceImpl.java

  // 레시피_리뷰 번호
	@Override
	public int cntBno(Recipe_reviewVO vo) throws Exception {
		return dao.cntBno(vo);
	}
	
	// 레시피_리뷰 목록
	@Override
	public List<Recipe_reviewVO> list() throws Exception {
		return dao.list();
	}
	
	// 레시피_리뷰 작성
	@Override
	public void write(Recipe_reviewVO vo) throws Exception {
		dao.write(vo);
	}
	
	// 레시피_리뷰 조회
	@Override
	public Recipe_reviewVO view(int r_r_bno) throws Exception {
		dao.hit(r_r_bno);
		return dao.view(r_r_bno);
	}
	
	// 레시피_리뷰 수정
	@Override
	public void modify(Recipe_reviewVO vo) throws Exception {
		dao.modify(vo);
	}
	
	// 레시피_리뷰 삭제
	public void delete(int r_r_bno) throws Exception {
		dao.delete(r_r_bno);
	}
	
	// 레시피_리뷰 총 수
	@Override
	public int count() throws Exception {
		return dao.count();
	}
	
	// 레시피_리뷰 목록 + 페이징 + 검색
	@Override
	public List<Recipe_reviewVO> listPageSearch(int displayPost, int postNum, String searchType, String keyword) throws Exception {
		return dao.listPageSearch(displayPost, postNum, searchType, keyword);
	}
	
	// 레시피_리뷰 총 수
	@Override
	public int searchCount(String searchType, String keyword) throws Exception {
		return dao.searchCount(searchType, keyword);
	}
```
```java
// UploadFileUtils.java

	static final int THUMB_WIDTH = 300;
	static final int THUMB_HEIGHT = 300;
	 
	public static String fileUpload(String uploadPath,
	  String fileName,
	  byte[] fileData,
    String ymdPath) throws Exception {

	  UUID uid = UUID.randomUUID();
	  
	  String newFileName = uid + "_" + fileName;
	  String imgPath = uploadPath + ymdPath;

	  File target = new File(imgPath, newFileName);
	  FileCopyUtils.copy(fileData, target);
	  
	  String thumbFileName = "s_" + newFileName;
	  File image = new File(imgPath + File.separator + newFileName);

	  File thumbnail = new File(imgPath + File.separator + "s" + File.separator + thumbFileName);

	  if (image.exists()) {
	    thumbnail.getParentFile().mkdirs();
	    Thumbnails.of(image).size(THUMB_WIDTH, THUMB_HEIGHT).toFile(thumbnail);
	  }
	  return newFileName;
	}

	public static String calcPath(String uploadPath) {
	  Calendar cal = Calendar.getInstance();
	  String yearPath = File.separator + cal.get(Calendar.YEAR);
	  String monthPath = yearPath + File.separator + new DecimalFormat("00").format(cal.get(Calendar.MONTH) + 1);
	  String datePath = monthPath + File.separator + new DecimalFormat("00").format(cal.get(Calendar.DATE));

	  makeDir(uploadPath, yearPath, monthPath, datePath);
	  makeDir(uploadPath, yearPath, monthPath, datePath + "\\s");

	  return datePath;
	}

	private static void makeDir(String uploadPath, String... paths) {

	  if (new File(paths[paths.length - 1]).exists()) { return; }

	  for (String path : paths) {
	    File dirPath = new File(uploadPath + path);
	    if (!dirPath.exists()) {
	      dirPath.mkdir();
      }
	  }
    
	}
```

![recipe_review_comment](https://user-images.githubusercontent.com/68595933/190326240-9030924e-cafc-4690-9f4b-19acdae01222.png)

- 4.3. 댓글 CRUD
  - 댓글 등록/읽기/수정/삭제 가능합니다.
  - 내가 쓴 댓글만 수정/삭제 버튼을 보여줍니다.
  
```java
// Recipe_review_commentController.java

@RequestMapping(value = "/rlist") //댓글 리스트
	@ResponseBody
	private List<Recipe_review_commentVO> listComment(Recipe_review_commentVO vo, Model model) throws Exception{
	  return service.listComment(vo);
	}
	
	@RequestMapping(value = "/rinsert") //댓글 작성 
	@ResponseBody
	private int insertComment(@RequestParam int r_r_c_bno, 
	  @RequestParam String r_r_c_content, 
	  @RequestParam String r_r_c_nickname ) throws Exception{
		  Recipe_review_commentVO vo = new Recipe_review_commentVO();
    	vo.setR_r_c_bno(r_r_c_bno);
    	vo.setR_r_c_content(r_r_c_content);
    	vo.setR_r_c_nickname(r_r_c_nickname);
      return service.insertComment(vo);
	}
	
	@RequestMapping("/rupdate") //댓글 수정  
	@ResponseBody
	private int updateComment(Recipe_review_commentVO vo) throws Exception{   
	  return service.updateComment(vo);
	}
	
	@RequestMapping(value = "/rdelete/{r_r_c_cno}")
	@ResponseBody
	private int deleteComment(@PathVariable int r_r_c_cno) throws Exception{
	  return service.deleteComment(r_r_c_cno);
	}
```
```java
// Recipe_review_commentVO.java

	private int r_r_c_cno;
	private int r_r_c_bno;
	private String r_r_c_content;
	private String r_r_c_nickname;
	private Timestamp r_r_c_date;
	
	public Recipe_review_commentVO(int r_r_c_cno, int r_r_c_bno, String r_r_c_content, String r_r_c_nickname,
		Timestamp r_r_c_date) {
		super();
		this.r_r_c_cno = r_r_c_cno;
		this.r_r_c_bno = r_r_c_bno;
		this.r_r_c_content = r_r_c_content;
		this.r_r_c_nickname = r_r_c_nickname;
		this.r_r_c_date = r_r_c_date;
	}
	public Recipe_review_commentVO() {}
	
	public int getR_r_c_cno() {
		return r_r_c_cno;
	}
	public void setR_r_c_cno(int r_r_c_cno) {
		this.r_r_c_cno = r_r_c_cno;
	}
	public int getR_r_c_bno() {
		return r_r_c_bno;
	}
	public void setR_r_c_bno(int r_r_c_bno) {
		this.r_r_c_bno = r_r_c_bno;
	}
	public String getR_r_c_content() {
		return r_r_c_content;
	}
	public void setR_r_c_content(String r_r_c_content) {
		this.r_r_c_content = r_r_c_content;
	}
	public String getR_r_c_nickname() {
		return r_r_c_nickname;
	}
	public void setR_r_c_nickname(String r_r_c_nickname) {
		this.r_r_c_nickname = r_r_c_nickname;
	}
	public Timestamp getR_r_c_date() {
		return r_r_c_date;
	}
	public void setR_r_c_date(Timestamp r_r_c_date) {
		this.r_r_c_date = r_r_c_date;
	}
	
	@Override
	public String toString() {
		return "Recipe_review_commentVO [r_r_c_cno=" + r_r_c_cno + ", r_r_c_bno=" + r_r_c_bno + ", r_r_c_content="
			+ r_r_c_content + ", r_r_c_nickname=" + r_r_c_nickname + ", r_r_c_date=" + r_r_c_date
			+ "]";
	}
```
```java
// Recipe_review_commentDAO.java

	  // DB서버의 시간정보를 가져오기
    String getTime();
	
	  // 댓글 개수
    int cntComment() throws Exception;
 
    // 댓글 목록
    List<Recipe_review_commentVO> listComment(Recipe_review_commentVO vo) throws Exception;
 
    // 댓글 작성
    int insertComment(Recipe_review_commentVO vo) throws Exception;
    
    // 댓글 수정
    int updateComment(Recipe_review_commentVO vo) throws Exception;
 
    // 댓글 삭제
    int deleteComment(int r_r_c_cno) throws Exception;
    
// Recipe_review_commentDAOImpl.java

  // 시간정보추가
	@Override
	public String getTime() {
		System.out.println("DAO : DB접근 sqlSession객체를 주입!");
		System.out.println("DAO : TEST에서 해당메서드 호출!!! ");
		System.out.println("DAO : memberMapper.xml 이동");
		System.out.println("DAO : Select구문을 실행하는 메서드를 실행해서 SQL구문 실행");
		// "com.itwillbs.mapper.MemberMapper.getTime";
		String result = sqlsession.selectOne(namespace + ".getTime");
		System.out.println("DAO : SQL 구문 실행완료! 값 리턴 후 테스트로 이동");
		return result;
	}

	// 댓글 갯수
	@Override
	public int cntComment() throws Exception {
		int result = sqlsession.selectOne(namespace+".cntComment");
		return result;
	}

	// 댓글 목록
	@Override
	public List<Recipe_review_commentVO> listComment(Recipe_review_commentVO vo) throws Exception {
		return sqlsession.selectList(namespace+".listComment", vo);
	}

	// 댓글 작성
	@Override
	public int insertComment(Recipe_review_commentVO vo) throws Exception {
		System.out.println("@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@DAO : " +vo.getR_r_c_bno() + "@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@");
		return sqlsession.insert(namespace+".inComment", vo);
	}

	// 댓글 수정
	@Override
	public int updateComment(Recipe_review_commentVO vo) throws Exception {
		return sqlsession.update(namespace+".upComment", vo);
	}

	// 댓글 삭제
	@Override
	public int deleteComment(int r_r_c_cno) throws Exception {
		return sqlsession.delete(namespace+".delComment", r_r_c_cno);
	}
```
```java
// Recipe_review_commentService.java

	// 댓글 목록
  List<Recipe_review_commentVO> listComment(Recipe_review_commentVO vo) throws Exception;
	
	// 댓글 작성
  int insertComment(Recipe_review_commentVO vo) throws Exception;
	
	// 댓글 수정
  int updateComment(Recipe_review_commentVO vo) throws Exception;
	
	// 댓글 삭제
  int deleteComment(int r_r_c_cno) throws Exception;
  
// Recipe_review_commentServiceImpl.java

	// 댓글 목록
	@Override
	public List<Recipe_review_commentVO> listComment(Recipe_review_commentVO vo) throws Exception {
		return rrcdao.listComment(vo);
	}

	// 댓글 작성
	@Override
	public int insertComment(Recipe_review_commentVO vo) throws Exception {
		return rrcdao.insertComment(vo);
	}

	// 댓글 수정
	@Override
	public int updateComment(Recipe_review_commentVO vo) throws Exception {
		return rrcdao.updateComment(vo);
	}

	// 댓글 삭제
	@Override
	public int deleteComment(int r_r_c_cno) throws Exception {
		return rrcdao.deleteComment(r_r_c_cno);
	}
```

![tip](https://user-images.githubusercontent.com/68595933/190140620-58af4a13-7d77-4e33-905d-29ef3c334f64.png)
![store_review](https://user-images.githubusercontent.com/68595933/190140201-ff2022a4-88f1-4d87-b449-0c5c27cb241f.png)
![notice_qna](https://user-images.githubusercontent.com/68595933/190332081-8ee891fd-9237-4e64-a581-39128da7769f.png)

- 자취생 노하우, 스토어 후기, 공지 및 QnA 게시판은 레시피 후기 게시판과 거의 동일하므로(CRUD) 설명 생략.

### 5. 스토어

![store](https://user-images.githubusercontent.com/68595933/190143826-734621cf-e53d-4ca4-9cee-7eac304bb2cc.png)

- 위와 중복되는 기능(CRUD) 설명 생략.

![cart](https://user-images.githubusercontent.com/68595933/190143055-b70fad3e-149b-4ee3-be1f-8729af57c442.png)

- 5.1 장바구니
  - 내가 담은 상품의 정보/수량/가격을 보여줍니다.
  
![payment](https://user-images.githubusercontent.com/68595933/190147408-98783ffa-4a92-4457-b4d3-d67cfcd94f8e.png)

- 5.2 주문하기/결제하기
  - 배송정보를 입력합니다.
  - 카카오페이로 결제합니다.

![order](https://user-images.githubusercontent.com/68595933/190148735-c636f25b-e101-4256-ae46-13e41f3d710e.png)

- 5.3 주문조회/고객정보
  - 주문 내역을 확인합니다.
  - 배송 상태를 확인합니다.

## DB 설계

![db_1](https://user-images.githubusercontent.com/68595933/190172557-938ff863-e208-4796-9147-6c4c876e7c99.png)
![db_2](https://user-images.githubusercontent.com/68595933/190148873-19e2820c-729d-4870-bb28-d01639c6b1b4.png)
- 전체 DB 구조 요약

---

## 피드백

### 문제점

1. 시간 부족으로 일부 기능 미구현.
2. 적응형 웹 디자인.

### 개선점

1. SNS/카카오톡 공유 기능이나 실시간 채팅 기능 등 구현할 것.
2. 반응형 웹으로 만들 것.

---

## 저작권

이 프로젝트는 MIT 라이센스에 따라 라이센스가 부여됩니다. 자세한 내용은 [LICENSE.md](LICENSE.md) 파일을 참조하십시오.

<!-- 링크 -->

[데모]: http://rustywhite404.cafe24.com/
