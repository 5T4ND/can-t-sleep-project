# can-t-sleep-project
from tkinter import *
def sum_but_all_buy_the_deep(i): # ฟังก์ชั่น บวกไปเรื่อยๆ ทบต้น ไอเป็นการบอก รอบ นับตัวแรกด้วย จะได้จำนวนหุ้นในแต่ละครั้งที่ซื้อ รวมถึงซื้อกี่ครั้งด้วย
    lis=[1]
    sum=1
    for j in range(i-1):
        sum*=2
        lis.append(sum)
    return lis
# จำนวนหุ้น ในแต่ละรอบ
def sum_many_stonk(i,number): # คำนวณหาจำนวนหุ้นในแต่ละรอบว่าจะซื้อจำนวนกี่หุ้น
    many=sum_but_all_buy_the_deep(i) # สร้างตัวแปร many มาเก็บ ข้อมูล list ว่ากี่รอบ 
    for j in range(len(many)):
        many[j]=many[j]*number
    return many
    # ต้องการรอบก่อน
    # แต่ละรอบ * จำนวนหุ้นที่ซื้อเริ่มต้น จะได้ จำนวนหุ้นที่จะซื้อในแต่ละรอบ
# จำนวนหุ้นที่ซื้อทั้งหมด
def sum_stonk_all(i,number): # เอาจำนวนที่ซื้อแต่ละครั้งมาบวกกัน จะได้จำนวนหุ้นที่ซื้อทั้งหมด i คือ รอบ number คือ จำนวนหุ้นเริ่มต้น ฟังก์ชั่นนี้ได้ q 
    lis_total_stonk_alll=sum_many_stonk(i,number) #สร้างตัวมารับค่าจำนวนหุ้นในแต่ละครั้งที่ซื้อ รวมถึงซื้อกี่ครั้งด้วย
    sum=0
    for j in range(len(lis_total_stonk_alll)): # นำ list มานับว่าซื้อไปกี่รอบก่อน
        sum+=lis_total_stonk_alll[j] # เอาแต่ละอันมาบวกกัน
    return sum
# ราคาที่ซื้อในแต่ละรอบ input Ex.5 4 3 2 1
def price_stonk_info(*args): # ดึงราคามาเก็บไว้ใน lis ข้อควรระวัง ถ้าไม่จัดในรูปของint ก่อนแล้วเอาเข้ามา มันจะเป็น str  ฟังก์ชั่นนี้ได้ p
    lis=[*args]
    return lis
# จำนวนเงินที่ซื้อในแต่ละรอบ p * q    
# ราคาเฉลี่ยหลังคิดภาษีแล้ว 
# กรณีขาดทุนเสียกี่บาท คิดเป็น % ด้วย 
# กรณีกำไร กี่บาท + % 
def sum_ma(i): # เอาตัวเลขใน list มาบวกกัน
    # ได้ lis มาแล้ว อยู่ในตัวย่อ i
    sum = 0
    for j in range(len(i)):
        sum+=i[j]
    return sum



def writetext(namefile,text): #สร้างไฟล์มาเก็บข้อความ
    f=open(namefile,"w",encoding="utf-8")
    f.write(text)
    f.close()



  
def createtext(price,many_stonk,sl,tp,start,priceAvg,spendtotal,losstotal,losspersent,gaintotal,gainpersent,rr): # สร้าง รูปแบบการแสดงผลของข้อความ
    text="Entry"
    text2="ซื้อเริ่มต้นที่ : {0:.2f} หุ้น\tราคาหุ้นเฉลี่ยหลังคิดภาษี : {1:.2f} บาท\tใช้เงินไปทั้งหมด : {2:.2f} บาท\nถ้าขาดทุนจะเสียเงิน : {3:.2f} บาท\tคิดเป็น : {4:.2f} %\nถ้ากำไรจะได้เงิน : {5:.2f} บาท\tคิดเป็น : {6:.2f} %\nRisk/Reward Ratio : {7:.2f} เท่า"
    x=0
    for i in range(len(price)):
        x=price[i]
        x=str(x)
        text= text + "\t" + x
    x=0
    text=text + "\n"+ "volume"
    for i in range(len(many_stonk)):
        x=many_stonk[i]
        x=str(x)
        text= text + "\t" + x
    x=0
    text+= "\n" "SL = "
    text+= str(sl) + "\n"
    text+= "TP = " + str(tp) + "\n"
    text2=text2.format(start,priceAvg,spendtotal,losstotal,losspersent,gaintotal,gainpersent,rr)
    text+= text2
    return text



def loop_wat(x):
    if x == "1" :
        pass
    if x == "2" :
        pass
    if x == "3" :
        pass
    if x == "4" :
        pass
    if x == "5" :
        pass
    if x == "6" :
        pass
    if x == "7" :
        pass
    if x == "8" :
        pass
    if x == "9" :
        pass
    if x == "10" :
        pass
    
    
    




    
   




