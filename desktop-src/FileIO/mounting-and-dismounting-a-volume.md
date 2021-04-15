---
description: La creación de una carpeta montada es un proceso de dos pasos.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Crear carpetas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688658"
---
# <a name="creating-mounted-folders"></a>Crear carpetas montadas

La creación de una carpeta montada es un proceso de dos pasos. En primer lugar, llame a [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) con el punto de montaje (letra de unidad, ruta de acceso de GUID de volumen o carpeta montada) del volumen que se va a asignar a la carpeta montada. A continuación, utilice la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para asociar la ruta de acceso del GUID de volumen devuelta al directorio deseado en otro volumen. Para ver un ejemplo de código, vea [crear una carpeta montada](mounting-a-volume-at-a-mount-point.md).

La aplicación puede designar cualquier directorio vacío en un volumen distinto de la raíz como una carpeta montada. Cuando se llama a la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , ese directorio se convierte en la carpeta montada. Puede asignar el mismo volumen a varias carpetas montadas.

Una vez establecida la carpeta montada, se mantiene a través de los reinicios del equipo automáticamente.

Si se produce un error en un volumen, ya no se puede tener acceso a los volúmenes asignados a las carpetas montadas en ese volumen a través de esas carpetas montadas. Por ejemplo, supongamos que tiene dos volúmenes, C: y D:, y que D: está asociado a la carpeta montada C: \\ montada \\ . Si se produce un error en el volumen C:, ya no se puede acceder al volumen D: a través de la ruta de acceso C: \\ montada \\ .

Solo los volúmenes del sistema de archivos NTFS pueden tener carpetas montadas, pero los volúmenes de destino de las carpetas montadas pueden ser volúmenes que no son NTFS.

Las carpetas montadas se implementan mediante puntos de análisis y están sujetas a sus restricciones. Para obtener más información, vea [puntos de reanálisis](reparse-points.md). No es necesario manipular los puntos de reanálisis para usar carpetas montadas; funciones como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) controlan todos los detalles del punto de reanálisis.

Dado que las carpetas montadas son directorios, puede cambiarles el nombre, quitarlas, moverlas y, de lo contrario, manipularlas, como haría con otros directorios.

(Nota: la documentación de TechNet usa el término *unidades montadas* para hacer referencia a *las carpetas montadas*).

 

 



