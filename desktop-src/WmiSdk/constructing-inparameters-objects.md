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
# <a name="constructing-inparameters-objects"></a><span data-ttu-id="a4d94-103">Construir objetos Parameters</span><span class="sxs-lookup"><span data-stu-id="a4d94-103">Constructing InParameters Objects</span></span>

<span data-ttu-id="a4d94-104">Un objeto [**Parameters**](swbemmethod-inparameters.md) contiene la lista de parámetros para llamar a métodos de proveedor cuando se usa un tipo **ExecMethod** de llamada.</span><span class="sxs-lookup"><span data-stu-id="a4d94-104">An [**InParameters**](swbemmethod-inparameters.md) object contains the parameter list for calling provider methods when using an **ExecMethod** type of call.</span></span> <span data-ttu-id="a4d94-105">Los métodos [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)y [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requieren un objeto Parameters. </span><span class="sxs-lookup"><span data-stu-id="a4d94-105">The [**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods all require an **InParameters** object.</span></span>

<span data-ttu-id="a4d94-106">En el procedimiento siguiente se describe cómo construir un objeto [**Parameters**](swbemmethod-inparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d94-106">The following procedure describes how to construct an [**InParameters**](swbemmethod-inparameters.md) object.</span></span>

<span data-ttu-id="a4d94-107">**Para construir el parámetro *objwbemInParams***</span><span class="sxs-lookup"><span data-stu-id="a4d94-107">**To construct the *objwbemInParams* parameter**</span></span>

1.  <span data-ttu-id="a4d94-108">Conéctese a WMI.</span><span class="sxs-lookup"><span data-stu-id="a4d94-108">Connect to WMI.</span></span>
2.  <span data-ttu-id="a4d94-109">Obtenga la definición de la clase WMI que define el método que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a4d94-109">Obtain the definition of the WMI class that defines the method you want to execute.</span></span>
3.  <span data-ttu-id="a4d94-110">Obtener un objeto [**Parameters**](swbemmethod-inparameters.md) específico del método de clase WMI que se desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a4d94-110">Obtain an [**InParameters**](swbemmethod-inparameters.md) object specific to the WMI class method you want to execute.</span></span>

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  <span data-ttu-id="a4d94-111">Establezca las propiedades de la instancia en cualquier valor que sea adecuado.</span><span class="sxs-lookup"><span data-stu-id="a4d94-111">Set the properties of the instance to whatever values are appropriate.</span></span> <span data-ttu-id="a4d94-112">Asegúrese de proporcionar valores a las propiedades de clave en la clase WMI que contiene el método que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a4d94-112">Be sure to give values to the key properties in the WMI class that contains the method you want to execute.</span></span>

    <span data-ttu-id="a4d94-113">Por ejemplo, si desea establecer un parámetro de entrada denominado myinputparam en el valor "ABC" en una instancia de [**Parameters**](swbemmethod-inparameters.md) denominada "inst", el código tendría este aspecto.</span><span class="sxs-lookup"><span data-stu-id="a4d94-113">For example, if you want to set an input parameter named myinputparam to the value "abc" in an instance of [**InParameters**](swbemmethod-inparameters.md) called "INST", the code would look like this.</span></span>

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  <span data-ttu-id="a4d94-114">Ejecute el método y obtenga el estado de retorno del método que está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a4d94-114">Execute the method and obtain the return status of the method you are executing.</span></span>

<span data-ttu-id="a4d94-115">En el ejemplo de código siguiente se muestra cómo configurar el objeto [**Parameters**](swbemmethod-inparameters.md) para crear un nuevo objeto WMI que representa un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="a4d94-115">The following code example illustrates setting up the [**InParameters**](swbemmethod-inparameters.md) object to create a new WMI object that represents a share.</span></span> <span data-ttu-id="a4d94-116">Para obtener más información sobre el objeto [**Parameters**](swbemmethod-outparameters.md) , vea [analizar objetos Parameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a4d94-116">For more information about the [**OutParameters**](swbemmethod-outparameters.md) object, see [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="a4d94-117">Este ejemplo devuelve un valor devuelto correcto (0) si hay una carpeta denominada "Share" en la ubicación "C:/Share".</span><span class="sxs-lookup"><span data-stu-id="a4d94-117">This example returns a successful return value (0) if there is a folder named "Share" at the location "C:/Share".</span></span> <span data-ttu-id="a4d94-118">Este ejemplo permite que esta carpeta se comparta con otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="a4d94-118">This example enables this folder to be shared with other users.</span></span>


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



 

 



