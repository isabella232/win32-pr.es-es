---
description: Contiene el objeto de aplicación de la colección de elementos de carpeta.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Propiedad FolderItems. Application (Shldisp. h)
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
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153607"
---
# <a name="folderitemsapplication-property"></a>Propiedad FolderItems. Application

Contiene el objeto de **aplicación** de la colección de elementos de carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>Valor de propiedad

Una referencia de objeto al objeto de aplicación.

## <a name="remarks"></a>Observaciones

La propiedad **Application** devuelve el objeto de automatización compatible con la aplicación que contiene el control WebBrowser, si ese objeto es accesible. De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.

Utilice esta propiedad con los comandos **set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de la aplicación de Windows Internet Explorer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 




