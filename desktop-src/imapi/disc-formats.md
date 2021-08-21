---
title: Formatos de disco
description: IMAPI admite tres formatos de sistema de archivos ISO 9660, Joliet y UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af71733ec2747ae227ac412a7b49f0faa73639cf1000f1332db5ec1d1d55db9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758608"
---
# <a name="disc-formats"></a>Formatos de disco

IMAPI admite tres formatos de sistema de [archivos: ISO 9660,](#iso-9660) [Joliet](#joliet)y [UDF.](#universal-disk-format-udf)

## <a name="iso-9660"></a>ISO 9660

El formato ISO 9660 es el sistema de archivos estándar original para discos de datos de CD. El formato se reconoce en varios sistemas operativos, incluidos MSDOS, Mac OS, UNIX y Windows operativo. El formato ISO 9660 se publica mediante Organización internacional de normalización (ISO).

El formato comienza en el sector 16 con el encabezado de volumen CD0001; el resto del encabezado sigue. Otros formatos derivados también comienzan en el sector 16, pero usan otra cadena para el encabezado del volumen. Por ejemplo, los discos high sierra usan la cadena CD-ROM0001 y el formato interactivo de disco compacto usa CD-I0001.

El encabezado apunta a las áreas del disco que almacenan los nombres de archivo en formato ISO 9660. La convención de nomenclatura de archivos y directorios consta de 8 caracteres, un punto y tres caracteres más. Se trata de la misma convención de nomenclatura que usa el sistema operativo MSDOS.

Los encabezados adicionales del sistema de archivos, para formatos como Joliet y UDF, pueden coexistir en un disco sin afectar a la legibilidad del formato ISO 9660. Después de los índices, un conjunto de archivos de datos ocupan el disco. Los índices de cada sistema de archivos hacen referencia de forma independiente a los archivos de datos del disco.

La especificación ISO 9660 define tres niveles del formato:

-   El nivel 1 define los nombres de archivo para usar el formato de caracteres 8.3.
-   El nivel 2 permite nombres de archivo más largos, como se encuentra en DOS 6.xx, MacIntosh y UNIX plataformas.
-   El nivel 3 permite que los archivos de datos y audio intercalados mejoren el rendimiento de recuperación (reproducción). Este nivel también quita el límite de archivos de 2 GB. Image Mastering API **no** admite este nivel.

Los discos DE DVD también pueden usar iso 9660; sin embargo, el sistema de archivos UDF es el sistema de archivos más frecuente que se usa con medios DE DVD.

## <a name="joliet"></a>Joliet

El formato Joliet es un derivado de ISO 9660. Este formato escribe el índice del sistema de archivos Joliet en la imagen de disco además del índice del sistema de archivos ISO 9660.

El índice Joliet proporciona las siguientes mejoras en el índice del sistema de archivos:

-   Reconoce nombres de archivo largos de hasta 32 caracteres.
-   Distingue entre letras mayúsculas y minúsculas en los nombres de archivo.
-   Admite caracteres Unicode en el nombre de archivo.

El encabezado de formato Joliet comienza en el sector 17 del disco.

Dado que el formato Joliet conserva el sistema de archivos ISO 9660 en un disco, se conserva la compatibilidad con dispositivos compatibles con ISO 9660.

## <a name="universal-disk-format-udf"></a>Formato de disco universal (UDF)

El formato de disco universal (UDF) es un sistema de archivos más reciente desarrollado para medios ópticos por la Asociación de tecnología de Storage ópticos ( TECHNOLOGY). UDF es un formato portátil reconocido por varios sistemas operativos. UDF reemplaza ISO 9660 como el nuevo estándar, especialmente con medios de lectura y escritura.

Entre las características de UDF se incluyen las siguientes:

-   Admite medios de hasta 2 TB de tamaño.
-   Admite medios flash, discos iomega REV y discos CD-MRW.
-   Almacena archivos de menos de 2 KB de longitud en el bloque Entrada de archivo.
-   Admite archivos de hasta 2 TB con nombres de archivo de hasta 255 caracteres.
-   Admite un amplio conjunto de atributos de archivo que se adaptan a varios sistemas operativos.
-   Admite un formato de puente donde los formatos ISO 9660, Joliet y UDF residen en el mismo disco. Se usa en aplicaciones de vídeo, como DVD-Video, DVD+VR y DVD-VR.
-   Admite secuencias con nombre y archivos "en tiempo real".

 

 




