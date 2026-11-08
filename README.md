# kgp-data

나이트건담이야기(로컬 구동판)의 **온라인 데이터**. 게임 타이틀의 「데이터 받기」가 여기서 받아 간다.

| 파일 | 내용 |
|---|---|
| `kgp_data.txt` | 판 정보 — `data=YYMMDD.HHMM`(한국 시각 데이터 판), `app=0.02.NN`(필요한 앱 판) |
| `kgp_data.zip` | 표 꾸러미 — `csv/*.csv` + `csv/_data_version.txt` (무압축 zip, XOR 로 가림) |
| `kgp_res.txt` | 리소스 묶음 정보 — `pack`(묶음 crc) · `size` · `files` · `part=<이름> <크기> <crc>` |
| `kgp_res.000…` | 게임 리소스(그림·소리·애니메이션) **한 묶음**을 40MB 조각으로 자른 것 (XOR 로 가림) |

XOR 은 보안이 아니라 가림막이다. 게임은 `pack` 이 기기에 받아 둔 것과 다를 때만 조각을 받아 이어 푼다.

게임은 `https://raw.githubusercontent.com/re4ever/kgp-data/main/kgp_data.txt` 를 먼저 받아 판을 견주고,
새 판이면 `…/kgp_data.zip` 을 받는다. 모두 본 저장소 에디터의 **「kgp-data 올리기」** 가 만들어 commit·push 한다 —
**둘을 같이 바꿔 올릴 것**, zip 을 손으로 다시 압축하지 말 것.

이 저장소는 공개다. 게임 표 말고는 아무것도 넣지 않는다.
