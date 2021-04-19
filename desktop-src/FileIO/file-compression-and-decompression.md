---
description: El sistema de archivos NTFS usa la compresión de Lempel-Ziv, que es un algoritmo de compresión sin pérdida.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Compresión y descompresión de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d1aa9d8d3540eff85413c03358fd1ba7e21300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688470"
---
# <a name="file-compression-and-decompression"></a>Compresión y descompresión de archivos

Los volúmenes del sistema de archivos NTFS admiten la compresión de archivos en cada archivo. El algoritmo de compresión de archivos que usa el sistema de archivos NTFS es Lempel-Ziv compresión. Se trata de un algoritmo de compresión sin *pérdida* , lo que significa que no se pierden datos al comprimir y descomprimir el archivo, en lugar de los algoritmos de compresión de *pérdida* , como JPEG, donde algunos datos se pierden cada vez que se produce la compresión y la descompresión de datos.

La compresión de datos reduce el tamaño de un archivo al minimizar los datos redundantes. En un archivo de texto, los datos redundantes pueden ser caracteres con frecuencia, como el carácter de espacio, o vocales comunes, como las letras e y a; también puede tener cadenas de caracteres que suelen aparecer. La compresión de datos crea una versión comprimida de un archivo al minimizar estos datos redundantes.

Cada tipo de algoritmo de compresión de datos reduce los datos redundantes de una manera única. Por ejemplo, el *algoritmo de codificación Huffman* asigna un código a los caracteres de un archivo en función de la frecuencia con que se producen esos caracteres. Otro algoritmo de compresión, denominado *codificación de longitud de ejecución*, genera un valor de dos partes para los caracteres repetidos: la primera parte especifica el número de veces que se repite el carácter y la segunda parte identifica el carácter. Otro algoritmo de compresión, conocido como el *algoritmo Lempel-Ziv*, convierte las cadenas de longitud variable en códigos de longitud fija que consumen menos espacio que las cadenas originales.

## <a name="the-ntfs-file-system-file-compression"></a>Compresión de archivo del sistema de archivos NTFS

En el sistema de archivos NTFS, la compresión se realiza de forma transparente. Esto significa que se puede usar sin necesidad de realizar cambios en las aplicaciones existentes. Las aplicaciones no pueden acceder a los bytes comprimidos del archivo; solo verán los datos sin comprimir. Por lo tanto, las aplicaciones que abren un archivo comprimido pueden trabajar en él como si no estuvieran comprimidos. Sin embargo, estos archivos no se pueden copiar en otro sistema de archivos.

Si comprime un archivo de más de 30 gigabytes, la compresión puede no realizarse correctamente.

En los temas siguientes se identifica la compresión de archivos del sistema de archivos NTFS:

-   [Atributo Compression](compression-attribute.md)
-   [Estado de compresión](compression-state.md)
-   [Obtención del tamaño de un archivo comprimido](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Bibliotecas de compresión y descompresión de archivos

Las bibliotecas de compresión y descompresión de archivos toman un archivo o archivos existentes y generan un archivo o archivos comprimidos de las versiones originales. La compresión también es sin pérdida de los mismos, pero la compresión no es transparente para las aplicaciones. Una aplicación solo puede operar en estos archivos con la ayuda de una biblioteca de compresión de archivos. Además, las únicas operaciones que puede realizar en estos archivos son crear un archivo comprimido a partir de un original y recuperar los datos originales de la versión descomprimida. Normalmente no se admite la edición y la búsqueda está limitada si se admite en absoluto.

Normalmente, una aplicación llama a funciones en Lz32.dll para descomprimir datos comprimidos mediante Compress.exe. Las funciones también pueden procesar archivos sin intentar descomprimirlos.

Puede usar las funciones de Lz32.dll para descomprimir uno o varios archivos. También puede usarlos para descomprimir archivos comprimidos de forma parcial.

En los temas siguientes se identifica la descompresión de archivos proporcionada por las funciones de Lz32.dll:

-   [Descompresión de un solo archivo](decompressing-a-single-file.md)
-   [Descomprimir varios archivos](decompressing-multiple-files.md)
-   [Leer archivos comprimidos](reading-from-compressed-files.md)

## <a name="cabinets"></a>Archiva

Los archivadores se crean mediante una biblioteca de compresión que admite características como la expansión de discos y la compresión de varios archivos. Para obtener más información, vea el kit de desarrollo de software de archivos. cab: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Atributo Compression](compression-attribute.md)<br/>                                     | En un volumen del sistema de archivos NTFS, cada archivo y directorio tiene un *atributo de compresión*.<br/>                                         |
| [Estado de compresión](compression-state.md)<br/>                                             | Cada archivo y directorio de un volumen que admite la compresión de archivos y directorios individuales tiene un *Estado de compresión*.<br/> |
| [Obtención del tamaño de un archivo comprimido](obtaining-the-size-of-a-compressed-file.md)<br/> | Para obtener el tamaño comprimido de un archivo, use la función GetCompressedFileSize.<br/>                                               |
| [Descompresión de un solo archivo](decompressing-a-single-file.md)<br/>                         | Una aplicación puede descomprimir un solo archivo comprimido mediante las funciones LZOpenFile, LZCopy y LZClose.<br/>                |
| [Descomprimir varios archivos](decompressing-multiple-files.md)<br/>                       | Una aplicación puede descomprimir varios archivos mediante las funciones LZOpenFile, LZCopy y LZClose.<br/>                          |
| [Leer archivos comprimidos](reading-from-compressed-files.md)<br/>                     | Una aplicación puede descomprimir un archivo comprimido en parte a la vez mediante las funciones LZSeek y LZRead.<br/>                 |



 

 

