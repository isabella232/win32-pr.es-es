---
description: El primer tipo de objeto que se puede recuperar es una clase WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Recuperación de una clase WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105697980"
---
# <a name="retrieving-a-wmi-class"></a><span data-ttu-id="454fc-103">Recuperación de una clase WMI</span><span class="sxs-lookup"><span data-stu-id="454fc-103">Retrieving a WMI Class</span></span>

<span data-ttu-id="454fc-104">El primer tipo de objeto que se puede recuperar es una clase WMI.</span><span class="sxs-lookup"><span data-stu-id="454fc-104">The first type of object you can retrieve is a WMI class.</span></span> <span data-ttu-id="454fc-105">Al recuperar una clase WMI, en realidad se recupera una definición de clase, que es una lista de las propiedades, calificadores y métodos que describen la clase por completo.</span><span class="sxs-lookup"><span data-stu-id="454fc-105">When retrieving a WMI class, you actually retrieve a class definition, which is a listing of the properties, qualifiers, and methods that fully describe the class.</span></span> <span data-ttu-id="454fc-106">Sin embargo, una definición de clase es básicamente la propia clase.</span><span class="sxs-lookup"><span data-stu-id="454fc-106">However, a class definition is basically the class itself.</span></span>

<span data-ttu-id="454fc-107">PowerShell usa una consulta estándar para recuperar definiciones de clase, mediante la clase **meta \_ Class** .</span><span class="sxs-lookup"><span data-stu-id="454fc-107">PowerShell uses a standard query to retrieve class definitions, using the **meta\_class** class.</span></span>

<span data-ttu-id="454fc-108">**Para recuperar una definición de clase en PowerShell**</span><span class="sxs-lookup"><span data-stu-id="454fc-108">**To retrieve a class definition in PowerShell**</span></span>

-   <span data-ttu-id="454fc-109">Use [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) con una consulta para la **\_ clase meta**, con la cláusula WHERE que contiene el nombre de la clase con la que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="454fc-109">Use the [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    <span data-ttu-id="454fc-110">[Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) es el cmdlet estándar que PowerShell usa para recuperar información de clase e instancia de WMI.</span><span class="sxs-lookup"><span data-stu-id="454fc-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) is the standard cmdlet PowerShell uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="454fc-111">La clase **meta \_ Class** define la consulta como una consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="454fc-111">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="454fc-112">Sin la clase **meta \_ Class** , esta consulta devolvería todas las instancias de Win32 \_ LogicalDisk.</span><span class="sxs-lookup"><span data-stu-id="454fc-112">Without the **meta\_class** class, this query would return all instances of Win32\_LogicalDisk.</span></span> <span data-ttu-id="454fc-113">Para obtener más información sobre cómo consultar WMI, vea [instrucción SELECT para consultas de esquema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="454fc-113">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="454fc-114">El proceso actual para recuperar una definición de WMI en C# es usar la clase **CIMInstance** .</span><span class="sxs-lookup"><span data-stu-id="454fc-114">The current process for retrieving a WMI definition in C# is to use **CIMInstance** class.</span></span>

<span data-ttu-id="454fc-115">**Para recuperar una definición de clase en C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="454fc-115">**To retrieve a class definition in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="454fc-116">Con el espacio de nombres **Microsoft. Management. Infrastructure** , cree una clase **CIMInstance** con el espacio de nombres y el nombre de clase especificados.</span><span class="sxs-lookup"><span data-stu-id="454fc-116">Using the **Microsoft.Management.Infrastructure** namespace, create a **CIMInstance** class with the specified namespace and class name.</span></span>

    <span data-ttu-id="454fc-117">La clase creada contendrá toda la información de la clase, pero no los datos de la instancia.</span><span class="sxs-lookup"><span data-stu-id="454fc-117">The created class will contain all of the class information, but no instance data.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="454fc-118">Como alternativa, como con PowerShell, también puede realizar una consulta mediante la etiqueta **meta \_ Class** como parte de la consulta.</span><span class="sxs-lookup"><span data-stu-id="454fc-118">Alternately, as with PowerShell, you could also perform a query, using the **meta\_class** tag as part of the query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

<span data-ttu-id="454fc-119">Al igual que con PowerShell, C# usa una consulta de **\_ metaclase** para recuperar definiciones de clase.</span><span class="sxs-lookup"><span data-stu-id="454fc-119">As with PowerShell, C# uses a **meta\_class** query to retrieve class definitions.</span></span> <span data-ttu-id="454fc-120">Como alternativa, puede crear un objeto **ManagementClass** para tener acceso directamente a la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="454fc-120">Alternately, you can create a **ManagementClass** object to access the class definition directly.</span></span>

> [!Note]  
> <span data-ttu-id="454fc-121">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="454fc-121">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="454fc-122">**Para recuperar una definición de clase en C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="454fc-122">**To retrieve a class definition in C# (System.Management)**</span></span>

1.  <span data-ttu-id="454fc-123">Puede usar [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) con una consulta a **meta \_ Class**, con la cláusula WHERE que contiene el nombre de la clase con la que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="454fc-123">You can use the [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    <span data-ttu-id="454fc-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) es la clase estándar que usa .net para recuperar información de clase e instancia de WMI.</span><span class="sxs-lookup"><span data-stu-id="454fc-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) is the standard class .NET uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="454fc-125">[ManagementObjectSerarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) devuelve un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contiene la clase de definición de esquema.</span><span class="sxs-lookup"><span data-stu-id="454fc-125">[ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains the schema definition class.</span></span> <span data-ttu-id="454fc-126">La clase **meta \_ Class** define la consulta como una consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="454fc-126">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="454fc-127">Sin la clase **meta \_ Class** , esta consulta devolvería todas las instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="454fc-127">Without the **meta\_class** class, this query would return all instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="454fc-128">Para obtener más información sobre cómo consultar WMI, vea [instrucción SELECT para consultas de esquema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="454fc-128">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

2.  <span data-ttu-id="454fc-129">Como alternativa, cree un nuevo objeto [ManagementClass](/dotnet/api/system.management.managementclass) , con el nombre de la ruta de acceso, para recuperar la clase.</span><span class="sxs-lookup"><span data-stu-id="454fc-129">Alternately, create a new [ManagementClass](/dotnet/api/system.management.managementclass) object, with the name as the path, to retrieve the class.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

<span data-ttu-id="454fc-130">Puede recuperar una definición de clase en VBScript de una manera similar a la recuperación de una instancia específica.</span><span class="sxs-lookup"><span data-stu-id="454fc-130">You can retrieve a class definition in VBScript in a similar way to retrieving a specific instance.</span></span>

<span data-ttu-id="454fc-131">**Para recuperar una definición de clase en VBScript**</span><span class="sxs-lookup"><span data-stu-id="454fc-131">**To retrieve a class definition in VBScript**</span></span>

1.  <span data-ttu-id="454fc-132">Llame a [**SWbemServices. Get**](swbemservices-get.md) pero no identifique una instancia específica en la ruta de acceso del objeto para la clase.</span><span class="sxs-lookup"><span data-stu-id="454fc-132">Call [**SWbemServices.Get**](swbemservices-get.md) but do not identify a specific instance in the object path for the class.</span></span>
2.  <span data-ttu-id="454fc-133">En el ejemplo de código siguiente se recupera la definición de clase para la clase que describe las unidades lógicas del equipo.</span><span class="sxs-lookup"><span data-stu-id="454fc-133">The following code example retrieves the class definition for the class that describes logical drives on your computer.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    <span data-ttu-id="454fc-134">Windows Script Host (WSH) también admite lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="454fc-134">Windows Script Host (WSH) also supports the following.</span></span>

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    <span data-ttu-id="454fc-135">En Active Server páginas (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) o [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) en el script del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="454fc-135">On Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) or [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) in the server-side script.</span></span> <span data-ttu-id="454fc-136">Para obtener más información, consulte [crear páginas Active Server para WMI](creating-active-server-pages-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="454fc-136">For more information, see [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).</span></span>

3.  <span data-ttu-id="454fc-137">También se puede especificar una clase o una instancia, en cuyo caso el objeto devuelto es un objeto WMI, por ejemplo, una instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), en lugar de un objeto Services.</span><span class="sxs-lookup"><span data-stu-id="454fc-137">A class or instance can also be specified, in which case the returned object is a WMI object, for example, an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), rather than a services object.</span></span> <span data-ttu-id="454fc-138">Tenga en cuenta que no puede utilizar las funciones [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) de VBScript para crear una instancia del objeto genérico [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="454fc-138">Note that you cannot use the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) functions to create an instance of the generic object [**SWbemObject**](swbemobject.md).</span></span>
4.  <span data-ttu-id="454fc-139">En las páginas HTML que se ejecutan en Microsoft Internet Explorer (IE), se puede producir un error en [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) y [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) , ya que los objetos de scripting de WMI, como los controles ActiveX, no se marcan como seguros para el scripting.</span><span class="sxs-lookup"><span data-stu-id="454fc-139">In HTML pages running in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) and [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) can fail because WMI scripting objects, like ActiveX controls, are not marked as safe for scripting.</span></span> <span data-ttu-id="454fc-140">La única excepción es el objeto [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="454fc-140">The one exception is the [**SWbemDateTime**](swbemdatetime.md) object.</span></span> <span data-ttu-id="454fc-141">La única manera en que estas llamadas se pueden realizar es cuando se reduce la configuración de seguridad de Internet Explorer, lo que no se recomienda.</span><span class="sxs-lookup"><span data-stu-id="454fc-141">The only way that these calls can succeed is when you lower the IE security settings, which is not recommended.</span></span>

<span data-ttu-id="454fc-142">Al recuperar una clase en C++, llame a la versión [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="454fc-142">When retrieving a class in C++, call the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) version of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="454fc-143">**Para recuperar una definición de clase en C++**</span><span class="sxs-lookup"><span data-stu-id="454fc-143">**To retrieve a class definition in C++**</span></span>

1.  <span data-ttu-id="454fc-144">Llame a los métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para recuperar la definición de una clase.</span><span class="sxs-lookup"><span data-stu-id="454fc-144">Call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to retrieve the definition of a class.</span></span>
2.  <span data-ttu-id="454fc-145">Una clase puede tener varias definiciones de clase, lo que suele ocurrir cuando se tiene más de un proveedor de clases cargado en un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="454fc-145">One class can have multiple class definitions, which happens typically when you have more than one class provider loaded into one namespace.</span></span> <span data-ttu-id="454fc-146">Cuando una clase tiene varias definiciones de clase, WMI devuelve la primera definición detectada y el código de estado de **\_ objetos WBEM S \_ duplicados \_** .</span><span class="sxs-lookup"><span data-stu-id="454fc-146">When a class has multiple class definitions, WMI returns the first definition discovered and the **WBEM\_S\_DUPLICATE\_OBJECTS** status code.</span></span>

<span data-ttu-id="454fc-147">Dado que [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) devuelve una definición de clase, se utiliza normalmente como primer paso para crear una instancia.</span><span class="sxs-lookup"><span data-stu-id="454fc-147">Because [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) returns a class definition, it is commonly used as the first step in creating an instance.</span></span> <span data-ttu-id="454fc-148">Para obtener más información sobre cómo usar **GetObject**, vea [crear y declarar una instancia de mediante C++](creating-and-declaring-an-instance-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="454fc-148">For more information on how to use **GetObject**, see [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).</span></span>

 

 
