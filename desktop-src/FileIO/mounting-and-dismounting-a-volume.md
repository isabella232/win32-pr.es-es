---
description: La creación de una carpeta montada es un proceso de dos pasos.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Crear carpetas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069905"
---
# <a name="creating-mounted-folders"></a>Crear carpetas montadas

La creación de una carpeta montada es un proceso de dos pasos. En primer lugar, llame a [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) con el punto de montaje (letra de unidad, ruta de acceso GUID del volumen o carpeta montada) del volumen que se va a asignar a la carpeta montada. A continuación, use [**la función SetVolumeMountPoint para**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) asociar la ruta de acceso GUID del volumen devuelta con el directorio deseado en otro volumen. Para obtener código de ejemplo, [vea Crear una carpeta montada.](mounting-a-volume-at-a-mount-point.md)

La aplicación puede designar cualquier directorio vacío en un volumen que no sea la raíz como una carpeta montada. Cuando se llama a [**la función SetVolumeMountPoint,**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) ese directorio se convierte en la carpeta montada. Puede asignar el mismo volumen a varias carpetas montadas.

Una vez establecida la carpeta montada, se mantiene mediante reinicios automáticos del equipo.

Si se produce un error en un volumen, ya no se puede acceder a los volúmenes asignados a carpetas montadas en ese volumen a través de esas carpetas montadas. Por ejemplo, supongamos que tiene dos volúmenes, C: y D:, y que D: está asociado a la carpeta montada C: \\ MountD \\ . Si se produce un error en el volumen C: , ya no se puede acceder al volumen D: a través de la ruta de acceso C: \\ MountD \\ .

Solo los volúmenes del sistema de archivos NTFS pueden tener carpetas montadas, pero los volúmenes de destino de las carpetas montadas pueden ser volúmenes que no sean NTFS.

Las carpetas montadas se implementan mediante puntos de reanúblo y están sujetas a sus restricciones. Para obtener más información, vea [Puntos de reanción.](reparse-points.md) No es necesario manipular puntos de reanús para usar carpetas montadas; Las funciones como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) controlan todos los detalles del punto de reanútil.

Dado que las carpetas montadas son directorios, puede cambiar el nombre, quitarlos, moverlos y manipularlos de otro modo, como haría con otros directorios.

(Nota: La documentación de TechNet usa el término unidades *montadas* para hacer referencia a *las carpetas montadas).*

 

 



