# mwp-korean-data
[한글 서술형 수학문제 데이터셋] 공개저장소 입니다.    



## 1. 데이터 구성
총 3,000개의 한국어 수학 문제와 답으로 구성되어 있습니다. 각 데이터는 8개의 유형로 구분되며,    
유형의 종류와 유형 별 문제 수는 아래와 같습니다.


| 산술연산 | 순서정하기 | 조합하기 | 수찾기1 | 수찾기2 | 수찾기3 | 크기비교 | 도형서술 | 총 문제 수 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 375 | 375 | 375 | 375 | 375 | 375 | 375 | 375 | **3,000** |


* 산술연산의 경우 사칙연산(+, -, *, /)이 포함된 수식(equation)이 데이터에 포함됩니다. 이외 유형은 수식(key)에 해당하는 값(value)는 "none"입니다.
     
     
     
## 2. 유형별 문제 예시

데이터는 JSON으로 작성하였으며, 데이터 구조 및 각 유형별 예시는 다음과 같습니다.

- 데이터 포맷
```
{
    문제 번호 (타입: 문자열): {
        "class": "문제 유형" (타입: 문자열),
        "question": "문제" (타입: 문자열),
        "answer" : "답" (타입: 문자열),
        "equation": "수식" (타입: 문자열)
    },
    
    .
    .
    .

    문제 번호 (타입: 문자열): {
        "class": "문제 유형" (타입: 문자열),
        "question": "문제" (타입: 문자열),
        "answer" : "답" (타입: 문자열),
		"equation" : "none" (타입: 문자열)
    },

}
```
- 유형별 예시
```
{   
	"1": {
		"class": "산술연산",
		"question": "송화는 친구 9명에게 붙임 딱지를 3장씩 주었습니다. 송화가 친구에게 준 붙임 딱지는 모두 몇 장입니까?",
		"answer": "27",
		"equation": "9*3"
	},
    	"2": {
		"class": "순서정하기",
		"question": "올림픽 체조경기에서 1위부터 6위까지 미국, 러시아. 한국, 중국, 호주, 그리스순으로 순위가 결정됐습니다. 4위는 어느 국가입니까?",
		"answer": "중국",
		"equation": "none"
	},
    	"3": {
		"class": "조합하기",
		"question": "어느 의류가게에는 8종류의 상의, 4종류의 하의, 3종류의 양말이 있다. 이 의류 가게에서 상의, 하의와 양말을 각각 하나씩 고르는 경우의 수를 구하시오",
		"answer": "96",
		"equation": "none"
	},
    	"4": {
		"class": "수찾기1",
		"question": "민주는 화단 왼쪽 끝에서부터 튤립은 6m 간격으로, 해바라기는 8m 간격으로 심으려고 합니다. 튤립과 해바라기가 처음으로 같이 심어지는 곳은 시작지점으로부터 몇 m 떨어진 곳입니까?",
		"answer": "24",
		"equation": "none"
	},
    	"5": {
		"class": "수찾기2",
		"question": "한 엘레베이터 당 탈 수 있는 인원은 A3명 입니다. 총 B대의 엘레베이터가 있을 때, 탈 수 있는 인원이 92명이라면, 이를 만족하는 A,B의 합은 무엇입니까?",
		"answer": "6",
		"equation": "none"
	},
    	"6": {
		"class": "수찾기3",
		"question": "정훈이는 35를 빼야하는 어떤 수를 잘못보고 25를 뺐더니 43이 되었습니다. 바르게 계산한 결과를 구하시오.",
		"answer": "33",
		"equation": "none"
	},
    	"7": {
		"class": "크기비교",
		"question": "호준이는 딱지를 145장, 지현이는 딱지를 134장, 양원이는 122장을 가지고 있습니다. 딱지를 더 적게 가지고 있는 사람은 누구입니까?",
		"answer": "지현",
		"equation": "none"
	},
    	"8": {
		"class": "도형산술",
		"question": "철사로 한 모서리의 길이가 8cm인 정육각형을 만들려고 합니다. 철사는 적어도 몇 cm가 필요합니까?",
		"answer": "48",
		"equation": "none"
	}
}
```



## 3. 지원
이 연구개발은 2021년도 정부(과학기술정보통신부)의 재원으로 정보통신기획평가원의 지원을 받아 수행한 연구 성과물의 일부입니다.
해당 연구과제에 대한 정보는 아래와 같습니다.
- 과제번호: 2021-0-02152
- 연구사업명: 인공지능산업원천기술개발
- 연구과제명: 서술형 수학문제 해결 인공지능 알고리즘 개발
- 주관연구기관: 한국원자력연구원 (인공지능응용전략실) 
- 공동연구기관: 주식회사 젠티
- 연구참여자: 유용균, 전태현, 고태영, 임소영, 임지연, 조희철, 허태일, 최은진, 기태경, 정지영



## 4. 데이터셋 구축 방법
저희가 공개한 한글 서술형 수학문제 데이터셋은 아래와 같이 크게 2가지의 방법으로 구축하였습니다.
- (주)셀렉트스타가 수행한 서술형 수학문제 구축 용역을 통해 구축된 데이터의 일부
- 연구참여자가 자체 구축한 데이터 일부   


