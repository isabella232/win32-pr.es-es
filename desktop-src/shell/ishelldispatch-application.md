---
description: Contiene un objeto que representa una aplicación.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Propiedad IShellDispatch.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257037"
---
# <a name="ishelldispatchapplication-property"></a>IShellDispatch.Application, propiedad

Contiene un objeto que representa una aplicación.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Valor de propiedad

Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de aplicación.

## <a name="remarks"></a>Observaciones

Esta propiedad se implementa y se accede a través de la [**propiedad Shell.EjectPC.**](shell-ejectpc.md)

La **propiedad Application** devuelve el objeto de automatización admitido por la aplicación que contiene el control WebBrowser, si ese objeto es accesible. De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.

Use esta propiedad con los comandos **Set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia del Windows Internet Explorer aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
