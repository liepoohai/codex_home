# Google Play 스토어 매출 랭킹 크롤러

Google Play 스토어의 **매출 상위(topgrossing)** 컬렉션 페이지를 HTML로 받아서
앱 ID와 제목을 추출하는 간단한 스크립트입니다.

> ⚠️ Google Play의 HTML 구조는 자주 변경됩니다. 결과가 비어 있으면
> 파싱 로직을 업데이트해야 합니다.

## 사용 방법

```bash
python play_store_grossing.py --hl ko --gl KR --limit 50
```

JSON 출력:

```bash
python play_store_grossing.py --json --limit 25
```

카테고리 필터(예: GAME):

```bash
python play_store_grossing.py --category GAME --limit 50
```

## 출력 예시 (CSV)

```text
rank,app_id,title
1,com.example.app,Example App
```

## 주의 사항

- 본 코드는 **공개 HTML**을 대상으로 한 간단한 스크레이핑 예제입니다.
- 대량 호출 시 서비스 약관 및 로봇 정책을 확인하고, 적절한 속도로 요청하세요.
