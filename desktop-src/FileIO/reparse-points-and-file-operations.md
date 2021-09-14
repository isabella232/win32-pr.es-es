---
description: Describe cómo los puntos de análisis habilitan el comportamiento del sistema de archivos que sale del comportamiento que Windows los desarrolladores esperan.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Análisis de puntos y operaciones de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069859"
---
# <a name="reparse-points-and-file-operations"></a>Análisis de puntos y operaciones de archivo

 Los puntos de análisis habilitan el comportamiento del sistema de archivos que sale del comportamiento al que pueden estar acostumbrados la mayoría de los desarrolladores de Windows, por lo que ser conscientes de estos comportamientos al escribir aplicaciones que manipulan archivos es fundamental para aplicaciones sólidas y confiables diseñadas para tener acceso a sistemas de archivos que admiten puntos de análisis. La extensión de estas consideraciones dependerá de la implementación específica y el comportamiento de filtro del sistema de archivos asociado de un punto de reanidad determinado, que se puede definir por el usuario. Para obtener más información, vea [Puntos de reanción.](reparse-points.md)

Tenga en cuenta los ejemplos siguientes relacionados con las implementaciones de punto de reanual de NTFS, que incluyen carpetas montadas, archivos vinculados y Microsoft Remote Storage Server:

-   Las aplicaciones de copia de seguridad que usan [secuencias](file-streams.md) de archivos deben especificar **BACKUP \_ REPARSE \_ DATA** en la estructura DE IDENTIFICADORES DE [**\_ SECUENCIAS \_ DE WIN32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) al realizar copias de seguridad de archivos con puntos de análisis.
-   Las aplicaciones que usan la [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) deben especificar la marca **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT** al abrir el archivo si es un punto de análisis. Para obtener más información, vea [Crear y abrir archivos](creating-and-opening-files.md).
-   El proceso de [desfragmentación de archivos requiere](defragmenting-files.md) un control especial para los puntos de reanamiento.
-   Las aplicaciones de detección de virus deben buscar puntos de análisis que indiquen archivos vinculados.
-   La mayoría de las aplicaciones deben realizar acciones especiales para los archivos que se han movido al almacenamiento a largo plazo, si solo para notificar al usuario que puede tardar un tiempo en recuperar el archivo.
-   La [**función OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) abrirá el archivo o el punto de análisis, en función del uso de la marca **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT.**
-   Los vínculos simbólicos, como puntos de análisis, tienen [ciertas consideraciones de programación](symbolic-link-programming-considerations.md) específicas.
-   Las actividades de administración de volúmenes para leer los registros de diario de cambio de número de secuencia de actualización (USN) requieren un control especial para los puntos de reanográfica cuando se usan las estructuras [**USN \_ RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y [**READ \_ USN \_ JOURNAL \_ DATA.**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Determinar si un directorio es una carpeta montada](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Creación de carpetas montadas](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Efectos simbólicos de vínculo en funciones de sistemas de archivos](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
