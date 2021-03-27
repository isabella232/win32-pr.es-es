---
description: Contiene el objeto de aplicación de la carpeta.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Propiedad Folder. Application (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496781"
---
# <a name="folderapplication-property"></a>Folder. Application (propiedad)

Contiene el objeto de aplicación de la carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Application = Folder.Application
```



## <a name="property-value"></a>Valor de propiedad

Una referencia de objeto al objeto de aplicación.

## <a name="remarks"></a>Observaciones

La propiedad **Application** devuelve el objeto de automatización compatible con la aplicación que contiene el control WebBrowser, si ese objeto es accesible. De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.

Utilice esta propiedad con los comandos **set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de la aplicación de Internet Explorer.

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL). Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                 |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




