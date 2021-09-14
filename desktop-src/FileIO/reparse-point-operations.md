---
description: Describe las operaciones de punto de análisis que puede realizar mediante DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Operaciones de punto de reanción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069856"
---
# <a name="reparse-point-operations"></a>Operaciones de punto de reanción

Para determinar si un sistema de archivos admite puntos de análisis, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine la marca de bits **FILE SUPPORTS \_ \_ REPARSE \_ POINTS.**

La [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) permite establecer, modificar, obtener y quitar puntos de rean aproximado. En la tabla siguiente se describen las operaciones de punto de análisis que puede realizar mediante **DeviceIoControl**.



| Operación                                                           | Descripción                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**PUNTO DE \_ \_ REAN APROXIMADO DE FSCTL SET \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | Permite que el programa que realiza la llamada establezca un nuevo punto de rean aproximado o modifique uno existente.<br/> |
| [**FSCTL \_ GET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | Obtiene la información almacenada en un punto de rean aproximado existente.<br/>                         |
| [**PUNTO DE \_ REAN APROXIMADO \_ DE ELIMINACIÓN DE \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | Quita un punto de reanexa existente.<br/>                                                   |



 

Si va a modificar, obtener o eliminar un punto de análisis, debe especificar la misma etiqueta de análisis en la operación contenida en el archivo. De lo contrario, la operación producirá el error **ERROR \_ REPARSE \_ TAG \_ MISMATCH**. Si va a modificar o eliminar un punto de análisis de análisis, también debe especificar el **GUID** de análisis de análisis en la operación contenida en el archivo. De lo contrario, la operación producirá el error **ERROR \_ REPARSE \_ ATTRIBUTE \_ CONFLICT**.

Para determinar si un archivo o directorio contiene un punto de análisis, use la [**función GetFileAttributes.**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) Si el archivo o directorio tiene un punto de análisis asociado, se establece el atributo **\_ FILE ATTRIBUTE \_ REPARSE \_ POINT.**

Para sobrescribir un punto de análisis existente sin tener ya un identificador para el archivo o directorio, llame a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT**. Esta marca le permite abrir el archivo independientemente de si el filtro del sistema de archivos correspondiente está instalado y funcionando correctamente.

 

