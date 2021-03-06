---



copyright:

  years: 2015, 2019
lastupdated: "2019-01-03"

---


{:shortdesc: .shortdesc}
{:gif: data-image-type='gif'}
{:new_window: target="_blank"}
{:tip: .tip}



# {{site.data.keyword.Bluemix_notm}} CLI 시작하기
{: #getting-started}

[여기](/docs/cli/index.html)에 설명된 방법을 사용하여 {{site.data.keyword.Bluemix_notm}} CLI 및 모든 권장 종속 항목을 설치하는 것이 좋습니다.
{: tip}


{{site.data.keyword.Bluemix_notm}} CLI는 {{site.data.keyword.Bluemix_notm}}에서 애플리케이션, 컨테이너, 인프라, 서비스 및 기타 리소스를 관리하기 위한 명령행 인터페이스를 제공합니다.


{{site.data.keyword.Bluemix_notm}} CLI를 시작하려면 다음을 수행하십시오.

1. 다운로드할 OS의 설치 프로그램 선택

   Mac OS X 64비트: [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx/checksum){: new_window} <br>
   Windows 64비트: [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64/checksum){: new_window} <br>
   Linux X86 64비트: [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64/checksum){: new_window} <br>
   Linux LE 64비트(ppc64le): [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le/checksum){: new_window} <br>

   **32비트 릴리스 및 이전 버전은 [여기서](/docs/cli/reference/ibmcloud/all_versions.html) 찾을 수 있습니다.

1. 설치 프로그램 실행
   * macOS 및 Windows의 경우 설치 프로그램을 실행하십시오.
   * Linux의 경우 패키지의 압축을 풀고 `install_bluemix_cli` 스크립트를 실행하십시오.

1. API 엔드포인트를 대상으로 지정 및 {{site.data.keyword.Bluemix_notm}}에 로그인

  ![예제](example.gif){: gif}

이제 {{site.data.keyword.Bluemix_notm}} 리소스를 관리할 준비가 되었습니다. 명령 설명을 보려면 `ibmcloud help`를 입력하십시오.

연합 ID를 사용하는 경우 [여기](/docs/iam/login_fedid.html#federated_id)의 지시사항을 따라 일회성 패스코드 또는 API 키로 로그인하십시오.
{: tip}

## {{site.data.keyword.Bluemix_notm}} CLI를 자세히 살펴보기 위한 기타 링크

* [{{site.data.keyword.Bluemix_notm}} CLI 다운로드 및 설치를 위한 추가 옵션](/docs/cli/reference/ibmcloud/download_cli.html)
* [플러그인으로 {{site.data.keyword.Bluemix_notm}} CLI 기능 확장](/docs/cli/reference/ibmcloud/extend_cli.html)
* [{{site.data.keyword.Bluemix_notm}} CLI 및 릴리스 정보의 모든 버전](/docs/cli/reference/ibmcloud/all_versions.html)
* [{{site.data.keyword.Bluemix_notm}} CLI 명령 사용법 문서](/docs/cli/reference/ibmcloud/bx_cli.html)


## 문제 보고 및 피드백 제출
{: #issues}

다음 옵션을 사용하여 문제를 보고하거나 새 기능 요청을 제출하십시오.
 * [GitHub](https://github.com/IBM-Bluemix/bluemix-cli-release/issues){: new_window} ![외부 링크 아이콘](../../../icons/launch-glyph.svg)에서 문제 작성
 * [Slack 채널](https://dwopen.slack.com/messages/bluemix-cli/){: new_window} ![외부 링크 아이콘](../../../icons/launch-glyph.svg)에 메시지 남기기
