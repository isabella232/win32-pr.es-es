---
description: Un objeto InParameters contiene la lista de parámetros para llamar a métodos de proveedor cuando se usa un tipo de llamada ExecMethod.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Construcción de objetos InParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465900"
---
# <a name="constructing-inparameters-objects"></a>Construcción de objetos InParameters

Un [**objeto InParameters**](swbemmethod-inparameters.md) contiene la lista de parámetros para llamar a métodos de proveedor cuando se usa un tipo de llamada **ExecMethod.** Los métodos [**SWbemObject.ExecMethod \_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync, \_**](swbemobject-execmethodasync-.md) [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)y [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requieren un **objeto InParameters.**

En el procedimiento siguiente se describe cómo construir un [**objeto InParameters.**](swbemmethod-inparameters.md)

**Para construir el *parámetro objwbemInParams***

1.  Conectar a WMI.
2.  Obtenga la definición de la clase WMI que define el método que desea ejecutar.
3.  Obtenga un [**objeto InParameters**](swbemmethod-inparameters.md) específico del método de clase WMI que desea ejecutar.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Establezca las propiedades de la instancia en los valores que sean adecuados. Asegúrese de proporcionar valores a las propiedades de clave de la clase WMI que contiene el método que desea ejecutar.

    Por ejemplo, si desea establecer un parámetro de entrada denominado myinputparam en el valor "abc" en una instancia de [**InParameters**](swbemmethod-inparameters.md) denominada "INST", el código tendría este aspecto.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Ejecute el método y obtenga el estado devuelto del método que está ejecutando.

En el ejemplo de código siguiente se muestra cómo configurar el [**objeto InParameters**](swbemmethod-inparameters.md) para crear un nuevo objeto WMI que representa un recurso compartido. Para obtener más información sobre el [**objeto OutParameters,**](swbemmethod-outparameters.md) vea [Analizar objetos OutParameters](parsing-outparameters-objects.md). Este ejemplo devuelve un valor devuelto correcto (0) si hay una carpeta denominada "Share" en la ubicación "C:/Share". Este ejemplo permite que esta carpeta se comparta con otros usuarios.


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



