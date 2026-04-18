# Python
Coding
# ___________Number Ones____________
def ones(x):
    if x == 0:
        return "Zero"
    elif x == 1:
        return "One"
    elif x == 2:
        return "Two"
    elif x == 3:
        return "Three"
    elif x == 4:
        return "Four"
    elif x == 5:
        return "Five"
    elif x == 6:
        return "Six"
    elif x == 7:
        return "Seven"
    elif x == 8:
        return "Eight"
    elif x == 9:
        return "Nine"


# __________Number Tens____________
def tens(x):
    if x == 10:
        return "Ten"
    elif x == 11:
        return "Eleven"
    elif x == 12:
        return "Twelve"
    elif x == 13:
        return "Thirteen"
    elif x == 14:
        return "Fourteen"
    elif x == 15:
        return "Fifteen"
    elif x == 16:
        return "Sixteen"
    elif x == 17:
        return "Seventeen"
    elif x == 18:
        return "Eighteen"
    elif x == 19:
        return "Nineteen"
    else:
        t = x // 10
        o = x % 10

        if t == 2:
            word = "Twenty"
        elif t == 3:
            word = "Thirty"
        elif t == 4:
            word = "Forty"
        elif t == 5:
            word = "Fifty"
        elif t == 6:
            word = "Sixty"
        elif t == 7:
            word = "Seventy"
        elif t == 8:
            word = "Eighty"
        elif t == 9:
            word = "Ninety"

        if o == 0:
            return word
        else:
            return word + " " + ones(o)


# __________Number Hundreds________
def hundreds(x):
    h = x // 100
    r = x % 100

    if r == 0:
        return ones(h) + " Hundred"
    elif r < 10:
        return ones(h) + " Hundred " + ones(r)
    else:
        return ones(h) + " Hundred " + tens(r)


# __________Number Thousands_______
def thousands(x):
    if x == 1000:
        return "One Thousand"


# Main Program
num = int(input("Enter a number: "))

if num < 10:
    print(ones(num))
elif num < 100:
    print(tens(num))
elif num < 1000:
    print(hundreds(num))
elif num == 1000:
    print(thousands(num))
else:
    print("Number out of range")
