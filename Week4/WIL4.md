#### 브랜치 관리의 필요성
-서로의 작업에 영향을 주지 않기 위해 브랜치의 분리 필요,각 브랜치가 어떤 작업을 위해 존재하는지 구분 필요,main 브랜치의 안전한 관리 필요

#### 브랜치 보호 규칙
-승인 없이 pull requset를 병합할 수 없도록 제한 가능, 특정 브랜치에 push 가능자를 제한 가능
### 브랜치 전략
- git flow vs github flow

#### git flow

- 브랜치 종류:main branch(main(master),develop),supporting branches(feature,release,hotfix)
- main:프로젝트 생성 시 기본으로 생성되는 브랜치,영원히 존재하는 첫 번째 브랜치, 병합될 때마다 새로운 버전이 탄생
- develop:영원히 존재하는 두 번째 브랜치,feature 브랜치의 기반이 됨.
- feature: develop 브랜치에서 분기하여 작업, 기능 개발 완료 후 다시 develop으로 병합
- release: 배포 준비를 위한 브랜치,자잘한 버그를 수정하고 QA 작업을 함,develop 브랜치에서 분기하여 main 브랜치로 병합
- hotfix: 배포 환경에서 즉각적인 수정이 필요할 경우 사용,main 브랜치에서 분기, main, develop 모두에 병합 필요
### GitHub Flow(요즘 대세)
- 브랜치 종류 mian과 feature 브랜치만 사용
- main:항상 배포 가능 상태로 유지, main으로 병합 전에 충분한 test 필요
- feature:Git Flow와 달리 이외 브랜치들을 구분하지 않음,main에서 분기하여 작업 후 다시 main으로 병합, 브랜치의 목적을 이름에 잘 담아야 함,Git Flow에 비해 코드 리뷰가 더 중요함.
### 마음 가짐
- convention을 만들어 사용하자
- 모를 때 구글링을 꼼꼼히 하자
- 돌아가기만 하는 코드보다는 잘 설계된 코드를 짜도록 노력하자
- 질문을 잘 하자
