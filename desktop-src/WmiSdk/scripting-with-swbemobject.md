---
description: El objeto de scripting SWbemObject es el objeto WMI genérico, que define las propiedades y los métodos que se pueden utilizar independientemente del objeto WMI específico al que está enlazado el objeto SWbemObject.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Scripting con SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155853"
---
# <a name="scripting-with-swbemobject"></a><span data-ttu-id="503de-103">Scripting con SWbemObject</span><span class="sxs-lookup"><span data-stu-id="503de-103">Scripting with SWbemObject</span></span>

<span data-ttu-id="503de-104">El objeto de scripting [**SWbemObject**](swbemobject.md) es el objeto WMI genérico, que define las propiedades y los métodos que se pueden utilizar independientemente del objeto WMI específico al que está enlazado el objeto **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="503de-104">The [**SWbemObject**](swbemobject.md) scripting object is the generic WMI object, defining properties and methods that can be used regardless of the specific WMI object to which the **SWbemObject** object is bound.</span></span> <span data-ttu-id="503de-105">Todos los objetos de WMI, como una instancia [**del \_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) o cualquier otra clase de datos de WMI, se representan mediante [**SWbemObject**](swbemobject.md) y pueden usar las propiedades y métodos comunes de **SWbemObject** además de sus propias propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="503de-105">All WMI objects, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or any other WMI data class, are represented by [**SWbemObject**](swbemobject.md) and can use the **SWbemObject** common properties and methods in addition to their own particular properties and methods.</span></span>

<span data-ttu-id="503de-106">Por ejemplo, use el siguiente script para obtener todas las instancias de un [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) llamando al método [**SWbemObject \_ . instances**](swbemobject-instances-.md) .</span><span class="sxs-lookup"><span data-stu-id="503de-106">For example, use the following script to obtain all of the instances of a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) by calling the [**SWbemObject.Instances\_**](swbemobject-instances-.md) method.</span></span> <span data-ttu-id="503de-107">ClsobjProcess representa la definición de clase de **\_ proceso de Win32** y un [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="503de-107">The clsobjProcess represents both the **Win32\_Process** class definition and an [**SWbemObject**](swbemobject.md).</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="503de-108">En el ejemplo siguiente se obtiene una instancia específica [**del \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) que representa el servicio de alerta y la almacena en objAlerter.</span><span class="sxs-lookup"><span data-stu-id="503de-108">The following example obtains a specific instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) that represents the Alerter service and stores it in objAlerter.</span></span> <span data-ttu-id="503de-109">A continuación, puede llamar a métodos [**SWbemObject**](swbemobject.md) , como Wscript. echo ObjAlerter. Path \_ , o a los métodos definidos por la clase de datos, como Wscript. echo objAlerter. state.</span><span class="sxs-lookup"><span data-stu-id="503de-109">You can then call either [**SWbemObject**](swbemobject.md) methods, such as WScript.Echo objAlerter.Path\_, or methods defined by the data class, such as WScript.Echo objAlerter.State.</span></span> <span data-ttu-id="503de-110">objAlerter que representa una instancia del servicio de Win32 \_ y un **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="503de-110">objAlerter which represents both an instance of Win32\_Service and an **SWbemObject**.</span></span>


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



<span data-ttu-id="503de-111">La llamada a [**SWbemObject. \_ instances**](swbemobject-instances-.md) obtiene otro objeto de scripting de WMI genérico, [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="503de-111">The call to [**SWbemObject.Instances\_**](swbemobject-instances-.md) obtains another generic WMI scripting object, [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="503de-112">Como se muestra, el objeto **SWbemObjectSet** se puede tratar como una [colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="503de-112">As shown, the **SWbemObjectSet** object can be treated as a [collection](accessing-a-collection.md).</span></span>


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



<span data-ttu-id="503de-113">Puede identificar los métodos de [**SWbemObject**](swbemobject.md) porque finalizan con un carácter de subrayado ( \_ ), por ejemplo, [**SWbemObject \_ . instances**](swbemobject-instances-.md).</span><span class="sxs-lookup"><span data-stu-id="503de-113">You can identify the [**SWbemObject**](swbemobject.md) methods because they all end with an underscore (\_), for example, [**SWbemObject.Instances\_**](swbemobject-instances-.md).</span></span>

<span data-ttu-id="503de-114">[**SWbemObjectEx**](swbemobjectex.md) extiende las propiedades de [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="503de-114">[**SWbemObjectEx**](swbemobjectex.md) extends the properties of [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="503de-115">Por ejemplo, ahora puede actualizar los datos de cualquier objeto WMI, como una instancia del proceso de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process), mediante una llamada a [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md).</span><span class="sxs-lookup"><span data-stu-id="503de-115">For example, you can now update the data of any WMI object, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process), by a call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md).</span></span>

<span data-ttu-id="503de-116">En el ejemplo siguiente se muestra cómo se pueden actualizar los datos de error de página de proceso del sistema cada cinco segundos.</span><span class="sxs-lookup"><span data-stu-id="503de-116">The following example shows how the system process page fault data can be refreshed every five seconds.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



<span data-ttu-id="503de-117">Para obtener más información sobre la actualización de datos mediante un objeto [**SWbemRefresher**](swbemrefresher.md) , vea [actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="503de-117">For more information about refreshing data using an [**SWbemRefresher**](swbemrefresher.md) object, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="503de-118">[**SWbemObject. put \_**](swbemobject-put-.md) y [**PutAsync \_**](swbemobject-putasync-.md) permiten volver a escribir los cambios en cualquier objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="503de-118">The [**SWbemObject.Put\_**](swbemobject-put-.md) and [**PutAsync\_**](swbemobject-putasync-.md) allow you to write changes back to any WMI object.</span></span> <span data-ttu-id="503de-119">Estos métodos solo confirman los cambios en un objeto en el espacio de nombres donde se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="503de-119">These methods only commit changes to an object in the namespace where the object was created.</span></span> <span data-ttu-id="503de-120">Puede escribir el objeto en un espacio de nombres diferente mediante [**SWbemServicesEx. put**](swbemservicesex-put.md) o [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md).</span><span class="sxs-lookup"><span data-stu-id="503de-120">You can write the object to a different namespace using [**SWbemServicesEx.Put**](swbemservicesex-put.md) or [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="503de-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="503de-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="503de-122">API de scripting para WMI</span><span class="sxs-lookup"><span data-stu-id="503de-122">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="503de-123">Creación de un script de WMI</span><span class="sxs-lookup"><span data-stu-id="503de-123">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="503de-124">Actualizar una instancia completa</span><span class="sxs-lookup"><span data-stu-id="503de-124">Updating an Entire Instance</span></span>](updating-an-entire-instance.md)
</dt> <dt>

[<span data-ttu-id="503de-125">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="503de-125">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
