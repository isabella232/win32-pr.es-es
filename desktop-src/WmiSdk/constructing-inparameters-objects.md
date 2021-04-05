---
description: Un objeto Parameters contiene la lista de parámetros para llamar a métodos de proveedor cuando se usa un tipo ExecMethod de llamada.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Construir objetos Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908683"
---
# <a name="constructing-inparameters-objects"></a>Construir objetos Parameters

Un objeto [**Parameters**](swbemmethod-inparameters.md) contiene la lista de parámetros para llamar a métodos de proveedor cuando se usa un tipo **ExecMethod** de llamada. Los métodos [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)y [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requieren un objeto Parameters. 

En el procedimiento siguiente se describe cómo construir un objeto [**Parameters**](swbemmethod-inparameters.md) .

**Para construir el parámetro *objwbemInParams***

1.  Conéctese a WMI.
2.  Obtenga la definición de la clase WMI que define el método que desea ejecutar.
3.  Obtener un objeto [**Parameters**](swbemmethod-inparameters.md) específico del método de clase WMI que se desea ejecutar.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Establezca las propiedades de la instancia en cualquier valor que sea adecuado. Asegúrese de proporcionar valores a las propiedades de clave en la clase WMI que contiene el método que desea ejecutar.

    Por ejemplo, si desea establecer un parámetro de entrada denominado myinputparam en el valor "ABC" en una instancia de [**Parameters**](swbemmethod-inparameters.md) denominada "inst", el código tendría este aspecto.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Ejecute el método y obtenga el estado de retorno del método que está ejecutando.

En el ejemplo de código siguiente se muestra cómo configurar el objeto [**Parameters**](swbemmethod-inparameters.md) para crear un nuevo objeto WMI que representa un recurso compartido. Para obtener más información sobre el objeto [**Parameters**](swbemmethod-outparameters.md) , vea [analizar objetos Parameters](parsing-outparameters-objects.md). Este ejemplo devuelve un valor devuelto correcto (0) si hay una carpeta denominada "Share" en la ubicación "C:/Share". Este ejemplo permite que esta carpeta se comparta con otros usuarios.


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



 

 



