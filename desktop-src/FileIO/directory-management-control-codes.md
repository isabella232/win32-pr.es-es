---
description: Códigos de control que se usan con compresión y descompresión de archivos y con puntos de análisis.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Códigos de control de administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1354d1a4ce72f2867ece1f15218d9c7cb3f364a12ea3eb0d3b16f66b0954e89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755195"
---
# <a name="directory-management-control-codes"></a>Códigos de control de administración de directorios

Los siguientes códigos de control se usan con compresión [y descompresión de archivos.](file-compression-and-decompression.md)



| Código de control                                             | Significado                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ GET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Recupera el estado de compresión actual de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por secuencia.<br/>    |
| [**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Establece el estado de compresión de un archivo o directorio en un volumen cuyo sistema de archivos admite la compresión por archivo y por directorio.<br/> |



 

Los siguientes códigos de control se usan con [puntos de reanción.](reparse-points.md)

## <a name="in-this-section"></a>En esta sección



| Código de control                                                                   | Descripción                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ DELETE \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Elimina un punto de reanual del archivo o directorio especificado.<br/>                                              |
| [**FSCTL \_ GET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Recupera los datos de punto de reanualción asociados al archivo o directorio identificado por el identificador especificado.<br/> |
| [**FSCTL \_ SET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Establece un punto de análisis en un archivo o directorio.<br/>                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de control de administración de archivos](file-management-control-codes.md)
</dt> <dt>

[Códigos de control de administración del volumen](volume-management-control-codes.md)
</dt> </dl>

 

