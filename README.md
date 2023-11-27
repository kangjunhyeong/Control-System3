# Control-System3
  
![image](https://github.com/kangjunhyeong/Control-System3/assets/144297425/20b449b9-2477-4fc8-a6f3-1b7cad572972)  

![image](https://github.com/kangjunhyeong/Control-System3/assets/144297425/56ba09c0-6ed9-4ce5-85c6-d06fc16f61f3)  

(a)  

$$T(s) = \frac{\frac{G(s)k}{0.25s + 1}}{1 + \frac{G(s)k}{0.2s + 1}}$$  

G(s)를 넣고 정리하면  

$$T(s) = \frac{100k}{100k + (s^2 + 25s + 100)(0.2s + 1)} \ $$  
위 식을 편미분 해주면  

$$\frac{\partial T}{\partial k} = \frac{\partial}{\partial k} \left(\frac{100k}{100k + (s^2 + 25s + 100)(0.2s + 1)}\right)\$$

$$=\frac{100(s^2 + 25s + 100)(0.2s + 1)}{(100k + (s^2 + 25s + 100)(0.2s + 1))^2} \$$
  
$$\frac{k}{T} = \frac{100k + (s^2 + 25s + 100)(0.2s + 1)}{100} \$$

이제 S(s)를 구해주면  

$$\ S(s) = \frac{(s^2 + 25s + 100)(0.2s + 1)}{100k + (s^2 + 25s + 100)(0.2s + 1)} \$$  

(b)  

이제 R(s)=0이라 가정하고 외란이 출력에 미치는 영향을 구하면  

$$ \frac{Y(s)}{T_d(s)} = \frac{20s+100}{(0.2s+1)(s^2+25s+100)+100k} \$$  

(c)  

T_d(s)를 계단외란입력 A/s 라고 할 때 K의 범위를 찾으면  

$$Y(s) = \frac{A(20s+100)}{(0.2s+1)(s^2+25s+100)+100k} < 0.1 \$$
  
$$\ \lim_{{s \to 0}} Y(s) = \frac{100A}{100 + 100k} < 0.1 \$$  

$$\ k > 10A - 1 \$$  

![image](https://github.com/kangjunhyeong/Control-System3/assets/144297425/d6b28798-7c21-40a5-a195-9ba61784bf7f)  

$$\ T_1(s) = \frac{G(s)}{1 + G(s)H(s)} \$$  

$$\= \frac{K_1 \cdot K_2}{s^2 + 3s - 4 + 6K_1 \cdot K_2} \$$  

왼쪽 폐루프를 합치면  

$$\ G_1(s) = \frac{K_1}{s + 4 - 2K_1} \ $$  

오른쪽 폐루프를 합치면  

$$\ G_2(s) = \frac{K_2}{s - 1 + 2K_2} \ $$

$$\ T_2(s) = \frac{K_1 \cdot K_2}{s^2 + (3 - 2K_1 + 2K_2)s + (2K_1 + 8K_2 - 4K_1K_2 - 4)} \$$

$$\frac{\partial T_1(s)}{\partial K_1} = \frac{(s^2 + 3s - 4)K_2}{(s^2 + 3s - 4 + 6K_1K_2)^2}\$$  

$$\ S^{T_1}_{K_1} = \frac{s^2 + 3s - 4}{s^2 + 3s - 4 + 6K_1K_2} \$$  

K1=K2=1이므로  

$$\ S^{T_1}_{K_1} = \frac{s^2 + 3s - 4}{s^2 + 3s - 4 + 6} \$$  

$$\frac{\partial T_2(s)}{\partial K_1} = \ \frac{K_2(s^2 + 3s - 4) + 2K_2^2s + 8K_2^2}{(s^2 + 3s - 4 - 2K_1s + 2K_2s + 2K_1 + 8K_2 - 4K_1K_2)^2} \$$  

$$\ S^{T_2}_{K_1} = \frac{s^2 + 5s + 4}{s^2 + 3s + 2} \$$  

![image](https://github.com/kangjunhyeong/Control-System3/assets/144297425/48b668cf-eb38-4e1c-9225-52356ca8e9b8)  
![image](https://github.com/kangjunhyeong/Control-System3/assets/144297425/ae20f8de-5333-4322-99d8-46394f03ca8b)  
![image](https://github.com/kangjunhyeong/Control-System3/assets/144297425/28d50704-4b3a-48ed-bdb5-cef1e127003f)  

(a)  

$$\\frac{\theta(s)}{\theta_d(s)} = \frac{\frac{K_i \cdot K \cdot K_m}{R_f \cdot(s(Js+b))}}{1 + \frac{K_f \cdot K \cdot K_m}{R_f \cdot (s(Js+b))}} \$$

Km=30,Rf=1,Kf=Ki=1,J=0.1,b=1,K=20이므로  

$$\\frac{\theta(s)}{\theta_d(s)} = \frac{6000}{s^2+10s+6000}\$$  

역라플라스를 해주면  

$$\ \frac{120 \cdot \sqrt{239} \cdot e^{-5t} \cdot \sin(5\sqrt{239}t)}{239} \$$

(b)  

$$\ \frac{\theta(s)}{T_d(s)} = \frac{-\frac{K_i}{s(Js+b)}}{1 + \frac{K \cdot K_m \cdot K_f}{s \cdot R_f \cdot (Js+b)}} \$$

$$\ = -\frac{1}{0.1s^2 + s + 600} \$$  

$$\ \theta(s)= -\frac{A}{s(0.1s^2 + s + 600)} \$$  

역라플라스를 취해주면  
$$\ \frac{A \cdot e^{-5t} \cdot (\cos(5\sqrt{239}t) + \frac{\sqrt{239} \cdot \sin(5\sqrt{239}t)}{239})}{600} - \frac{A}{600} \$$  

(c)  

