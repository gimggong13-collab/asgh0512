# 안성여고 지속가능한 공동체 프로젝트

## 배포 전 필수 작업

### 1. Supabase 테이블 생성
1. [supabase.com](https://supabase.com) → 본인 프로젝트 접속
2. 좌측 메뉴 **SQL Editor** 클릭
3. `supabase_setup.sql` 파일 내용을 전체 복사 후 붙여넣기 → **Run**

### 2. index.html에 Supabase 키 입력
`index.html` 파일 상단에서 아래 두 줄을 찾아서 교체하세요:

```js
const SUPABASE_URL = 'https://여기에-프로젝트-URL.supabase.co';
const SUPABASE_ANON_KEY = '여기에-anon-public-key를-붙여넣으세요';
```

키 확인 위치: Supabase 대시보드 → **Project Settings** → **API**
- `Project URL` → SUPABASE_URL
- `anon public` → SUPABASE_ANON_KEY

### 3. GitHub에 push
```bash
git add .
git commit -m "Add Supabase integration"
git push
```
Vercel이 자동으로 재배포합니다.

---

## 파일 구조
```
/
├── index.html         ← 메인 앱 (Supabase 연동 포함)
├── vercel.json        ← Vercel 라우팅 설정
├── supabase_setup.sql ← Supabase 테이블 생성 SQL
└── README.md
```

## 제출 데이터 확인
Supabase 대시보드 → **Table Editor** → `submissions` 테이블에서 확인하세요.
