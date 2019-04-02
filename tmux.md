# tmux명령어

- Ctrl+b "  
창이 가로로 나뉨

- Ctrl+b %  
창이 세로로 분할

- Ctrl+b d  
라고 하면 tmux 가 종료되는 것 처럼 보이지만 실제로는  
이전 상태를 유지하고 계속 실행되고 있이며

이를 동일 터미널 또는 다른 터미널에서

- $ tmux attach  
라고 하여 이전 실행되던 곳으로 돌아갈 수 있습니다.

- Ctrl+b q  
화면의 번호가 나온다

- Ctrl+b 화살표  
창이동을 할 수 있다.

- Ctrl+b PgUp  
- Ctrl+b PgDn  
키로 스크롤이 가능합니다.  
키로 스크롤을 했을 때는 q 로 끝내줘야 스크롤 모드가 끝납니다

- Ctrl+b c  
새로운 창을 만든다.

- Ctrl+d  
종료

- $ tmux ls  
tmux 세션을 볼 수 있다.

- $ tmux attach  
이전 세션 복원

- $ tmux attach -t 1  
해당세션을 볼 수 있다.