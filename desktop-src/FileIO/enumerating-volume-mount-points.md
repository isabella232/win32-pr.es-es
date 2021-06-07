---
description: Funciones que se usan para enumerar las carpetas montadas en un volumen.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Enumeración de carpetas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b047e4af74f33d6bc56476734f0f39c41dd14f
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386664"
---
# <a name="enumerating-mounted-folders"></a>Enumeración de carpetas montadas

Las siguientes funciones se usan para enumerar las carpetas montadas en un volumen NTFS especificado:

-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Estas funciones funcionan de forma muy similar a las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)y [**FindClose.**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)

Para enumerar las carpetas montadas en un volumen, primero debe averiguar si el volumen admite carpetas montadas. Para ello, use el nombre del volumen devuelto por las funciones [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) y [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) para llamar a la [**función GetVolumeInformation.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) Los nombres devueltos incluyen una barra diagonal inversa final ( ) para que sea compatible con la \\ [**función GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) y las funciones relacionadas. Para obtener más información sobre las funciones que se usan para examinar los volúmenes en un equipo, vea [Enumerar volúmenes](enumerating-volumes.md). Cuando se llama a **la función GetVolumeInformation,** si se devuelve "NTFS" en el parámetro *lpFileSystemNameBuffer,* el volumen es un volumen NTFS. El sistema de archivos NTFS admite carpetas montadas.

Si el volumen es un volumen NTFS, inicie una búsqueda de las carpetas montadas llamando a [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa). Si la búsqueda se realiza correctamente, procese los resultados según los requisitos de la aplicación. A [**continuación, use FindNextVolumeMountPoint en**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) un bucle para buscar y procesar las carpetas montadas de una en una. Cuando no haya más carpetas montadas para enumerar, cierre el identificador de búsqueda mediante una llamada a [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose). Tenga en cuenta que la búsqueda solo encontrará las carpetas montadas que están en el volumen especificado.

No debe asumir ninguna correlación entre el orden de las carpetas montadas que devuelven estas funciones y el orden de las carpetas montadas que devuelven otras funciones o herramientas.

 

 



