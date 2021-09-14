---
description: En MOF, los números son dígitos que describen valores numéricos. MOF proporciona una variedad de tipos de datos que se traducen en Automation y también permite que esos números se den en formatos diferentes. En la tabla siguiente se enumeran los valores numéricos que admite MOF.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Números (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973762"
---
# <a name="numbers-wmi"></a>Números (WMI)

En MOF, los números son dígitos que describen valores numéricos. MOF proporciona una variedad de tipos de datos que se traducen en Automation y también permite que esos números se den en formatos diferentes. En la tabla siguiente se enumeran los valores numéricos que admite MOF.



| Tipo de datos  | Tipo de automatización | Descripción                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **VT \_ I2**      | Entero de 8 bits con signo.<br/>                                                                                                                                        |
| **sint16** | **VT \_ I2**      | Entero de 16 bits con signo.<br/>                                                                                                                                       |
| **sint32** | VT \_ I4          | Entero de 32 bits con signo.<br/>                                                                                                                                       |
| **sint64** | **VT \_ BSTR**    | Entero de 64 bits con signo en forma de cadena. Este tipo sigue el formato hexadecimal o decimal según las American National Standards Institute (ANSI) de C.<br/> |
| **real32** | **VT \_ R4**      | Valor de punto flotante de 4 bytes que sigue el estándar instituto de ingenieros eléctricos y electrónicos, Inc. (IEEE).<br/>                                        |
| **real64** | **VT \_ R8**      | Valor de punto flotante de 8 bytes que sigue el estándar IEEE.<br/>                                                                                                  |
| **uint8**  | **VT \_ UI1**     | Entero de 8 bits sin signo.<br/>                                                                                                                                      |
| **uint16** | **VT \_ I4**      | Entero de 16 bits sin signo.<br/>                                                                                                                                     |
| **uint32** | **VT \_ I4**      | Entero de 32 bits sin signo.<br/>                                                                                                                                     |
| **uint64** | **VT \_ BSTR**    | Entero de 64 bits sin signo en forma de cadena. Este tipo sigue el formato hexadecimal o decimal según las reglas ANSI C.<br/>                                           |



 

Aunque es flexible, el código MOF encuentra algunos cambios al tratar con Automation:

-   Debe codificar enteros de 64 bits como cadenas.

    Automation no admite un tipo entero de 64 bits.

-   Los tipos de automatización no siempre se corresponden en tamaño de bits con tipos de datos MOF.

    Por ejemplo, Automation usa VT I4 para devolver un valor de \_ 16 bits sin signo. Esta discrepancia existe debido a problemas de extensión de inicio de sesión. Si Automation usa VT I2 en lugar de \_ VT \_ I4, 65 536 parecería ser el valor 1, lo que causaría problemas de tipo e intervalo. De forma similar, Automation representa el **tipo uint32** como VT I4 porque no existe ningún tipo entero mayor \_ que contenga **uint32**.

-   No es necesario cambiar ninguna representación para los tipos numéricos de 8 bits.

    Automation admite VT \_ UI1, un tipo de 8 bits sin signo.

MOF admite constantes largas. Una constante larga se declara mediante una serie simple de dígitos con un signo negativo opcional. Una constante larga no puede superar el tamaño de la variable declarada para contenerla. Algunos ejemplos de constantes largas son 1000 y 12310.

MOF también admite formatos numéricos alternativos. En la tabla siguiente se enumeran los caracteres especiales que debe usar para describir las constantes hexadecimales, binarias y octales.



| Constante               | Carácter especial     | Ejemplo                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | None<br/>       | val = 65<br/>       |
| Hexadecimal<br/> | Prefijo 0x<br/>  | val = 0x41<br/>     |
| Octal<br/>       | Inicial 0<br/>  | val = 0101<br/>     |
| Binary<br/>      | Final B<br/> | val = 1000001B<br/> |



 

Puede usar una constante de punto flotante para representar la notación científica, así como las fracciones, como se muestra a continuación:

``` syntax
3.14
-3.14
-1.2778E+02
```

WMI considera constantes de punto flotante como **tipos \_ VT R8** para Automation.

En el ejemplo siguiente se describen declaraciones de clase e instancia que muestran cómo usar cada uno de los tipos de datos numéricos para establecer propiedades:

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




