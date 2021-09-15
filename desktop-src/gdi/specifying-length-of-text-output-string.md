---
description: Varias de las funciones de fuente y salida de texto tienen un parámetro que especifica la longitud de la cadena de salida de texto. Un ejemplo típico es el parámetro cchText de DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Especificación de la longitud de la cadena de salida de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c120026d1b65170b6fe35bc65400280f6f1ffa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567644"
---
# <a name="specifying-length-of-text-output-string"></a>Especificación de la longitud de la cadena de salida de texto

Varias de las funciones de fuente y salida de texto tienen un parámetro que especifica la longitud de la cadena de salida de texto. Un ejemplo típico es *el parámetro cchText* de [**DrawTextEx.**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)

Cada una de estas funciones tiene una versión "ANSI" y una versión Unicode (por ejemplo, [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) y **DrawTextExW,** respectivamente). Para la versión "ANSI" de cada función, la longitud se especifica como un recuento BYTE y para la función Unicode se especifica como un recuento DE PALABRAS.

Es tradicional pensar en esto como un "recuento de caracteres". Esto suele ser preciso para muchos idiomas, incluido el inglés, pero no es preciso en general. En las cadenas "ANSI", los caracteres de las páginas de códigos [SBCS](../intl/single-byte-character-sets.md) toman un byte cada una, pero la mayoría de los caracteres de las páginas de [códigos DBCS](../intl/double-byte-character-sets.md) toman dos bytes. Del mismo modo, la mayoría de los caracteres Unicode definidos actualmente residen en el plano multilingüe básico (BMP) y sus representaciones UTF-16 caben en una palabra, pero los caracteres adicionales se representan en Unicode mediante "suplentes", que requieren dos WORD.

Cada una de estas funciones toma un recuento de longitud. Para la versión "ANSI" de cada función, la longitud se especifica como una longitud de recuento DE BYTES de una cadena sin incluir el terminador **NULL.** Para la función Unicode, el recuento de longitud es el recuento de bytes dividido por sizeof(WCHAR), que es 2, sin incluir el terminador **NULL.** El recuento de caracteres es el recuento del número de caracteres, que podría no ser igual al recuento de longitud de la cadena. En algunos casos, los caracteres toman más de un BYTE para ANSI (por ejemplo, el carácter [DBCS)](../intl/double-byte-character-sets.md) y más de una palabra para Unicode (por ejemplo, caracteres suplentes). Además, el número de glifos podría no ser igual al número de caracteres porque varios caracteres podrían estar compuestos para crear un glifo. El recuento de longitud es la cantidad de datos. Recuento de caracteres es el número de unidades que se procesan como una entidad. Los glifos son lo que se representa. Por ejemplo, en Unicode, puede tener una cadena con una longitud de 3, que es de 2 caracteres y que da como resultado la representación de un glifo. Sin embargo, normalmente, la mayoría de las cadenas Unicode, el recuento de caracteres y el número de glifos representados son iguales.

Puede usar \_ tcslen() para obtener la longitud de la cadena. Para ANSI, \_ tcslen() devuelve el número de bytes. Para Unicode, \_ tcslen() devuelve el número de WCHAR (es decir, WORD).

Los caracteres de procesamiento especiales, como tabulaciones y guiones flexibles que no siempre se dibujan, pueden afectar a la salida dibujada. Se incluyen en los recuentos de caracteres y longitud de cadena, pero es posible que no se represente directamente mediante un glifo representado.

Algunas de estas funciones permiten al autor de la llamada especificar la longitud como -1 para indicar que la cadena termina en NULL; En ese caso, la función calculará automáticamente el recuento de caracteres. No todas las funciones ofrecen esta funcionalidad. Esto se especifica en función de la función; consulte la documentación de la función individual.

 

 
