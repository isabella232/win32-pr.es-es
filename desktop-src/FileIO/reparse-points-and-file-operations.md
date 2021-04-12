---
description: Describe cómo los puntos de reanálisis habilitan el comportamiento del sistema de archivos que se deriva del comportamiento que esperan la mayoría de los desarrolladores de Windows.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Puntos de análisis y operaciones de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278280"
---
# <a name="reparse-points-and-file-operations"></a>Puntos de análisis y operaciones de archivo

Los *puntos de reanálisis* habilitan el comportamiento del sistema de archivos que se deriva del comportamiento que pueden estar acostumbrados a la mayoría de los desarrolladores de Windows, por lo que es consciente de estos comportamientos cuando la escritura de aplicaciones que manipulan archivos es vital para aplicaciones sólidas y confiables para tener acceso a sistemas de archivos que admiten puntos de análisis. La extensión de estas consideraciones dependerá de la implementación específica y del comportamiento del filtro del sistema de archivos asociado de un punto de análisis determinado, que puede ser definido por el usuario. Para obtener más información, vea [puntos de reanálisis](reparse-points.md).

Considere los ejemplos siguientes con respecto a las implementaciones de punto de reanálisis de NTFS, entre las que se incluyen las carpetas montadas, los archivos vinculados y el servidor de almacenamiento remoto de Microsoft:

-   Las aplicaciones de copia de seguridad que usan [secuencias de archivos](file-streams.md) deben especificar los **\_ \_ datos de reanálisis de copia de seguridad** en la estructura de la [**\_ secuencia \_ de Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) al realizar copias de seguridad de archivos con puntos de reanálisis.
-   Las aplicaciones que utilizan la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) deben especificar el indicador de **\_ \_ \_ \_ punto de reanálisis** de la marca de archivo al abrir el archivo si es un punto de análisis. Para obtener más información, vea [crear y abrir archivos](creating-and-opening-files.md).
-   El proceso de [desfragmentación de archivos](defragmenting-files.md) requiere un tratamiento especial para los puntos de reanálisis.
-   Las aplicaciones de detección de virus deben buscar puntos de repetición de análisis que indiquen archivos vinculados.
-   La mayoría de las aplicaciones deben tomar medidas especiales para los archivos que se han migrado a un almacenamiento a largo plazo, si solo se notifica al usuario que puede tardar algún tiempo en recuperar el archivo.
-   La función [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) abrirá el archivo o el punto de reanálisis, en función del uso de la marca de **\_ \_ \_ \_ punto de reanálisis** de la marca de archivo.
-   Los vínculos simbólicos, como puntos de análisis, tienen ciertas [consideraciones de programación](symbolic-link-programming-considerations.md) específicas para ellos.
-   Las actividades de administración de volúmenes para leer los registros del diario de cambios del número de secuencias actualizadas (USN) requieren un tratamiento especial para los puntos de reanálisis cuando se usa el [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y se leen las estructuras de [**\_ \_ \_ datos del diario USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Determinar si un directorio es una carpeta montada](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Crear carpetas montadas](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Efectos simbólicos de los vínculos en las funciones del sistema de archivos](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
