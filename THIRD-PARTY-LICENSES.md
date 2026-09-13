<!--
  배포하는 실행 파일에 함께 담기는 제3자 구성 요소의 라이선스 고지.

  🔴 번들 dumpcap 을 다른 버전으로 갈면 아래 버전·소스 링크도 그 버전으로 바꾼다.
     버전이 실제 번들과 어긋나면 GPL 고지가 무효다.
-->

# 제3자 라이선스 고지

G-Tracker 설치본에는 아래 제3자 구성 요소가 함께 담겨 있습니다. 각 라이선스를 준수하며,
원저작물의 소스 입수 경로를 함께 밝힙니다.

---

## dumpcap (Wireshark)

- **용도** — 네트워크 패킷 캡처. G-Tracker 는 dumpcap 을 **별도 프로세스로 실행**해 표준
  출력으로 결과만 받습니다. 코드를 링크하지 않으며(단순 병치), **원본을 수정하지 않고
  그대로** 사용합니다.
- **라이선스** — GNU General Public License, version 2 (GPLv2)
- **저작권** — © Gerald Combs 및 Wireshark 기여자들
- **담긴 버전** — Wireshark 4.6.8 의 dumpcap
- **소스 코드** — 위 버전의 대응 소스를 아래에서 받을 수 있습니다.
  `https://www.wireshark.org/download/src/all-versions/wireshark-4.6.8.tar.xz`
- **라이선스 전문** — 함께 담긴 `licenses/GPL-2.0.txt`
  (원문: `https://www.gnu.org/licenses/old-licenses/gpl-2.0.html`)
- **소스 제공** — 요청하시면 위 버전의 대응 소스를 제공합니다(GPLv2 §3). 위 링크가 그
  버전을 그대로 제공하고 있어, 대개 링크로 갈음됩니다. 요청은 아래 [연락처](#연락처)로 보내 주세요.

### dumpcap 이 함께 쓰는 지원 라이브러리

dumpcap.exe 혼자로는 뜨지 않아, 그것이 부르는 라이브러리도 같이 담습니다(전부 Wireshark
4.6.8 배포본에서 그대로 꺼낸 것이며 수정하지 않았습니다). Windows 기본 제공 DLL 과
`vcruntime140.dll`(Microsoft Visual C++ 재배포 런타임, Microsoft 재배포 조건에 따라 동봉)은
별도이며, 그 외 담긴 라이브러리는 아래와 같습니다.

| 파일 | 라이브러리 | 라이선스 | 전문 | 소스 |
|---|---|---|---|---|
| `glib-2.0-0.dll`, `gmodule-2.0-0.dll` | GLib | LGPL-2.1+ | `licenses/LGPL-2.1.txt` | https://gitlab.gnome.org/GNOME/glib |
| `intl-8.dll` | GNU gettext (libintl) | LGPL-2.1+ | `licenses/LGPL-2.1.txt` | https://ftp.gnu.org/gnu/gettext/ |
| `iconv-2.dll` | GNU libiconv | LGPL-2.1+ | `licenses/LGPL-2.1.txt` | https://ftp.gnu.org/gnu/libiconv/ |
| `pcre2-8.dll` | PCRE2 | BSD | `licenses/PCRE2.txt` | https://github.com/PCRE2Project/pcre2 |
| `zlib-ng2.dll` | zlib-ng | zlib | `licenses/zlib-ng.txt` | https://github.com/zlib-ng/zlib-ng |
| `zstd.dll` | Zstandard | BSD-3 (GPL-2.0 이중) | `licenses/zstd.txt` | https://github.com/facebook/zstd |
| `lz4.dll` | LZ4 | BSD-2 | `licenses/LZ4.txt` | https://github.com/lz4/lz4 |
| `xxhash.dll` | xxHash | BSD-2 | `licenses/xxHash.txt` | https://github.com/Cyan4973/xxHash |

각 라이선스 전문은 이 문서 옆 `licenses/` 폴더에 함께 둡니다(배포물과 함께 전달).

**🔴 LGPL 소스 제공** — GLib·gettext·libiconv 는 LGPL 이라 라이브러리 소스도 제공해야 합니다.
전부 수정 없이 그대로 담았고, 대응 소스는 위 upstream 에서 받을 수 있습니다. **요청하시면
우리가 담은 그 버전의 대응 소스를 제공합니다**(아래 [연락처](#연락처)). LGPL 라이브러리는 수정 없이 별도 DLL 로 담겨
있어, 사용자가 같은 이름의 DLL 로 교체할 수 있습니다(LGPL 준수).

---

## Npcap

G-Tracker 는 Npcap 을 **재배포하지 않습니다.** 패킷을 잡는 드라이버인 Npcap 은 사용자가
직접 [npcap.com](https://npcap.com) 에서 받아 설치합니다. 설치본에 담기지 않으므로 이
고지의 대상이 아닙니다.

---

## 연락처

라이선스 문의와 대응 소스 요청은 아래로 보내 주세요.

- **이메일** — ghj667067@gmail.com

---

마지막 갱신: 2026-09-13. 번들 구성(버전·DLL 목록)이 바뀌면 이 문서도 함께 갱신합니다.
