# sun-core
hello world
#include<stdio.h>
void main()
{
	double a, b, c,x0,x1;
	printf("请输入系数a,b,c：");
	scanf_s("%lf%lf%lf", &a, &b, &c);
	if (b * b - 4 * a * c < 0)
		printf("该方程无实数解");
	else
	{
		printf("请输入一个近似解：");
		scanf_s("%lf", &x0);
			x1 = x0 - (a * x0 * x0 + b * x0 + c) / (2 * a * x0 + b );
			while (fabs(x1 - x0) >= 1e-6)
			{
				x0 = x1;
				x1 = x0 - (a * x0 * x0 + b * x0 + c) / (2 * a * x0 + b );
		}
			printf("该方程的一个近似解为：%lf", x1);
	}
}
