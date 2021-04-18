---
description: Un calificador es una etiqueta que proporciona más información sobre un objeto, un método o una propiedad de WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Obtener acceso a un calificador de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707102"
---
# <a name="accessing-a-wmi-qualifier"></a><span data-ttu-id="ac928-103">Obtener acceso a un calificador de WMI</span><span class="sxs-lookup"><span data-stu-id="ac928-103">Accessing a WMI Qualifier</span></span>

<span data-ttu-id="ac928-104">Un calificador es una etiqueta que proporciona más información sobre un objeto, un método o una propiedad de WMI.</span><span class="sxs-lookup"><span data-stu-id="ac928-104">A qualifier is a tag that provides more information about a WMI object, method, or property.</span></span> <span data-ttu-id="ac928-105">En ocasiones, puede que necesite tener acceso a los datos almacenados en un calificador.</span><span class="sxs-lookup"><span data-stu-id="ac928-105">At times, you may need to access the data stored in a qualifier.</span></span> <span data-ttu-id="ac928-106">Por ejemplo, una tarea común es determinar si un proveedor implementa un método intentando recuperar el calificador **implementado** para ese método.</span><span class="sxs-lookup"><span data-stu-id="ac928-106">For example, a common task is to determine if a provider implements a method by attempting to retrieve the **Implemented** qualifier for that method.</span></span> <span data-ttu-id="ac928-107">Para obtener más información, vea [calificadores de WMI](wmi-qualifiers.md) y [Agregar un calificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-107">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="ac928-108">Puede recuperar los calificadores de un objeto WMI en PowerShell; para ello, recupere primero el objeto y, a continuación, examine los calificadores como lo haría con cualquier otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="ac928-108">You can retrieve the qualifiers on a WMI object in PowerShell by first retrieving the object, and then examining the qualifiers as you would any other property.</span></span>

<span data-ttu-id="ac928-109">**Para recuperar un calificador mediante PowerShell**</span><span class="sxs-lookup"><span data-stu-id="ac928-109">**To retrieve a qualifier using PowerShell**</span></span>

-   <span data-ttu-id="ac928-110">Recupere el objeto cuyos calificadores desea ver mediante [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx)y, a continuación, acceda a los calificadores a través de la propiedad **Qualifiers** :</span><span class="sxs-lookup"><span data-stu-id="ac928-110">Retrieve the object whose qualifiers you want to view using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), and then access the qualifiers through the **Qualifiers** property:</span></span>

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    <span data-ttu-id="ac928-111">Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-111">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="ac928-112">Puede recuperar los calificadores de una instancia de WMI en C#; para ello, recupere primero el objeto y, a continuación, examine los calificadores como una colección.</span><span class="sxs-lookup"><span data-stu-id="ac928-112">You can retrieve the qualifiers on a WMI instance in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

<span data-ttu-id="ac928-113">**Para recuperar un calificador mediante C# (Microsoft.SysTEM. Administración**</span><span class="sxs-lookup"><span data-stu-id="ac928-113">**To retrieve a qualifier using C# (Microsoft.System.Management)**</span></span>

1.  <span data-ttu-id="ac928-114">Recupere la clase cuyos calificadores desea ver creando un objeto CimInstance con el nombre de clase y el espacio de nombres especificados.</span><span class="sxs-lookup"><span data-stu-id="ac928-114">Retrieve the class whose qualifiers you want to view by creating a CimInstance object, using the specified class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    <span data-ttu-id="ac928-115">Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-115">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="ac928-116">Puede recuperar los calificadores de clase de [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), los calificadores de propiedad de [CimInstance. CimClass. CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))y los calificadores de método de [CimInstance. CimClass. CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac928-116">You can retrieve the class qualifiers from the [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), the property qualifiers from [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85)), and the method qualifiers from [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span></span>

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    <span data-ttu-id="ac928-117">Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-117">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="ac928-118">Puede recuperar los calificadores de un objeto WMI en C#; para ello, recupere primero el objeto y, a continuación, examine los calificadores como una colección.</span><span class="sxs-lookup"><span data-stu-id="ac928-118">You can retrieve the qualifiers on a WMI object in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

> [!Note]  
> <span data-ttu-id="ac928-119">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="ac928-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="ac928-120">**Para recuperar un calificador mediante C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="ac928-120">**To retrieve a qualifier using C# (System.Management)**</span></span>

1.  <span data-ttu-id="ac928-121">Recupere el objeto cuyos calificadores desea ver mediante [ManagementObject](/dotnet/api/system.management.managementobject).</span><span class="sxs-lookup"><span data-stu-id="ac928-121">Retrieve the object whose qualifiers you want to view using [ManagementObject](/dotnet/api/system.management.managementobject).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    <span data-ttu-id="ac928-122">Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-122">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="ac928-123">Coloque los calificadores en un [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)y enumere los valores de [QualifierData](/dotnet/api/system.management.qualifierdata) .</span><span class="sxs-lookup"><span data-stu-id="ac928-123">Place the qualifiers into a [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection), and enumerate through the [QualifierData](/dotnet/api/system.management.qualifierdata) values.</span></span>

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    <span data-ttu-id="ac928-124">Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-124">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="ac928-125">En el procedimiento siguiente se describe cómo recuperar un calificador mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="ac928-125">The following procedure describes how to retrieve a qualifier using VBScript.</span></span>

<span data-ttu-id="ac928-126">**Para recuperar un calificador mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="ac928-126">**To retrieve a qualifier using VBScript**</span></span>

1.  <span data-ttu-id="ac928-127">Recupere el objeto cuyos calificadores desea ver, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ac928-127">Retrieve the object whose qualifiers you want to view, as shown in the following example:</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    <span data-ttu-id="ac928-128">La forma más común de recuperar un objeto es mediante el método [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="ac928-128">The most common way to retrieve an object is by using the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method.</span></span> <span data-ttu-id="ac928-129">Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-129">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="ac928-130">Obtenga acceso a los calificadores del objeto a través de la propiedad [**SWbemObject. Qualifiers \_**](swbemobject-qualifiers-.md) , como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ac928-130">Access the qualifiers of the object through the [**SWbemObject.Qualifiers\_**](swbemobject-qualifiers-.md) property, as shown in the following example:</span></span>

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

<span data-ttu-id="ac928-131">En el ejemplo de código siguiente se describe cómo obtener acceso a todos los calificadores de un objeto de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="ac928-131">The following code example describes how to access all the qualifiers on a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object.</span></span>


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="ac928-132">En el procedimiento siguiente se describe cómo recuperar un calificador mediante C++.</span><span class="sxs-lookup"><span data-stu-id="ac928-132">The following procedure describes how to retrieve a qualifier using C++.</span></span>

<span data-ttu-id="ac928-133">**Para recuperar un calificador mediante C++**</span><span class="sxs-lookup"><span data-stu-id="ac928-133">**To retrieve a qualifier using C++**</span></span>

1.  <span data-ttu-id="ac928-134">Recupere el objeto cuyos calificadores desea ver.</span><span class="sxs-lookup"><span data-stu-id="ac928-134">Retrieve the object whose qualifiers you want to view.</span></span>

    <span data-ttu-id="ac928-135">La forma más común de recuperar un objeto es mediante una llamada a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="ac928-135">The most common way to retrieve an object is by using a call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="ac928-136">Para obtener más información, consulte [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="ac928-136">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="ac928-137">Recupera el conjunto de calificador para una propiedad determinada con una llamada a los métodos [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) o [**IWbemClassObject:: GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="ac928-137">Retrieve the qualifier set for a given property with a call to [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) or [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) methods.</span></span>

3.  <span data-ttu-id="ac928-138">Obtenga acceso a los calificadores del objeto a través de la interfaz [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) devuelta.</span><span class="sxs-lookup"><span data-stu-id="ac928-138">Access the qualifiers of the object through the returned [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="ac928-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ac928-139">Examples</span></span>

<span data-ttu-id="ac928-140">Para obtener más información sobre cómo recuperar calificadores, vea el ejemplo de código de PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) en la galería de TechNet.</span><span class="sxs-lookup"><span data-stu-id="ac928-140">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

 

 
