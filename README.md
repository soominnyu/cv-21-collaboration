# cv-21-collaboration
naver boostcamp cv-21 team github study
# CLI, 버전관리

1. **버전 관리가 무엇인가?**
   - 동일한 파일명에 진행과정 기록하는 것
     - 버전 관리는 파일이나 소스 코드의 변화를 시간에 따라 기록하고 관리하는 시스템입니다. 이를 통해 과거 버전으로의 복구, 변경 사항 추적, 협업 등이 가능합니다.

2. **CLI(Command Line Interface)를 왜 배워야 하는가?**
   - CLI는 어렵기 때문에 배워야 한다
     - CLI는 명령어 기반으로 컴퓨터와 상호작용하는 인터페이스입니다. 이를 배우면 자동화, 효율적인 작업 수행, 그리고 GUI로는 할 수 없는 고급 기능을 사용할 수 있게 됩니다.

# git != GitHub

1. **git 과 github는 다릅니다. 어떻게 다른가요?**
   - Git: 분산 버전 관리 시스템으로, 코드의 변경 이력을 관리하고 여러 사람이 동시에 작업할 수 있게 합니다.
   - GitHub: Git 저장소를 호스팅하는 웹 서비스로, Git의 기능을 기반으로 협업, 코드 리뷰, 이슈 추적 등을 지원합니다.

# init, clone

1. **Repository를 local에 생성하는 방법은 init, clone 두 가지가 있습니다. 이 두 가지가 무엇이 다른가요?**
   - `init`: 새로 로컬 저장소를 생성합니다. 즉, 기존의 버전 관리가 없는 디렉토리를 버전 관리하기 시작합니다.
   - `clone`: 원격 저장소를 복제하여 로컬에 저장소를 생성합니다. 원격 저장소의 내용을 가져와서 로컬에 동일한 버전 관리 환경을 설정합니다.

2. **git clone하는 절차와 명령어를 적어주세요.**
   - 원격 저장소 URL을 사용하여 로컬로 복제합니다.
   ```bash
   git clone <repository-url>
   ```

3. **.git 폴더에는 어떤 내용이 들어가있나요? 삭제하면 어떻게 되나요?**
   - `.git` 폴더에는 Git 저장소의 모든 버전 정보, 설정, 리포지토리 데이터 등이 포함되어 있습니다. 이 폴더를 삭제하면 해당 디렉토리는 Git 저장소가 아니게 되며, 버전 관리 정보가 모두 사라집니다.

# Workflow

1. **git workflow는 working tree, staging area, repository 3가지가 있습니다. 어떻게 다른 지 정리해보세요.**
   - Working Tree: 현재 작업 중인 파일들이 있는 디렉토리입니다.
   - Staging Area: 커밋을 위해 준비된 파일들이 모여 있는 영역입니다.
   - Repository: 최종적으로 커밋된 파일들이 저장되는 영역입니다.

2. **각 단계를 넘어가는 명령어는 무엇인지 적어주세요.**
   ```bash
   git add <file> # Working Tree에서 Staging Area로 파일을 추가합니다.
   git commit -m "commit message" # Staging Area에서 Repository로 파일을 커밋합니다.
   git push <remote> <branch> # 로컬 Repository에서 원격 Repository로 파일을 푸시합니다.
   ```

3. **repository에 저장된 버전을 확인하려면 어떤 명령어를 써야하나요?**
   ```bash
   git log
   ```

# 여러 파일로 하나의 버전

1. **tracked file, untracked file의 차이는 무엇인가요?**
   - Tracked File: Git이 버전 관리를 하고 있는 파일로, 이미 커밋되었거나 staging area에 있는 파일들입니다.
   - Untracked File: Git이 아직 버전 관리하지 않는 파일로, 워킹 디렉토리에 새로 추가되었지만 git add 명령어로 스테이징 되지 않은 파일들입니다.

2. **git은 모든 파일을 항상 track(추적)하지 않는데 왜 그럴까요?**
   - 불필요한 파일들까지 버전 관리하게 되면 저장소가 커지고, 성능 저하와 혼란이 발생할 수 있기 때문입니다. 따라서, 중요한 파일들만 추적하여 효율적인 버전 관리를 합니다.

3. **항상 무엇을 생활화하자?**
   - 커밋 메시지를 작성하는 습관을 생활화하자.
     - 의미 있는 커밋 메시지는 프로젝트의 변경 이력을 쉽게 이해하고 관리하는 데 도움을 줍니다.
