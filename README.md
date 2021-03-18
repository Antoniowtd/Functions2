# Functions2
Functions2
### ex01.c:
### 1

#include <stdio.h>
 
void main()
{
    int num1, num2, num3;
 
    printf("Enter the values of number 1, number 2 and number 3\n");
    scanf("%d %d %d", &num1, &num2, &num3);
    printf("num1 = %d\tnum2 = %d\tnum3 = %d\n", num1, num2, num3);
    if (num1 > num2)
    {
        if (num1 > num3)
        {
            printf("%d is the greatest \n", num1);
        }
        else
        {
            printf("%d is the greatest \n", num3);
        }
    }
    else if (num2 > num3)
        printf("%d is the greatest \n", num2);
    else
        printf("%d is the greatest \n", num3);
}

### 2

#include <stdio.h>

void main()
{
    int num1, num2, num3;
    int s;
    printf("Enter the values of number 1, number 2 and number 3\n");
    scanf("%d %d %d", &num1, &num2, &num3);
    s = num1+num2+num3;
    printf("The sum is %d", s);
}

### 3

#include <stdio.h>

void main()
{
    int num1, num2, num3;
    int s;
    printf("Enter the values of number 1, number 2 and number 3\n");
    scanf("%d %d %d", &num1, &num2, &num3);
    s = num1*num2*num3;
    printf("The multiplication of the numbers is %d", s);
}

### 4

#include <stdio.h>
int main()
{
  char str[1000], rev[1000];
  int i, j, count = 0;
  scanf("%s", str);
  printf("\nString Before Reverse: %s", str);
 
  while (str[count] != '\0')
  {
    count++;
  }
  j = count - 1;


  for (i = 0; i < count; i++)
  {
    rev[i] = str[j];
    j--;
  }

  printf("\nString After Reverse: %s", rev);
}

### 5

#include <stdio.h>
 
int main()
{
  int c, n, f = 1;
 
  printf("Enter a number\n");
  scanf("%d", &n);
  for (c = 1; c <= n; c++)
    f = f * c;
 
  printf("Factorial of %d = %d\n", n, f);
 
  return 0;
}

### 6

#include<stdio.h>
 
int main() {
    int num, min, max;
     
    printf("Enter an integer\n");
    scanf("%d", &num);
    printf("Enter the minimum and maximum range\n");
    scanf("%d %d", &min, &max);
     
    if((num-min)*(num-max) <= 0){
        printf("%d is in range of [%d, %d]", num, min, max);
    } else {
     printf("%d is not in range of [%d, %d]", num, min, max);
    }
 
    return 0;
}

### 7

#include <stdio.h>

int main()
{
    char str[30];
    int countL,countU;
    int counter;
 
    countL=countU=0;
 
    printf("Enter a string: ");
    gets(str);
 
    for(counter=0;str[counter]!=NULL;counter++){
 
        if(str[counter]>='A' && str[counter]<='Z')
            countU++;
        else if(str[counter]>='a' && str[counter]<='z')
            countL++;   
    }
 
    printf("The total Upper case characters is %d" ,countU);
    printf(" and the ");
    printf("total Lower Case characters is %d", countL);
 
    return 0;
}

### 8

#include <stdio.h>
int main()
{
    int a[10000],b[10000],i,j,n,c=0 ;
    printf("Enter size of the array : ");
    scanf("%d", &n);
    printf("Enter elements in array : ");
    for(i=0; i<n; i++)
    {
        scanf("%d",&a[i]);
    }
  for(i=0; i<n; i++)
    {
        c=1;
        if(a[i]!=-1)
		{
		    for(j=i+1; j<n; j++)
            {
        	   if(a[i]==a[j])
        	    {
			       c++;
			       a[j]=-1;
		       }
	       }
	       b[i]=c;
		}
    }
            printf("unique numbers in the  array :\n");
 for(i=0; i<n; i++)
    {
         if(a[i]!=-1)
        {
        	if(b[i]==1)
        	printf("%d\n",a[i]);
		} 
    }    
    return 0;
} 

### 9

#include<stdio.h>
int PrimeOrNot(int);
int main()
{
    int n1,prime;
    printf(" Input a positive number : ");
    scanf("%d",&n1);
    prime = PrimeOrNot(n1);
   if(prime==1)
        printf(" The number %d is a prime number.\n",n1);
   else
      printf(" The number %d is not a prime number.\n",n1);
   return 0;
}
int PrimeOrNot(int n1)
{
    int i=2;
    while(i<=n1/2)
    {
         if(n1%i==0)
             return 0;
         else
             i++;
    }
    return 1;
}

### 10

#include <stdio.h>
print(int *a,int n)
 { 
    int i;
    for(i=0; i<n; i++)
    {
        	printf("%d  ",a[i]);	 
    }
 }
  
 
int main()
{
    int a[10000],b[10000],c[20000],i,j,k,n1,n2,n ;
   
    printf("Enter size of the  array : ");
    scanf("%d", &n);
    printf("Enter elements in array : ");
    for(i=0; i<n; i++)
    {
        scanf("%d",&a[i]);
    }
     printf("\n original array  \n");
 
    print(a,n);
    j=k=0;
    for(i=0; i<n; i++)
    {
        if(a[i]%2==0)
          b[j++]=a[i];
        else
          c[k++]=a[i];
    }
    printf(" \n even array \n");
    print(b,j);
    return 0;
} 

### 11

#include<stdio.h>  

void main()  
{  
// declare and initialize the variables  
int num, rem, sum = 0, i;  
// take an input from the user.  
printf("Enter a number\n");  
scanf("%d", &num);      
// find all divisors and add them  
for(i = 1; i < num; i++)  
                     {  
                              rem = num % i;  
                             if (rem == 0)  
                                        {  
                                               sum = sum + i;  
                                         }  
                        }  
if (sum == num)  
                      printf(" %d is a Perfect Number", num);  
           else  
                      printf("\n %d is not a Perfect Number", num); 
    return 0;
}  

### 12

#include <stdio.h> 
#include <string.h> 

void isPalindrome(char str[]) 
{ 
    int l = 0; 
    int h = strlen(str) - 1; 
    while (h > l) 
    { 
        if (str[l++] != str[h--]) 
        { 
            printf("%s is Not Palindrome", str); 
            return; 
        } 
    } 
    printf("%s is palindrome", str); 
} 

int main() 
{ 
    isPalindrome("ala"); 
    return 0; 
}

### ex01.py:
### 1

def max_of_two( x, y ):
    if x > y:
        return x
    return y
def max_of_three( x, y, z ):
    return max_of_two( x, max_of_two( y, z ) )
print(max_of_three(7, 8, 9))

### 2

def sum(numbers):
    total = 0
    for x in numbers:
        total += x
    return total
print(sum((1, 2, 3, 4, 5)))

### 3

def multiply(numbers):  
    total = 1
    for x in numbers:
        total *= x  
    return total  
print(multiply((1, 2, 3, 4, 5)))

### 4

def string_reverse(str1):

    rstr1 = ''
    index = len(str1)
    while index > 0:
        rstr1 += str1[ index - 1 ]
        index = index - 1
    return rstr1
print(string_reverse('ala'))

### 5

def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)
n=int(input("Input a number to compute the factiorial : "))
print(factorial(n))

### 6

def test_range(n):
    if n in range(1,10):
        print( " %s is in the range"%str(n))
    else :
        print("The number is outside the given range.")
test_range(5)

### 7

def string_test(s):
    d={"UPPER_CASE":0, "LOWER_CASE":0}
    for c in s:
        if c.isupper():
           d["UPPER_CASE"]+=1
        elif c.islower():
           d["LOWER_CASE"]+=1
        else:
           pass
    print ("Original String : ", s)
    print ("No. of Upper case characters : ", d["UPPER_CASE"])
    print ("No. of Lower case Characters : ", d["LOWER_CASE"])

string_test('He Is Ok')

### 8

def unique_list(l):
  x = []
  for a in l:
    if a not in x:
      x.append(a)
  return x

print(unique_list([1,2,3,4,5,6,7,8,8,8,8,8,8,9])) 

### 9

def test_prime(n):
    if (n==1):
        return False
    elif (n==2):
        return True;
    else:
        for x in range(2,n):
            if(n % x==0):
                return False
        return True             
print(test_prime(7))

### 10

def is_even_num(l):
    enum = []
    for n in l:
        if n % 2 == 0:
            enum.append(n)
    return enum
print(is_even_num([1, 2, 3, 4, 5, 6, 7, 8, 9]))
 

### 11

def perfect_number(n):
    sum = 0
    for x in range(1, n):
        if n % x == 0:
            sum += x
    return sum == n
print(perfect_number(45))

### 12

def isPalindrome(string):
	left_pos = 0
	right_pos = len(string) - 1
	
	while right_pos >= left_pos:
		if not string[left_pos] == string[right_pos]:
			return False
		left_pos += 1
		right_pos -= 1
	return True
print(isPalindrome('reconocer')) 
