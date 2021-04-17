---
description: Mediante el uso de carpetas montadas, puede unificar sistemas de archivos dispares como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un solo volumen NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Carpetas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687789"
---
# <a name="mounted-folders"></a>Carpetas montadas

El sistema de archivos NTFS admite carpetas montadas. Una *carpeta montada* es una asociación entre un volumen y un directorio de otro volumen. Cuando se crea una carpeta montada, los usuarios y las aplicaciones pueden acceder al volumen de destino mediante la ruta de acceso a la carpeta montada o mediante la letra de unidad del volumen. Por ejemplo, un usuario puede crear una carpeta montada para asociar la unidad D: a la carpeta C: \\ mnt \\ DDrive de la unidad c. Después de crear la carpeta montada, el usuario puede usar la ruta de acceso "C: \\ mnt \\ DDrive" para acceder a la unidad D: como si fuera una carpeta en la unidad C:.

Mediante el uso de carpetas montadas, puede unificar sistemas de archivos dispares como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un solo volumen NTFS. Ni los usuarios ni las aplicaciones necesitan información sobre el volumen de destino en el que se encuentra un archivo específico. Toda la información que necesitan para localizar un archivo específico es una ruta de acceso completa que usa una carpeta montada en el volumen NTFS. Los volúmenes se pueden reorganizar, sustituir o subdividir en muchos volúmenes sin necesidad de que los usuarios o las aplicaciones cambien la configuración.

Para obtener información sobre las carpetas montadas, vea los temas siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                         | Descripción                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Crear carpetas montadas](mounting-and-dismounting-a-volume.md)<br/>                                                  | La creación de una carpeta montada es un proceso de dos pasos.<br/>                                                                                                                                                                 |
| [Enumerar carpetas montadas](enumerating-volume-mount-points.md)<br/>                                                 | Funciones que se usan para enumerar las carpetas montadas en un volumen.<br/>                                                                                                                                                       |
| [Determinar si un directorio es una carpeta montada](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | Cómo determinar si un directorio especificado es una carpeta montada.<br/>                                                                                                                                              |
| [Asignación de una letra de unidad a un volumen](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | Puede asignar una letra de unidad (por ejemplo, X: \) a un volumen local mediante la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , siempre que no haya ningún volumen ya asignado a esa letra de unidad).<br/> |
| [Funciones de carpeta montada](volume-mount-point-functions.md)<br/>                                                       | Funciones que se usan para administrar carpetas montadas.<br/>                                                                                                                                                                        |



 

Para obtener ejemplos, vea [ejemplos de carpeta montada](volume-mount-point-examples.md).

 

 




