---
description: Códigos de control que se usan con la compresión y descompresión de archivos y con puntos de reanálisis.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Códigos de control de administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912313"
---
# <a name="directory-management-control-codes"></a>Códigos de control de administración de directorios

Los siguientes códigos de control se usan con la [compresión y descompresión de archivos](file-compression-and-decompression.md).



| Código de control                                             | Significado                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**compresión de FSCTL \_ obtener \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Recupera el estado de compresión actual de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por secuencia.<br/>    |
| [**\_configuración de \_ compresión de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Establece el estado de compresión de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por archivo y por directorio.<br/> |



 

Los siguientes códigos de control se utilizan con [puntos de repetición de análisis](reparse-points.md).

## <a name="in-this-section"></a>En esta sección



| Código de control                                                                   | Descripción                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_punto de \_ reanálisis de eliminación de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Elimina un punto de análisis del archivo o directorio especificado.<br/>                                              |
| [**\_punto de \_ repetición de análisis de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Recupera los datos del punto de reanálisis asociados al archivo o directorio identificado por el identificador especificado.<br/> |
| [**\_grupo de \_ análisis de conjunto de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Establece un punto de repetición de análisis en un archivo o directorio.<br/>                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de control de administración de archivos](file-management-control-codes.md)
</dt> <dt>

[Códigos de control de administración del volumen](volume-management-control-codes.md)
</dt> </dl>

 

