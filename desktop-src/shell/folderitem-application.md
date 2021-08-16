---
description: Contiene el objeto Application del elemento de carpeta.
ms.assetid: cd8d6dea-1d16-4d62-b56b-c915192f730b
title: Propiedad FolderItem.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 684edfbcd830cd0e2f6b70162d045c1f8035dc7e4477ace1c39220bc076215cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860242"
---
# <a name="folderitemapplication-property"></a>Propiedad FolderItem.Application

Contiene el **objeto Application** del elemento de carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objApplication = FolderItem.Application
```



## <a name="property-value"></a>Valor de propiedad

Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el **objeto Application.**

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



 

 
