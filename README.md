# surface-adsporption

## 1.获得初始结构
手动建立FeCo2S4结构；

## 2.获得源胞
使用软件（vasp）进行结构优化（如果不收敛，回到1），然后作为源胞；

## 3.切面
根据源胞按晶面进行切面，定义模型原子层数（设置六层原子，固定底面的两层原子），晶体表面放置I*；模型（三组）：

### 3.1
- (311)晶面(4个样本)   
   (311)-Fe-I*，(311)-Co-I*, (311)-S-I*, (311)-Vs-I* (S vacancy)

### 3.2
- (422)晶面    
 (422)-Fe-I*，(422)-Co-I*, (422)-S-I*, (422)-Vs-I* (S vacancy)

### 3.3 
- (440)晶面    
 (440)-Fe-I*，(440)-Co-I*, (440)-S-I*, (440)-Vs-I* (S vacancy)

## 4.结构优化
对3x4个样本进行结构优化（寻找I*在界面的吸附距离，我们先设置若干组样本，设置I-x的距离从1.5~3.5，看最后是否最后优化的I-x距离是否相近，如果相近，则取最低值作为吸附距离）；
### 4.1
- (422)晶面，Co-I  

|初始值 | 优化值（点-点） | z坐标差值（点-面）| 能量 |
| - | :-: | :-:  |-: | 
|1.5 | 4.2   | 0.103| -.85541651E+03 |
|2   | 2.606 | 0.062|  -.85545278E+03 |
|2.5 | 2.49	 | 0.09 | -.85531031E+03 | 
|3.0 | 2.478 | 0.09 | -.85518054E+03 |
|3.5 | 2.48	 | 0.091| -.85657293E+03 |

- (422)晶面，Fe-I 

|初始值 | 优化值（点-点） | z坐标差值（点-面）| 能量 |
| - | :-: | :-:  |-: | 
|2.5 | 2.995  | 0.065| -.85567898E+03 |
|2.7 | 4.99   | 0.08 | -.85605523E+03 |
|2.85 | 4.91  | 0.079 | -.85425337E+03 | 
|2.4 | 3.07	  | 0.089 | -0.855704894439E+03 |
|2.3 | 3	     | 0.067| -.85572271E+03 |


## 5.计算吸附能
根据优化结构，展开3x4个样本进行吸附能计算（如果不收敛，回到4）；

将4算出的结构，固定结构后在算能量E；
计算公式：
E(adsorption energy)=E(interface) + 1/2E(I2) - E(I/interface)

## 6.验证
实验验证。
