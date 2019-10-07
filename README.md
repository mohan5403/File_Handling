# File_Handling
# Basic Reading and Write Operations on File Handling
# write single line in file
'''f=open('LICENSE1.txt','a')
f.write('mohan1\n')
f.write('mohan sarma1\n')
print('Is Writable :',f.writable())
print('Data written sucessfully')
f.close()'''

# Write group of lines
'''
f=open('LICENSE1.txt','a')
list = ['mohan\n', 'mohan1\n', 'mohan2\n', 'mohan3\n']
f.writelines(list)
print('Data written sucessfully')
f.close()
'''

# Reading character data from file :
       # f.read()
       # f.read(n) => To read 'n' characters from file
       # f.readline() => To read only one line
       # f.readlines() => To read all line
'''
f = open('LICENSE1.txt', 'r')
data1 = f.readline()
print(data1,'\n')
data2 = f.readline()
print(data2,'\n')
data3 = f.readlines() # used to write in list
print(data3)
data4 = f.read()      # used to write as in the file
print(data4)
f.close()

f=open('LICENSE1.txt', 'r')
lines = f.readlines()
for line in lines :
    print(line)
f.close()   
'''

# with Statements :
        # f.close() is not requried by using with statements
'''
f1=open('LICENSE1.txt', 'r')
f2=open('LICENSE2.txt', 'w')
f2.write(f1.read())
f1.close()
f2.close()
print('File stored sucessfully')
'''

with open('LICENSE2.txt', 'w') as f :
    f.write('with statements\n')
    f.write('with statements1\n')
    try :
        print(10/0)
    except ZeroDivisionError:
        print('Zero Division Error')
    print('Is closed : ', f.closed)
print('Is closed : ', f.closed)  
