---
description: El sistema de archivos NTFS usa Lempel-Ziv compresión, que es un algoritmo de compresión sin pérdida.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Compresión y descompresión de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61c19449d1bfb31dfdd6e55e8c5ffa204bda36af597c43204693c55b13254e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927814"
---
# <a name="file-compression-and-decompression"></a>Compresión y descompresión de archivos

Los volúmenes del sistema de archivos NTFS admiten la compresión de archivos de forma individual. El algoritmo de compresión de archivos utilizado por el sistema de archivos NTFS Lempel-Ziv compresión. Se trata  de un algoritmo de compresión sin pérdida, lo que significa que no se pierde ningún dato al comprimir y descomprimir el archivo, en lugar de algoritmos de compresión con pérdida, como JPEG, donde se pierden algunos datos cada vez que se produce la compresión y la *descompresión* de datos.

La compresión de datos reduce el tamaño de un archivo minimizando los datos redundantes. En un archivo de texto, los datos redundantes pueden ser caracteres que se producen con frecuencia, como el carácter de espacio, o las votos comunes, como las letras e y a; también pueden ser cadenas de caracteres que se producen con frecuencia. La compresión de datos crea una versión comprimida de un archivo minimizando estos datos redundantes.

Cada tipo de algoritmo de compresión de datos minimiza los datos redundantes de una manera única. Por ejemplo, el *algoritmo de codificación Huffman* asigna un código a los caracteres de un archivo en función de la frecuencia con la que se producen esos caracteres. Otro algoritmo de compresión, denominado codificación de longitud de *ejecución,* genera un valor de dos partes para caracteres repetidos: la primera parte especifica el número de veces que se repite el carácter y la segunda parte identifica el carácter. Otro algoritmo de compresión, conocido como algoritmo *Lempel-Ziv,* convierte las cadenas de longitud variable en códigos de longitud fija que consumen menos espacio que las cadenas originales.

## <a name="the-ntfs-file-system-file-compression"></a>Compresión de archivos del sistema de archivos NTFS

En el sistema de archivos NTFS, la compresión se realiza de forma transparente. Esto significa que se puede usar sin necesidad de cambios en las aplicaciones existentes. Las aplicaciones no pueden acceder a los bytes comprimidos del archivo; solo ven los datos sin comprimir. Por lo tanto, las aplicaciones que abren un archivo comprimido pueden operar en él como si no estuvieran comprimidas. Sin embargo, estos archivos no se pueden copiar en otro sistema de archivos.

Si comprime un archivo de más de 30 gigabytes, es posible que la compresión no se haya hecho correctamente.

En los temas siguientes se identifica la compresión de archivos del sistema de archivos NTFS:

-   [Atributo de compresión](compression-attribute.md)
-   [Estado de compresión](compression-state.md)
-   [Obtener el tamaño de un archivo comprimido](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Bibliotecas de compresión y descompresión de archivos

Las bibliotecas de compresión y descompresión de archivos toman un archivo o archivos existentes y generan un archivo o archivos que son versiones comprimidas de los originales. La compresión también no tiene pérdidas, pero la compresión no es transparente para las aplicaciones. Una aplicación solo puede funcionar en estos archivos con la ayuda de una biblioteca de compresión de archivos. Además, las únicas operaciones que puede realizar en estos archivos son crear un archivo comprimido a partir de un original y recuperar los datos originales de la versión descomprimida. Normalmente no se admite la edición y la búsqueda está limitada si se admite en absoluto.

Normalmente, una aplicación llama a funciones de Lz32.dll para descomprimir los datos comprimidos mediante Compress.exe. Las funciones también pueden procesar archivos sin intentar descomprimirlos.

Puede usar las funciones de Lz32.dll para descomprimir uno o varios archivos. También puede usarlos para descomprimir archivos comprimidos una parte a la vez.

En los temas siguientes se identifica la descompresión de archivos que proporcionan las funciones de Lz32.dll:

-   [Descompresión de un solo archivo](decompressing-a-single-file.md)
-   [Descompresión de varios archivos](decompressing-multiple-files.md)
-   [Lectura desde archivos comprimidos](reading-from-compressed-files.md)

## <a name="cabinets"></a>Gabinetes

Los gabinetes se crean mediante una biblioteca de compresión que admite características como la expansión de disco y la compresión de varios archivos. Para obtener más información, vea Kit de desarrollo de software de Gabinete: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Atributo de compresión](compression-attribute.md)<br/>                                     | En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un *atributo de compresión*.<br/>                                         |
| [Estado de compresión](compression-state.md)<br/>                                             | Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un *estado de compresión*.<br/> |
| [Obtener el tamaño de un archivo comprimido](obtaining-the-size-of-a-compressed-file.md)<br/> | Para obtener el tamaño comprimido de un archivo, use la función GetCompressedFileSize.<br/>                                               |
| [Descomprimir un solo archivo](decompressing-a-single-file.md)<br/>                         | Una aplicación puede descomprimir un único archivo comprimido mediante las funciones LZOpenFile, LZCopy y LZClose.<br/>                |
| [Descompresión de varios archivos](decompressing-multiple-files.md)<br/>                       | Una aplicación puede descomprimir varios archivos mediante las funciones LZOpenFile, LZCopy y LZClose.<br/>                          |
| [Lectura desde archivos comprimidos](reading-from-compressed-files.md)<br/>                     | Una aplicación puede descomprimir un archivo comprimido una parte a la vez mediante las funciones LZSeek y LZRead.<br/>                 |



 

 

