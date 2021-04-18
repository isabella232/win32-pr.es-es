---
description: Una ruta de acceso de objeto de clase describe la ubicación de una clase dentro de un espacio de nombres.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Describir una ruta de acceso de objeto de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706814"
---
# <a name="describing-a-class-object-path"></a><span data-ttu-id="698f9-103">Describir una ruta de acceso de objeto de clase</span><span class="sxs-lookup"><span data-stu-id="698f9-103">Describing a Class Object Path</span></span>

<span data-ttu-id="698f9-104">Una ruta de acceso de objeto de clase describe la ubicación de una clase dentro de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="698f9-104">A class object path describes the location of a class within a namespace.</span></span>

<span data-ttu-id="698f9-105">Puede usar los métodos siguientes para especificar una ruta de acceso de objeto:</span><span class="sxs-lookup"><span data-stu-id="698f9-105">You can use the following methods to specify an object path:</span></span>

-   <span data-ttu-id="698f9-106">Una ruta de acceso de objeto completa a una clase anexa el nombre de la clase a una ruta de acceso del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="698f9-106">A full object path to a class appends the class name to a namespace path.</span></span>

    <span data-ttu-id="698f9-107">En el ejemplo siguiente se muestra la ubicación de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de \\ nombres root Cimv2 en el servidor denominado admin.</span><span class="sxs-lookup"><span data-stu-id="698f9-107">The following example shows the location of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class within the \\root\\cimv2 namespace on the server named Admin.</span></span>

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   <span data-ttu-id="698f9-108">Una ruta de acceso relativa al objeto representa una clase que reside en el espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="698f9-108">A relative object path represents a class that resides in the current namespace.</span></span> <span data-ttu-id="698f9-109">Una ruta de acceso relativa a un objeto para una clase contiene solo el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="698f9-109">A relative object path to a class contains only the class name.</span></span>

    <span data-ttu-id="698f9-110">En el ejemplo siguiente se muestra la ruta de acceso relativa a la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="698f9-110">The following example shows the relative path to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

    ``` syntax
    Win32_LogicalDisk
    ```

<span data-ttu-id="698f9-111">Cuando se consulta un nombre de clase pero no se especifica ninguna instancia, WMI devuelve la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="698f9-111">When you query for a class name but specify no instances, WMI returns the class definition.</span></span> <span data-ttu-id="698f9-112">En el procedimiento siguiente se describe cómo recuperar una definición de clase en VBScript.</span><span class="sxs-lookup"><span data-stu-id="698f9-112">The following procedure describes how to retrieve a class definition in VBScript.</span></span>

<span data-ttu-id="698f9-113">**Para recuperar una definición de clase en VBScript**</span><span class="sxs-lookup"><span data-stu-id="698f9-113">**To retrieve a class definition in VBScript**</span></span>

-   <span data-ttu-id="698f9-114">Puede usar la conexión de moniker con una consulta o [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="698f9-114">You can use the moniker connection either with a query or [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span></span> <span data-ttu-id="698f9-115">También puede usar [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="698f9-115">You can also use [**SWbemServices.Get**](swbemservices-get.md).</span></span>

    <span data-ttu-id="698f9-116">En el ejemplo siguiente se muestra cómo usar [GetObject](/previous-versions//kdccchxa(v=vs.85)) para obtener una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="698f9-116">The following example shows how to use [GetObject](/previous-versions//kdccchxa(v=vs.85)) to get a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    <span data-ttu-id="698f9-117">En el ejemplo siguiente se muestra cómo consultar una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="698f9-117">The following example shows how to query for a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

<span data-ttu-id="698f9-118">Puede recuperar una definición de clase en C++ especificando solo el nombre de clase y sin ruta de acceso a una instancia determinada.</span><span class="sxs-lookup"><span data-stu-id="698f9-118">You can retrieve a class definition in C++ by specifying only the class name and no path to a particular instance.</span></span> <span data-ttu-id="698f9-119">En el procedimiento siguiente se describe cómo recuperar una definición de clase en C++.</span><span class="sxs-lookup"><span data-stu-id="698f9-119">The following procedure describes how to retrieve a class definition in C++.</span></span>

<span data-ttu-id="698f9-120">**Para recuperar una definición de clase en C++**</span><span class="sxs-lookup"><span data-stu-id="698f9-120">**To retrieve a class definition in C++**</span></span>

-   <span data-ttu-id="698f9-121">Realice una llamada a las funciones [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="698f9-121">Make a call to the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) functions.</span></span>

    <span data-ttu-id="698f9-122">En el ejemplo siguiente se muestra cómo llamar a la función [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="698f9-122">The following example shows how to call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) function.</span></span>

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    <span data-ttu-id="698f9-123">En el ejemplo de código anterior se requiere que la siguiente \# instrucción include se compile correctamente.</span><span class="sxs-lookup"><span data-stu-id="698f9-123">The previous code example requires the following \#include statement to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
