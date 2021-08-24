---
description: Los volúmenes se implementan mediante un controlador de dispositivo denominado administrador de volúmenes.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Acerca de la administración de volúmenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5446726b7caf448eef74884e8b6afc9d27dc4d4fdc6ffadd4572e667aaeb2cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766315"
---
# <a name="about-volume-management"></a>Acerca de la administración de volúmenes

Los volúmenes se implementan mediante un controlador de dispositivo denominado administrador de volúmenes. Algunos ejemplos son ftdisk manager, logical disk manager (LDM) y VERITAS Logical Volume Manager (LVM). Los administradores de volúmenes proporcionan una capa de abstracción física, protección de datos (mediante algún tipo de RAID) y rendimiento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconocimiento del sistema de archivos](file-system-recognition.md)<br/>           | El objetivo del reconocimiento del sistema de archivos es permitir que el sistema operativo Windows tenga una opción adicional para un sistema de archivos válido pero no reconocido que no sea "RAW".<br/>                                                                                                         |
| [Asignar un nombre a un volumen](naming-a-volume.md)<br/>                           | Una etiqueta es un nombre descriptivo que se asigna a un volumen, normalmente por un usuario final, para que sea más fácil de reconocer. Un volumen puede tener una etiqueta, una letra de unidad, ambas o ninguna. Para establecer la etiqueta de un volumen, use la [**función SetVolumeLabel.**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/> |
| [Enumeración de volúmenes](enumerating-volumes.md)<br/>                   | Para crear una lista completa de los volúmenes de un equipo o manipular cada volumen a su vez, puede enumerar los volúmenes.<br/>                                                                                                                                                       |
| [Obtención de información de volumen](obtaining-volume-information.md)<br/> | Antes de acceder a los archivos y directorios de un volumen determinado, debe determinar las funcionalidades del sistema de archivos mediante la [**función GetVolumeInformation.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                              |
| [Cambiar diario](change-journals.md)<br/>                           | Cuando se realiza algún cambio en un archivo o directorio de un volumen, el diario de cambios de USN de ese volumen se actualiza con una descripción del cambio y el nombre del archivo o directorio.<br/>                                                                                        |
| [Carpetas montadas](volume-mount-points.md)<br/>                       | Con las carpetas montadas, puede unificar sistemas de archivos dispares, como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un sistema de archivos lógico en un único volumen NTFS.<br/>                                                      |
| [Tabla de archivos maestros](master-file-table.md)<br/>                       | Toda la información sobre un archivo, incluidos su tamaño, marcas de hora y fecha, permisos y contenido de datos, se almacena en entradas de la tabla de archivos maestras (MFT) o en un espacio fuera de MFT descrito por las entradas de MFT.<br/>                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia técnica de discos y volúmenes básicos](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Referencia técnica de discos dinámicos y volúmenes](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Referencia de administración de volúmenes](volume-management-reference.md)
</dt> </dl>

 

