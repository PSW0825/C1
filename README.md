1. union의 예제를 하나 만들고 설명하시오.
#include <stdio.h>



// Union 정의

union Data {

    int intValue;

    float floatValue;

    char stringValue[20];

};



int main() {

    union Data data;



    // 데이터 할당

    data.intValue = 42;



    // 멤버 접근 및 출력

    printf("정수값: %d\n", data.intValue);



    // 다른 멤버 할당 및 출력

    data.floatValue = 3.14;

    printf("부동소수점값: %.2f\n", data.floatValue);



    // 다시 다른 멤버 할당 및 출력

    strcpy(data.stringValue, "Hello, Union!");

    printf("문자열값: %s\n", data.stringValue);



    return 0;

}



이 예제에서는 'union Data'를 정의하고, 정수, 부동소수점 및 문자열을 저장하는 세가지 멤버를 갖는 'union'을 만듭니다. 프로그램에서는 먼저 정수 값을 할당하고 출력한 다음, 부동소수점  값과 문자열을 할당하고 출력합니다. 주의할 점은 'union'을 사용할 때 한 번에 하나의 멤버만 사용해야 한다는 것입니다. 'union'은 메모리를 공유하므로 주로 여러 데이터 형식 중 하나만 필요한 경우나, 다양한 데이터 형식을 사용하는 대신 메모리를 절약하고자 할 때 유용합니다.





2. enum 의 예제를 하나 만들고 설명하시오.

#include <stdio.h>



// 열거형 정의

enum Days {

    SUNDAY,    // 0

    MONDAY,    // 1

    TUESDAY,   // 2

    WEDNESDAY, // 3

    THURSDAY,  // 4

    FRIDAY,    // 5

    SATURDAY   // 6

};



int main() {

    // 열거형 변수 선언 및 초기화

    enum Days today = WEDNESDAY;



    // 열거형 상수 사용

    if (today == WEDNESDAY) {

        printf("오늘은 수요일입니다.\n");

    } else {

        printf("오늘은 수요일이 아닙니다.\n");

    }



    // 열거형 상수를 배열 인덱스로 사용

    const char* daysOfWeek[] = {

        "일요일", "월요일", "화요일", "수요일", "목요일", "금요일", "토요일"

    };



    printf("오늘은 %s입니다.\n", daysOfWeek[today]);



    return 0;

}



이 예제에서는 'enum Days'를 정의하여 일주일의 요일을 나타냅니다. 각 상수에는 기본적으로 0부터 시작하는 정수 값이 할당됩니다. 'enum' 변수 'today'를 선언하고 'WEDNESDAY'로 초기화한 후, 'if' 문을 사용하여 오늘이 수요일인지 확인합니다. 또한, 'daysOfweek' 라는 문자열 배열을 사용하여 열거형 상수를 요일의 이름으로 변환합니다. 이렇게 하면 열거형 상수를 사용하며 요일의 인덱스로 사용할 수 있습니다. 'enum'은 코드를 읽기 쉽게 만들어주며, 관련된 상수를 그룹화하여 사용할 때 유용합니다. 열거형을 사용하면 의미 있는 이름을 부여하고, 코드를 이해하기 쉽게  만들 수 있습니다.
