---
description: Varias de las funciones de fuente y de salida de texto tienen un parámetro que especifica la longitud de la cadena de salida de texto. Un ejemplo típico es el parámetro cchText de DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Especificar la longitud de la cadena de salida de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c120026d1b65170b6fe35bc65400280f6f1ffa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002733"
---
# <a name="specifying-length-of-text-output-string"></a>Especificar la longitud de la cadena de salida de texto

Varias de las funciones de fuente y de salida de texto tienen un parámetro que especifica la longitud de la cadena de salida de texto. Un ejemplo típico es el parámetro *cchText* de [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa).

Cada una de estas funciones tiene una versión "ANSI" y una versión Unicode (por ejemplo, [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) y **DrawTextExW**, respectivamente). Para la versión "ANSI" de cada función, la longitud se especifica como un recuento de BYTEs y para la función Unicode se especifica como un recuento de palabras.

Es tradicional pensar en esto como un "número de caracteres". Esto suele ser preciso para muchos idiomas, incluido el inglés, pero no es preciso en general. En las cadenas "ANSI", los caracteres de las páginas de códigos [SBCS](../intl/single-byte-character-sets.md) toman un byte cada uno, pero la mayoría de los caracteres de las páginas de códigos [DBCS](../intl/double-byte-character-sets.md) tienen dos bytes. Del mismo modo, la mayoría de los caracteres Unicode definidos actualmente residen en el plano básico multilingüe (BMP) y sus representaciones UTF-16 caben en una palabra, pero los caracteres adicionales se representan en Unicode por ' ' suplentes ' ', que requieren dos palabras.

Cada una de estas funciones toma un recuento de longitud. Para la versión "ANSI" de cada función, la longitud se especifica como una longitud de recuento de BYTEs de una cadena, sin incluir el terminador **null** . En el caso de la función Unicode, el recuento de longitud es el recuento de bytes dividido por sizeof (WCHAR), que es 2, sin incluir el terminador **null** . El recuento de caracteres es el recuento del número de caracteres, que puede no ser igual al recuento de longitud de la cadena. En algunos casos, los caracteres toman más de un BYTE para ANSI (por ejemplo, carácter [DBCS](../intl/double-byte-character-sets.md) ) y más de una palabra para Unicode (por ejemplo, caracteres suplentes). Además, es posible que el número de glifos no sea igual al número de caracteres porque se pueden componer varios caracteres para crear un glifo. El recuento de longitud es la cantidad de datos. Recuento de caracteres es el número de unidades que se procesan como una entidad. Los glifos son lo que se representa. Por ejemplo, en Unicode, puede tener una cadena con una longitud de 3, que es 2 caracteres y que da como resultado que se represente un glifo. Sin embargo, normalmente, la mayoría de la longitud de las cadenas Unicode, el recuento de caracteres y el número de glifos representados son iguales.

Puede usar \_ tcslen () para obtener la longitud de la cadena. En el caso de ANSI, \_ tcslen () devuelve el número de bytes. En el caso de Unicode, \_ tcslen () devuelve el número de WCHARs (es decir, palabras).

Los caracteres de procesamiento especiales como las pestañas y los guiones flexibles que no se dibujan siempre pueden afectar a la salida dibujada. Se incluyen en la longitud de la cadena y en los recuentos de caracteres, pero es posible que no se representen directamente mediante un glifo representado.

Algunas de estas funciones permiten al llamador especificar la longitud como-1 para indicar que la cadena termina en null; en ese caso, la función calculará el recuento de caracteres automáticamente. No todas las funciones ofrecen esta funcionalidad. Esto se especifica según la función; Consulte la documentación de la función individual.

 

 
