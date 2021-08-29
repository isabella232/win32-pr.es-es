---
description: Antefir siempre un archivo de texto sin formato Unicode con una marca de orden de bytes, que informa a una aplicación que recibe el archivo de que el archivo está ordenado por bytes.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Usar marcas de orden de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b496787f5d20c887e7338e6f9a1f25c294074f25f6c69c151b46658172c500ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897865"
---
# <a name="using-byte-order-marks"></a>Usar marcas de orden de bytes

Antefir siempre un archivo de texto sin formato Unicode con una marca de orden de bytes, que informa a una aplicación que recibe el archivo de que el archivo está ordenado por bytes. Las marcas de orden de bytes disponibles se enumeran en la tabla siguiente. Dado que el texto sin formato Unicode es una secuencia de valores de código de 16 bits, es sensible a la ordenación de bytes utilizada cuando se escribe el texto.

> [!Note]  
> Una marca de orden de bytes no es un carácter de control que selecciona el orden de bytes del texto.

 



| Marca de orden de bytes | Descripción           |
|-----------------|-----------------------|
| EF BB BF        | UTF-8                 |
| FF FE           | UTF-16, little endian |
| FE FF           | UTF-16, big endian    |
| FF FE 00 00     | UTF-32, little endian |
| 00 00 FE FF     | UTF-32, big-endian    |



 

> [!Note]  
> Microsoft usa UTF-16, little endian orden de bytes.

 

Lo ideal es que todo el texto Unicode siga solo un conjunto de reglas de ordenación de bytes. Sin embargo, esto no es posible porque los microprocesadores difieren en la ubicación del byte menos significativo. Los procesadores Intel y MIPS sitúan primero el byte menos significativo, mientras que los procesadores Deg (y todos los archivos Unicode invertidos en bytes) lo sitúan en último lugar. Con un único conjunto de reglas de ordenación de bytes, los usuarios de un tipo de microprocesador se ven obligados a intercambiar el orden de bytes cada vez que se lee un archivo de texto sin formato o se escribe en él, incluso si el archivo nunca se transfiere a otro sistema operativo basado en un microprocesador diferente.

El lugar preferido para especificar el orden de bytes es en un encabezado de archivo, pero los archivos de texto no tienen encabezados. Por lo tanto, Unicode ha definido un carácter (U+FEFF) y un no caracteres (U+FFFE) como marcas de orden de bytes. Son imágenes de bytes reflejados entre sí.

Dado que la secuencia U+FEFF es muy poco frecuente al principio de un archivo de texto normal no Unicode, puede actuar como marcador o firma implícito para identificar el archivo como un archivo Unicode. Las aplicaciones que leen archivos de texto Unicode y no Unicode deben usar la presencia de esta secuencia como indicador de que el archivo es probablemente un archivo Unicode. Compare esta técnica con el uso del marcador EOF MS-DOS para finalizar los archivos de texto.

Cuando una aplicación encuentra U+FEFF al principio de un archivo de texto, normalmente procesa el archivo como un archivo Unicode, aunque puede realizar comprobaciones heurísticas adicionales para la comprobación. Esta comprobación puede ser tan sencilla como probar para averiguar si la variación en los bytes de orden inferior es mucho mayor que la variación en los bytes de orden alto. Por ejemplo, si el texto ASCII se convierte en texto Unicode, cada segundo byte es 0. Además, comprobar tanto los caracteres de retorno de línea como de retorno de carro (U+000A y U+000D) y el tamaño de archivo par o impar puede proporcionar un indicador sólido de la naturaleza del archivo.

Cuando una aplicación encuentra U+FFFE al principio de un archivo de texto, lo interpreta para significar que el archivo es un archivo Unicode invertido en bytes. La aplicación puede intercambiar el orden de los bytes o alertar al usuario de que se ha producido un error.

Puesto que el carácter de marca de orden de bytes Unicode no se encuentra en ninguna página de códigos, desaparece si los datos se convierten a ANSI. A diferencia de otros caracteres Unicode, no se reemplaza por un carácter predeterminado cuando se convierte. Si se encuentra una marca de orden de bytes en medio de un archivo, no se interpreta como un carácter Unicode y no tiene ningún efecto en la salida de texto.

> [!Note]  
> El valor Unicode U+FFFF no es válido en los archivos de texto sin formato y no se puede pasar entre aplicaciones. Está reservado para el uso privado de una aplicación.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



