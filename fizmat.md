# 📘 Fiziksel Matematik – Konu Özetleri ve Soru Listesi

---

## 1. Kuadratik Denklemler ve Matris Formülasyonu

### 1.1. Kuadratik Denklem Nedir?
- Derecesi en fazla 2 olan polinom denklemleridir.  
  **Örnek:**  
  $$2x^2 + 3x + 1 = 0$$

### 1.2. İki Değişkenli Konik Kesit Denklemi
- Genel form:  
  $$
  Ax^2 + 2H\,xy + B\,y^2 = K
  $$  
- Elips, hiperbol veya parabol gibi eğrileri tanımlar.

### 1.3. Matris Gösterimi
- Blok matris biçimi:  
  $$
  \begin{bmatrix}
    x & y
  \end{bmatrix}
  \begin{bmatrix}
    A & H \\
    H & B
  \end{bmatrix}
  \begin{bmatrix}
    x \\[2pt] y
  \end{bmatrix}
  = K.
  $$

### 1.4. Diagonalizasyonla Basitleştirme
1. **Matris tanımı:**  
   $$
   M = \begin{bmatrix}
     A & H \\[4pt]
     H & B
   \end{bmatrix}.
   $$
2. **Özdeğer denklemi:**  
   $$
   \det(M - \lambda I)
   = (A - \lambda)(B - \lambda) - H^2 = 0
   \quad\Longrightarrow\quad
   \lambda_1,\;\lambda_2.
   $$
3. **Özvektörler:**  
   $$
   (M - \lambda_i I)\,v_i = 0,
   \quad i=1,2.
   $$
4. **Dönüşüm matrisi:**  
   $$
   P = [\,v_1\;v_2], 
   \qquad
   P^{-1} M P = \begin{bmatrix}
     \lambda_1 & 0 \\[4pt]
     0 & \lambda_2
   \end{bmatrix}.
   $$
5. **Yeni değişkenler:**  
   $$
   \begin{bmatrix}u\\v\end{bmatrix}
   = P^{-1}\begin{bmatrix}x\\y\end{bmatrix},
   \qquad
   \lambda_1\,u^2 + \lambda_2\,v^2 = K.
   $$

---

## 2. Koordinat Sistemleri ve Ölçek Faktörleri

### Neden Farklı Koordinatlar?
Düzlemsel (kartezyen) eksenler, silindir veya küre simetrisi gerektiren problemlerde uygun olmayabilir; bu durumlarda silindirik ve küresel sistemler tercih edilir.

### Ölçek Faktörleri
Her koordinat eksenindeki birim artışın fiziksel uzunluktaki karşılığını gösterir.

### 2.1. Silindirik Koordinatlar \((r,\theta,z)\)
- **Dönüşüm:**  
  $$
  x = r\cos\theta,\quad
  y = r\sin\theta,\quad
  z = z.
  $$
- **Ölçek faktörleri:**  
  $$
  h_r = 1,\quad
  h_\theta = r,\quad
  h_z = 1.
  $$
- **İnfinitezimal uzunluk:**  
  $$
  dl^2 = dr^2 + r^2\,d\theta^2 + dz^2.
  $$
- **Hacim elemanı:**  
  $$
  dV = r\,dr\,d\theta\,dz.
  $$

### 2.2. Küresel Koordinatlar \((\rho,\phi,\theta)\)
- **Dönüşüm:**  
  $$
  x = \rho\sin\phi\cos\theta,\quad
  y = \rho\sin\phi\sin\theta,\quad
  z = \rho\cos\phi.
  $$
- **Ölçek faktörleri:**  
  $$
  h_\rho = 1,\quad
  h_\phi = \rho,\quad
  h_\theta = \rho\sin\phi.
  $$
- **İnfinitezimal uzunluk:**  
  $$
  dl^2 = d\rho^2 + \rho^2\,d\phi^2 + \rho^2\sin^2\!\phi\,d\theta^2.
  $$
- **Hacim elemanı:**  
  $$
  dV = \rho^2\sin\phi\,d\rho\,d\phi\,d\theta.
  $$

---

## 3. Karmaşık Sayılar ve İşlemleri

### 3.1. Temel Tanımlar
- **Karmaşık sayı:**  
  $$
  z = x + yi,
  \qquad
  i^2 = -1.
  $$
- **Gerçek ve imajiner kısımlar:**  
  $$
  \Re(z) = x,\quad
  \Im(z) = y.
  $$

### 3.2. Modül ve Eşlenik
- **Modül:**  
  $$
  |z| = \sqrt{x^2 + y^2}.
  $$
- **Eşlenik:**  
  $$
  \overline{z} = x - yi.
  $$

### 3.3. Bölme Örneği
Aşağıda adım adım gösterilmiştir:

$$
\frac{1}{2 + i}
= \frac{1}{2 + i}\,\frac{2 - i}{2 - i}
= \frac{2 - i}{(2)^2 + (1)^2}
= \frac{2 - i}{5}
= \frac{2}{5} - \frac{1}{5}\,i.
$$

---

## 4. Matris İşlemleri

### 4.1. Matrisin Tersi (3×3 için)
$$
A^{-1} = \frac{1}{\det A}\,\mathrm{adj}(A),
$$
- \(\det A\): determinant  
- \(\mathrm{adj}(A)\): kofaktör matrisinin transpozu

### 4.2. Diagonalizasyon
$$
A = P\,D\,P^{-1},
\qquad
D = \mathrm{diag}(\lambda_1,\dots,\lambda_n),
$$
- \(P\): sütunlarında özvektörler  
- \(D\): köşegeninde özdeğerler

---

## 5. Metrik Tensörler ve İnfinitezimal Hesaplamalar

### 5.1. Metrik Tensör
$$
ds^2 = g_{ij}\,du^i\,du^j,
$$
- \(g_{ij}\): ölçüm tensörü bileşenleri

### 5.2. Eliptik Silindirik Koordinatlarda
- **Dönüşüm:** \((\mu,\nu,z)\)  
  $$
  x = a\cosh\mu\cos\nu,\quad
  y = a\sinh\mu\sin\nu,\quad
  z = z.
  $$
- **Ölçek faktörleri:**  
  $$
  h_\mu = a\sqrt{\sinh^2\mu + \sin^2\nu},\quad
  h_\nu = a\sqrt{\sinh^2\mu + \sin^2\nu},\quad
  h_z = 1.
  $$
- **İnfinitezimal uzunluk:**  
  $$
  ds^2 = h_\mu^2\,d\mu^2 + h_\nu^2\,d\nu^2 + dz^2.
  $$
- **Hacim elemanı:**  
  $$
  dV = h_\mu\,h_\nu\,h_z\,d\mu\,d\nu\,dz.
  $$

---

## 6. Titreşim Frekansları ve Lagrangian

### 6.1. Lagrangian ve Euler–Lagrange Denklemi
$$
L = T - V,
\qquad
\frac{d}{dt}\!\Bigl(\frac{\partial L}{\partial \dot q_i}\Bigr)
- \frac{\partial L}{\partial q_i} = 0.
$$

### 6.2. Tek Kütle–Yay Örneği
1. \(T = \tfrac12 m\dot x^2,\quad V = \tfrac12 kx^2.\)  
2. \(L = \tfrac12 m\dot x^2 - \tfrac12 kx^2.\)  
3. Hareket denklemi:  
   $$
   m\ddot x + kx = 0
   \quad\Longrightarrow\quad
   \omega = \sqrt{\frac{k}{m}}.
   $$

### 6.3. Çoklu Kütle–Yay
$$
M\ddot{\mathbf{x}} + K\,\mathbf{x} = 0,
\qquad
\det(K - \omega^2 M) = 0.
$$

---

## 7. Konik Kesitler ve Matris Diagonalizasyonu

Genel denklem:
$$
Ax^2 + 2Hxy + By^2 + 2Gx + 2Fy + C = 0.
$$
- İkinci dereceli kısım:  
  $$M = \begin{bmatrix}A & H\\[4pt] H & B\end{bmatrix}.$$
- Diagonalizasyon:  
  $$P^{-1} M P = \mathrm{diag}(\lambda_1, \lambda_2).$$

---

## 8. Küresel Koordinatlar ve Yüzey Hesaplamaları

### 8.1. Konum Vektörü
$$
\mathbf{r}(\theta,\phi)
= R\bigl(\sin\phi\cos\theta,\;\sin\phi\sin\theta,\;\cos\phi\bigr).
$$

### 8.2. Yüzey Alanı
$$
dS = R^2\sin\phi\,d\phi\,d\theta,
\qquad
S = \int_{0}^{2\pi}\!\!\int_{0}^{\pi}R^2\sin\phi\,d\phi\,d\theta
  = 4\pi R^2.
$$

---

## Çözülecek Sorular

### Sayfa 1
1. $5x^2 - 4y^2 + 2y^2 = 30$ denkleminin eşdeğer özelliklerini tartışın.  
2. $(x - y)\bigl(\tfrac{5}{-2} - \tfrac{2}{2}\bigr)y = 30$ denklemini çözün.  
3. $C_1^1 \cup C_2^1 = (6,6) = D$ ifadesinin anlamını açıklayın.  
4. $x^2 + 6y^2 = 30$ denklemini analiz edin.  
5. $4x^2 - 2y^2 \times y + y^2 = 16$ denkleminin eşdeğer özelliklerini bulun.  
6. $x^2 + 6xy - 2y^2 - 2yz + z^2 = 24$ denklemindeki ikinci derece alt seviyesini inceleyin.  
7. Aşağıdaki matris denklemini çözerek $x,y,z$ değerlerini bulun:

   $$
   \begin{bmatrix}
     1 & 3 & 0 \\[4pt]
     3 & -2 & -1 \\[4pt]
     0 & -1 & 1
   \end{bmatrix}
   \begin{bmatrix}x\\y\\z\end{bmatrix}
   =
   \begin{bmatrix}ax\\ay\\yz\end{bmatrix}.
   $$

8. $\mu=1$, $\mu=-4$ ve $\mu=3$ için $C$ matrisini hesaplayın.

### Sayfa 2
9. Silindirik koordinatlarda:  
   a) Dairesel bir halkanın üzerindeki bir noktanın konum vektörünü $\mathbf{T}$ olarak yazın.  
   b) Halka boyunca $dl$ diferansiyel elemanını hesaplayın.  
   c) Halkanın toplam uzunluğunu bulun.

### Sayfa 3
10. Karmaşık sayılar için:
    a) $\frac{1}{2+i}$ ifadesini $x + yi$ formunda yazın.  
    b) $\frac{1}{2-i}$ ifadesini $x + yi$ formunda yazın.  
    c) $\frac{1}{3-3i}$ ifadesini $x + yi$ formunda yazın.  
    d) $\frac{3+3i}{3+5i}$ ifadesini $x + yi$ formunda yazın.  
    e) $\frac{3+3i}{9+9}$ ifadesini $x + yi$ formunda yazın.  
    f) $\frac{1}{6} + \frac{1}{6}i$ ifadesini sadeleştirin.  
    g) $\frac{2+4i}{6+8i}$ ifadesini $x + yi$ formunda yazın.  
    h) $\frac{1}{10} + \frac{1}{5}i$ ifadesini sadeleştirin.  
11. $R(z)=\frac{1}{2}\bigl(z+\overline{z}\bigr)$ ve $\Im(z)=\frac{1}{2i}\bigl(z-\overline{z}\bigr)$ olduğunu gösterin.  
12. $z=\frac{3i}{i-13}$ için $|z|$, $R(z)$ ve $\Im(z)$ değerlerini hesaplayın.

### Sayfa 4
13. 3×3 bir matrisin tersini bulma yöntemini öğrenin.  
14. Eliptik silindirik koordinatlarda:  
    a) İnfinitezimal uzunluk elemanını ($ds^2$) yazın.  
    b) Hacim elemanını ($dV$) hesaplayın.  
15. Metrik tensörü sıfır matris olan bir koordinat sisteminde:  
    a) Metrik tensörün tersini bulun.  
    b) Hacim elemanını hesaplayın.

### Sayfa 6
16. Matris diagonalizasyonunu kullanarak $M$ matrisini köşegenleştirin.  
17. Konik kesit denklemini $Ax^2 + 2Hxy + By^2 = K$ ana eksenlere göre basitleştirin.

### Sayfa 8
18. Verilen kinetik ve potansiyel enerji ifadelerini kullanarak karakteristik titreşim frekanslarını $\omega$ bulun.

### Sayfa 11
19. $Sx_1 - x_2 = x_1$ ve $-2x_2 + 2y_1 = by_1$ denklemlerini matris formunda çözün.  
20. Benzerlik dönüşümü kullanarak $M$ matrisini köşegenleştirin.

### Sayfa 12
21. $R$ yarıçaplı bir küre için:  
    a) Yüzeydeki bir noktanın konum vektörünü yazın.  
    b) Yüzey alanını hesaplayın.
