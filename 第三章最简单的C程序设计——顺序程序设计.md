#### 例3.1 ℉转化为℃

```c
#include <stdio.h>
int main() {
    double f = 0;
    printf("请输入您要转换的℉ :\n");
    scanf("%lf", &f);
    double c = (5.0 / 9) * (f - 32);
    printf("%.2lf ℉ = %.2lf ℃\n", f, c);
    return 0;
}
```

#### 例3.2 计算存款利息

```c
#include <stdio.h>
int main() {
    float p = 1000, p1, p2, p3;
    float r1 = 0.0036, r2 = 0.0225, r3 = 0.0198;
    p1 = p * (1 + r1);
    p2 = p * (1 + r2);
    p3 = p * (1 + r3 / 2) * (1 + r3 / 2);
    printf("p1 = %f\n", p1);
    printf("p2 = %f\n", p2);
    printf("p3 = %f\n", p3);
    return 0;
}
```

#### 例3.3 给定一个大写字母,用小写字母输出

```c
#include <stdio.h>
int main() {
    puts("请输入一个大写字母");	//这里用puts就不用\n了
    char a = getchar();
    if (a >= 'A' && a <= 'Z') {
        a += 32;
        printf("%c", a);
    } else
        puts("输入错误!");
    return 0;
}
```

#### 例3.4 给出三角形三边长,求三角形面积

```c
#include <math.h>
#include <stdio.h>
int main() {
    float a = 0, b = 0, c = 0;
    float S = 0;
    puts("请输入三角形三边长:");
    scanf("%f%f%f", &a, &b, &c);
    float p = (a + b + c) / 2;
    S = sqrt(p * (p - a) * (p - b) * (p - c));
    printf("%.2f", S);
    return 0;
}
```

#### 例3.5 求 ax²+bx+c=0 的根

```c
#include <math.h>
#include <stdio.h>
int main() {
    double a, b, c, x1, x2, DT;		//DT = Δ
    puts("请输入一元二次方程a,b,c 三个系数的值:");
    scanf("%lf%lf%lf", &a, &b, &c);
    DT = sqrt(b * b - (4 * a * c));
    if (DT >= 0) {
        x1 = (-b + DT) / 2 * a;
        x2 = (-b - DT) / 2 * a;
        printf("x1 = %.2lf x2 = %.2lf", x1, x2);
    } else
        puts("无实根");
    return 0;
}
```

#### 1.假如我国国民生产总值的年增长率为7%,计算10年后我国国民生产增长总值与现在比增长多少百分比 计算公式为 p=(1+r)^n

```c
#include <math.h>
#include <stdio.h>
int main() {
    double p, r = 0.07;
    p = pow(1 + r, 10);		// pow() 求m的n次方
    printf("%lf", p);
    return 0;
}
```

2.

```c
#include <math.h>
#include <stdio.h>
int main() {
    double r0 = 0.0035;
    double r1 = 0.015;
    double r2 = 0.021;
    double r3 = 0.0275;
    double r5 = 0.03;
    double p = 1000;
    double p1, p2, p3, p4, p5;
    p1 = p * (1 + 5 * r5);
    p2 = p * (1 + 2 * r2) * (1 + 3 * r3);
    p3 = p * (1 + 3 * r3) * (1 + 2 * r2);
    p4 = p * pow(1 + r1, 5);
    p5 = p * pow(1 + r0 / 4, 4 * 5);
    printf("%lf\n", p1);
    printf("%lf\n", p2);
    printf("%lf\n", p3);
    printf("%lf\n", p4);
    printf("%lf\n", p5);
    return 0;
}
```

3.

```c
#include <math.h>
#include <stdio.h>
int main() {
    int d = 300000;
    int p = 6000;
    float r = 0.01;
    float m = log10(p / (p - d * r)) / log10(1 + r);
    printf("%.1f", m);
    return 0;
}
```

6.

```c
#include <stdio.h>
int main() {
    char c1 = 'C', c2 = 'h', c3 = 'i', c4 = 'n', c5 = 'a';
    c1 += 4;
    c2 += 4;
    c3 += 4;
    c4 += 4;
    c5 += 4;
    printf("%c%c%c%c%c", c1, c2, c3, c4, c5);
    return 0;
}
```

7.

```c
#include <math.h>
#include <stdio.h>
#define PI 3.1415926;
int main() {
    float r, h;
    float Ly, Sy, Sq, Vq, Vz;
    puts("请输入圆的半径r,圆柱高h:");
    scanf("%f%f", &r, &h);
    Ly = 2 * r * PI;
    Sy = r * r * PI;
    Sq = 4 * r * r * PI;
    Vq = 4 / 3 * (r * r * r) * PI;	// 这个地方书上貌似是不对的,我查阅了资料 Vq = 4/3Πr³
    Vz = Sy * h;
    printf("圆的周长= %.2f\n", Ly);
    printf("圆的面积= %.2f\n", Sy);
    printf("圆球的表面积= %.2f\n", Sq);
    printf("圆圆球的体积= %.2f\n", Vq);
    printf("圆圆柱的体积= %.2f\n", Vz);
    return 0;
}
```

