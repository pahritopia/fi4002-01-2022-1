# 10218027
JihadFachriRamadhanBilqisthi


## materi sebelumnya
+ lotka-volterra, runge-kutta orde 4, euler, monte carlo, bilangan random dan aplikasinya untuk enkripsi


## materi paling menarik
+ lotka-volterra karena paling mudah
+ bilangan random karena tidak benar-benar random, karena sebenarnya memiliki pola


## materi paling membosankan
+ belum menemukan materi yang membosankan


## materi yang sudah dipami
+ lotka-volterra, runge-kutta orde 4, euler, dan bilangan random. tetapi biangan random hanya konsepnya saja


## materi yang belum dipahami
+ monte carlo


## contoh program
+ Buat suatu contoh program dalam Python dan sertakan di sini dengan hasil keluarnnya.

```python
# contoh program python

'''
Jihad Fahri Ramadhan Bilqisthi
10218027

'''


import matplotlib.pyplot as plt
import numpy as np

def rk4(r, t, h):    
    
        # Runge-Kutta Orde 4
        
        k1 = h*f(r, t)
        k2 = h*f(r+0.5*k1, t+0.5*h)
        k3 = h*f(r+0.5*k2, t+0.5*h)
        k4 = h*f(r+k3, t+h)
        return (k1 + 2*k2 + 2*k3 + k4)/6

def f(r, t):
    
        # Parameter
        # x adalah prey
        # y adalah predator
        alpha = 1.0
        beta = 0.5
        gamma = 0.5
        sigma = 2.0
        x, y = r[0], r[1]
        fxd = (x*alpha) - (beta*x*y)       # dx/dt
        fyd = (-y*gamma) + (sigma*x*y)     # dy/dt
        return np.array([fxd, fyd], float) 

h=0.001                               
tpoints = np.arange(0, 30, h)   # dari t = 0 ke t = 30      
xpoints, ypoints  = [], []
r = np.array([2, 2], float)     # kondisi awal x = y = 2
for t in tpoints:
        xpoints.append(r[0])          
        ypoints.append(r[1])          
        r += rk4(r, t, h)             
plt.plot(tpoints, xpoints)      # grafik prey (biru)
plt.plot(tpoints, ypoints)      # grafik predator (kuning)
plt.xlabel("Waktu")
plt.ylabel("Populasi")
plt.title("Lotka-Volterra Model")
plt.savefig("Lotka_Volterra.png")
plt.show()
```

Hasilnya adalah

```
![pr01-10218027-JIHAD FACHRI R B](https://user-images.githubusercontent.com/111943406/196595749-36e1c222-1a08-41df-b381-cfa252b8e5b1.PNG)

```


## cara perkuliahan
+ perkuliahan kurang efektif untuk saya yang masih gagap programming. saya mengusulkan agar mahasiswa praktek langsung 


## topik sistem fisis
+ image processing terkait warna dan ukuran benda. karena klasifikasi warna sangat berguna di bidanng agrikultur.
+ ukuran benda sangat berguna untuk monitoring pertumbuhan hewan ternak


## simulasi dan visualisasi
+ saya tertarik visualisasi data, karena berkaitan dengan reporting, dimana dapat meningkatkan efisiensi dan efektivitas suatu kegiatan atau apapun.
