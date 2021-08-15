---
description: Un objeto InParameters contiene la lista de parámetros para llamar a métodos de proveedor cuando se usa un tipo de llamada ExecMethod.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Construir objetos InParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc13a51687954331a050337fe785bab29b23ee9c72785ffde78d4f8a8e0d198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131587"
---
# <a name="constructing-inparameters-objects"></a>Construir objetos InParameters

Un [**objeto InParameters**](swbemmethod-inparameters.md) contiene la lista de parámetros para llamar a métodos de proveedor cuando se usa un tipo de llamada **ExecMethod.** Los [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md),SWbemObject.Exe [**cMethodAsync \_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)ySWbemServices.Exe [**métodos cMethodAsync**](swbemservices-execmethodasync.md) requieren un **objeto InParameters.**

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

En el ejemplo de código siguiente se muestra cómo configurar el [**objeto InParameters**](swbemmethod-inparameters.md) para crear un nuevo objeto WMI que representa un recurso compartido. Para obtener más información sobre [**el objeto OutParameters,**](swbemmethod-outparameters.md) vea [Analizar objetos OutParameters](parsing-outparameters-objects.md). Este ejemplo devuelve un valor devuelto correcto (0) si hay una carpeta denominada "Share" en la ubicación "C:/Share". Este ejemplo permite que esta carpeta se comparta con otros usuarios.


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



 

 



