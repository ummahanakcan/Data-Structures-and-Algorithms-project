# Data-Structures-and-Algorithms-project
Proje 1
[22,27,16,2,18,6] -> Insertion Sort

1 a) Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.
Cevap:  Insertion Sort'a göre verilen dizinin adımları şu şekildedir:

[22, 27, 16, 2, 18, 6] (Başlangıç)
[22, 27, 16, 2, 18, 6] (22 sabit, diğerleri ile karşılaştırma)
[16, 22, 27, 2, 18, 6] (16 yerine geçti)
[2, 16, 22, 27, 18, 6] (2 yerine geçti)
[2, 16, 18, 22, 27, 6] (18 yerine geçti)
[2, 6, 16, 18, 22, 27] (6 yerine geçti)

1 b)Big-O gösterimini yazınız.
Cevap: Insertion Sort algoritması, her adımda, sıralanmamış bölgenin ilk elemanını alıp, bu elemanı sıralı bölgedeki doğru konumuna yerleştirir. Bu işlem, dizi boyunca tekrarlanır.

En Kötü Durum (Worst Case): Dizinin tamamen ters sıralı olduğu durumdur. Bu durumda, her bir elemanı, sıralı bölge içinde doğru yerine koymak için, o elemanın sıralı bölgedeki tüm önceki elemanlarla karşılaştırılması gerekebilir.
Matematiksel olarak, n elemanlı bir dizi için, ilk eleman yerinde olduğu için n-1  elemanı yerleştirmemiz gerekir. İlk yerleştirme için 1 karşılaştırma, ikinci için 2 karşılaştırma,..., n-1 eleman için n-1 karşılaştırma yapılır. Bu durumda toplam karşılaştırma sayısı:
       1+2+3+......+(n-1)=n(n-1)/2 
Bu O(n^2) zaman karmaşıklığına tekabül eder.

1 c) Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız

Average case: Aradığımız sayının ortada olması
Worst case: Aradığımız sayının sonda olması
Best case: Aradığımız sayının dizinin en başında olması.
Cevap: Time Complexity, bir algoritmanın çalışma zamanının girdi boyutuna (genellikle eleman sayısı n olarak ifade edilir) bağlı olarak nasıl değiştiğini tanımlar. Insertion Sort'un Time Complexity'si:

Average case: Ortalama durumda, her elemanın sıralanması için diğer elemanlarla karşılaştırma yapılır. Bu durumda, her eleman için n/2 karşılaştırma yapılabilir. Dolayısıyla, ortalama durumda Time Complexity O(n^2) olur.

Worst case: En kötü durumda, her elemanı doğru konuma yerleştirmek için, o anki elemanın dizinin tüm önceki elemanlarıyla karşılaştırması yapılabilir. Bu durumda da Time Complexity O(n^2) olur.

Best case: En iyi durumda, dizi zaten sıralıysa, her elemanın karşılaştırma yapılmasına gerek kalmadan doğru konumuna yerleştirilebilir. Bu durumda Time Complexity O(n) olur.

Bu nedenle, 18 sayısının Best case'e girmesi, yani aranan sayının dizinin en başında olması durumunda Time Complexity O(1) olur. Çünkü sıralama yapıldıktan sonra aranan sayı hemen bulunabilir


.



[7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.
Cevap: Adım 1:

[7, 3, 5, 8, 2, 9, 4, 15, 6] (Başlangıçta dizi)
[2, 3, 5, 8, 7, 9, 4, 15, 6] (En küçük eleman olan 2, ilk eleman ile yer değiştirir.)

Adım 2:

[2, 3, 5, 8, 7, 9, 4, 15, 6] (2 sabit, diğerleri ile karşılaştırma)
[2, 3, 5, 8, 7, 9, 4, 15, 6] (3 sabit, diğerleri ile karşılaştırma)
[2, 3, 4, 8, 7, 9, 5, 15, 6] (4, en küçük ikinci eleman olduğu için, 4 ve 5 yer değiştirir.)

Adım 3:

[2, 3, 4, 8, 7, 9, 5, 15, 6] (2, 3, 4 sabit, diğerleri ile karşılaştırma)
[2, 3, 4, 5, 7, 9, 8, 15, 6] (5, en küçük üçüncü eleman olduğu için, 5 ve 8 yer değiştirir.)

Adım 4:

[2, 3, 4, 5, 7, 9, 8, 15, 6] (2, 3, 4, 5 sabit, diğerleri ile karşılaştırma)
[2, 3, 4, 5, 6, 9, 8, 15, 7] (6, en küçük dördüncü eleman olduğu için, 6 ve 7 yer değiştirir.)

Proje 2
[16,21,11,8,12,22] -> Merge Sort

2 a) Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
Cevap: 
2 a) Merge Sort Aşamaları
Merge Sort, dizi elemanlarını böl, elemanları tekil (veya daha yönetilebilir boyutlara) kadar ayır ve sonra bunları sıralayarak birleştir prensibi ile çalışır. İşte [16,21,11,8,12,22] dizisinin Merge Sort ile sıralanma aşamaları:

Bölme Aşaması:

[16,21,11,8,12,22] -> İkiye bölünür -> [16,21,11] ve [8,12,22]

[16,21,11] -> İkiye bölünür -> [16] ve [21,11] | [8,12,22] -> İkiye bölünür -> [8] ve [12,22]

[21,11] -> İkiye bölünür -> [21] ve [11] | [12,22] -> İkiye bölünür -> [12] ve [22]

Birleştirme ve Sıralama Aşaması:

[16] ve [21,11] -> [16] ve [11,21] -> Birleştirilir ve sıralanır -> [11,16,21]

[8] ve [12,22] -> [8] ve [12,22] -> Birleştirilir ve sıralanır -> [8,12,22]

[11,16,21] ve [8,12,22] -> Birleştirilir ve sıralanır -> [8,11,12,16,21,22]

Sonuç olarak dizi sıralanmış olur: [8,11,12,16,21,22]

2 b) Big-O gösterimini yazınız.
Cevap: Merge Sort'un zaman karmaşıklığı, her bölme işleminin diziyi iki eşit parçaya ayırması ve sonrasında bu parçaları birleştirirken tüm elemanların karşılaştırılması üzerine kuruludur. Bu, her seviyede O(n) işlem yapılmasını gerektirir ve diziyi bölme sayısı logaritmik olduğundan, toplam zaman karmaşıklığı O(nlogn) olur.

Bu nedenle, Merge Sort için Big-O gösterimi O(n log n) şeklindedir. 


Proje 3
[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree aşamalarını yazınız.

Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.
Cevap: Root 7'dir. Solunda 5, sağında 8 bulunur.
5'in solunda 1, sağında 6 bulunur.
1'in solunda 0, sağında 3 bulunur.
3'ün sağında 2 bulunur.
8'in solunda 6, sağında 9 bulunur.
6'nın solunda 4 bulunur.
BST ağacı şu şekilde oluşur:

       7
     /   \
    5     8
   / \     \
  1   6     9
 / \       
0   3     
   / \   
  2   4  
