# PYTHON-CODE-Prime-and-Even-Numbers
#Program for showing Prime and Even numbers between two given values

class Numbers:
    def __init__(self, min_num, max_num):
        self.min = min_num
        self.max = max_num

    def even_nums(self):
        even_nums_array = []
        for n in range(self.min, self.max + 1):
            if n % 2 == 0:
                even_nums_array.append(n)
        print(even_nums_array)

    def prime_nums(self):
        prime_nums_array = []
        for num in range(self.min, self.max + 1):
            if num > 1:
                for i in range(2, num):
                    if (num % i) == 0:
                        break
                else:
                    prime_nums_array.append(num)
        print(prime_nums_array)


min_num = int(input("min no: "))
max_num = int(input("max no: "))
check = Numbers(min_num, max_num)
print(f"Even numbers between {min_num} and {max_num} are", end=' ')
check.even_nums()
print(f"Prime numbers between {min_num} and {max_num} are", end=' ')
check.prime_nums()
