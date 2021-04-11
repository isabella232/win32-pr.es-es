---
description: La recuperación de una instancia de es uno de los procedimientos de recuperación más comunes que es probable que se realice en WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Recuperación de una instancia de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083384"
---
# <a name="retrieving-a-wmi-instance"></a><span data-ttu-id="ad519-103">Recuperación de una instancia de WMI</span><span class="sxs-lookup"><span data-stu-id="ad519-103">Retrieving a WMI Instance</span></span>

<span data-ttu-id="ad519-104">La recuperación de una instancia de es uno de los procedimientos de recuperación más comunes que es probable que se realice en WMI.</span><span class="sxs-lookup"><span data-stu-id="ad519-104">Retrieving an instance is one of the most common retrieval procedures you are likely to perform in WMI.</span></span> <span data-ttu-id="ad519-105">Puede recuperar una instancia existente o crear una nueva instancia sin nombre.</span><span class="sxs-lookup"><span data-stu-id="ad519-105">You can retrieve an existing instance or create a new unnamed instance.</span></span> <span data-ttu-id="ad519-106">La ruta de acceso WMI a la instancia existente es un parámetro necesario.</span><span class="sxs-lookup"><span data-stu-id="ad519-106">The WMI path to the existing instance is a required parameter.</span></span> <span data-ttu-id="ad519-107">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="ad519-107">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

> [!Note]  
> <span data-ttu-id="ad519-108">Al proporcionar una instancia, es posible que un proveedor no pueda proporcionar un valor para ciertas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ad519-108">When providing an instance, a provider may be unable to provide a value for certain properties.</span></span> <span data-ttu-id="ad519-109">A menos que se indique lo contrario en la descripción de la propiedad, no se puede inferir ningún significado de un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="ad519-109">Unless otherwise stated in the property description, you cannot infer any meaning from an empty value.</span></span> <span data-ttu-id="ad519-110">No se debe confundir con una cadena que tiene un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="ad519-110">This is not to be confused with a string which has a **NULL** value.</span></span> <span data-ttu-id="ad519-111">En este caso, el valor se rellena.</span><span class="sxs-lookup"><span data-stu-id="ad519-111">In this case, the value is populated.</span></span> <span data-ttu-id="ad519-112">Está vacía pero tiene un valor: **null**.</span><span class="sxs-lookup"><span data-stu-id="ad519-112">It is empty but has a value: **NULL**.</span></span>

 

<span data-ttu-id="ad519-113">Recupere una copia local de la instancia con una llamada al cmdlet [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad519-113">Retrieve a local copy of the instance with a call to the PowerShell [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

<span data-ttu-id="ad519-114">**Para recuperar una instancia de una clase WMI mediante PowerShell**</span><span class="sxs-lookup"><span data-stu-id="ad519-114">**To retrieve an instance of a WMI class using PowerShell**</span></span>

-   <span data-ttu-id="ad519-115">Puede recuperar instancias específicas mediante los parámetros *-Class* y *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="ad519-115">You can retrieve specific instances using the *-class* and *-filter* parameters.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="ad519-116">Puede recuperar una instancia de WMI mediante C# si crea un objeto de búsqueda mediante [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))y, a continuación, lo rellena con los valores de clave pertinentes y, a continuación, busca ese objeto con una llamada a [CimSession. getInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ad519-116">You can retrieve a WMI instance using C# by creating a search object using [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), and then filling it with the relevant key values, and then searching for that object with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

<span data-ttu-id="ad519-117">**Para recuperar una instancia de una clase WMI mediante C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="ad519-117">**To retrieve an instance of a WMI class using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="ad519-118">Con el espacio de nombres [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , cree un nuevo objeto [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) con el nombre de clase y el espacio de nombres pertinentes.</span><span class="sxs-lookup"><span data-stu-id="ad519-118">Using the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, create a new [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) object with the relevant class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="ad519-119">Cree un [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) que contenga el nombre y el valor de la propiedad clave de la instancia que desea buscar y agregue esa propiedad al objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="ad519-119">Create a [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) that contains the name and value of the key property of the instance you wish to search for, and add that property to your class object.</span></span>

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  <span data-ttu-id="ad519-120">Recupere el objeto de WMI con una llamada a [CimSession. getInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ad519-120">Retrieve the object from WMI with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

<span data-ttu-id="ad519-121">Puede recuperar una instancia de clase WMI específica, o una colección de instancias de clase WMI, mediante clases en el espacio de nombres [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="ad519-121">You can retrieve either a specific WMI class instance, or a collection of WMI class instances, using classes in the [System.Management](/dotnet/api/system.management) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="ad519-122">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="ad519-122">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="ad519-123">**Para recuperar una instancia de una clase WMI mediante C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="ad519-123">**To retrieve an instance of a WMI class using C# (System.Management)**</span></span>

1.  <span data-ttu-id="ad519-124">Recuperar una copia local de una instancia específica creando una nueva [ManagementObject](/dotnet/api/system.management.managementobject), con el nombre y el valor de instancia específico pasados a través del parámetro *ManagementPath* .</span><span class="sxs-lookup"><span data-stu-id="ad519-124">Retrieve a local copy of a specific instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject), with the name and specific instance value passed in though the *ManagementPath* parameter.</span></span> <span data-ttu-id="ad519-125">A continuación, puede recuperar los datos de instancia llamando explícitamente a [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="ad519-125">You can then retrieve the instance data by explicitly calling [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  <span data-ttu-id="ad519-126">Como alternativa, puede recuperar todas las instancias de una clase WMI buscándolas con un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)y, a continuación, enumerando el [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)devuelto.</span><span class="sxs-lookup"><span data-stu-id="ad519-126">Alternately, you can retrieve all instances of a WMI class by searching for them with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), and then enumerating through the returned [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    <span data-ttu-id="ad519-127">Puede llamar implícitamente al método **Get** accediendo a la instancia.</span><span class="sxs-lookup"><span data-stu-id="ad519-127">You can implicitly call the **Get** method by accessing the instance.</span></span> <span data-ttu-id="ad519-128">Para obtener más información, consulte [recuperar parte de una instancia de WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ad519-128">For more information, see [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

<span data-ttu-id="ad519-129">Recuperar una copia local de la instancia con una llamada al método [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="ad519-129">Retrieve a local copy of the instance with a call to the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) method.</span></span>

<span data-ttu-id="ad519-130">**Para recuperar una instancia de una clase WMI mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="ad519-130">**To retrieve an instance of a WMI class using VBScript**</span></span>

-   <span data-ttu-id="ad519-131">Llame a [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) con la ruta de acceso del objeto de la instancia, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ad519-131">Call [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) with the object path of the instance as shown in the following example.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    <span data-ttu-id="ad519-132">Para recuperar una instancia concreta, es necesario asignar un nombre como parte de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ad519-132">Retrieving a specific instance requires giving a name as part of the object path.</span></span>

<span data-ttu-id="ad519-133">En C++, llame a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="ad519-133">In C++, call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="ad519-134">**Para recuperar una instancia de una clase WMI mediante C++**</span><span class="sxs-lookup"><span data-stu-id="ad519-134">**To retrieve an instance of a WMI class using C++**</span></span>

-   <span data-ttu-id="ad519-135">Recupere una copia local de la instancia de con una llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="ad519-135">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="ad519-136">Se debe incluir la ruta de acceso WMI al objeto.</span><span class="sxs-lookup"><span data-stu-id="ad519-136">The WMI path to the object must be included.</span></span>

    <span data-ttu-id="ad519-137">Como su nombre implica, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) recupera la instancia de forma asincrónica, mientras que [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) recupera la instancia de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="ad519-137">As the name implies, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) retrieves the instance asynchronously, while [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retrieves the instance synchronously.</span></span> <span data-ttu-id="ad519-138">Si desea usar la recuperación asincrónica, debe implementar la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="ad519-138">If you want to use asynchronous retrieval, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="ad519-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ad519-139">Examples</span></span>

<span data-ttu-id="ad519-140">Para ver un ejemplo de VBScript que se utiliza como plantilla para recuperar información de clase e instancia, vea el ejemplo de [script de plantilla WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) en la galería de TechNet.</span><span class="sxs-lookup"><span data-stu-id="ad519-140">For a VBScript example to use as a template to retrieve class and instance information, see the [WMI Template Script](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) example on TechNet Gallery.</span></span> <span data-ttu-id="ad519-141">En este ejemplo concreto se usa GetObject para recuperar el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="ad519-141">This particular example uses GetObject to retrieve the WMI Service.</span></span>

 

 
