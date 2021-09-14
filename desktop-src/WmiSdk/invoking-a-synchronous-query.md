---
description: Una consulta sincrónica es una consulta que mantiene el control sobre el proceso de la aplicación mientras dure la consulta.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Invocación de una consulta sincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070463"
---
# <a name="invoking-a-synchronous-query"></a>Invocación de una consulta sincrónica

Una consulta sincrónica es una consulta que mantiene el control sobre el proceso de la aplicación mientras dure la consulta. Una consulta sincrónica requiere una sola llamada de interfaz y, por tanto, es más sencilla que una llamada asincrónica. Sin embargo, una consulta sincrónica tiene la posibilidad de bloquear la aplicación para consultas o consultas de gran tamaño a través de una red.

En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónica mediante PowerShell.

**Para emitir una consulta de datos sincrónica en PowerShell**

-   Describa la consulta a WMI mediante el cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) de WMI y el *parámetro -query.* El cmdlet devuelve un único objeto o una colección de objetos, en función del número de objetos que se ajusten a la consulta.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónica mediante C#.

**Para emitir una consulta de datos sincrónica en C# (Microsoft.Management.Infrastructure)**

1.  Describa la consulta a WMI mediante CimSession.QueryInstances. Este método devuelve una colección de objetos CimInstance.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  Use técnicas estándar de colección de lenguajes de C# para tener acceso a cada objeto devuelto.

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónica mediante C#.

**Para emitir una consulta de datos sincrónica en C# (System.Management)**

1.  Cree la consulta con un [objeto ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) y recupere la información con una llamada a [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).

    Este método devuelve un [objeto ManagementObjectCollection.](/dotnet/api/system.management.managementobjectcollection)

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  Use técnicas estándar de colección de lenguajes de C# para tener acceso a cada objeto devuelto.

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónica mediante VBScript.

**Para emitir una consulta de datos sincrónica en VBScript**

1.  Describa la consulta a WMI [**mediante SWbemServices.ExecQuery**](swbemservices-execquery.md). Este método devuelve un [**objeto SWbemObjectSet.**](swbemobjectset.md)

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  Use técnicas de recopilación de [lenguajes de scripting](accessing-a-collection.md) estándar para acceder a cada objeto devuelto.

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

En el procedimiento siguiente se describe cómo emitir una consulta de datos sincrónica mediante C++.

**Para emitir una consulta sincrónica en C++**

1.  Describa la consulta a WMI mediante una llamada a [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    El [**método ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) toma una cadena de búsqueda WQL como parámetro que describe la consulta. WMI realiza la consulta y devuelve un puntero de interfaz [**IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) A través **de la interfaz IEnumWbemClassObject,** puede tener acceso a las clases o instancias que forma el conjunto de resultados.

2.  Después de recibir la consulta, puede enumerar la consulta con una llamada a [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next). Para obtener más información, [vea Enumerar WMI.](enumerating-wmi.md)

    En el ejemplo de código siguiente se requieren las siguientes referencias \# e instrucciones include para compilarse correctamente.

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    En el ejemplo de código siguiente se describe cómo consultar los objetos que representan a los usuarios y grupos en WMI.

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

    

 

 
