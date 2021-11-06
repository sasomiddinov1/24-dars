# 24-dars
lambda YOHUD NOMSIZ FUNKSIYA


Pythonning o'ziga xos xususiyatlaridan biri, nomsiz vaqtinchalik funksiyalar yaratish imkoniyati. Bunday funksiyalarni yaratishda def operatori o'rniga lambda operatori ishlatilgani uchun ham lambda funskiyalar deb ataladi. 
Nomsiz funksiyalar quyidagicha yaratiladi:
lambda argument:ifoda
Lambda funksiyalari istalgan miqdordagi argumentlarga ega bo'lishi mumkin, ammo funksiya badanida faqat bitta ifoda mavjud bo'ladi. Ifoda bajariladi va qaytariladi (return operatori shart emas).
Nomsiz funksiyalar biror ifodani tezda hisoblab olishda qulay. Misol uchun quyidgai lambda funksiya ikkita argument qabul qiladi (  ), va aylana uzunligini qaytaradi: 
import mathuzunlik = lambda pi, r : 2*pi*rprint(uzunlik(math.pi,10))
Natija: 62.83185307179586
Kodni tahlil qilamiz, 1-qatorda math modulini chaqirib oldik. 2-qatorda lambda funksiyani yaratdik, funksiyamiz pi va r argumentlarini qabul qilib, 2*pi*r qiymatni qaytaradi. Funksiyaga nom bermadik, lekin unga uzunlik identifikatori orqali murojat qilishimiz mumkin. 3-qatorda funksiyamizga murojat qildik va natijani konsolga chiqardik.
Yana bir misol, topingchi quyidagi funksiyaning vazfiasi nima?
product = lambda x, y : x ** yprint(product(3, 2))
 Shu yerda so'rashingiz mumkin, nima uchun lambda nomsiz deb ataladi, ahir unga hozirgina nomi bilan murojat qildikku?
Gap shundaki, lambda finksiyalarning asl mohiyati boshqa funskiyalar bilan birga ishlaganda ko'rinadi. Keling, tushunarli bo'lishi uchun oddiyroq misol ko'ramiz.
Quyidagi dasturda biz avval daraja degan funksiya yasadik, bu funskiyamiz n degan o'zgaruvchi qabul qilib oladi va funksiya ichidagi noma'lum x ning n-darajasini qaytaradi. Aslida daraja bu funksiya yasaydigan funksya bo'ldi. Xo'sh, undan qanday foydalanamiz? 4-5-qatorlarda esa daraja funksiyasidan yana 2 ta funksiya yasadik: kvadrat - kiritilgan sonning kvadratini hisoblaydi, kub - kiritilgan sonning kubini hisoblaydi.
def daraja(n):    return lambda x : x**nkvadrat = daraja(2)kub = daraja(3)print(f"3-ning kvadrati {kvadrat(3)} ga, kubi {kub(3)} ga teng")
Natija: 3-ning kvadrati 9 ga, kubi 27 ga teng
Lambda funksiyalaridan argument sifatida boshqa funksyani qabul qiluvchi funksiyalar bilan ishlashda ham keng foydalaniladi. Misol uchun map() va filter() funksiyalari.






































