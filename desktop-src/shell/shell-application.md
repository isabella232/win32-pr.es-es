---
description: 'Propiedad Shell.Application: contiene el objeto Application del objeto .'
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Propiedad Shell.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5a90b3953ed54b8a3652d6c9c26533d433ffb600
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083863"
---
# <a name="shellapplication-property"></a>Propiedad Shell.Application

Contiene el objeto Application del objeto .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Valor de propiedad

Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto Application.

## <a name="remarks"></a>Comentarios

La **propiedad Application** devuelve el objeto de automatización admitido por la aplicación que contiene el control WebBrowser, si ese objeto es accesible. De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.

Use esta propiedad con los comandos **Set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de windows Internet Explorer aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
