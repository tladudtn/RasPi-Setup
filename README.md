# RasPi-Setup

컵라면 에디션

## 목록

0. 초기설정
1. 업데이트
2. 폰트/입력기 설치
3. IP 변경
4. 기타설정

### 0. 초기설정

#### 0.1 MICRO SD 카드 권장 스펙

최소 : 8G 용량, CLASS 10

권장 : 16G~ 용량, R/W 속도 30~MB/s+, A1 또는 A2

#### 0.2 OS 초기설정

언어, 입력방식, 시간대는 한국으로 설정하되  
아래에 있는 USE Eng~ 체크(**필수**)

### 1. 업데이트

```bash
sudo apt-get update -y && sudo apt-get upgrade -y
```

### 2. 폰트, 입력기 설치

```bash
# 폰트
apt-get install fonts-nanum-coding

# 입력기
apt-get install ibus ibus-hangul

## 위 2개 전부 설치후 재부팅
```

### 3. IP 변경

```bash
nano /etc/dhcpcd.conf # interface 수정할필요 x
sudo systemctl restart dhcpcd
```



### 4. 기타 설정

#### 4.1 더 많은 비디오 메모리가 필요한경우

Raspberry Pi Configuration -> Performance -> GPU men(기본 78mb)

#### 4.2 SSH / VNC 활성화

Raspberry Pi Configuration -> Interfaces -> SSH/VNC enable(설정은 알아서)

