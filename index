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
