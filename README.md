4-Bit Aritmetik Mantık Birimi (ALU)

Bu proje, Logisim (new) kullanılarak tasarlanmış 4-bit bir Aritmetik Mantık Birimi (ALU) uygulamasıdır.

ALU, iki adet 4-bit operand üzerinde aritmetik ve mantıksal işlemler gerçekleştirmektedir. Yapılacak işlem, 4-bit Opcode girişi üzerinden seçilmektedir.

🛠️ Kullanılan Program

Logisim (new)

Devre dosyası: .circ

⚙️ Desteklenen İşlemler
Aritmetik İşlemler

Toplama

Çıkarma

Artırma

Azaltma

Bölme

Mantıksal İşlemler

AND

OR

XOR

NOT

🔌 Girişler
Giriş	Genişlik	Açıklama
Operand_A	4 bit	Birinci operand
Operand_B	4 bit	İkinci operand
Opcode	4 bit	Yapılacak işlemi seçer
LOAD_Btn	1 bit	Operandları yükler
EXEC_Btn	1 bit	Seçilen işlemi çalıştırır
RESET_Btn	1 bit	Devreyi sıfırlar
Clock	1 bit	Saat sinyali
📤 Çıkışlar
Çıkış	Genişlik	Açıklama
Result	4 bit	İşlem sonucu
Carry	1 bit	Taşıma bilgisi
Sign	1 bit	İşaret bilgisi
Zero	1 bit	Sonucun sıfır olduğunu gösterir

Sonuç ayrıca Hex Digit Display üzerinde gösterilmektedir.

🧩 Devre Yapısı

Proje aşağıdaki temel alt devrelerden oluşmaktadır:

FullAdder — 1-bit tam toplayıcı

Adder4 — 4-bit toplama

Subtractor4 — 4-bit çıkarma

Incrementer4 — 4-bit artırma

Decrementer4 — 4-bit azaltma

Divider4 — 4-bit bölme

LogicUnit — mantıksal işlemler

main — ana ALU devresi

🔢 Full Adder

FullAdder, iki adet 1-bit veri ve bir taşıma girişini kullanarak toplama işlemi gerçekleştirir.

Girişler

A

B

Cin

Çıkışlar

S

Cout

🔀 Opcode

ALU'da gerçekleştirilecek işlem 4-bit Opcode girişi ile belirlenmektedir.

Opcode, ilgili aritmetik veya mantıksal işlemin seçilmesini sağlar.

Opcode değerlerinin hangi işlemlere karşılık geldiği .circ dosyasındaki devre bağlantılarından kontrol edilebilir.

🔄 Çalışma Mantığı

Genel veri akışı şu şekildedir:

Operand A ──┐
            │
            ▼
        ┌─────────┐
        │   ALU   │ ◄── Opcode
        └────┬────┘
             │
Operand B ───┘
             │
             ▼
          Result
             │
             ▼
       Hex Display


Operandlar registerlarda tutulur. Opcode ile işlem seçilir ve ALU tarafından sonuç üretilir.

🎛️ Kontrol Sinyalleri

LOAD_Btn: Operandların registerlara yüklenmesini sağlar.

EXEC_Btn: Seçilen işlemi çalıştırır.

RESET_Btn: Devreyi başlangıç durumuna getirir.

Clock: Register ve flip-flopların çalışmasını sağlar.

📌 Örnek İşlem

Aşağıdaki iki operandın toplandığını düşünelim:

Operand A = 0101
Operand B = 0011


Toplama işlemi:

  0101
+ 0011
------
  1000


Sonuç:

Result = 1000

📁 Proje Yapısı
4-bit-ALU/
│
├── README.md
└── ALU.circ


.circ dosyası Logisim (new) ile açılabilir.

🎯 Projenin Amacı

Bu projenin amacı, temel dijital devre elemanlarını kullanarak bir 4-bit ALU'nun nasıl tasarlanabileceğini göstermektir.

Projede;

Kombinasyonel mantık devreleri

Full Adder

Multiplexer

Register

Flip-Flop

Saat sinyali

Kontrol sinyalleri

bir arada kullanılmıştır.

📌 Sonuç

Bu proje ile Logisim (new) kullanılarak temel bir 4-bit ALU tasarlanmıştır.

ALU; operandların alınması, işlemin Opcode ile seçilmesi, işlemin gerçekleştirilmesi ve sonucun görüntülenmesi aşamalarını kapsamaktadır.
