---
title: "[CS] 가상화에 대해서"
data: 2020-10-17
published: true
tags: ['CS', 'Virtualization', 'Citrix', 'F5', '가상화']
series: false,
cover_image: ./images/Virtualization.png
canonical_url: false
description: " 가상화에 대한 글입니다. "

---

# Citrix와 F5

장비에 Citrix에서 F5 등이 있다는데 이 장비들은 무슨 장비고 어떠한 장단점을 들고 있는지 의문점이 들었다.

따로 찾아보니 Citrix와 F5 모두 가상화 제품으로 확인되었다. Citrix와 F5를 알기전에 가상화와 가상화 제품이란 어떠 것인가를 찾아보았다.

<br/>

## 가상화

가상하는 하드웨어 기능을 시뮬레이션하여서 애플리케이션 서버, 스토리지 및 네트워크와 같은 소프트웨어 기반 IT 서비스를 생성하는 기술이다.

### 작동은 어떻게 하나요?

가상화는 하이퍼바이저라고 하는 소프트웨어를 사용하여 하나의 물리적 머신에 다수의 가상 머신을 만든다. 이러한 가상머신은 하나의 컴퓨터 리소스에 의존하여 물리적 머신과 같이 작동하기 때문에 가상회를 사용하면 IT조직은 단일 서버(호스트)에서 여러개의 운영 체제를 실행할 수 있다. 이러한 운영이 훨씩 효율적이고 하이퍼라이저는 컴퓨터 리소스를 필요에 따라 각 가상 머신에 할당한다. 이 결과, IT 운영이 훨씬 효율적이고 경제적으로 된다. 또한 유연한 리소스 할당으로 인해 가상화 클라우드 컴퓨팅의 기초를 세울 수 있다.

### 가상화와 클라우드 컴퓨팅의 비교

클라우드 컴퓨팅 : 인터넷을 통해 공유 컴퓨팅 리소스, 소프트웨어 또는 데이터를 제공하는 방식

가상화 기술 : 관리 소프트웨어 계층을 사용하여 가상 리소스를 손쉽게 관리하고 구축할 수 있는 중앙 집중식 풀로 할당해 클라우드 컴퓨팅을 가능하게 한다. 작동방법은 다음과 같습니다.
1. 가상화는 하이퍼바이저를 사용해서 물리적 서벙서 가상 머신을 생성함으로써, 서버의 컴퓨팅 파워, 애플리케이션 또는 스토리지를 가상 환경에 제공한다.
2. 가상 리소스는 중앙 위치에서 함께 풀링되어 다른 컴퓨터가 네트워크를 통해 액세스할 수 있습니다. 이 중앙 집중식 리소스 풀을 **클라우드**라고 합니다.
3. 네트워크의 컴퓨터에 많은 스토리지 또는 컴퓨터 파워가 필요한 경우, 클라우드의 관리 소프트웨어를 통해서 관리자들이 이러한 리소스를 손쉽게 프로비지닝하고 요청하는 컴퓨터에 제공할 수 있다. 이 단계는 클라우드의 "셀프 서비스" 요소를 활성화할 수 있도록 자동화할 수도 있으므로 사용자들은 관리자의 승인을 기다릴 필요가 없다.
4. 요청 컴퓨터가 더 이상 클라우드 컴퓨팅 또는 스토리지를 필요로 하지 않으면 클라우드의 자동화 기능이 추가 리소스를 비활성화하여 낭비를 줄이고 컴퓨팅 비용을 제어할 수 있다. 이는 **탄력적, 자동화 인프라 확장**이라고 합니다.

### 가상화의 장점

#### 1. 효율성

- 가상화는 하나의 머신이 여러 개의 가상 머신에 서비스 제공 가능. 이는 필요 서버가 줄어들며 보유하는 서버를 최대한 활용 가능하다. 즉, **환경적 장점, 냉각 및 유지보수 비용 절감 효과**를 얻을 수 있다.
- 가상화를 통해 여러 벤더에 분리된 서버를 요구하지 않고 단일 머신에서 여러 유형의 앱, 데스크탑 및 운영 체제를 운영할 수 있다. 따라서 특정 벤더에 의존하지 않아도 되며 IT 리소스의 관리에 드는 시가을 훨씬 줄일 수 있어 **IT팀의 생산성을 높일 수 있음**

#### 2. 안정성

- 가상화 기술을 사용하면 기존 서버의 가상 머신 스냅샷을 사용해 **데이터를 손쉽게 백업하고 복구**할 수 있다. 
- 모든 데이터를 최신 상태로 유지하기 위해 이 백업 프로세스를 자동화하는 것도 간단하다
- 긴급 상황이 발생하여 백업된 가상 머신에서 복원해야할 경우, 이 가상 머신을 몇 분만에 새 위치로 손쉽게 마이그레이션할 수 있다. 이로 인해 재해 또는 손실 복구가 용이해지기 때문에 **안정성과 비즈니스 연속성이 향상**한다.

#### 3. 비즈니스 및 전략

- 가상화 소프트웨어를 사용하여 조직이 **리소스를 테스트하고 할당하는 방법이 더욱 유연**해진다.
- 가상 머신을 백업하고 복원하기 너무 쉽기 때문에 IT팀은 새로운 기술을 손쉽게 테스트하고 실험할 수 있다.
- 가상 머신 리소스를 조직의 공유된 풀 안에 할당하여 클라우드 전략을 만들 수 있다. 이 클라우드 기반 인프라는 IT팀이 누가 어떤 리소스를 어떤 기기에서 액세스하는지 제어할 수 있게 하여, **보안과 유연성을 개선**할 수 있다.

### 다양한 유형의 가상화

#### 1. 서버 가상화

IT 부서가 서버당 하나의 작업 또는 애플리케이션을 지정하는 것이 일반적이지만 이로 인해 많은 경우 용량 활용도가 떨어지고 유지보수 비용이 높아질 수 있다. 

서버 가상화는 하이퍼바이저를 사용하여 물리적 서버를 여러 가상 서버로 파티션을 나누어 각 서버가 자체 운영 시스템을 운영한다. 이를 통해 물리 서버의 파워를 최대한 활용하여 하드웨어와 운영 비용을 대폭 줄일 수 있다.

#### 2. 앱 가상화 및 데스크탑 가상화

가상화는 전체 서버를 시뮬레이션할 필요는 없습니다. 이 기술은 개별 애플리케이션 계층 또는 데스크탑도 가상화할 수 있기 때문입니다.

- **애플리케이션 가상화**를 통해, 사용자는 사용 중인 운영 체제와 관계없이 분리된 형태로 애플리케이션을 실행할 수 있다. 이것은 일반적으로 Linux 또는 Mac 운영 체제 내에서 Windows 애플리케이션을 실행하는 데 사용된다.
- **데스크탑 가상화**를 사용하면 사용자가 데스크의 씬 클라이언트와 같은 연결된 기기에서 원격으로 데스크탑에 액세스하기 위해 워크스테이션 부하를 활성화할 수 있다. 따라서 데스크탑 가상화를 통해 데이터 센터 리소스에 훨씬 더 안전하고 휴대 가능한 액세스를 할 수 있다.

특징
- 직원이 자기 소유의 기기를 사용하고 사무실 밖에서 자신의 앱에 액세스하고 싶어 하기 때문이다. 동시에, 각 사용자에 대해 개별 컴퓨터에서 앱과 데스크탑을 설치하고 유지보수하려면 비용이 많이 들고 관리하기 어렵다.
- 가상 앱 및 데스크탑은 IT 부서가 수백 개의 시뮬레이션된 앱 및 데스크탑을 사용자에게 한 번에 구축할 수 있는 중앙 서버에 의존하여 더 나은 솔루션을 제공한다. 이를 통해, 이러한 앱 및 데스크탑 (및 패치와 업데이트)를 각 컴퓨터에 설치할 필요가 없으며 사용자는 가상 앱 및 데스크탑과 기본과 동일한 사용자 환경으로 상호작용할 수 있다. 
- 가상 앱 및 데스크탑은 조직들이 규제 준수, 재해 복구 및 비즈니스 연속성을 보장하는 데도 도움을 준다.


#### 3. 네트워킹 가상화

네트워크 가상화는 사용 가능한 대역폭을 독립 채널로 분리하여 진행하는데 필요에 따라 각각 서버 또는 기기에 배정할 수 있다. 네트워크 가상화를 이용하면 기본 인프라를 조정할 필요 없이 더 쉽게 부하 분산 및 방화벽과 같이 네트워크를 프로그래밍하고 프로비저닝할 수 있다. 

IT 부서는 일반적으로 소프트웨어 기반 관리자 콘솔을 사용하여 소프트웨어 구성 요소를 관리한다. 컴퓨팅 요구사항이 높아지더라도 IT 부서는 네트워크 가상화를 통해 작업 부하를 배포, 확장 및 조정하는 방식을 간소화할 수 있다.

#### 4. 스토리지 가상화

스토리지 가상화는 네트워크의 여러 기기에서 물리적 스토리지를 중앙 콘솔에서 관리되는 통합된 가상 스토리지 기기로 함께 풀링된다. 스토리지를 가상화하려면 물리적 기기에서 사용 가능한 용량을 식별하고 그 용량을 가상 환경에 함께 종합할 수 있는 가상화 소프트웨어가 필요하다. 최종 사용자가 보기에, 가상 스토리지는 표준 물리적 하드 드라이브와 같다. 

가상 스토리지는 하이퍼 수렴 인프라와 같은 IT 전략의 중요한 구성 요소로서 이를 통해 IT 관리자는 백업, 보관 및 복구와 같은 스토리지 활동을 간소화할 수 있다.

#### 5. 데이터 가상화

데이터 가상화를 사용하면 애플리케이션이 데이터가 물리적으로 위치한 장소나 데이터에 지정된 형식과 같은 세부 정보가 없어도 데이터에 액세스하고 활용할 수 있다. 따라서 해당 데이터를 이동하거나 복사하지 않고도 여러 소스의 데이터를 한 가지로 표현할 수 있다. 이 데이터 종합은 데이터 가상화 소프트웨어에 의존하여 대시보드를 통해 데이터를 가상으로 통합 및 시각화하므로, 사용자가 데이터의 저장 위치가 어디이든 단일 액세스 지점으로부터 대규모 데이터 세트에 액세스할 수 있다. 데이터 가상화는 모든 종류의 분석 또는 비즈니스 인텔리전스 애플리케이션에 중요하다.


### 가상화의 보안 위험

비즈니스의 데이터의 보안을 유지하려면 가상화를 올바로 관리해야 한다. 가상 머신은 서버의 사본이기 때문에, 가상 머신이 많을수록 중요 데이터에 액세스하려는 공격자로부터 보호해야 하는 대상이 많아진다. 

이러한 보안 취약성으로 인해, 가상 머신을 모니터링하고 무단 액세스로부터 보호하기 위한 중앙 집중식 관리 솔루션을 보유하고 있는 것이 중요하다. **가상화 보안**은 가상 데스크탑 인프라, 즉 VDI의 필수적인 요소다.

### 업무 공간 내의 가상화

> 회사에서 사용하는 회사망을 어떻게 구성하는 지 궁금했는데, 이러한 방법을 사용하는 것이였구나.

**업무 공간 가상화**는 여러 개의 앱을 하나의 통합된 디지털 업무 공간으로 번들링하여 애플리케이션 가상화를 기반으로 구축된다. 이를 통해 가상 머신에서 전체 컴퓨팅 업무 공간을 시뮬레이션할 수 있어, 사용자의 애플리케이션이 물리적 머신에서와 동일한 방법으로 상호작용할 수 있다. 예를 들어, 업무 공간 가상화를 통해 사용자가 워드 프로세싱 문서에 스프레드시트를 임베딩할 수 있습니다. 기존 애플리케이션 가상화에서는 각 개별 앱을 따로 가상화하여 서로 상호작용할 수 없었습니다.

또한 업무 공간 가상화를 통해 사용자는 **자체 설정과 데이터를 가상화된 업무 공간 내에 유지**할 수 있다. 따라서 가상화된 업무 공간은 물리적 머신과 동일한 방법으로 각 사용자에 맞게 사용자 지정할 수 있다. 또한 사용자는 고유 가상 업무 공간을 다른 운영 체제 또는 머신으로 이동하는 동시에 모든 앱과 데이터는 보존할 수 있다. 이를 통해 사용자가 업무에 필요한 앱과 데이터를 자신이 선택하는 기기에서 액세스하는 방법을 더 유연하게 만들 수 있다.




---

**출처**

https://www.citrix.com/ko-kr/glossary/what-is-virtualization.html