---
description: Los volúmenes se implementan mediante un controlador de dispositivo denominado administrador de volúmenes.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Acerca de la administración de volúmenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688480"
---
# <a name="about-volume-management"></a>Acerca de la administración de volúmenes

Los volúmenes se implementan mediante un controlador de dispositivo denominado administrador de volúmenes. Algunos ejemplos son el administrador de FtDisk, el administrador de discos lógicos (LDM) y el administrador de volúmenes lógicos (LVM) de VERITAS. Los administradores de volúmenes ofrecen una capa de abstracción física, protección de datos (con algún tipo de RAID) y rendimiento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconocimiento del sistema de archivos](file-system-recognition.md)<br/>           | El objetivo del reconocimiento del sistema de archivos es permitir que el sistema operativo Windows tenga una opción adicional para un sistema de archivos válido pero no reconocido distinto de "sin procesar".<br/>                                                                                                         |
| [Asignar un nombre a un volumen](naming-a-volume.md)<br/>                           | Una etiqueta es un nombre descriptivo que se asigna a un volumen, normalmente por un usuario final, para que sea más fácil de reconocer. Un volumen puede tener una etiqueta, una letra de unidad, ambas o ninguna de ellas. Para establecer la etiqueta de un volumen, utilice la función [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .<br/> |
| [Enumerar volúmenes](enumerating-volumes.md)<br/>                   | Para realizar una lista completa de los volúmenes de un equipo o para manipular cada volumen a su vez, puede enumerar los volúmenes.<br/>                                                                                                                                                       |
| [Obtención de información de volumen](obtaining-volume-information.md)<br/> | Antes de tener acceso a los archivos y directorios de un volumen determinado, debe determinar las capacidades del sistema de archivos mediante la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) .<br/>                                                                              |
| [Cambiar diarios](change-journals.md)<br/>                           | Cuando se realiza cualquier cambio en un archivo o directorio de un volumen, el diario de cambios USN para ese volumen se actualiza con una descripción del cambio y el nombre del archivo o directorio.<br/>                                                                                        |
| [Carpetas montadas](volume-mount-points.md)<br/>                       | Mediante el uso de carpetas montadas, puede unificar sistemas de archivos dispares como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un solo volumen NTFS.<br/>                                                      |
| [Tabla de archivos maestros](master-file-table.md)<br/>                       | Toda la información acerca de un archivo, incluido el tamaño, las marcas de fecha y hora, los permisos y el contenido de los datos, se almacena en las entradas de la tabla maestra de archivos (MFT) o en el espacio fuera de la MFT que se describe en las entradas de MFT.<br/>                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia técnica de discos y volúmenes básicos](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Referencia técnica de volúmenes y discos dinámicos](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Referencia de administración de volúmenes](volume-management-reference.md)
</dt> </dl>

 

