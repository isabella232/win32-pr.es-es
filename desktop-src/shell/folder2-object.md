---
description: Extiende el objeto de carpeta para admitir carpetas sin conexión.
title: Objeto Carpeta2 (Shldisp. h)
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
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985498"
---
# <a name="folder2-object"></a>Carpeta2 (objeto)

Extiende el objeto de [**carpeta**](folder.md) para admitir carpetas sin conexión.

## <a name="members"></a>Miembros

El objeto **Carpeta2** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **Carpeta2** tiene estos métodos.



| Método                                                                 | Descripción                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBarricade**](folder2-dismissedwebviewbarricade.md) | Se llama en respuesta a la vista Web Barricade que el usuario está descartando.<br/> |
| [**Sincronizándose**](folder2-synchronize.md)                             | Sincroniza todos los archivos sin conexión de la carpeta.<br/>                             |



 

### <a name="properties"></a>Propiedades

El objeto **Carpeta2** tiene estas propiedades.



| Propiedad                                                                            | Tipo de acceso          | Descripción                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Solo lectura<br/> | No se admite actualmente.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Solo lectura<br/> | Contiene el estado sin conexión de la carpeta.<br/>                     |
| [**Mismo**](folder2-self.md)<br/>                                             | Solo lectura<br/> | Contiene el objeto [**carpeta**](folderitem.md) de la carpeta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Carpeta**](folder.md)
</dt> </dl>

 

 




