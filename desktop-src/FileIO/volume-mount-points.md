---
description: Con las carpetas montadas, puede unificar sistemas de archivos dispares, como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un sistema de archivos lógico en un único volumen NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Carpetas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe4360377ba94fc23701d13fc62defd666ba9cb3074c4385d98ea87a9354200
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746775"
---
# <a name="mounted-folders"></a>Carpetas montadas

El sistema de archivos NTFS admite carpetas montadas. Una *carpeta montada es* una asociación entre un volumen y un directorio en otro volumen. Cuando se crea una carpeta montada, los usuarios y las aplicaciones pueden acceder al volumen de destino mediante la ruta de acceso a la carpeta montada o mediante la letra de unidad del volumen. Por ejemplo, un usuario puede crear una carpeta montada para asociar la unidad D: con la carpeta C: \\ Mnt \\ DDrive de la unidad C. Después de crear la carpeta montada, el usuario puede usar la ruta de acceso "C: Mnt DDrive" para acceder a la unidad D: como si fuera una carpeta de la \\ \\ unidad C:.

Con las carpetas montadas, puede unificar sistemas de archivos dispares, como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un sistema de archivos lógico en un único volumen NTFS. Ni los usuarios ni las aplicaciones necesitan información sobre el volumen de destino en el que se encuentra un archivo específico. Toda la información que necesitan para buscar un archivo especificado es una ruta de acceso completa mediante una carpeta montada en el volumen NTFS. Los volúmenes se pueden reorganizar, sustituir o subdividir en muchos volúmenes sin que los usuarios o las aplicaciones necesiten cambiar la configuración.

Para obtener información sobre las carpetas montadas, consulte los temas siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                         | Descripción                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creación de carpetas montadas](mounting-and-dismounting-a-volume.md)<br/>                                                  | La creación de una carpeta montada es un proceso de dos pasos.<br/>                                                                                                                                                                 |
| [Enumeración de carpetas montadas](enumerating-volume-mount-points.md)<br/>                                                 | Funciones que se usan para enumerar las carpetas montadas en un volumen.<br/>                                                                                                                                                       |
| [Determinar si un directorio es una carpeta montada](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | Cómo determinar si un directorio especificado es una carpeta montada.<br/>                                                                                                                                              |
| [Asignación de una letra de unidad a un volumen](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | Puede asignar una letra de unidad (por ejemplo, X: a un volumen local mediante la función \) [**SetVolumeMountPoint,**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) siempre que no haya ningún volumen asignado a esa letra de unidad).<br/> |
| [Funciones de carpeta montadas](volume-mount-point-functions.md)<br/>                                                       | Funciones que se usan para administrar carpetas montadas.<br/>                                                                                                                                                                        |



 

Para obtener ejemplos, vea [Ejemplos de carpetas montadas.](volume-mount-point-examples.md)

 

 




