## Heres a random block of code from one of my IT1040 (python)


``` py
def get_highway_number():
    valid = False
    while not valid:
        n = int(input("Please enter a highway number (1 to 999): "))
        if n > 0 and n < 1000:
            if n < 100:
                valid = True
            else:
                if n % 100 != 0:
                    valid = True
        if not valid:
            print(n, "is not a valid highway number. Try again.")
    return n

def print_highway_info(n):
    info = input("What would you like to know about the highway (type or direction)? ")
    while info != "type" and info != "direction":
        print("Wrong command. Try again.")
        info = input("What would you like to know about the highway (type or direction)? ")
    if info == "type":
        if n < 100:
            print("I-" + str(n) + " is a primary highway.")
        else:
            serving = n % 100
            print("I-" + str(n) + " is an auxiliary highway, serving I-" + str(serving) + ".")
    else:
        if n % 2 == 1:
            print("I-" + str(n) + " goes north/south.")
        else:
            print("I-" + str(n) + " goes east/west.")

if __name__ == "__main__":
    n = get_highway_number()
    print_highway_info(n)
```


[BACK](https://github.com/parth122p/IT1400MidtermProject2023/blob/a86b2aafc9b5f5f4a8cb8ff332311c502d6760ea/README.md)