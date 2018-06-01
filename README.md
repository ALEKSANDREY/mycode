<h1> Birthday Problem <h1>

'''Birthday problem
June 1 2018'''

import random

NUM_PEOPLE = 30

def trial():
    birthday_list = []

    for i in range(NUM_PEOPLE):
        birthday_list.append(random.randint(1,365))

    print(birthday_list)

    for n in birthday_list:
        countN = birthday_list.count(n)
        if countN > 1:
          #print(n, countN)
            return True
    return False

successes = 0
trials = 1100

for i in range(trials):
    if trial()== True:
        successes +=1

print(successes / trials)
