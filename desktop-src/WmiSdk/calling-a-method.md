---
description: WMI proporciona métodos en la API de COM y la API de scripting para obtener información o manipular objetos en un sistema empresarial.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Llamar a un método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697844"
---
# <a name="calling-a-wmi-method"></a><span data-ttu-id="491e9-103">Llamar a un método WMI</span><span class="sxs-lookup"><span data-stu-id="491e9-103">Calling a WMI Method</span></span>

<span data-ttu-id="491e9-104">WMI proporciona métodos en la [API de com](com-api-for-wmi.md) y la [API de scripting](scripting-api-for-wmi.md) para obtener información o manipular objetos en un sistema empresarial.</span><span class="sxs-lookup"><span data-stu-id="491e9-104">WMI supplies methods in the [COM API](com-api-for-wmi.md) and the [scripting API](scripting-api-for-wmi.md) to obtain information or manipulate objects in an enterprise system.</span></span> <span data-ttu-id="491e9-105">Por ejemplo, el método de scripting de WMI [**SWbemServices.ExecQuery**](swbemservices-execquery.md) consulta los datos.</span><span class="sxs-lookup"><span data-stu-id="491e9-105">For example, the WMI scripting method [**SWbemServices.ExecQuery**](swbemservices-execquery.md) queries for data.</span></span> <span data-ttu-id="491e9-106">Los proveedores también tienen métodos definidos en las clases que registran.</span><span class="sxs-lookup"><span data-stu-id="491e9-106">Providers also have methods defined in the classes they register.</span></span> <span data-ttu-id="491e9-107">Algunos ejemplos son los métodos [**\_ lógicos Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , [**CHKDSK**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) y [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) suministrados por el [proveedor de Win32](/windows/desktop/CIMWin32Prov/win32-provider).</span><span class="sxs-lookup"><span data-stu-id="491e9-107">Examples are the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) methods [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) and [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) supplied by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider).</span></span>

<span data-ttu-id="491e9-108">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="491e9-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="491e9-109">Métodos de WMI en comparación con los métodos de proveedor</span><span class="sxs-lookup"><span data-stu-id="491e9-109">WMI Methods Compared to Provider Methods</span></span>](#wmi-methods-compared-to-provider-methods)
-   [<span data-ttu-id="491e9-110">Modos de llamada a métodos en WMI</span><span class="sxs-lookup"><span data-stu-id="491e9-110">Method-Calling Modes in WMI</span></span>](#method-calling-modes-in-wmi)
    -   [<span data-ttu-id="491e9-111">Modo sincrónico</span><span class="sxs-lookup"><span data-stu-id="491e9-111">Synchronous Mode</span></span>](#synchronous-mode)
    -   [<span data-ttu-id="491e9-112">Modo asincrónico</span><span class="sxs-lookup"><span data-stu-id="491e9-112">Asynchronous Mode</span></span>](#asynchronous-mode)
    -   [<span data-ttu-id="491e9-113">Modo semisincrónico</span><span class="sxs-lookup"><span data-stu-id="491e9-113">Semisynchronous Mode</span></span>](#semisynchronous-mode)
-   [<span data-ttu-id="491e9-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="491e9-114">Related topics</span></span>](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a><span data-ttu-id="491e9-115">Métodos de WMI en comparación con los métodos de proveedor</span><span class="sxs-lookup"><span data-stu-id="491e9-115">WMI Methods Compared to Provider Methods</span></span>

<span data-ttu-id="491e9-116">Mediante el uso de llamadas a [*métodos WMI*](gloss-w.md) combinadas con llamadas a [*métodos de proveedor*](gloss-p.md) , puede recuperar y manipular información sobre su empresa.</span><span class="sxs-lookup"><span data-stu-id="491e9-116">By using [*WMI method*](gloss-w.md) calls combined with [*provider method*](gloss-p.md) calls, you can retrieve and manipulate information about your enterprise.</span></span> <span data-ttu-id="491e9-117">Para obtener más información, consulte [llamar a un método WMI](calling-a-wmi-method.md) y [llamar a un método de proveedor](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="491e9-117">For more information, see [Calling a WMI Method](calling-a-wmi-method.md) and [Calling a Provider Method](calling-a-provider-method.md).</span></span>

<span data-ttu-id="491e9-118">Los métodos del objeto de scripting de WMI [**SWbemObject**](swbemobject.md) tienen un estado especial, ya que se pueden aplicar a cualquier clase de datos de WMI.</span><span class="sxs-lookup"><span data-stu-id="491e9-118">The methods of the WMI scripting object [**SWbemObject**](swbemobject.md) have a special status because they can apply to any WMI data class.</span></span> <span data-ttu-id="491e9-119">Para obtener más información, consulte [scripting con SWbemObject](scripting-with-swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="491e9-119">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

<span data-ttu-id="491e9-120">En el ejemplo de código siguiente se llama a los métodos de WMI y de proveedor.</span><span class="sxs-lookup"><span data-stu-id="491e9-120">The following code example calls both WMI and provider methods.</span></span>

<span data-ttu-id="491e9-121">Los siguientes métodos de WMI y proveedor se encuentran en la [API de scripting para WMI](scripting-api-for-wmi.md):</span><span class="sxs-lookup"><span data-stu-id="491e9-121">The following WMI and provider methods are located in the [Scripting API for WMI](scripting-api-for-wmi.md):</span></span>

-   <span data-ttu-id="491e9-122">**objWMIService.ExecQuery** llama al método de scripting de WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span><span class="sxs-lookup"><span data-stu-id="491e9-122">**objWMIService.ExecQuery** calls the WMI scripting method [**SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span></span>
-   <span data-ttu-id="491e9-123">**objService. StopService ()** llama al método de proveedor [ **Win32 \_ Service. stopservice**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="491e9-123">**objService.StopService()** calls the provider method [**Win32\_Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span></span>

<span data-ttu-id="491e9-124">Puede buscar el código que puede aparecer en "Return" en la sección códigos de retorno para [**el \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="491e9-124">You can look up the code that may appear in "Return" in the Return Codes section for [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a><span data-ttu-id="491e9-125">Modos de Method-Calling en WMI</span><span class="sxs-lookup"><span data-stu-id="491e9-125">Method-Calling Modes in WMI</span></span>

<span data-ttu-id="491e9-126">Normalmente, el modo de llamada semisincrónico proporciona el mejor equilibrio entre seguridad y rendimiento.</span><span class="sxs-lookup"><span data-stu-id="491e9-126">The semisynchronous calling mode usually provides the best balance between security and performance.</span></span>

<span data-ttu-id="491e9-127">Para obtener más información acerca de cada uno de los modos posibles, consulte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="491e9-127">For more information about each of the possible modes, see the following:</span></span>

-   [<span data-ttu-id="491e9-128">Sincrónica</span><span class="sxs-lookup"><span data-stu-id="491e9-128">Synchronous</span></span>](#synchronous-mode)
-   [<span data-ttu-id="491e9-129">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="491e9-129">Asynchronous</span></span>](#asynchronous-mode)
-   [<span data-ttu-id="491e9-130">Semisincrónico</span><span class="sxs-lookup"><span data-stu-id="491e9-130">Semisynchronous</span></span>](#semisynchronous-mode)

### <a name="synchronous-mode"></a><span data-ttu-id="491e9-131">Modo sincrónico</span><span class="sxs-lookup"><span data-stu-id="491e9-131">Synchronous Mode</span></span>

<span data-ttu-id="491e9-132">El modo sincrónico se produce cuando el programa o los scripts se pausan hasta que la llamada al método devuelve un objeto de colección [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="491e9-132">Synchronous mode occurs when the program or scripts pauses until the method call returns a [**SWbemObjectSet**](swbemobjectset.md) collection object.</span></span> <span data-ttu-id="491e9-133">WMI compila esta colección en memoria antes de devolver el objeto de colección al programa o script que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="491e9-133">WMI builds this collection in memory before returning the collection object to the calling program or script.</span></span>

<span data-ttu-id="491e9-134">El modo sincrónico puede tener un efecto adverso en el rendimiento del programa o del script en el equipo que ejecuta el programa o el script.</span><span class="sxs-lookup"><span data-stu-id="491e9-134">Synchronous mode can have an adverse effect of program or script performance on the computer running the program or script.</span></span> <span data-ttu-id="491e9-135">Por ejemplo, la recuperación sincrónica de miles de eventos del registro de eventos puede tardar mucho tiempo y usar una gran cantidad de memoria porque WMI crea un objeto a partir de cada evento y, a continuación, coloca esos objetos en una colección antes de pasar la colección al método.</span><span class="sxs-lookup"><span data-stu-id="491e9-135">For example, synchronously retrieving thousands of events from the event log can take a long time and use a lot of memory because WMI creates an object from each event and then puts those objects into a collection before passing the collection to the method.</span></span>

<span data-ttu-id="491e9-136">Solo debe llamar a métodos que no devuelvan grandes conjuntos de datos en modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="491e9-136">You should only call methods that do not return large data sets in synchronous mode.</span></span> <span data-ttu-id="491e9-137">Se puede llamar a los siguientes métodos de [**SWbemServices**](swbemservices.md) de forma segura en modo sincrónico:</span><span class="sxs-lookup"><span data-stu-id="491e9-137">The following [**SWbemServices**](swbemservices.md) methods can be safely called in synchronous mode:</span></span>

-   [<span data-ttu-id="491e9-138">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="491e9-138">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="491e9-139">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="491e9-139">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="491e9-140">**SWbemServices. get**</span><span class="sxs-lookup"><span data-stu-id="491e9-140">**SWbemServices.Get**</span></span>](swbemservices-get.md)

<span data-ttu-id="491e9-141">Se puede llamar a cualquier método de [**SWbemServices**](swbemservices.md) sin la palabra "Async" en el nombre en modo sincrónico estableciendo el valor de **wbemFlagReturnWhenComplete** en el parámetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="491e9-141">Any [**SWbemServices**](swbemservices.md) methods without the word, "Async" in the name can be called in synchronous mode by setting the **wbemFlagReturnWhenComplete** value in the *iFlags* parameter.</span></span>

### <a name="asynchronous-mode"></a><span data-ttu-id="491e9-142">Modo asíncrono</span><span class="sxs-lookup"><span data-stu-id="491e9-142">Asynchronous Mode</span></span>

<span data-ttu-id="491e9-143">El modo asincrónico se produce cuando el programa o el script continúan ejecutándose después de llamar al método.</span><span class="sxs-lookup"><span data-stu-id="491e9-143">Asynchronous mode occurs when the program or script continues to run after calling the method.</span></span> <span data-ttu-id="491e9-144">WMI devuelve todos los objetos del método a un objeto [**SWbemSink**](swbemsink.md) a medida que se crea cada objeto.</span><span class="sxs-lookup"><span data-stu-id="491e9-144">WMI returns all objects from the method to a [**SWbemSink**](swbemsink.md) object as each object is created.</span></span> <span data-ttu-id="491e9-145">El programa o script que realiza la llamada debe tener un objeto **SWbemSink** y un controlador de eventos [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) para procesar los objetos devueltos.</span><span class="sxs-lookup"><span data-stu-id="491e9-145">The calling program or script must have an **SWbemSink** object and an [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event handler to process the returned objects.</span></span> <span data-ttu-id="491e9-146">Para obtener más información sobre cómo crear un controlador de eventos para el modo asincrónico, consulte [recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="491e9-146">For more information about creating an event handler for asynchronous mode, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="491e9-147">Aunque este modo no tiene la penalización de rendimiento y recursos del modo sincrónico, el modo asincrónico puede crear riesgos de seguridad graves, ya que los resultados almacenados en el objeto [**SWbemSink**](swbemsink.md) pueden no provienen del programa o script de llamada.</span><span class="sxs-lookup"><span data-stu-id="491e9-147">While this mode does not have the performance and resource penalty of synchronous mode, asynchronous mode can create serious security risks because the results stored in the [**SWbemSink**](swbemsink.md) object may not come from the calling program or script.</span></span> <span data-ttu-id="491e9-148">WMI reduce el nivel de autenticación en el objeto **SWbemSink** hasta que el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="491e9-148">WMI lowers the authentication level on the **SWbemSink** object until the method succeeds.</span></span> <span data-ttu-id="491e9-149">Para obtener más información sobre cómo mitigar estos riesgos de seguridad, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="491e9-149">For more information about how to mitigate these security risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="491e9-150">Los métodos anexados con la palabra Async son métodos para el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="491e9-150">Methods appended with the word Async are methods for asynchronous mode.</span></span> <span data-ttu-id="491e9-151">Los métodos siguientes son llamadas asincrónicas:</span><span class="sxs-lookup"><span data-stu-id="491e9-151">The following methods are asynchronous calls:</span></span>

-   [<span data-ttu-id="491e9-152">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-152">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
-   [<span data-ttu-id="491e9-153">**SWbemServices. DeleteAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-153">**SWbemServices.DeleteAsync**</span></span>](swbemservices-deleteasync.md)
-   [<span data-ttu-id="491e9-154">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-154">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
-   [<span data-ttu-id="491e9-155">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-155">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)
-   [<span data-ttu-id="491e9-156">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-156">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
-   [<span data-ttu-id="491e9-157">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-157">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)
-   [<span data-ttu-id="491e9-158">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-158">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="491e9-159">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="491e9-159">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)

<span data-ttu-id="491e9-160">Para obtener más información sobre el modo asincrónico, vea:</span><span class="sxs-lookup"><span data-stu-id="491e9-160">For more information about asynchronous mode, see:</span></span>

-   [<span data-ttu-id="491e9-161">Realización de una llamada asincrónica con C++</span><span class="sxs-lookup"><span data-stu-id="491e9-161">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
-   [<span data-ttu-id="491e9-162">Realización de una llamada asincrónica con VBScript</span><span class="sxs-lookup"><span data-stu-id="491e9-162">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a><span data-ttu-id="491e9-163">Modo semisincrónico</span><span class="sxs-lookup"><span data-stu-id="491e9-163">Semisynchronous Mode</span></span>

<span data-ttu-id="491e9-164">El modo semisincrónico es similar al modo asincrónico en que el programa o script continúa ejecutándose después de llamar al método.</span><span class="sxs-lookup"><span data-stu-id="491e9-164">Semisynchronous mode is similar to asynchronous mode in that the program or script continues to run after calling the method.</span></span> <span data-ttu-id="491e9-165">En el modo semisincrónico, WMI recupera los objetos en segundo plano a medida que el script o programa continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="491e9-165">In semisynchronous mode, WMI retrieves the objects in the background as your script or program continues to run.</span></span> <span data-ttu-id="491e9-166">WMI devuelve cada objeto devuelto al método de llamada justo después de que se cree el objeto.</span><span class="sxs-lookup"><span data-stu-id="491e9-166">WMI returns each object returned to the calling method right after the object is created.</span></span>

<span data-ttu-id="491e9-167">Dado que WMI administra el objeto, el modo semisincrónico es más seguro que el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="491e9-167">Because WMI manages the object, semisynchronous mode is more secure than asynchronous mode.</span></span> <span data-ttu-id="491e9-168">Sin embargo, si utiliza el modo semisincrónico con más de 1.000 instancias, la recuperación de instancias puede monopolizar los recursos disponibles, lo que puede degradar el rendimiento del programa o el script y el equipo que usa el programa o el script.</span><span class="sxs-lookup"><span data-stu-id="491e9-168">However, if you use semisynchronous mode with more than 1,000 instances, instance retrieval can monopolize the available resources, which can degrade the performance of the program or script and the computer using the program or script.</span></span> <span data-ttu-id="491e9-169">Cada objeto ocupa los recursos necesarios hasta que se libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="491e9-169">Each object takes up the necessary resources until the memory is released.</span></span>

<span data-ttu-id="491e9-170">Para solucionar esta situación, puede llamar al método con el parámetro *iFlags* establecido con las marcas **wbemFlagForwardOnly** y **wbemFlagReturnImmediately** para indicar a WMI que devuelva un [**SWbemObjectSet**](swbemobjectset.md)de solo avance.</span><span class="sxs-lookup"><span data-stu-id="491e9-170">To work around this condition, you can call the method with the *iFlags* parameter set with the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags to instruct WMI to return a forward-only [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="491e9-171">Un **SWbemObjectSet** de solo avance elimina el problema de rendimiento causado por un conjunto de datos grande liberando la memoria después de que se haya enumerado el objeto.</span><span class="sxs-lookup"><span data-stu-id="491e9-171">A forward-only **SWbemObjectSet** eliminates the performance problem caused by a large data set by releasing the memory after the object is enumerated.</span></span>

<span data-ttu-id="491e9-172">Cualquier método [**SWbemServices**](swbemservices.md) al que no se pueda llamar en modo sincrónico o asincrónico se llama en modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="491e9-172">Any [**SWbemServices**](swbemservices.md) method that cannot be called in either synchronous or asynchronous mode is called in semisynchronous mode.</span></span>

<span data-ttu-id="491e9-173">Se llama a los métodos siguientes en modo semisincrónico:</span><span class="sxs-lookup"><span data-stu-id="491e9-173">The following methods are called in semisynchronous mode:</span></span>

-   [<span data-ttu-id="491e9-174">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="491e9-174">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="491e9-175">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="491e9-175">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="491e9-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="491e9-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="491e9-177">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="491e9-177">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
-   [<span data-ttu-id="491e9-178">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="491e9-178">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="491e9-179">**SWbemServices. get**</span><span class="sxs-lookup"><span data-stu-id="491e9-179">**SWbemServices.Get**</span></span>](swbemservices-get.md)
-   [<span data-ttu-id="491e9-180">**SWbemServices. instances**</span><span class="sxs-lookup"><span data-stu-id="491e9-180">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="491e9-181">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="491e9-181">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="491e9-182">**SWbemServices. subclasses**</span><span class="sxs-lookup"><span data-stu-id="491e9-182">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)
-   [<span data-ttu-id="491e9-183">**SWbemServices. put**</span><span class="sxs-lookup"><span data-stu-id="491e9-183">**SWbemServices.Put**</span></span>](swbemservicesex-put.md)

<span data-ttu-id="491e9-184">Para obtener más información sobre el modo semisincrónico, vea [crear una llamada semisincrónica con C++](making-a-semisynchronous-call-with-c--.md) y [crear una llamada semisincrónica con VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="491e9-184">For more information about semisynchronous mode, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="491e9-185">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="491e9-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="491e9-186">Mejorar el rendimiento de la enumeración</span><span class="sxs-lookup"><span data-stu-id="491e9-186">Improving Enumeration Performance</span></span>](improving-enumeration-performance.md)
</dt> <dt>

[<span data-ttu-id="491e9-187">Scripting con SWbemObject</span><span class="sxs-lookup"><span data-stu-id="491e9-187">Scripting with SWbemObject</span></span>](scripting-with-swbemobject.md)
</dt> <dt>

[<span data-ttu-id="491e9-188">**WbemFlagEnum**</span><span class="sxs-lookup"><span data-stu-id="491e9-188">**WbemFlagEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
