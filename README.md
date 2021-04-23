# 가사 찾기 알고리즘
-----------------------------------------------
  
### 풀이 과정  
  
풀이를 완료한 2020 카카오 코딩 테스트 문제 가장 삽질을 많이 하게 된 문제이다..  
해답 조건 중 효율성이 붙게 되면 출제자가 원하는 알고리즘이 아닌 이상 삽질을 피할 수 없다는 것을 뼈저리게 느끼는 과정이었다.  
우선 해당 문제의 요점은 Trie 알고리즘을 응용할 수 있는가 를 확인하는 게 요점이었던 것 같다.  
아직 트리라는 단어만 봐도 기피증이 오는 나는 어리석게도 Trie 알고리즘을 사용하지 않고 풀려고 했었다.  
그 결과는 하루 종일 삽질.. 또 삽질.. 그리고 결국 멘탈이 나가고 말았다.  
효율성 테스트의 테스트 케이스를 추측하고 예외 처리를 해나가며 더러워지는 코드를 애써 무시하면서까지 해봤지만 결국 풀 수 없었다.  
  
뒤늦게 " 아 이건 진짜 선형 자료구조로는 풀 수 없는 문제구나 " 를 깨닫고 울며 겨자 먹기로 Trie 자료구조를 파해하기 시작하니..  
10분 채 안되서 구조 파악을 해버린 후 허탈감만 잔뜩 느꼈다.  
" 아 이 쉬운 걸 왜 하려고 하질 않았지.. "  
이 생각만 5분은 했던 것 같다.
분노의 라면 먹방 이후 마음을 다 잡고 다시 초심으로 Trie 를 활용해 문제를 푸니..  
20분도 안되서 풀 수 있었다..  
물론 Trie 를 사용한다고 바로 풀리는 문제는 아니었고 만약 검색어 중 "fr???" 이라는 단어가 있다면
fr 로 시작하고 동일한 길이의 문자열을 모두 찾아서 그 개수를 확인하는 것이 이번 문제가 요구하는 답이었다.
이 개수를 어떻게 알 수 있을까? 를 좀 고민을 하게 되었다.  
동일한 길이의 문자열 같은 경우 map 을 사용해서 사전에 길이를 검사하여 key 에 등록한 후에 value 값으로 Trie 를 사용해서 간단하게 해결할 수 있었다.  
이제 문제는 fr 로 시작하는 단어를 어떻게 찾고, 그 개수를 어떻게 확인하는가? 만 남았고,
" 이거 그냥 와일드 문자 바로 전 노드의 자식 노드들의 마지막 노드 개수를 카운팅하면 되는 거 아닌가? "  
라는 생각이 들어서 그렇게 설계를 했더니 정말 시원하게 정확성,효율성 모두 정답 처리가 되며 풀 수 있었다.  
  
### 깨달은 점
  
제발 지뢰 겁먹지 말자 와 똥고집을 부리지 말자.  
딱 이 두 생각이 제일 크게 들었던 것 같다.  
만약 트리를 쓰지 않고 풀겠다는 고집을 좀 더 빨리 꺾었다면 시간이 훨씬 절약할 수 있었을텐데..  
그래도 마지막에 시원하게 뚫리는 테스트 케이스들을 보고 희열을 느낀 것을 보면 역시 프로그래밍은 이 맛에 하는 것이란 걸 다시금 깨달았다.  
