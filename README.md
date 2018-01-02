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
- (400)晶面，Co-I  

|Co-I初始距离 | 图片| 能量 |
| - | :-:  |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-co-1.5.png" width="30%" /> | -.42895371E+03 |
|2   | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-co-2.0.png" width="30%" /> |  -.42844921E+03 |
|2.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-co-2.5.png" width="30%" /> | -.42892336E+03 | 
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-co-3.0.png" width="30%" /> | -.42825192E+03 |
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-co-3.5.png" width="30%" /> | -.42892827E+03 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-co-4.0.png" width="30%" /> | **-.42899335E+03** |

- (400)晶面，Fe-I 

|Fe-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-fe-1.5.png" width="30%" /> | -.42855536E+03 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-fe-2.0.png" width="30%" /> | --.42852913E+03 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-fe-2.5.png" width="30%" /> | -.42857576E+03 |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-fe-3.0.png" width="30%" /> | **-.42867647E+03** | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-fe-3.5.png" width="30%" /> | -.42853184E+03 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-fe-4.0.png" width="30%" /> | -.42844734E+03 |

- (400)晶面，S-I 

|S-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-s-1.5.png" width="30%" /> |  -.42504783E+03 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-s-2.0.png" width="30%" /> |  -.42880188E+03 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-s-2.5.png" width="30%" /> |  -.42859546E+03 |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-s-3.0.png" width="30%" /> |  -.42866197E+03 | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-s-3.5.png" width="30%" /> |  -.42867291E+03 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/440-s-4.0.png" width="30%" /> |  **-.42902563E+03** |

---------------------------------

- (422)晶面，Co-I 

|Co-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-co-1.5.png" width="30%" /> | -.85023109E+03 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-co-2.0.png" width="30%" /> | --.85608607E+03 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-co-2.5.png" width="30%" /> | **-.85754918E+03** |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-co-3.0.png" width="30%" /> | -.85697968E+03 | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-co-3.5.png" width="30%" /> | -.85607625E+03 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-co-4.0.png" width="30%" /> | -.85648219E+03 |

- (422)晶面，Fe-I 

|Fe-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-fe-1.5.png" width="30%" /> |  -.85741619E+03 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-fe-2.0.png" width="30%" /> |  -.85706426E+03 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-fe-2.5.png" width="30%" /> |  -.85739634E+03 |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-fe-3.0.png" width="30%" /> |  -.85641044E+03 | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-fe-3.5.png" width="30%" /> |  -.85751095E+03 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-fe-4.0.png" width="30%" /> |  **-.85588381E+03** |

- (422)晶面，S-I 

|S-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-s-1.5.png" width="30%" /> |  -.85566366E+03 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-s-2.0.png" width="30%" /> |  -.85546646E+03 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-s-2.5.png" width="30%" /> |  -.85555913E+03 |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-s-3.0.png" width="30%" /> |  **-.85599415E+03** | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-s-3.5.png" width="30%" /> |  -.85530942E+03 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/422-s-4.0.png" width="30%" /> |  -.85413165E+03 |

-------------------
- (311)晶面，Co-I 

|Co-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-co-1.5.png" width="30%" /> | -.17124145E+04 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-co-2.0.png" width="30%" /> | --.17133902E+04 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-co-2.5.png" width="30%" /> | **-.17138645E+04** |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-co-3.0.png" width="30%" /> | -.17159405E+04 | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-co-3.5.png" width="30%" /> | -.17141722E+04 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-co-4.0.png" width="30%" /> | -.17147285E+04 |

- (311)晶面，Fe-I 

|Fe-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-fe-1.5.png" width="30%" /> |  -.17136094E+04 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-fe-2.0.png" width="30%" /> |  -.17165546E+04 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-fe-2.5.png" width="30%" /> |  -.17159265E+04 |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-fe-3.0.png" width="30%" /> |  -.17129494E+04 | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-fe-3.5.png" width="30%" /> |  **-.17168628E+04** |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-fe-4.0.png" width="30%" /> | -.17156130E+04 |

- (311)晶面，S-I 

|S-I初始距离 |图片| 能量 |
| - | :-: |-: | 
|1.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-s-1.5.png" width="30%" /> |  -.17131743E+04 |
|2.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-s-2.0.png" width="30%" /> |  -.17157548E+04 |
|2.5 |<img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-s-2.5.png" width="30%" /> |  **-.17167747E+04** |
|3.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-s-3.0.png" width="30%" /> |  -.17140186E+04 | 
|3.5 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-s-3.5.png" width="30%" /> |  -.17128288E+04 |
|4.0 | <img src="https://github.com/pincher-chen/surface-adsporption/blob/master/opt_picture/311-s-4.0.png" width="30%" /> | -.17150751E+04 |



## 5.计算吸附能
根据优化结构，展开3x4个样本进行吸附能计算（如果不收敛，回到4）；

将4算出的结构，固定结构后在算能量E；\\    

计算公式：    
E(adsorption energy)=E(interface) + 1/2E(I2) - E(I/interface)

## 6.验证
实验验证。
