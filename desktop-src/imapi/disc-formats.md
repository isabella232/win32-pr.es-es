---
title: Formatos de disco
description: IMAPi admite tres formatos de sistema de archivos ISO 9660, Joliet y UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357125"
---
# <a name="disc-formats"></a>Formatos de disco

IMAPi admite tres formatos de sistema de archivos: [ISO 9660](#iso-9660), [Joliet](#joliet)y [UDF](#universal-disk-format-udf).

## <a name="iso-9660"></a>ISO 9660

El formato ISO 9660 es el sistema de archivos estándar original para los discos de datos de CD. El formato se reconoce en varios sistemas operativos, como MSDOS, el Mac OS, UNIX y el sistema operativo Windows. El formato ISO 9660 se publica mediante el Organización internacional de normalización (ISO).

El formato comienza en el sector 16 con el encabezado Volume, CD0001; a continuación se muestra el resto del encabezado. Otros formatos derivados también comienzan en el sector 16, pero usan otra cadena para el encabezado de volumen. Por ejemplo, los discos de sierra alta usan la cadena CD-ROM0001 y el formato interactivo de disco compacto usa CD-I0001.

El encabezado apunta a las áreas del disco donde se almacenan los nombres de archivo en formato ISO 9660. La Convención de nomenclatura de archivos y directorios consta de 8 caracteres, un punto y 3 más caracteres. Esta es la misma Convención de nomenclatura usada por el sistema operativo MSDOS.

Los encabezados adicionales del sistema de archivos, para formatos como Joliet y UDF, pueden coexistir en un disco sin que ello afecte a la legibilidad del formato ISO 9660. Después de los índices, un conjunto de archivos de datos ocupa el disco. Los índices de cada sistema de archivos hacen referencia de forma independiente a los archivos de datos del disco.

La especificación ISO 9660 define tres niveles de formato:

-   El nivel 1 define los nombres de archivo para usar el formato de caracteres 8,3.
-   El nivel 2 permite nombres de archivo más largos, como se encuentra en las plataformas DOS. XX, MacIntosh y UNIX.
-   El nivel 3 permite que los datos intercalados y los archivos de audio mejoren el rendimiento de la recuperación (reproducción). Este nivel también quita el límite de 2 GB de archivo. Este nivel **no** es compatible con la API de masterización de imágenes.

Los discos DVD también pueden usar ISO 9660; sin embargo, el sistema de archivos UDF es el sistema de archivos más frecuente que se usa con los medios DVD.

## <a name="joliet"></a>Joliet

El formato Joliet es un derivado de ISO 9660. Este formato escribe el índice del sistema de archivos Joliet en la imagen de disco, además del índice del sistema de archivos ISO 9660.

El índice de Joliet proporciona las siguientes mejoras en el índice del sistema de archivos:

-   Reconoce los nombres de archivo largos hasta 32 caracteres.
-   Distingue entre mayúsculas y minúsculas en los nombres de archivo.
-   Admite caracteres Unicode en el nombre de archivo.

El encabezado de formato Joliet comienza en el sector 17 del disco.

Dado que el formato Joliet conserva el sistema de archivos ISO 9660 en un disco, se conserva la compatibilidad con dispositivos compatibles con ISO 9660.

## <a name="universal-disk-format-udf"></a>Formato de disco universal (UDF)

El formato de disco universal (UDF) es un sistema de archivos más reciente desarrollado para medios ópticos por la Asociación de tecnología de almacenamiento óptico (OSTA). UDF es un formato portátil reconocido por varios sistemas operativos. UDF reemplaza a ISO 9660 como el nuevo estándar, especialmente con medios de lectura y escritura.

Entre las características de UDF se incluyen las siguientes:

-   Admite medios con un tamaño máximo de 2 TB.
-   Es compatible con Flash, discos Iomega REV y discos CD-MRW.
-   Almacena archivos con una longitud inferior a 2 KB en el bloque de entrada del archivo.
-   Admite archivos de hasta 2 TB con nombres de archivo, con un máximo de 255 caracteres.
-   Admite un amplio conjunto de atributos de archivo que se adaptan a los distintos sistemas operativos.
-   Admite un formato de puente en el que todos los formatos ISO 9660, Joliet y UDF residan en el mismo disco. Se usa en aplicaciones de vídeo, como DVD-video, DVD + VR y DVD-VR.
-   Admite secuencias con nombre y archivos ' en tiempo real '.

 

 




