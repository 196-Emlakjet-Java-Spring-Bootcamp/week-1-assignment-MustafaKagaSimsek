# week-1-assignment-MustafaKagaSimsek

Java 8

Lambda expressions
herhangi bir class olmadan fonksiyonlara iş yaptırabileceğiz.

Functional interfaces
 Interface 'lerin içine function yazabiliriz.

Method references

Stream API
bir listeyi toplu şekilde for döngüsüne sokmadan işlem yapabilirsiniz.
 filter (filtreleme)
 forEach (itere etme)
 map (dönüştürme)
 reduce (indirgeme)
 distinct (tekil hale getirme)
 limit (limitleme)
 collect (toplama)
 count (sayma)
 min / max  (sıralama ile max-min eleman bulma)

Optional class
Null point exception'ların önüne geçildi

Concurrency Enhancements
Thread nesneleri oluşturmak ve yönetmek zorunda kalmayacağız.

JDBC Enhancements 

Java 11
Nest-Based Access Control
Dynamic Class-File Constants
Improve Aarch64 Intrinsics
Epsilon: A No-Op Garbage Collector (Experimental)
Remove the Java EE and CORBA Modules
HTTP Client (Standard)
Local-Variable Syntax for Lambda Parameters
Key Agreement with Curve25519 and Curve448
Unicode 10
Flight Recorder
ChaCha20 and Poly1305 Cryptographic Algorithms
Launch Single-File Source-Code Programs
Low-Overhead Heap Profiling
Transport Layer Security (TLS) 1.3
ZGC: A Scalable Low-Latency Garbage Collector (Experimental)
Deprecate the Nashorn JavaScript Engine
Deprecate the Pack200 Tools and API

Running Java File with single command( Java Dosyasını tek komutla çalıştırma)
Artık Dosyaları doyrdan javac komutu yerine java komutu ile çalıştırılabilecekç

Java String Methods(Java String Yöntemleri)
isBlank(): bir stringin boş olup olmamasını kontrol eden method, eğer strig sadece boşluktan oluşuyorsa bile true değerini döndürür yani boş olduğunu belirtir.
lines():Satırlara bölünmüş stringleri diziye dönüştürür
strip():Stringin sağındaki ve solundaki boşlukları kaldırır.
repeat(int): String'i girilen değer kadar tekrar etmesini sağlar.

HTTP Client(HTTP İstemcisi)
Http CLient API'sini standart hale getirdi.Yeni API, hem HTTP/1.1 hem de HTTP/2'yi destekler.Api ile iletişimin performansını arttırmıştır.Ayrıca WebSockets'i yerel olarak destekler.

Flight Recorder(Uçuş Kaydedici)
Flight Recorder artık açık kaynaklı.

Reading/Writing Strings to and from the Files(Dosyalara ve Dosyalardan Dizeleri Okuma/Yazma)
readString(),writeString() methodları tantıldı ve dosyadan string alma ve yaz işlemlerini kolaştırdı.

Java 17
Restore Always-Strict Floating-Point Semantics
Enhanced Pseudo-Random Number Generators
New macOS Rendering Pipeline
macOS/AArch64 Port
Deprecate the Applet API for Removal
Strongly Encapsulate JDK Internals
Pattern Matching for switch (Preview)
 if…else chain
 Pattern matching and null
 Refining patterns in switch
Remove RMI Activation
Sealed Classes
Remove the Experimental AOT and JIT Compiler
Deprecate the Security Manager for Removal
Foreign Function & Memory API (Incubator)
Vector API (Second incubator)
Context-Specific Deserialization Filters


Enhanced Pseudo-Random Number Generator
RandomGenerator interface'i tanıltıldı, PRNG algoritmalarını uygulamayı ve kullanmayı daha kolay hale getirdi.

New macOS Rendering Pipeline
Apple, daha iyi performans için yeni Metal framework lehine  macOS 10.14 release (Eylül 2018) OpenGL oluşturma kitaplığını kullanımdan kaldırdı.


Pattern Matching for switch
if else eşlestimeler ve switch case yazımında değişiklikler yapılmıştır.
String formatted = "unknown";
      if (o instanceof Integer i) {
          formatted = String.format("int %d", i);
      } else if (o instanceof Long l) {
          formatted = String.format("long %d", l);
      } else if (o instanceof Double d) {
          formatted = String.format("double %f", d);
      } else if (o instanceof String s) {
          formatted = String.format("String %s", s);
      }
      return formatted;

yeni formatı->

 return switch (o) {
            case Integer i -> String.format("int %d", i);
            case Long l    -> String.format("long %d", l);
            case Double d  -> String.format("double %f", d);
            case String s  -> String.format("String %s", s);
            default        -> o.toString();
        };
Switch caselerde null değerleri doğrudan eşleştirebiliriz

 case null                   -> System.out.println("Unknown!");
