# Min Oklid Mesafesinin Hesaplanmasi

Bu kodun işleyişi şu şekildedir:
<ul>
  <li>euklid_mesafesi fonksiyonu iki nokta arasındaki Öklid Mesafesini hesaplar.</li>
  <li>minimum_euklid_mesafesi fonksiyonu, verilen noktalar listesindeki tüm noktalar arasındaki minimum mesafeyi ve bu mesafeye sahip noktaları bulur.</li>
  <li>main fonksiyonu bir dizi nokta tanımlar ve minimum mesafeyi hesaplayarak sonucu yazdırır.</li>
</ul>

Bu kodu çalıştırarak verilen noktalar arasındaki minimum Öklid Mesafesini ve bu mesafeye sahip olan noktaları bulabilirsiniz.

--- Code ---

    import math

    def euklid_mesafesi(nokta1, nokta2):
    return math.sqrt((nokta2[0] - nokta1[0]) ** 2 + (nokta2[1] - nokta1[1]) ** 2)

    def minimum_euklid_mesafesi(noktalar):
    min_mesafe = float('inf')
    min_noktalar = (None, None)
    
    for i in range(len(noktalar)):
        for j in range(i + 1, len(noktalar)):
            mesafe = euklid_mesafesi(noktalar[i], noktalar[j])
            if mesafe < min_mesafe:
                min_mesafe = mesafe
                min_noktalar = (noktalar[i], noktalar[j])
    
    return min_mesafe, min_noktalar

    def main():
    noktalar = [(1, 2), (3, 4), (5, 6), (7, 8), (2, 1)]
    min_mesafe, min_noktalar = minimum_euklid_mesafesi(noktalar)
    
    print(f"Minimum Öklid Mesafesi: {min_mesafe}")
    print(f"En yakın noktalar: {min_noktalar}")

    if __name__ == "__main__":
    main()


--- Output ---

    Minimum Öklid Mesafesi: 1.4142135623730951
    En yakın noktalar: ((1, 2), (2, 1))

