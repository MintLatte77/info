# 정보 수행평가

### 삼각형의 넓이를 구하고, 이를 소숫점 아래 3자리까지 표현하시오.

```c
#include <stdio.h>
main(){
	float a, b; //int 선언하면 안됨!! 밑변 길이 입력하자마자 튕김 
	printf("밑변의 길이 : "); //여기에 \n 넣는 애들 많은데 가급적이면 X (예시1 참고) 
	scanf("%f", &a); // float로 선언했으니 %f 적고 뒤에는 변수 선언 & 붙여서!! 
	printf("높이 : "); //위에랑 똑같음 
	scanf("%f", &b);
	printf("넓이 : %.3f\n", a*b/2.0); // 소숫점 아래 3자리니 %.3f 특히 .이나 숫자 헷갈리지 말고 뒤에 나누는 부분 /2 써도 되는데 안전빵으로 /2.0 추천 
} // 꼭 중괄호 닫으시고 세미콜론 안적은거 있는지 확인!! 
```

#### 예시1

```c
#include <stdio.h>
main(){
	float a, b;
	printf("밑변의 길이 : \n"); 
	scanf("%f", &a);
	printf("높이 : \n");
	scanf("%f", &b);
	printf("넓이 : %.3f\n", a*b/2.0);
}
```

로 실행하면

<div align="left">

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

</div>

이런 식으로 입력받아서 보기 안좋음 그래서 \n은 마지막 줄에만 적으세요

### 직사각형의 넓이를 구하고, 이를 소숫점 아래 3자리까지 표현하시오.

```c
#include <stdio.h>
main(){
	float a, b; //무조건 float!! int로 받으면 넓이 구할때 오류남 
	printf("밑변의 길이 : "); 
	scanf("%f", &a);
	printf("높이 : ");
	scanf("%f", &b);
	printf("넓이 : %.3f\n", a*b);
}
```

### 원의 넓이를 구하고, 이를 소숫점 아래 3자리까지 표현하시오. (단, 원주율은 3.14로 한다)

```c
#include <stdio.h>
main(){
	float a; //int해도 되긴 한데 정수형으로 받으란 얘기 없으면 float로 적는게 나음 
	printf("반지름 : "); 
	scanf("%f", &a);
	printf("넓이 : %.3f", a*a*3.14); //혹시 반지름 다른 숫자로 제시되어 있을 수 있으니 꼭 확인!! 
}
```
