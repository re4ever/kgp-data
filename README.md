# kgp-data

나이트건담이야기(로컬 구동판)의 **온라인 데이터**. 게임 타이틀의 「데이터 받기」가 여기서 받아 간다.

| 파일 | 내용 |
|---|---|
| `kgp_data.txt` | 판 정보 — `data=YYMMDD.HHMM`(한국 시각 데이터 판), `app=0.02.NN`(필요한 앱 판) |
| `kgp_data.zip` | 표 꾸러미 — `csv/*.csv` + `csv/_data_version.txt`, **무압축**(게임이 압축을 풀지 않는다) |

게임은 `https://raw.githubusercontent.com/re4ever/kgp-data/main/kgp_data.txt` 를 먼저 받아 판을 견주고,
새 판이면 `…/kgp_data.zip` 을 받는다. 두 파일은 본 저장소의 에디터 「온라인 데이터」 가 함께 만든다 —
**둘을 같이 바꿔 올릴 것**, zip 을 손으로 다시 압축하지 말 것.

이 저장소는 공개다. 게임 표 말고는 아무것도 넣지 않는다.
