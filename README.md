# 'mapper' 연결문제 발생

> 원인 WriteDAO.xml에서 33번째줄 경로 잘못 기제
```xml
<select id="selectByUid" resultType="com.lec.spring.WriteDTO">
==> <select id="selectByUid" resultType="com.lec.spring.domain.WriteDTO">
```

# '신규등록'시 작성자를 생략해도 등록되는 증상 발생
> 원인 Write.jsp에서 28번째 줄에 return false 생략
```jsp
return false; // 28번째줄에 추가
```

# '삭제'시 uid를 못 찾고 오류 발생
> 원인 WriteDAO.xml에서 60번째줄 uid 잘못 입력
```xml
WHERE uid = #{uid} ==> WHERE wr_uid = #{uid}
```