# 3진법 뒤집기

def solution(n):
    answer = []
    result = 0
    while n > 0:
        n, mod = divmod(n, 3)
        answer.append(mod)

    answer.reverse()
    
    for i in range(len(answer)):
        result += answer[i] * (3 ** i)

    return result

# print(solution(45))
#ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

def solution(n):
    tmp = ''
    while n:
        tmp += str(n % 3)
        print('tmp',tmp)
        n = n // 3
        print('n',n)

    answer = int(tmp, 4)
    return answer
