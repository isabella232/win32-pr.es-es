---
description: Es un entero vinculado a una propiedad con los calificadores BitMap y BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Calificadores BitMap y BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652555"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Calificadores BitMap y BitValue

Un mapa de bits es un entero vinculado a una propiedad con los calificadores **Bitmap** y **BitValue** . Cada bit del valor de la propiedad actúa como un índice en la matriz de valores de la lista **BitValue** . Dado que varios bits en el valor de la propiedad pueden ser "ON" al mismo tiempo, se puede usar un valor de propiedad único para indicar varios valores simultáneos.

Por ejemplo, en el siguiente ejemplo de código MOF se establece la propiedad **filetype** como con los calificadores **Bitmap** y **BitValues** . Además, establece que el bit de orden inferior (bit 0) corresponde al valor "Read Only". El siguiente bit (bit 1) corresponde a "Hidden", y así sucesivamente. (No todos los bits deben ser significativos. En este sistema de ocho bits, los dos bits de orden superior, 6 y 7, no tienen importancia.)

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

Si la propiedad **filetype** informa del valor 7 (bits 0000 0111), el archivo es "Read Only", "System" y "Hidden". Si la propiedad **filetype** informa del valor 18 (0X12, bits 0001 0010), se trata de un subdirectorio oculto.

Hay dos tipos diferentes de mapas de bits que usan código MOF:

-   Bits significativos consecutivos que empiezan por el bit de orden inferior (bit 0)

    Puede definir una matriz de valores de bit sin especificar explícitamente los bits significativos si los bits significativos comienzan con el bit de orden inferior (bit 0) y progresan hacia arriba sin interrupción a través de todos los elementos de la matriz **BitValue** . El siguiente ejemplo de código MOF realiza la misma función que en el ejemplo anterior.

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   Bit significativo precedido por un bit no significativo

    Si el bit de orden inferior es insignificante o la secuencia de bits significativos no es continua, debe especificar los calificadores **Bitmap** y **BitValues** . En el siguiente ejemplo de código MOF se muestra una situación en la que el bit de orden inferior no es significativo y hay un hueco en la secuencia de bits significativos.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    En este caso, el establecimiento del bit de orden inferior (bit 0) no tiene importancia y se omite. Sin embargo, la configuración de bit 1 (0X2) indica que este mensaje de correo electrónico está marcado para seguimiento, el valor bit 4 (0x8) indica que se debe enviar una confirmación de entrega al remitente cuando el mensaje de correo electrónico ha llegado al buzón del destinatario y el valor de bit 5 (0x10) especifica que se debe enviar una confirmación de lectura al remitente cuando el destinatario Abra el mensaje de correo. Al establecer los tres bits significativos (0x1A), se especifican las tres condiciones del mensaje de correo electrónico.

## <a name="remarks"></a>Observaciones

A **la hora** de decidir si usar los / calificadores de valores **BitValues** o **ValueMap** /  , determine si alguno de los valores que se indican podría producirse al mismo tiempo. Si pueden existir varios valores simultáneos, debe usar el **mapa de bits** / **BitValues**. Si todos los valores son mutuamente excluyentes, debe usar los  / calificadores de **valores** ValueMap.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Valores de ValueMap y calificadores de valor](value-map.md)
</dt> </dl>

 

 



