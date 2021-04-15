---
description: Una consulta sincrónica es una consulta que mantiene el control sobre el proceso de la aplicación mientras dure la consulta.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Invocar una consulta sincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688612"
---
# <a name="invoking-a-synchronous-query"></a><span data-ttu-id="8b430-103">Invocar una consulta sincrónica</span><span class="sxs-lookup"><span data-stu-id="8b430-103">Invoking a Synchronous Query</span></span>

<span data-ttu-id="8b430-104">Una consulta sincrónica es una consulta que mantiene el control sobre el proceso de la aplicación mientras dure la consulta.</span><span class="sxs-lookup"><span data-stu-id="8b430-104">A synchronous query is a query that maintains control over the process of your application for the duration of the query.</span></span> <span data-ttu-id="8b430-105">Una consulta sincrónica requiere una única llamada de interfaz y, por lo tanto, es más sencilla que una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8b430-105">A synchronous query requires a single interface call, and is therefore more simple than an asynchronous call.</span></span> <span data-ttu-id="8b430-106">Sin embargo, una consulta sincrónica tiene la posibilidad de bloquear la aplicación para consultas o consultas grandes a través de una red.</span><span class="sxs-lookup"><span data-stu-id="8b430-106">However, a synchronous query has the potential of locking up your application for large queries or queries over a network.</span></span>

<span data-ttu-id="8b430-107">En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónicos mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b430-107">The following procedure describes how to issue a synchronous data query using PowerShell.</span></span>

<span data-ttu-id="8b430-108">**Para emitir una consulta de datos sincrónicos en PowerShell**</span><span class="sxs-lookup"><span data-stu-id="8b430-108">**To issue a synchronous data query in PowerShell**</span></span>

-   <span data-ttu-id="8b430-109">Describa la consulta a WMI mediante el cmdlet [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) de WMI y el parámetro *-query* .</span><span class="sxs-lookup"><span data-stu-id="8b430-109">Describe your query to WMI using the WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet and the *-query* parameter.</span></span> <span data-ttu-id="8b430-110">El cmdlet devuelve un solo objeto o una colección de objetos, en función del número de objetos que se ajusten a la consulta.</span><span class="sxs-lookup"><span data-stu-id="8b430-110">The cmdlet returns either a single object, or a collection of objects, depending on how many objects fit the query.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="8b430-111">En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónicos mediante C#.</span><span class="sxs-lookup"><span data-stu-id="8b430-111">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="8b430-112">**Para emitir una consulta de datos sincrónicos en C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="8b430-112">**To issue a synchronous data query in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="8b430-113">Describa la consulta a WMI mediante CimSession. QueryInstances.</span><span class="sxs-lookup"><span data-stu-id="8b430-113">Describe your query to WMI using CimSession.QueryInstances.</span></span> <span data-ttu-id="8b430-114">Este método devuelve una colección de objetos CimInstance.</span><span class="sxs-lookup"><span data-stu-id="8b430-114">This method returns a collection of CimInstance objects.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  <span data-ttu-id="8b430-115">Use técnicas estándar de colección de lenguaje C# para tener acceso a cada objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="8b430-115">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

<span data-ttu-id="8b430-116">En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónicos mediante C#.</span><span class="sxs-lookup"><span data-stu-id="8b430-116">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="8b430-117">**Para emitir una consulta de datos sincrónicos en C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="8b430-117">**To issue a synchronous data query in C# (System.Management)**</span></span>

1.  <span data-ttu-id="8b430-118">Cree la consulta con un objeto [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) y recupere la información con una llamada a [ManagementObjectSearcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span><span class="sxs-lookup"><span data-stu-id="8b430-118">Create the query with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) object, and retrieve the information with a call to [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span></span>

    <span data-ttu-id="8b430-119">Este método devuelve un objeto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) .</span><span class="sxs-lookup"><span data-stu-id="8b430-119">This method returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  <span data-ttu-id="8b430-120">Use técnicas estándar de colección de lenguaje C# para tener acceso a cada objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="8b430-120">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

<span data-ttu-id="8b430-121">En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónicos mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="8b430-121">The following procedure describes how to issue a synchronous data query using VBScript.</span></span>

<span data-ttu-id="8b430-122">**Para emitir una consulta de datos sincrónicos en VBScript**</span><span class="sxs-lookup"><span data-stu-id="8b430-122">**To issue a synchronous data query in VBScript**</span></span>

1.  <span data-ttu-id="8b430-123">Describa la consulta a WMI mediante [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="8b430-123">Describe your query to WMI using [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="8b430-124">Este método devuelve un [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="8b430-124">This method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  <span data-ttu-id="8b430-125">Utilice técnicas de [colección](accessing-a-collection.md) de lenguajes de scripting estándar para tener acceso a cada objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="8b430-125">Use standard scripting language [collection](accessing-a-collection.md) techniques to access each returned object.</span></span>

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

<span data-ttu-id="8b430-126">En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónicos mediante C++.</span><span class="sxs-lookup"><span data-stu-id="8b430-126">The following procedure describes how to issue a synchronous data query using C++.</span></span>

<span data-ttu-id="8b430-127">**Para emitir una consulta sincrónica en C++**</span><span class="sxs-lookup"><span data-stu-id="8b430-127">**To issue a synchronous query in C++**</span></span>

1.  <span data-ttu-id="8b430-128">Describa la consulta a WMI a través de una llamada a [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="8b430-128">Describe your query to WMI through a call to [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="8b430-129">El método [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) toma una cadena de búsqueda de WQL como parámetro que describe la consulta.</span><span class="sxs-lookup"><span data-stu-id="8b430-129">The [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) method takes a WQL search string as a parameter that describes your query.</span></span> <span data-ttu-id="8b430-130">WMI realiza la consulta y devuelve un puntero de la interfaz [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="8b430-130">WMI performs the query and returns an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="8b430-131">A través de la interfaz **IEnumWbemClassObject** , puede tener acceso a las clases o instancias que componen el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="8b430-131">Through the **IEnumWbemClassObject** interface, you can access the classes or instances that make up the result set.</span></span>

2.  <span data-ttu-id="8b430-132">Después de recibir la consulta, puede enumerar la consulta con una llamada a [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span><span class="sxs-lookup"><span data-stu-id="8b430-132">After you receive your query, you can enumerate your query with a call to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span></span> <span data-ttu-id="8b430-133">Para obtener más información, consulte [enumeración de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="8b430-133">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

    <span data-ttu-id="8b430-134">En el ejemplo de código siguiente se requieren las siguientes referencias e \# instrucciones include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="8b430-134">The following code example requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    <span data-ttu-id="8b430-135">En el ejemplo de código siguiente se describe cómo consultar los objetos que representan a los usuarios y grupos en WMI.</span><span class="sxs-lookup"><span data-stu-id="8b430-135">The following code example describes how to query for the objects that represent the users and groups in WMI.</span></span>

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
