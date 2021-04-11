---
description: Se crea un objeto SWbemMethod. Parameters y se proporciona con datos mediante el método de proveedor que se está ejecutando.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analizar objetos Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361378"
---
# <a name="parsing-outparameters-objects"></a>Analizar objetos Parameters

Se crea un objeto [**SWbemMethod. Parameters**](swbemmethod-outparameters.md) y se proporciona con datos mediante el método de proveedor que se está ejecutando. Las propiedades del objeto **Parameters** son específicas del método llamado. Por ejemplo, en el script siguiente, *SD* (incluido en *outParam*) es el parámetro de salida definido para el método **\_ \_ SystemSecurity.** . La propiedad **ReturnValue** es una propiedad genérica disponible para todos los objetos **Parameters** que contienen el resultado de la operación.

En el ejemplo de código siguiente se muestra cómo obtener los parámetros de salida de la ejecución [**del método obtenido en la clase**](--systemsecurity-getsd.md) [**\_ \_ SystemSecurity**](--systemsecurity.md) para el sistema local.


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



Para obtener más información, consulte [**SWbemMethod. Parameters**](swbemmethod-inparameters.md).

 

 



