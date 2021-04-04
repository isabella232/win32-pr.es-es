---
description: Describe las operaciones de punto de reanálisis que se pueden realizar mediante DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Operaciones de punto de análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083160"
---
# <a name="reparse-point-operations"></a>Operaciones de punto de análisis

Para determinar si un sistema de archivos admite puntos de análisis, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine el archivo compatible con la marca de bits **\_ \_ \_ puntos de reanálisis** .

La función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) permite establecer, modificar, obtener y quitar puntos de reanálisis. En la tabla siguiente se describen las operaciones de punto de reanálisis que se pueden realizar con **DeviceIoControl**.



| Operación                                                           | Descripción                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_grupo de \_ análisis de conjunto de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | Permite al programa que realiza la llamada establecer un nuevo punto de análisis o modificar uno existente.<br/> |
| [**\_punto de \_ repetición de análisis de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | Obtiene la información almacenada en un punto de reanálisis existente.<br/>                         |
| [**\_punto de \_ reanálisis de eliminación de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | Quita un punto de reanálisis existente.<br/>                                                   |



 

Si va a modificar, obtener o eliminar un punto de repetición de análisis, debe especificar la misma etiqueta de reanálisis en la operación incluida en el archivo. De lo contrario, se producirá un error en la operación y la **etiqueta de REanálisis de errores de error \_ \_ \_ no coincide**. Si va a modificar o eliminar un punto de repetición de análisis, también debe especificar el **GUID** de reanálisis en la operación contenida en el archivo. De lo contrario, se producirá un error en la operación con el **\_ conflicto de \_ atributos \_ de reanálisis de errores**.

Para determinar si un archivo o directorio contiene un punto de reanálisis, utilice la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) . Si el archivo o el directorio tiene un punto de análisis asociado, se establece el atributo de **\_ \_ \_ punto de reanálisis del atributo de archivo** .

Para sobrescribir un punto de reanálisis existente sin tener ya un identificador para el archivo o directorio, llame a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el **marcador de archivo abrir el \_ \_ \_ \_ punto de reanálisis**. Esta marca permite abrir el archivo independientemente de si el filtro del sistema de archivos correspondiente está instalado y funciona correctamente.

 

