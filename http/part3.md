## HTTP api 만들기

### 요구사항 / API URI 설계
 - 회원 목록 조회 / read-member-list  -> get /member
 - 회원 조회 / read-member-by-id -> get /member/{id}
 - 회원 등록 / create-member - post /member/
 - 회원 수정 / update-member - update /member/{id}
 - 회원 삭제 / delete-member - delete /member/{id}

위의 설계가 정말 좋은 URI 설계일까? (왼쪽 read,create,update부분의 uri)
 - 가장 중요한 것은 리소스 식별 

### API URI 고민
 - 리소스의 의미
```
회읜을 등록하고 수정하고 조회하는게 리소스가 아님
회원이라는 개념 자체가 바로 리소스
```

 - 리소스를 어떻게 식별하는게 좋을까?
```
회원을 등록하고 수정하고 조회하는 것을 모두 배제
회원이라는 리소스만 식별하면 된다 -> 회원 리소스를 uri에 매핑
```

