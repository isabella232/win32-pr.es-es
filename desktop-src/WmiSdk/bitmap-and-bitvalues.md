---
description: Es un entero vinculado a una propiedad con los calificadores BitMap y BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Calificadores BitMap y BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073066"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Calificadores BitMap y BitValue

Un mapa de bits es un entero vinculado a una propiedad con los **calificadores BitMap** y **BitValue.** Cada bit del valor de propiedad actúa como un índice en la matriz de valores de la **lista BitValue.** Dado que varios bits del valor de propiedad pueden estar "on" al mismo tiempo, es posible usar un valor de propiedad única para indicar varios valores simultáneos.

Por ejemplo, el siguiente ejemplo de código MOF establece que la propiedad **FileType** tiene los calificadores **BitMap** y **BitValues.** Además, establece que el bit de orden bajo (bit 0) corresponde al valor "Solo lectura". El bit siguiente (bit 1) corresponde a "Hidden", y así sucesivamente. (No todos los bits deben ser significativos. En este sistema de ocho bits, los dos bits de orden superior, 6 y 7, no tienen ninguna importancia).

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

Si la **propiedad FileType** notifica el valor 7 (bits 0000 0111), el archivo es "Read Only", "System" y "Hidden". Si la **propiedad FileType** notifica el valor 18 (0x12 bits 0001 0010), es un subdirectorio oculto.

Hay dos tipos diferentes de mapas de bits mediante código MOF:

-   Bits significativos consecutivos que comienzan por el bit de orden inferior (bit 0)

    Puede definir una matriz de valores de bits sin especificar explícitamente los bits significativos si los bits significativos comienzan por el bit de orden bajo (bit 0) y progresan hacia arriba sin interrupción a través de todos los elementos de la matriz **BitValue.** El siguiente ejemplo de código MOF realiza la misma función que en el ejemplo anterior.

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   Bit significativo precedido de un bit no significativo

    Si el bit de orden inferior es insignificante o la secuencia de bits significativos no es continua, debe especificar los calificadores **BitMap** y **BitValues.** En el siguiente ejemplo de código MOF se muestra una situación en la que el bit de orden bajo no es significativo y hay una brecha en la secuencia de bits significativos.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    En este caso, establecer el bit de orden bajo (bit 0) no tiene ninguna importancia y se omite. Sin embargo, al establecer el bit 1 (0x2) se indica que este mensaje de correo electrónico está marcado para seguimiento, al establecer el bit 4 (0x8) se indica que se debe enviar un recibo de entrega al remitente cuando el mensaje de correo electrónico haya llegado al buzón del destinatario y el valor del bit 5 (0x10) especifica que se debe enviar un recibo de lectura al remitente cuando el destinatario abra el mensaje de correo electrónico. Al establecer los tres bits significativos (0x1A) se especifican las tres condiciones para el mensaje de correo electrónico.

## <a name="remarks"></a>Observaciones

Al decidir si se deben usar los calificadores BitValues o ValueMap Values de **BitMap,** determine si alguno de los valores que se indican puede /   /  producirse simultáneamente. Si pueden existir varios valores simultáneos, debe usar **BitMap** / **BitValues**. Si todos los valores son mutuamente excluyentes, debe usar los calificadores **ValueMap** / **Values.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Calificadores ValueMap y Value](value-map.md)
</dt> </dl>

 

 



