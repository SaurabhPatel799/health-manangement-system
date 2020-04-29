# OPEN HEART SURGERY PATIENT LOG BOOK
import datetime
def gettime():
    return datetime.datetime.now()

def take(k):
    c = int(input("Enter 1 for BREAKFAST , 2 for LUNCH , 3 for SNACKS , 4 for DINNER , 5 for BP MEASUREMENT "
                  " 6 for DIABETES MEASUREMENT , 7 for QUANITY OF ML URINE IN A DAY \n"))
    if c==1:
        value = input("Type here \n")
        with open("patient-breakfast.txt","a") as op:
            op.write(str([str(gettime())]) + ":" + value + "\n")
            print("Breakfast added successfully")
    elif c==2:
        value = input("Type here \n")
        with open("patient-lunch.txt","a") as op:
            op.write(str([str(gettime())]) + ":" + value + "\n")
            print("Lunch added successfully")
    elif c==3:
        value = input("Type here \n")
        with open("patient-snacks.txt","a") as op:
            op.write(str([str(gettime())]) + ":" + value + "\n")
            print("Snacks added successfully")
    elif c==4:
        value = input("Type here \n")
        with open("patient-dinner.txt","a") as op:
            op.write(str([str(gettime())]) + ":" + value + "\n")
            print("Dinner added successfully")
    elif c==5:
        value = input("Type here \n")
        with open("patient-bpmeasurement.txt","a") as op:
            op.write(str([str(gettime())]) + ":" + value + "\n")
            print("BP MEASUREMENT added successfully")
    elif c==6:
        value = input("Type here \n")
        with open("patient-diabetesmeasurement.txt","a") as op:
            op.write(str([str(gettime())]) + ":" + value + "\n")
            print("DIABETES MEASUREMENT added successfully")
    elif c==7:
        value = input("Type here \n")
        with open("patient-urinequantity.txt","a") as op:
            op.write(str([str(gettime())]) + ":" + value + "\n")
            print("URINE QUANTITY added successfully")
    else:
        print("Please select correct choice: \n")
def retrieve(k):
    c = int(input("Enter 1 for BREAKFAST , 2 for LUNCH , 3 for SNACKS , 4 for DINNER , 5 for BP MEASUREMENT "
                  " 6 for DIABETES MEASUREMENT , 7 for QUANITY OF ML URINE IN A DAY \n" ))
    if c==1:
        with open("patient-breakfast.txt") as op:
            for i in op:
                print(i,end="")
    elif c==2:
        with open("patient-lunch.txt") as op:
            for i in op:
                print(i,end="")
    elif c==3:
        with open("patient-snacks.txt") as op:
            for i in op:
                print(i,end="")
    elif c==4:
        with open("patient-dinner.txt") as op:
            for i in op:
                print(i,end="")
    elif c==5:
        with open("patient-bpmeasurement.txt") as op:
            for i in op:
                print(i, end="")
    elif c==6:
        with open("patient-diabetesmeasurement.txt") as op:
            for i in op:
                print(i, end="")
    elif c==7:
        with open("patient-urinequantity.txt") as op:
            for i in op:
                print(i, end="")
    else:
        print("Please select correct choice")

print("OPEN HEART SURGERY PATIENT LOG BOOK")
ch = input("Please enter patient name")
k = int(input("Enter 1 for log and 2 for Retrieve: \n"))
if k==1:
    take(k)
elif k==2:
    retrieve(k)
else:
    print("please enter correct option")
