#include <stdio.h>
#include <math.h>
int main(){
    int a, b, c;
    scanf("%d%d%d", &a, &b, &c);
    
    
	if (a == 0)
	{
		if (b == 0)
		{
			if (c== 0)
			{
				printf("INF");
			}
			else
			{
				printf("NO"); 
			}
		}
        else
		{
			
			if(c == 0){
                printf("NO");
            }
            else{
               float x = (float)-b / c;
                printf("%.2f", x);
            }
		}
	}
    else
	{
        if(c == 0){
            printf("NO");
        }
        else
        {
            float delta = (float)(b * b) - (4 * a * c);
		if (delta < 0)
		{
			printf("NO");
		}
		else if (delta == 0)
		{
			float x = (float)-b / (2 * a);
			printf("%.2f", x);
		}
		else
		{
         printf("%.2f %.2f\n",(float)(-b - sqrt(delta)) / (2 * a), (float)(-b + sqrt(delta)) / (2 * a));
		}
       }
	}
    return 0;
}
