a = input("*****   TAŞ KAĞIT MAKAS OYUNUNA HOŞ GELDİN   *******").lower()
import random
pc_list = ["t", "k", "m"]
counter=0
computer=0
sen=0
while counter != 10:
    
    pc = pc_list[random.randint(0,2)]
    you = input("birini seç: t: taş, m: makas, k: kağıt").lower()
    if (pc == "t" and you == "m") or (pc == "m" and you == "k") or (pc == "k" and you == "t"):
        computer += 10
        print("kazanan bilgisayar")
        
    elif (pc == "m" and you == "t") or (pc == "k" and you == "m") or (pc == "t" and you == "k"):
        sen += 10
        print("kazanan sensin")
        
    elif (pc == "m" and you == "m") or (pc == "k" and you == "k") or (pc == "t" and you == "t"):
        sen += 5
        computer +=5
        print("berabere")      
    else:
        print("hatalı giriş")
    counter += 1
if sen > computer:
    print ("OYUN BİTTİ, Tebrikler Kazandın.")
elif sen < computer:
    print ("OYUN BİTTİ, Ne Yazık ki Kaybettin....")
elif sen == computer:
    print ("Berabere Bitti")
print(f"senin puanın :{sen}, bilgisayarın puanı :{computer}, GAME OVER")
