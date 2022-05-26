# week-1-assignment-MustafaKaganSimsek

Java 8

Lambda expressions<br/>
herhangi bir class olmadan fonksiyonlara iş yaptırabileceğiz.

Functional interfaces
 Interface 'lerin içine function yazabiliriz.

Method references

Stream API<br/>
bir listeyi toplu şekilde for döngüsüne sokmadan işlem yapabilirsiniz.<br/>
 •filter (filtreleme)<br/>
 •forEach (itere etme)<br/>
 •map (dönüştürme)<br/>
 •reduce (indirgeme)<br/>
 •distinct (tekil hale getirme)<br/>
 •limit (limitleme)<br/>
 •collect (toplama)<br/>
 •count (sayma)<br/>
 •min / max  (sıralama ile max-min eleman bulma)

Optional class<br/>
Null point exception'ların önüne geçildi

Concurrency Enhancements<br/>
Thread nesneleri oluşturmak ve yönetmek zorunda kalmayacağız.

JDBC Enhancements 

Java 11<br/>
•Nest-Based Access Control<br/>
•Dynamic Class-File Constants<br/>
•Improve Aarch64 Intrinsics<br/>
•Epsilon: A No-Op Garbage Collector (Experimental)<br/>
•Remove the Java EE and CORBA Modules<br/>
•HTTP Client (Standard)<br/>
•Local-Variable Syntax for Lambda Parameters<br/>
•Key Agreement with Curve25519 and Curve448<br/>
•Unicode 10<br/>
•Flight Recorder<br/>
•ChaCha20 and Poly1305 Cryptographic Algorithms<br/>
•Launch Single-File Source-Code Programs<br/>
•Low-Overhead Heap Profiling<br/>
•Transport Layer Security (TLS) 1.3<br/>
•ZGC: A Scalable Low-Latency Garbage Collector (Experimental)<br/>
•Deprecate the Nashorn JavaScript Engine<br/>
•Deprecate the Pack200 Tools and API<br/>

Running Java File with single command( Java Dosyasını tek komutla çalıştırma)<br/>
Artık Dosyaları doyrdan javac komutu yerine java komutu ile çalıştırılabilecek.

Java String Methods(Java String Yöntemleri)<br/>
isBlank(): bir stringin boş olup olmamasını kontrol eden method, eğer strig sadece boşluktan oluşuyorsa bile true değerini döndürür yani boş olduğunu belirtir.<br/>
lines():Satırlara bölünmüş stringleri diziye dönüştürür<br/>
strip():Stringin sağındaki ve solundaki boşlukları kaldırır.<br/>
repeat(int): String'i girilen değer kadar tekrar etmesini sağlar.<br/>

HTTP Client(HTTP İstemcisi)<br/>
Http CLient API'sini standart hale getirdi.Yeni API, hem HTTP/1.1 hem de HTTP/2'yi destekler.Api ile iletişimin performansını arttırmıştır.Ayrıca WebSockets'i yerel olarak destekler.

Flight Recorder(Uçuş Kaydedici)<br/>
Flight Recorder artık açık kaynaklı.

Reading/Writing Strings to and from the Files(Dosyalara ve Dosyalardan Dizeleri Okuma/Yazma)<br/>
readString(),writeString() methodları tantıldı ve dosyadan string alma ve yaz işlemlerini kolaştırdı.

Java 17<br/>
•Restore Always-Strict Floating-Point Semantics<br/>
•Enhanced Pseudo-Random Number Generators<br/>
•New macOS Rendering Pipeline<br/>
•macOS/AArch64 Port<br/>
•Deprecate the Applet API for Removal<br/>
•Strongly Encapsulate JDK Internals<br/>
•Pattern Matching for switch (Preview)<br/>
 if…else chain<br/>
 Pattern matching and null<br/>
 Refining patterns in switch<br/>
•Remove RMI Activation<br/>
•Sealed Classes<br/>
•Remove the Experimental AOT and JIT Compiler<br/>
•Deprecate the Security Manager for Removal<br/>
•Foreign Function & Memory API (Incubator)<br/>
•Vector API (Second incubator)<br/>
•Context-Specific Deserialization Filters<br/>


Enhanced Pseudo-Random Number Generator<br/>
RandomGenerator interface'i tanıltıldı, PRNG algoritmalarını uygulamayı ve kullanmayı daha kolay hale getirdi.

New macOS Rendering Pipeline<br/>
Apple, daha iyi performans için yeni Metal framework lehine  macOS 10.14 release (Eylül 2018) OpenGL oluşturma kitaplığını kullanımdan kaldırdı.


Pattern Matching for switch<br/>
if else eşlestimeler ve switch case yazımında değişiklikler yapılmıştır.<br/>
String formatted = "unknown";<br/>
      if (o instanceof Integer i) {<br/>
          formatted = String.format("int %d", i);<br/>
      } else if (o instanceof Long l) {<br/>
          formatted = String.format("long %d", l);<br/>
      } else if (o instanceof Double d) {<br/>
          formatted = String.format("double %f", d);<br/>
      } else if (o instanceof String s) {<br/>
          formatted = String.format("String %s", s);<br/>
      }<br/>
      return formatted;

yeni formatı-><br/>

 return switch (o) {<br/>
            case Integer i -> String.format("int %d", i);<br/>
            case Long l    -> String.format("long %d", l);<br/>
            case Double d  -> String.format("double %f", d);<br/>
            case String s  -> String.format("String %s", s);<br/>
            default        -> o.toString();<br/>
        };<br/>
Switch caselerde null değerleri doğrudan eşleştirebiliriz<br/>

 case null                   -> System.out.println("Unknown!");
