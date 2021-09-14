---
description: El método de proveedor que se está ejecutando crea un objeto SWbemMethod.OutParameters y proporciona datos.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analizar objetos OutParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063945"
---
# <a name="parsing-outparameters-objects"></a>Analizar objetos OutParameters

El método de proveedor que se está ejecutando crea un objeto [**SWbemMethod.OutParameters**](swbemmethod-outparameters.md) y proporciona datos. Las propiedades del **objeto OutParameters** son específicas del método llamado. Por ejemplo, en el script siguiente, *SD* (incluido en *outParam)* es el parámetro de salida definido para el **\_ \_ método SystemSecurity.GetSD.** La **propiedad ReturnValue** es una propiedad genérica disponible para todos los **objetos OutParameters** que contienen el resultado de la operación.

En el ejemplo de código siguiente se muestra cómo obtener parámetros de salida al ejecutar el [**método GetSD**](--systemsecurity-getsd.md) en la clase [**\_ \_ SystemSecurity**](--systemsecurity.md) para el sistema local.


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



Para obtener más información, [**vea SWbemMethod.InParameters**](swbemmethod-inparameters.md).

 

 



