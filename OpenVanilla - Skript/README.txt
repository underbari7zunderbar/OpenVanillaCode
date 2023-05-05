# 소개
마인크래프트 OpenVanilla 서버에서 자체 개발되었던 기능의 일부입니다. 이 기능들은 Skript로 구현되었습니다.

# Skript 코드의 사용권
저는 간단한 아이디어에서 시작했던 독창적인 기능이 마인크래프트를 더 다채롭게 만들 수 있기를 바랍니다. 이 문서를 포함하여 함께 배포된 코드는 '퍼블릭 도메인'으로 지적재산권을 포기함을 명시합니다. 누구나 언제든 어디에든 자유롭게 사용할 수 있습니다. 따라서 귀하는 개인적인 사용 이외에도 코드 디버깅 또는 리버싱을 포함한 모든 권한을 가집니다. 수정하여 재배포할 수 있고, 그 자체로도 재배포할 수 있습니다. 단, 저작인격권은 영구적으로 보존됩니다. 자세한 사항은 아래 바로가기를 참고해주세요.

https://ko.wikipedia.org/wiki/퍼블릭_도메인

서명: remsomets (yourheart3123@gmail.com)

# OpenVanilla 브랜드 및 로고 등의 사용권
OpenVanilla의 상표(마인크래프트 개인 서버) 및 로고, 이미지 등은 저작자의 동의 없이 공개적, 상업적으로 사용할 수 없습니다. 해당 파일에는 관련된 파일이 포함되어 있으며, 이는 개인적으로만 사용할 수 있습니다. 위 코드를 퍼블릭 도메인으로 전환하더라도 OpenVanilla 자체의 상표권을 포기하는 것은 아니며, 퍼블릭 도메인으로 전환되는 것은 일부 코드에 한합니다. 서버가 중지되거나 코드가 퍼블릭 도메인으로 배포되어도 상표권은 엄격하게 보호됩니다.

# 코드 열람 시 주의 사항
비속어 필터 기능에서 사용하는 비속어 목록에는 일반적으로 불쾌하게 여겨질 수 있는 단어가 다수 포함되어 있습니다.

# 코드 설명
이 코드는 마인크래프트 1.19.3 및 Skript 2.6.3에서 마지막으로 정상 실행되었습니다.

이 코드를 실행하기 위해서는 아래 애드온(Add-on) 및 플러그인이 필요합니다.
 * SkriptJSON (1.1.0)
 * Skent (3.1.0)
 * SkQuery (4.1.7)
 * skript-reflect (2.3)
 * skript-vorifier-hook (1.1.0)
 * NuVotifier
 * Vault
 * Bukkit 호환 권한 플러그인 (LuckPerms 권장)
 * ServerBrand (1.0)

각 코드는 다음 기능을 구현합니다.
 * 0/Debug - 임시 디버그 코드용 디렉터리
 * 0/Initialize - 구동 시작 시 실행되는 코드 디렉터리
 * 0/Libraries - 대다수의 코드에서 참조하는 함수
 * 1/CopyMapToWorld - 특정 지도를 세계에 덮어씌움
 * 1/EasyNBT - 일부 아이템의 데이터를 더 쉽게 수정할 수 있음
 * 1/FirstJoinItems - 최초 접속 시 아이템을 지급함
 * 1/FixSoulBlockClip - 미구현 (개발 도중 서버 중지)
 * 1/GriefAlert - 특정 행위(주민 학살 등)가 발생하면 관리자에게 알림을 보냄
 * 1/GriefPrevention - 특정 엔티티 및 몹이 블록을 파괴할 수 없도록 함
 * 1/InventoryViewer - 관리자가 플레이어의 보관함을 확인하는 명령어
 * 1/PrevenItemFlooding - 세계에 한 아이템이 너무 많이 생성되면 자동으로 삭제함
 * 1/RandomizeEndCitySeed - 엔더 시티 생성 시드를 로드할 때마다 다시 생성함
 * 1/ResetPlayerData - 플레이어 데이터를 제거하는 명령어
 * 1/RestoreOptions - 게임 설정 및 규칙을 로드할 때마다 재설정함
 * 1/SkriptAdditional - Skript 관련 부가 기능
 * 2/ClaimChunk - 청크 단위 지역 보호 기능
 * 2/VoteListener - Votifier 추천 패킷 수신 및 처리 기능
 * 3/ConnectionBasics - 연결 정보 수집기
 * 3/PlayerBasics - 플레이어 정보 수집기
 * 3/PlayerSettings - 플레이어별 부가 설정 저장 및 불러오기 기능
 * 4/Branding - OpenVanilla 상표 표시 관련 기능 및 명령어
 * 4/Query - 관리자가 수집된 정보를 열람하는 명령어
 * 4/Social - 사회적 상호작용 및 대화, 알림 기능 및 명령어