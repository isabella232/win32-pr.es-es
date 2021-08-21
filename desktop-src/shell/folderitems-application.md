---
description: Contiene el objeto Application de la colección de elementos de carpeta.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Propiedad FolderItems.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3809d76576b69c53f6fc5f8a11ab954242e3a89c9a369ada2f4fa47c460f523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032613"
---
# <a name="folderitemsapplication-property"></a>Propiedad FolderItems.Application

Contiene el **objeto Application** de la colección de elementos de carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>Valor de propiedad

Referencia de objeto al objeto Application.

## <a name="remarks"></a>Comentarios

La **propiedad Application** devuelve el objeto de automatización admitido por la aplicación que contiene el control WebBrowser, si ese objeto es accesible. De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.

Use esta propiedad con los **comandos Set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de la Windows Internet Explorer aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




