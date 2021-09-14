---
description: Extiende el objeto Folder para admitir carpetas sin conexión.
title: Objeto Folder2 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363126"
---
# <a name="folder2-object"></a>Objeto Folder2

Extiende el objeto [**Folder para**](folder.md) admitir carpetas sin conexión.

## <a name="members"></a>Members

El **objeto Folder2** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Folder2** tiene estos métodos.



| Método                                                                 | Descripción                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBarricade**](folder2-dismissedwebviewbarricade.md) | Se llama en respuesta a que el usuario descarta la vista web.<br/> |
| [**Sincronizar**](folder2-synchronize.md)                             | Sincroniza todos los archivos sin conexión de la carpeta .<br/>                             |



 

### <a name="properties"></a>Propiedades

El **objeto Folder2** tiene estas propiedades.



| Propiedad.                                                                            | Tipo de acceso          | Descripción                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Solo lectura<br/> | No se admite actualmente.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Solo lectura<br/> | Contiene el estado sin conexión de la carpeta.<br/>                     |
| [**Propio**](folder2-self.md)<br/>                                             | Solo lectura<br/> | Contiene el objeto [**FolderItem de la**](folderitem.md) carpeta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Carpeta**](folder.md)
</dt> </dl>

 

 




