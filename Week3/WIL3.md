### HEAD
-HEAD는 현재 작업 중인 위치를 가르킨다. 현재 작업중인 브랜치의 가장 최근 commit,다음 commit의 base가 되는 commit,새로운 commit이 생기면 HEAD도 변겨
#### commit --amned
-마지막 commit의 내용에 변경이 있을 때 사용,완전히 새로운 commit으로 대체,commit id가 바뀜,vim으로 진입하여 commit 메시지를 수정하게 돤다.

-git commit --amend -m "커밋 메시지" <- '-m'option으로 vim 진입 없이 commit 메시지 수정함

-git commit --amend --no-edit<-commit 메시지 수정 없이 commit 수정

## reset
- commit을 제거하는데 사용 
-git reset '--option' "<commit id>"
- reset --soft
-커밋만 취소,변경 사항이 Staging Area로 돌아감
-reset --mixed
-커밋을 취소,변경 사항을 working directory로 돌아감
-reset --hard
-커밋을 취소,변경 사항을 모두 제거하고 이전 커밋으로 돌아감

## revert
-commit을 제거하지 않고 되돌림,되돌리기 위한 새로운 commit이 생성됨.

-git revert <커밋 id>
