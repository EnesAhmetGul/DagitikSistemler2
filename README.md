MPI ve OpenMP Performans Karşılaştırma Raporu
Proje Özeti
Bu projede, bir görüntü veri seti (JPEG formatında) dağıtık sistem mimarisi kullanılarak işlenmiştir.

Her konteyner bir MPI süreci olarak çalışmış, veri parçalanarak her düğüme dağıtılmıştır.

Her düğüm içinde OpenMP ile çok çekirdekli paralel işlem yapılmıştır.
Amaç: Her görselin ortalama RGB değerini hızlı ve ölçeklenebilir şekilde hesaplamaktır.

Teknoloji Kullanımı
Özellik	                  MPI	                                                        OpenMP
Paralellik Tipi	          Dağıtık (birden çok konteyner/düğüm)	                      Paylaşımlı bellek (tek düğüm içinde)
Kullanım Yeri	            Veri parçalama ve düğüm yönetimi	                          Her düğümde paralel işlem
Başlatma Hızı	            Daha yavaş (ağ + konteyner kurulumu)	                      Daha hızlı
İşlemci Kullanımı	        1 işlemci çekirdeği / süreç	                                Çok çekirdek / süreç
Kod Karmaşıklığı	        Yüksek	                                                     Orta


Yorumlar
-OpenMP, işlemci seviyesinde yüksek performans sunar ancak sadece tek düğüm içindir.
-MPI, düğümler arası iş bölümü sağlar, ancak veri paylaşımı daha maliyetlidir.
-MPI ile iş yükü dağıtılır,
-OpenMP ile her düğüm kendi işini hızlıca tamamlar.

Sonuç
Bu proje kapsamında:
-MPI, dağıtık yapı sayesinde yükü böldü.
-OpenMP, her düğümdeki hesaplamaları paralel hale getirdi.
-Böylece yüksek verimlilik, düşük işlem süresi ve ölçeklenebilirlik sağlandı.



Youtube Linki: https://youtu.be/jvtoN1pDyus
