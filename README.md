# Dağıtık Sistemler Ödevi
# Proje Açıklaması:

Bu proje, Docker, MPI (Message Passing Interface) ve OpenMP (Open Multi-Processing) kullanarak dağıtık bir hesaplama ortamı oluşturmayı hedeflemektedir. Proje, büyük veri kümesinin paralel işlenmesi için farklı düğümler arasında veri paylaşımı ve her düğümde çok çekirdekli paralel işlem gerçekleştirilmiştir.

# Kullanılan Teknolojiler:
Docker: Dağıtık sistemin kurulumu ve konteyner yönetimi için kullandım.

MPI: Düğümler arası veri paylaşımını sağlamak için kullandım.

OpenMP: Her düğümde çok çekirdekli paralel işlem için kullandım.

# Proje Yapısı
Dockerfile/Docker Compose: Dağıtık sistemin kurulumu için gerekli yapılandırmalar içerir.

MPI ve OpenMP Kodları: Veri işleme için paralel hesaplama kodları içerir.

# Çalıştırma Talimatları
Docker Compose ile konteynerlerinizi başlatın:

docker build -t benim-sistemim .
docker run benim-sistemim

# Performans Karşılaştırması:
Sonuçları karşılaştırdığımızda, MPI ve OpenMP'nin birlikte kullanımının önemli bir performans artışı sağladığını görebiliyoruz. MPI, birden fazla düğüm arasında veri paylaşımını gerçekleştirirken, OpenMP her düğümde çok çekirdekli paralel işlem yaparak işlem süresini büyük ölçüde azaltmıştır. Bu sayede toplam işlem süresi 0.150402 saniye'ye kadar düşmüştür.

Paralel işlem sırasında elde edilen detaylar şu şekildedir:

MPI Sürümü 1, 2, ve 3 her biri farklı düğümlerde çalışırken, her biri 16 thread'lik OpenMP paralel işleme gücüyle işlem yapmıştır.

Toplam Değer: 700860777

Maksimum Değer: 999

OpenMP'nin 16 thread ile paralel işlemesi, her bir düğümdeki işlem gücünü verimli şekilde kullanarak işleme süresini hızlandırmıştır. Ancak, MPI'nin düğümler arası veri iletimi sırasında yaşanan bazı iletişim gecikmeleri, çok büyük veri kümelerinde performansı sınırlayabilir. Yine de, her iki teknolojinin birlikte kullanılması, tek başına kullanılan herhangi bir yönteme göre belirgin bir hız artışı sağlamıştır ve toplam işlem süresi çok daha kısa hale gelmiştir.


# Video link:
https://youtu.be/sAALCaKNVsY

