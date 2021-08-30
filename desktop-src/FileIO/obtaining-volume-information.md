---
description: Antes de acceder a los archivos y directorios de un volumen determinado, debe determinar las funcionalidades del sistema de archivos mediante la función GetVolumeInformation.
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: Obtener información de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fb7f30cac87e43ba5fb1675251fd18fe2ed042bd7950d192ab750c38eaf3f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130725"
---
# <a name="obtaining-volume-information"></a>Obtener información de volumen

La [**función GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) recupera información sobre el sistema de archivos en un volumen determinado. Esta información incluye el nombre del volumen, el número de serie del volumen, el nombre del sistema de archivos, las marcas del sistema de archivos, la longitud máxima de un nombre de archivo, y así sucesivamente. Antes de acceder a los archivos y directorios de un volumen determinado, debe determinar las funcionalidades del sistema de archivos mediante la [**función GetVolumeInformation.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) Esta función devuelve valores que puede usar para adaptar la aplicación para que funcione de forma eficaz con el sistema de archivos.

En general, debe evitar el uso de búferes estáticos para rutas de acceso y nombres de archivo. En su lugar, use los valores devueltos [**por GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) para asignar búferes a medida que los necesite. Si debe usar búferes estáticos, reserve 256 caracteres para los nombres de archivo y 260 caracteres para las rutas de acceso.

Las [**funciones GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) y [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recuperan las rutas de acceso al directorio del sistema y Windows directorio, respectivamente.

La [**función GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea) recupera información organizativa sobre un volumen, incluido el número de bytes por sector, el número de sectores por clúster, el número de clústeres libres y el número total de clústeres. Sin embargo, **GetDiskFreeSpace** no puede notificar tamaños de volumen superiores a 2 GB. Para asegurarse de que la aplicación funciona con unidades de disco duro de gran capacidad, use la [**función GetDiskFreeSpaceEx.**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)

La [**función GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) indica si el volumen al que hace referencia la letra de unidad especificada es una unidad extraíble, fija, CD-ROM, RAM o de red.

La [**función GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) identifica los volúmenes presentes. La [**función GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw) recupera una cadena terminada en NULL para cada volumen presente. Use estas cadenas siempre que se requiera un directorio raíz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reconocimiento del sistema de archivos](file-system-recognition.md)
</dt> </dl>

 

 
