# git rebase

> 다른 브랜치 위에 있는 커밋을 다시 적용합니다.
> 주로 전체 브랜치를 다른 기저로 "이동"하여 새 위치에 커밋의 복사본을 만들 때 사용됩니다.
> 더 많은 정보: <https://git-scm.com/docs/git-rebase>.

- 현재 브랜치를 다른 지정된 브랜치 위에 리베이스:

`git rebase {{새_기저_브랜치}}`

- 커밋을 재배치, 생략, 결합 또는 수정할 수 있도록 하는 대화형 리베이스 시작:

`git rebase {{[-i|--interactive]}} {{대상_기저_브랜치_또는_커밋_해시}}`

- 충돌하는 파일 편집 후, 병합 실패로 중단된 리베이스 계속하기:

`git rebase --continue`

- 충돌이 발생한 커밋을 건너뛸 때, 병합 충돌로 일시 중지된 리베이스를 건너뛰어서 계속하기:

`git rebase --skip`

- 진행 중인 리베이스 중단 (예: 병합 충돌로 인해 중단된 경우):

`git rebase --abort`

- 시작할 수 있는 오래된 베이스 제공 및 현재 브랜치 일부를 새 베이스로 이동:

`git rebase --onto {{새_기저}} {{이전_기저}}`

- 마지막 5개의 커밋을 그대로 다시 적용해, 재배치, 생략, 결합 또는 수정할 수 있도록 멈추기:

`git rebase {{[-i|--interactive]}} {{HEAD~5}}`

- 작업 브랜치 버전을 우선하는 방식으로 모든 충돌을 자동으로 해결 (`theirs` 키워드는 이 경우 반대 의미를 갖습니다):

`git rebase {{[-X|--strategy-option]}} theirs {{브랜치_이름}}`
