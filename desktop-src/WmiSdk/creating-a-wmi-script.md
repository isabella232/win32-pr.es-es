---
description: Puede ver o manipular cualquier información disponible a través de WMI mediante scripts.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Creación de un script de WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003108"
---
# <a name="creating-a-wmi-script"></a><span data-ttu-id="5364a-103">Creación de un script de WMI</span><span class="sxs-lookup"><span data-stu-id="5364a-103">Creating a WMI Script</span></span>

<span data-ttu-id="5364a-104">Puede ver o manipular cualquier información disponible a través de WMI mediante scripts.</span><span class="sxs-lookup"><span data-stu-id="5364a-104">You can view or manipulate any information made available through WMI using scripts.</span></span> <span data-ttu-id="5364a-105">Los scripts se pueden escribir en cualquier lenguaje de scripting que admita el hospedaje de scripts de Microsoft ActiveX, incluido Visual Basic Scripting Edition (VBScript), PowerShell y Perl.</span><span class="sxs-lookup"><span data-stu-id="5364a-105">Scripts can be written in any scripting language that supports Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript), PowerShell, and Perl.</span></span> <span data-ttu-id="5364a-106">Windows Script Host (WSH), las páginas de Active Server e Internet Explorer pueden hospedar todos los scripts de WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-106">Windows Script Host (WSH), Active Server Pages, and Internet Explorer can all host WMI scripts.</span></span>

> [!Note]
>
> <span data-ttu-id="5364a-107">El lenguaje de scripting principal que actualmente admite WMI es PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5364a-107">The primary scripting language currently supported by WMI is PowerShell.</span></span> <span data-ttu-id="5364a-108">Sin embargo, WMI también contiene un cuerpo sólido de compatibilidad con scripting para VBScript y otros lenguajes que tienen acceso a la [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-108">However, WMI also contains a robust body of scripting support for VBScript and other languages that access the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

 

## <a name="wmi-scripting-languages"></a><span data-ttu-id="5364a-109">Lenguajes de scripting de WMI</span><span class="sxs-lookup"><span data-stu-id="5364a-109">WMI Scripting Languages</span></span>

<span data-ttu-id="5364a-110">Los dos idiomas principales admitidos por WMI son PowerShell y VBScript (a través de Windows Script Host o WSH).</span><span class="sxs-lookup"><span data-stu-id="5364a-110">The two main languages supported by WMI are PowerShell and VBScript (through the Windows Script Host, or WSH).</span></span>

-   <span data-ttu-id="5364a-111">**PowerShell** se diseñó con la estrecha integración con WMI en mente.</span><span class="sxs-lookup"><span data-stu-id="5364a-111">**PowerShell** was designed with tight integration with WMI in mind.</span></span> <span data-ttu-id="5364a-112">Como tal, gran parte de los elementos subyacentes de WMI se integran en los cmdlets de WMI: [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)y [Remove-WMIObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span><span class="sxs-lookup"><span data-stu-id="5364a-112">As such, much of the underlying elements of WMI are built into the WMI cmdlets: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1), and [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span></span> <span data-ttu-id="5364a-113">En la tabla siguiente se describen los procesos generales que se usan para obtener acceso a la información de WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-113">The following table describes the general processes used for accessing WMI information.</span></span> <span data-ttu-id="5364a-114">Tenga en cuenta que, aunque la mayoría de estos ejemplos usan Get-WMIObject, muchos de los cmdlets de WMI de PowerShell tienen los mismos parámetros, como *-Class* o *-Credentials*.</span><span class="sxs-lookup"><span data-stu-id="5364a-114">Note that while most of these examples use Get-WMIObject, many of the PowerShell WMI cmdlets have the same parameters, such as *-Class* or *-Credentials*.</span></span> <span data-ttu-id="5364a-115">Por lo tanto, muchos de estos procesos también funcionan para otros objetos.</span><span class="sxs-lookup"><span data-stu-id="5364a-115">Therefore, many of these processes also work for other objects.</span></span> <span data-ttu-id="5364a-116">Para obtener una explicación más detallada de PowerShell y WMI, consulte [usar el Cmdlet Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) y [Windows PowerShell-la conexión WMI](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="5364a-116">For a more in-depth discussion of PowerShell and WMI, see [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and [Windows PowerShell - the WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span></span>

-   <span data-ttu-id="5364a-117">En cambio, **VBScript** realiza llamadas explícitamente a la [API de scripting para WMI](scripting-api-for-wmi.md), tal y como se mencionó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5364a-117">**VBScript**, in contrast, explicitly makes calls to the [Scripting API for WMI](scripting-api-for-wmi.md), as mentioned above.</span></span> <span data-ttu-id="5364a-118">Otros lenguajes, como Perl, también pueden usar la API de scripting para WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-118">Other languages, such as Perl, can also use the scripting API for WMI.</span></span> <span data-ttu-id="5364a-119">Sin embargo, para los fines de esta documentación, la mayoría de los ejemplos que muestran la API de scripting para WMI usarán VBScript.</span><span class="sxs-lookup"><span data-stu-id="5364a-119">However, for the purposes of this documentation, most samples that demonstrate the scripting API for WMI will use VBScript.</span></span> <span data-ttu-id="5364a-120">Sin embargo, cuando una técnica de programación es específica de VBScript, se le llamará.</span><span class="sxs-lookup"><span data-stu-id="5364a-120">When a programming technique is specific to VBScript, however, it will be called out.</span></span>

    <span data-ttu-id="5364a-121">VBScript esencialmente tiene dos maneras independientes de obtener acceso a WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-121">VBScript has essentially two separate ways of accessing WMI.</span></span> <span data-ttu-id="5364a-122">El primero es el uso de un objeto [**SWbemLocator**](swbemlocator.md) para conectarse a WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-122">The first is using an [**SWbemLocator**](swbemlocator.md) object to connect to WMI.</span></span> <span data-ttu-id="5364a-123">Como alternativa, puede usar [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) y un moniker.</span><span class="sxs-lookup"><span data-stu-id="5364a-123">Alternately, you can use [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) and a moniker.</span></span> <span data-ttu-id="5364a-124">Un moniker es una cadena que puede describir un número de elementos: las credenciales, la configuración de suplantación, el equipo al que desea conectarse, el [*espacio de nombres*](gloss-n.md) de WMI (es decir, la ubicación general donde WMI almacena los grupos de objetos) y el objeto WMI que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="5364a-124">A moniker is a string that can describe a number of elements: your credentials, impersonation settings, what computer you want to connect to, the WMI [*namespace*](gloss-n.md) (ie, the general location where WMI stores groups of objects), and what WMI object you want to retrieve.</span></span> <span data-ttu-id="5364a-125">Muchos de los ejemplos siguientes describen ambas técnicas.</span><span class="sxs-lookup"><span data-stu-id="5364a-125">Many of the examples below describe both techniques.</span></span> <span data-ttu-id="5364a-126">Para obtener más información, vea [construir una cadena de moniker](constructing-a-moniker-string.md) y [describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-126">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md) and [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

    <span data-ttu-id="5364a-127">Independientemente de la técnica que utilice para conectarse a WMI, es probable que recupere uno o más objetos de la API de scripting.</span><span class="sxs-lookup"><span data-stu-id="5364a-127">Regardless of what technique you use to connect to WMI, you will likely retrieve one or more objects from the Scripting API.</span></span> <span data-ttu-id="5364a-128">El más común es [**SWbemObject**](swbemobject.md), que WMI usa para describir un objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-128">The most common is [**SWbemObject**](swbemobject.md), which WMI uses to describe a WMI object.</span></span> <span data-ttu-id="5364a-129">Como alternativa, puede usar un objeto [**SWbemServices**](swbemservices.md) para describir el propio servicio WMI o un objeto [**SWbemObjectPath**](swbemobjectpath.md) para describir la ubicación de un objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-129">Alternately, you may use an [**SWbemServices**](swbemservices.md) object to describe the WMI service itself, or an [**SWbemObjectPath**](swbemobjectpath.md) object to describe the location of a WMI object.</span></span> <span data-ttu-id="5364a-130">Para obtener más información, vea [scripting con](scripting-with-swbemobject.md) [objetos auxiliares de scripting](scripting-helper-objects.md)y SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="5364a-130">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md) and [Scripting Helper Objects](scripting-helper-objects.md).</span></span>

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a><span data-ttu-id="5364a-131">Usar WMI y un lenguaje de scripting, cómo...</span><span class="sxs-lookup"><span data-stu-id="5364a-131">Using WMI and a Scripting Language, How Do I...</span></span>

<dl> <dt>

<span data-ttu-id="5364a-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... ¿conectarse a WMI?</span><span class="sxs-lookup"><span data-stu-id="5364a-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...connect to WMI?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-133">Para VBScript y la API de scripting para WMI, recupere un objeto [**SWbemServices**](swbemservices.md) con un moniker y una llamada a [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span><span class="sxs-lookup"><span data-stu-id="5364a-133">For VBScript and the Scripting API for WMI, retrieve an [**SWbemServices**](swbemservices.md) object with a moniker and a call to [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span></span> <span data-ttu-id="5364a-134">Como alternativa, puede conectarse al servidor con una llamada a [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="5364a-134">Alternately, you can connect to the server with a call to [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="5364a-135">A continuación, puede utilizar el objeto para tener acceso a un espacio de nombres WMI específico o a una instancia de clase WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-135">You can then use the object to access a specific WMI namespace or WMI class instance.</span></span>

<span data-ttu-id="5364a-136">Para PowerShell, la conexión a WMI normalmente se realiza directamente en la llamada de cmdlet; como tal, no es necesario realizar ningún paso adicional.</span><span class="sxs-lookup"><span data-stu-id="5364a-136">For PowerShell, connecting to WMI is generally done directly in the cmdlet call; as such, no additional steps are necessary.</span></span>

<span data-ttu-id="5364a-137">Para obtener más información, vea [describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md), [construir una cadena de moniker](constructing-a-moniker-string.md)y [conectarse a WMI con VBScript](connecting-to-wmi-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-137">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md), [Constructing a Moniker String](constructing-a-moniker-string.md), and [Connecting to WMI with VBScript](connecting-to-wmi-with-vbscript.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span data-ttu-id="5364a-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... ¿recuperar información de WMI?</span><span class="sxs-lookup"><span data-stu-id="5364a-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...retrieve information from WMI?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-139">Para VBScript y la API de scripting para WMI, use una función de recuperación, como [**WbemServices. Get**](swbemservices-get.md) o [**WbemServices. instances**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-139">For VBScript and the Scripting API for WMI, use a retrieval function, such as [**WbemServices.Get**](swbemservices-get.md) or [**WbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span> <span data-ttu-id="5364a-140">También puede colocar el nombre de clase del objeto que se va a recuperar en un moniker, que puede ser más eficaz.</span><span class="sxs-lookup"><span data-stu-id="5364a-140">You may also place the class name of the object to retrieve in a moniker, which may be more efficient.</span></span>

<span data-ttu-id="5364a-141">Para PowerShell, use el parámetro *-Class* .</span><span class="sxs-lookup"><span data-stu-id="5364a-141">For PowerShell, use the *-Class* parameter.</span></span> <span data-ttu-id="5364a-142">Tenga en cuenta que-Class es el parámetro predeterminado; como tal, no es necesario que lo indique explícitamente.</span><span class="sxs-lookup"><span data-stu-id="5364a-142">Note that -Class is the default parameter; as such, you don't need to explicitly state it.</span></span>

<span data-ttu-id="5364a-143">Para obtener más información, consulte [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-143">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span data-ttu-id="5364a-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... ¿crear una consulta WMI?</span><span class="sxs-lookup"><span data-stu-id="5364a-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...create a WMI query?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-145">Para VBScript y la API de scripting para WMI, use el método [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .</span><span class="sxs-lookup"><span data-stu-id="5364a-145">For VBScript and the Scripting API for WMI, use the [**SWbemServices.ExecQuery**](swbemservices-execquery.md) method.</span></span>

<span data-ttu-id="5364a-146">Para PowerShell, use el parámetro *-query* .</span><span class="sxs-lookup"><span data-stu-id="5364a-146">For PowerShell, use the *-Query* parameter.</span></span> <span data-ttu-id="5364a-147">También puede filtrar mediante el parámetro *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="5364a-147">You can also filter using the *-Filter* parameter.</span></span>

<span data-ttu-id="5364a-148">Para obtener más información, consulte [consultar WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-148">For more information, see [Querying WMI](querying-wmi.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span data-ttu-id="5364a-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... ¿enumerar a través de una lista de objetos WMI?</span><span class="sxs-lookup"><span data-stu-id="5364a-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...enumerate through a list of WMI objects?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-150">Para VBScript y la API de scripting para WMI, use el objeto contenedor [**SWbemObjectSet**](swbemobjectset.md) , que se trata en el script como una colección que se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="5364a-150">For VBScript and the Scripting API for WMI, use the [**SWbemObjectSet**](swbemobjectset.md) container object, which is treated in script as a collection that can be enumerated.</span></span> <span data-ttu-id="5364a-151">Puede recuperar un **SWbemObjectSet** de una llamada desde [**SWbemServices. instances**](swbemservices-instancesof.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-151">You can retrieve an **SWbemObjectSet** from a call from [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="5364a-152">PowerShell puede recuperar y controlar las enumeraciones como lo haría con cualquier otro objeto. no hay nada particularmente único en WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-152">PowerShell is able to retrieve and handle enumerations as it would any other object; there is nothing particularly unique to WMI.</span></span>

<span data-ttu-id="5364a-153">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-153">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span data-ttu-id="5364a-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... ¿tiene acceso a un espacio de nombres WMI diferente?</span><span class="sxs-lookup"><span data-stu-id="5364a-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...access a different WMI namespace?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-155">Para VBScript y la API de scripting para WMI, establezca el espacio de nombres en el moniker o, de lo contrario, puede indicar explícitamente el espacio de nombres en la llamada a [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="5364a-155">For VBScript and the Scripting API for WMI, state the namespace in the moniker, or else you can explicitly state the namespace in the call to [**SwbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

<span data-ttu-id="5364a-156">Para PowerShell, use el parámetro *-namespace* .</span><span class="sxs-lookup"><span data-stu-id="5364a-156">For PowerShell, use the *-Namespace* parameter.</span></span> <span data-ttu-id="5364a-157">El espacio de nombres predeterminado es "root \\ cimV2"; sin embargo, muchas clases anteriores se almacenan en "root \\ default".</span><span class="sxs-lookup"><span data-stu-id="5364a-157">The default namespace is "root\\cimV2"; however, many older classes are stored in "root\\default".</span></span>

<span data-ttu-id="5364a-158">Para buscar la ubicación de una clase WMI determinada, examine la página de referencia.</span><span class="sxs-lookup"><span data-stu-id="5364a-158">To find the location of a given WMI class, look at the reference page.</span></span> <span data-ttu-id="5364a-159">Como alternativa, puede explorar manualmente un espacio de nombres mediante Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="5364a-159">Alternately, you can manually explore a namespace using get-WmiObject.</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span data-ttu-id="5364a-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... ¿recuperar todas las instancias secundarias de una clase?</span><span class="sxs-lookup"><span data-stu-id="5364a-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...retrieve all child instances of a class?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-161">Para los lenguajes que usan directamente la API de scripting para WMI y PowerShell, WMI admite la recuperación de las clases secundarias de una clase base.</span><span class="sxs-lookup"><span data-stu-id="5364a-161">For languages that directly use the Scripting API for WMI and PowerShell, WMI supports retrieving the child classes of a base class.</span></span> <span data-ttu-id="5364a-162">Por lo tanto, para recuperar las instancias secundarias, solo necesita buscar la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="5364a-162">As such, in order to retrieve the child instances, you need to only search for the parent class.</span></span> <span data-ttu-id="5364a-163">En el siguiente ejemplo se busca [**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), que es una clase WMI preinstalada que representa discos lógicos en un sistema de equipo basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="5364a-163">The following example searches for [**CIM\_LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), which is a preinstalled WMI class that represents logical disks on a Windows-based computer system.</span></span> <span data-ttu-id="5364a-164">Como tal, la búsqueda de esta clase primaria también devuelve instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), que es lo que usa Windows para describir las unidades de disco duro.</span><span class="sxs-lookup"><span data-stu-id="5364a-164">As such, searching for this parent class also returns instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which is what Windows uses to describe hard drives.</span></span> <span data-ttu-id="5364a-165">Para obtener más información, vea [modelo de información común](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-165">For more information, see [Common Information Model](common-information-model.md).</span></span> <span data-ttu-id="5364a-166">WMI proporciona un esquema completo de estas clases preinstaladas que le permiten tener acceso a objetos administrados y controlarlos.</span><span class="sxs-lookup"><span data-stu-id="5364a-166">WMI supplies an entire schema of such preinstalled classes that allow you to access and control managed objects.</span></span> <span data-ttu-id="5364a-167">Para obtener más información, vea [clases Win32](/windows/desktop/CIMWin32Prov/win32-provider) y [clases WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-167">For more information, see [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) and [WMI Classes](wmi-classes.md)..</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span data-ttu-id="5364a-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... ¿buscar un objeto WMI?</span><span class="sxs-lookup"><span data-stu-id="5364a-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...locate a WMI object?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-169">En el caso de la API de scripting para WMI y PowerShell, WMI utiliza una combinación de espacio de nombres, nombre de clase y propiedades de clave para identificar de forma única una instancia de WMI determinada.</span><span class="sxs-lookup"><span data-stu-id="5364a-169">For both the Scripting API for WMI and PowerShell, WMI uses a combination of namespace, class name, and key properties to uniquely identify a given WMI instance.</span></span> <span data-ttu-id="5364a-170">En conjunto, esto se conoce como la ruta de acceso del objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="5364a-170">Together, this is known as the WMI object path.</span></span> <span data-ttu-id="5364a-171">En el caso de VBScript, la propiedad [**SWbemObject. Path \_**](swbemobject-path-.md) describe la ruta de acceso de cualquier objeto dado devuelto por la API de scripting.</span><span class="sxs-lookup"><span data-stu-id="5364a-171">For VBScript, the [**SWbemObject.Path\_**](swbemobject-path-.md) property describes the path for any given object returned by the scripting API.</span></span> <span data-ttu-id="5364a-172">Para PowerShell, cada objeto WMI tendrá una \_ \_ propiedad path.</span><span class="sxs-lookup"><span data-stu-id="5364a-172">For PowerShell, every WMI object will have a \_\_PATH property.</span></span> <span data-ttu-id="5364a-173">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5364a-173">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md)</span></span>

<span data-ttu-id="5364a-174">Además del espacio de nombres y el nombre de clase, un objeto WMI también tendrá una propiedad clave que identifica de forma única esa instancia en comparación con otras instancias de su equipo.</span><span class="sxs-lookup"><span data-stu-id="5364a-174">In addition to namespace and class name, a WMI object will also have a key property, which uniquely identifies that instance compared to other instances on your machine.</span></span> <span data-ttu-id="5364a-175">Por ejemplo, la propiedad **DeviceID** es la propiedad clave de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="5364a-175">For example, the **DeviceID** property is the key property for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="5364a-176">Para obtener más información, consulte [Managed Object Format (MOF)](managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-176">For more information, see [Managed Object Format (MOF)](managed-object-format--mof-.md).</span></span>

<span data-ttu-id="5364a-177">Por último, la ruta de acceso relativa es simplemente una forma abreviada de la ruta de acceso e incluye el nombre de la clase y el valor de la clave.</span><span class="sxs-lookup"><span data-stu-id="5364a-177">Finally, the Relative path is simply a shortened form of the path, and includes the class name and key value.</span></span> <span data-ttu-id="5364a-178">En los ejemplos siguientes, la ruta de acceso puede ser " \\ \\ computerName \\ root \\ cimv2: Win32 \_ LogicalDisk. DeviceID =" d: "", mientras que la ruta de acceso relativa sería "" Win32LogicalDisk. DeviceID = "d" "".</span><span class="sxs-lookup"><span data-stu-id="5364a-178">In the examples below, the path may be "\\\\computerName\\root\\cimv2:Win32\_LogicalDisk.DeviceID="D:"", while the relative path would be ""Win32LogicalDisk.DeviceID="D""".</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span data-ttu-id="5364a-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... ¿establecer información en WMI?</span><span class="sxs-lookup"><span data-stu-id="5364a-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...set information in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-180">Para VBScript y la API de scripting para WMI, use el método [**SWbemObject \_ . put**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="5364a-180">For VBScript and the Scripting API for WMI, use the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span>

<span data-ttu-id="5364a-181">En el caso de PowerShell, puede usar el método put, o bien [set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="5364a-181">For PowerShell, you can either use the Put method, or else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

<span data-ttu-id="5364a-182">Para obtener más información, vea [modificar una propiedad de instancia](modifying-an-instance-property.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-182">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span data-ttu-id="5364a-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... ¿usar credenciales diferentes?</span><span class="sxs-lookup"><span data-stu-id="5364a-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...use different credentials?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-184">En el caso de VBScript y la API de scripting para WMI, use los parámetros de *nombre de usuario* y *contraseña* en el método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="5364a-184">For VBScript and the Scripting API for WMI, use the *UserName* and *Password* parameters in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

<span data-ttu-id="5364a-185">Para PowerShell, use el parámetro *-Credential* .</span><span class="sxs-lookup"><span data-stu-id="5364a-185">For PowerShell, use the *-Credential* parameter.</span></span>

<span data-ttu-id="5364a-186">Tenga en cuenta que solo puede usar credenciales alternativas en un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="5364a-186">Note that you can only use alternate credentials on a remote system.</span></span> <span data-ttu-id="5364a-187">Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-187">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="5364a-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... ¿tiene acceso a un equipo remoto?</span><span class="sxs-lookup"><span data-stu-id="5364a-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...access a remote computer?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-189">En el caso de VBScript y la API de scripting para WMI, indique explícitamente el nombre del equipo en el moniker, o bien en la llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-189">For VBScript and the Scripting API for WMI, explicitly state the name of the computer in either the moniker, or else in the call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="5364a-190">Para obtener más información, vea [conectarse a WMI de forma remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-190">For more information, see [Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span></span>

<span data-ttu-id="5364a-191">Para PowerShell, use el parámetro *-ComputerName* .</span><span class="sxs-lookup"><span data-stu-id="5364a-191">For PowerShell, use the *-ComputerName* parameter.</span></span> <span data-ttu-id="5364a-192">Para obtener más información, consulte [conexión a WMI de forma remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-192">For more information, see [Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="5364a-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... ¿establecer los niveles de autenticación y suplantación?</span><span class="sxs-lookup"><span data-stu-id="5364a-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...set the Authentication and Impersonation levels?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-194">Para VBScript y la API de scripting para WMI, use la propiedad [**SWbemServices \_ . Security**](swbemlocator-security-.md) en el objeto de servidor devuelto, o bien establezca los valores relevantes en el moniker.</span><span class="sxs-lookup"><span data-stu-id="5364a-194">For VBScript and the Scripting API for WMI, use the [**SWbemServices.Security\_**](swbemlocator-security-.md) property on the returned server object, or else set the relevant values in the moniker.</span></span>

<span data-ttu-id="5364a-195">Para PowerShell, use los parámetros *-Authentication* y *-Impersonation* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5364a-195">For PowerShell, use the *-Authentication* and *-Impersonation* parameters, respectively.</span></span> <span data-ttu-id="5364a-196">Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-196">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="5364a-197">Para obtener más información, consulte [protección de los clientes de scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-197">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="5364a-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... ¿controlar los errores en WMI?</span><span class="sxs-lookup"><span data-stu-id="5364a-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...handle errors in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="5364a-199">En el caso de la API de scripting para WMI, el proveedor puede proporcionar un objeto [**SWbemLastError**](swbemlasterror.md) para proporcionar más información sobre un error.</span><span class="sxs-lookup"><span data-stu-id="5364a-199">For the Scripting API for WMI, the provider may supply an [**SWbemLastError**](swbemlasterror.md) object to give further information on an error.</span></span>

<span data-ttu-id="5364a-200">En VBScript, en concreto, el control de errores también se admite mediante el objeto **Err** nativo.</span><span class="sxs-lookup"><span data-stu-id="5364a-200">In VBScript in particular, error handling is also supported using the native **Err** object.</span></span> <span data-ttu-id="5364a-201">También puede tener acceso al objeto [**SWbemLastError**](swbemlasterror.md), tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5364a-201">You may also access the [**SWbemLastError**](swbemlasterror.md)object, as described above.</span></span> <span data-ttu-id="5364a-202">Para obtener más información, vea [recuperar un código de error](retrieving-an-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="5364a-202">For more information, see [Retrieving an Error Code](retrieving-an-error-code.md).</span></span>

<span data-ttu-id="5364a-203">Para PowerShell, puede usar las técnicas estándar de control de errores de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5364a-203">For PowerShell, you can use the standard PowerShell error handling techniques.</span></span> <span data-ttu-id="5364a-204">Para obtener más información, vea [Introducción al control de errores en PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="5364a-204">For more information, see [An Introduction to Error Handling in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span></span>


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
