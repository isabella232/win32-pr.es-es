---
description: Antes de tener acceso a los archivos y directorios de un volumen determinado, debe determinar las capacidades del sistema de archivos mediante la función GetVolumeInformation.
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: Obtención de información de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5323c3f82db1115a81902f156e9366abad31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542750"
---
# <a name="obtaining-volume-information"></a>Obtención de información de volumen

La función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) recupera información sobre el sistema de archivos en un volumen determinado. Esta información incluye el nombre del volumen, el número de serie del volumen, el nombre del sistema de archivos, las marcas del sistema de archivos, la longitud máxima de un nombre de archivo, etc. Antes de tener acceso a los archivos y directorios de un volumen determinado, debe determinar las capacidades del sistema de archivos mediante la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . Esta función devuelve valores que puede usar para adaptar la aplicación para que funcione de forma eficaz con el sistema de archivos.

En general, debe evitar el uso de búferes estáticos para los nombres de archivo y las rutas de acceso. En su lugar, use los valores devueltos por [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) para asignar búferes a medida que los necesite. Si debe usar búferes estáticos, Reserve 256 caracteres para los nombres de archivo y 260 caracteres para las rutas de acceso.

Las funciones [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) y [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recuperan las rutas de acceso al directorio del sistema y al directorio de Windows, respectivamente.

La función [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea) recupera información de la organización sobre un volumen, incluido el número de bytes por sector, el número de sectores por clúster, el número de clústeres libres y el número total de clústeres. Sin embargo, **GetDiskFreeSpace** no puede notificar tamaños de volúmenes mayores de 2 GB. Para asegurarse de que la aplicación funciona con unidades de disco duro de gran capacidad, use la función [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) .

La función [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) indica si el volumen al que hace referencia la letra de unidad especificada es extraíble, fija, de CD-ROM, RAM o unidad de red.

La función [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) identifica los volúmenes presentes. La función [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw) recupera una cadena terminada en null para cada volumen presente. Use estas cadenas siempre que se requiera un directorio raíz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reconocimiento del sistema de archivos](file-system-recognition.md)
</dt> </dl>

 

 
