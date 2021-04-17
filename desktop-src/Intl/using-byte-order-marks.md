---
description: Prefije siempre un archivo de texto sin formato Unicode con una marca de orden de bytes, que informa a una aplicación que recibe el archivo de que el archivo está ordenado por bytes.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Usar marcas de orden de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653089"
---
# <a name="using-byte-order-marks"></a>Usar marcas de orden de bytes

Prefije siempre un archivo de texto sin formato Unicode con una marca de orden de bytes, que informa a una aplicación que recibe el archivo de que el archivo está ordenado por bytes. En la tabla siguiente se enumeran las marcas de orden de bytes disponibles. Dado que el texto sin formato Unicode es una secuencia de valores de código de 16 bits, es sensible al orden de bytes que se usa cuando se escribe el texto.

> [!Note]  
> Una marca de orden de bytes no es un carácter de control que seleccione el orden de los bytes del texto.

 



| Marca de orden de bytes | Descripción           |
|-----------------|-----------------------|
| EF BB BF        | UTF-8                 |
| FF FE           | UTF-16, little endian |
| FE FF           | UTF-16, big endian    |
| FF FE 00 00     | UTF-32, little endian |
| 00 00 FE FF     | UTF-32, Big-Endian    |



 

> [!Note]  
> Microsoft usa UTF-16, little endian el orden de los bytes.

 

Idealmente, todo el texto Unicode sigue a un solo conjunto de reglas de ordenación de bytes. Sin embargo, esto no es posible porque los microprocesadores difieren en la posición del byte menos significativo. Los procesadores Intel y MIPS colocan primero el byte menos significativo, mientras que los procesadores Motorola (y todos los archivos Unicode inversos en bytes) lo colocan en último lugar. Con un solo conjunto de reglas de ordenación de bytes, los usuarios de un tipo de microprocesador deben cambiar el orden de los bytes cada vez que se lee o se escribe un archivo de texto sin formato, incluso si el archivo nunca se transfiere a otro sistema operativo basado en un microprocesador diferente.

El lugar preferido para especificar el orden de los bytes se encuentra en un encabezado de archivo, pero los archivos de texto no tienen encabezados. Por lo tanto, Unicode ha definido un carácter (U + FEFF) y un carácter (U + FFFE) como marcas de orden de bytes. Son imágenes de bytes reflejadas entre sí.

Dado que la secuencia U + FEFF es más rara vez al principio de un archivo de texto no Unicode normal, puede actuar como marcador implícito o firma para identificar el archivo como un archivo Unicode. Las aplicaciones que leen archivos de texto Unicode y no Unicode deben usar la presencia de esta secuencia como un indicador de que es más probable que el archivo sea un archivo Unicode. Compare esta técnica con el uso del marcador EOF de MS-DOS para terminar archivos de texto.

Cuando una aplicación encuentra U + FEFF al principio de un archivo de texto, normalmente procesa el archivo como un archivo Unicode, aunque puede realizar comprobaciones heurísticas adicionales para la comprobación. Este tipo de comprobación puede ser tan sencillo como realizar pruebas para averiguar si la variación en los bytes de orden inferior es mucho mayor que la variación en los bytes de orden superior. Por ejemplo, si el texto ASCII se convierte en texto Unicode, cada segundo byte es 0. Además, la comprobación de los caracteres de avance de carro y retorno de carro (U + 000A y U + 000D) y para el tamaño de archivo par o impar puede proporcionar un indicador fuerte de la naturaleza del archivo.

Cuando una aplicación encuentra U + FFFE al principio de un archivo de texto, lo interpreta para indicar que el archivo es un archivo Unicode invertido en bytes. La aplicación puede intercambiar el orden de los bytes o alertar al usuario de que se ha producido un error.

Puesto que el carácter de marca de orden de bytes Unicode no se encuentra en ninguna página de códigos, desaparece si los datos se convierten en ANSI. A diferencia de otros caracteres Unicode, no se sustituye por un carácter predeterminado cuando se convierte. Si se encuentra una marca de orden de bytes en medio de un archivo, no se interpreta como un carácter Unicode y no tiene ningún efecto en la salida de texto.

> [!Note]  
> El valor Unicode U + FFFF no es válido en archivos de texto sin formato y no puede pasarse entre aplicaciones. Está reservado para el uso privado de una aplicación.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



