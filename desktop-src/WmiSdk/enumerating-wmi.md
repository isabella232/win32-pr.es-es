---
description: La enumeración es el acto de desplazarse por un conjunto de objetos y, posiblemente, modificar cada objeto como se hace.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Enumerar WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715831"
---
# <a name="enumerating-wmi"></a><span data-ttu-id="d1880-103">Enumerar WMI</span><span class="sxs-lookup"><span data-stu-id="d1880-103">Enumerating WMI</span></span>

<span data-ttu-id="d1880-104">La enumeración es el acto de desplazarse por un conjunto de objetos y, posiblemente, modificar cada objeto como se hace.</span><span class="sxs-lookup"><span data-stu-id="d1880-104">Enumeration is the act of moving through a set of objects and possibly modifying each object as you do so.</span></span> <span data-ttu-id="d1880-105">Por ejemplo, puede enumerar un conjunto de objetos [**\_ DiskDrive de Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) para buscar un número de serie determinado.</span><span class="sxs-lookup"><span data-stu-id="d1880-105">For example, you can enumerate through a set of [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) objects to find a particular serial number.</span></span> <span data-ttu-id="d1880-106">Tenga en cuenta que aunque puede enumerar cualquier objeto, WMI solo devuelve objetos a los que tiene acceso de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d1880-106">Note that although you can enumerate any object, WMI only returns objects to which you have security access.</span></span>

<span data-ttu-id="d1880-107">Las enumeraciones de grandes conjuntos de datos pueden requerir una gran cantidad de recursos y degradar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d1880-107">Enumerations of large data sets can require a large amount of resources and degrade performance.</span></span> <span data-ttu-id="d1880-108">Para obtener más información, vea mejorar el rendimiento de la [enumeración](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-108">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span> <span data-ttu-id="d1880-109">También puede solicitar datos con una consulta más específica.</span><span class="sxs-lookup"><span data-stu-id="d1880-109">You also can request data with a more specific query.</span></span> <span data-ttu-id="d1880-110">Para obtener más información, consulte [consultar WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-110">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="d1880-111">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="d1880-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="d1880-112">Enumeración de WMI mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1880-112">Enumerating WMI Using PowerShell</span></span>](#enumerating-wmi-using-powershell)
-   [<span data-ttu-id="d1880-113">Enumeración de WMI mediante C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="d1880-113">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [<span data-ttu-id="d1880-114">Enumerar WMI mediante C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="d1880-114">Enumerating WMI Using C# (System.Management)</span></span>](#enumerating-wmi-using-c-systemmanagement)
-   [<span data-ttu-id="d1880-115">Enumerar WMI mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="d1880-115">Enumerating WMI Using VBScript</span></span>](#enumerating-wmi-using-vbscript)
-   [<span data-ttu-id="d1880-116">Enumerar WMI mediante C++</span><span class="sxs-lookup"><span data-stu-id="d1880-116">Enumerating WMI Using C++</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a><span data-ttu-id="d1880-117">Enumeración de WMI mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1880-117">Enumerating WMI Using PowerShell</span></span>

<span data-ttu-id="d1880-118">Si no conoce la ruta de acceso del objeto para una instancia específica o desea recuperar todas las instancias de una clase específica, use [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx)con el nombre de la clase en el parámetro *-Class* .</span><span class="sxs-lookup"><span data-stu-id="d1880-118">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), with the name of the class in the *-class* parameter.</span></span> <span data-ttu-id="d1880-119">Si desea utilizar una consulta, puede usar el parámetro *-query* .</span><span class="sxs-lookup"><span data-stu-id="d1880-119">If you want to use a query, you can use the *-query* parameter.</span></span>

<span data-ttu-id="d1880-120">En el procedimiento siguiente se describe cómo enumerar las instancias de una clase mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d1880-120">The following procedure describes how to enumerate the instances of a class using PowerShell.</span></span>

<span data-ttu-id="d1880-121">**Para enumerar las instancias de una clase mediante PowerShell**</span><span class="sxs-lookup"><span data-stu-id="d1880-121">**To enumerate the instances of a class using PowerShell**</span></span>

1.  <span data-ttu-id="d1880-122">Enumerar las instancias con una llamada al cmdlet [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d1880-122">Enumerate the instances with a call to [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

    <span data-ttu-id="d1880-123">[Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) devuelve una colección de uno o más objetos de WMI, a través de los cuales se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="d1880-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) returns a collection of one or more WMI objects, through which you can enumerate.</span></span> <span data-ttu-id="d1880-124">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-124">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

    <span data-ttu-id="d1880-125">Si desea recuperar una instancia de clase WMI en otro espacio de nombres o en un equipo diferente, especifique el equipo y el espacio de nombres en los parámetros *-Computer* y *-namespace* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d1880-125">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *-computer* and *-namespace* parameters, respectively.</span></span> <span data-ttu-id="d1880-126">Para obtener más información, vea [crear un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="d1880-127">Esto solo funciona si tiene los privilegios de acceso adecuados.</span><span class="sxs-lookup"><span data-stu-id="d1880-127">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="d1880-128">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md) y [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-128">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="d1880-129">Recupere todas las instancias individuales que desee mediante los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="d1880-129">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="d1880-130">En el ejemplo de código siguiente se recupera una colección de PowerShell y, a continuación, se muestra la propiedad Size para todas las instancias de unidades lógicas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d1880-130">The following code example retrieves an PowerShell collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a><span data-ttu-id="d1880-131">Enumeración de WMI mediante C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="d1880-131">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>

1.  <span data-ttu-id="d1880-132">Agregue una referencia al ensamblado de referencia **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="d1880-132">Add a reference to the **Microsoft.Management.Infrastructure** reference assembly.</span></span> <span data-ttu-id="d1880-133">(Este ensamblado se incluye como parte del [Kit de desarrollo de software (SDK) de Windows para Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)).</span><span class="sxs-lookup"><span data-stu-id="d1880-133">(This assembly ships as part of the [Windows Software Development Kit (SDK) for Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span></span>
2.  <span data-ttu-id="d1880-134">Agregue una instrucción **using** para el espacio de nombres **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="d1880-134">Add a **using** statement for the **Microsoft.Management.Infrastructure** namespace.</span></span>

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  <span data-ttu-id="d1880-135">Cree una instancia de un objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d1880-135">Instantiate a [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object.</span></span> <span data-ttu-id="d1880-136">El siguiente fragmento de código usa el valor estándar "localhost" para el método [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d1880-136">The following snippet uses the standard "localhost" value for the [**CimSession.Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) method.</span></span>

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  <span data-ttu-id="d1880-137">Llame al método [**CimSession. QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) pasando el espacio de nombres CIM deseado y el WQL que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d1880-137">Call the [**CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) method passing the desired CIM namespace and WQL to use.</span></span> <span data-ttu-id="d1880-138">El siguiente fragmento de código devolverá dos instancias de que representan dos procesos estándar de Windows en los que la propiedad Handle (que representa un identificador de proceso o un PID) tiene un valor de 0 o 4.</span><span class="sxs-lookup"><span data-stu-id="d1880-138">The following snippet will return two instances representing two standard Windows processes where the handle property (representing a process ID, or PID) has a value of either 0 or 4.</span></span>

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  <span data-ttu-id="d1880-139">Recorra los objetos [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) devueltos.</span><span class="sxs-lookup"><span data-stu-id="d1880-139">Loop through the returned [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) objects.</span></span>

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

<span data-ttu-id="d1880-140">En el ejemplo de código siguiente se enumeran todas las instancias de la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) (que representa los procesos activos) en el equipo local y se imprime el nombre de cada proceso.</span><span class="sxs-lookup"><span data-stu-id="d1880-140">The following code sample enumerates all instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class (which represents active processes) on the local machine, and prints the name of each process.</span></span>

> [!Note]  
> <span data-ttu-id="d1880-141">En una aplicación real definiría como parámetros el nombre de equipo ("localhost") y el espacio de nombres CIM ("root \\ cimv2").</span><span class="sxs-lookup"><span data-stu-id="d1880-141">In a real application you would define as parameters the computer name ("localhost") and CIM namespace ("root\\cimv2").</span></span> <span data-ttu-id="d1880-142">Por motivos de simplicidad, se han codificado de forma rígida en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d1880-142">For purposes of simplicity, these have been hardcoded in this example.</span></span>

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a><span data-ttu-id="d1880-143">Enumerar WMI mediante C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="d1880-143">Enumerating WMI Using C# (System.Management)</span></span>

<span data-ttu-id="d1880-144">Si no conoce la ruta de acceso del objeto para una instancia específica o desea recuperar todas las instancias de una clase concreta, use el objeto [ManagementClass](/dotnet/api/system.management.managementclass) para recuperar un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contiene todas las instancias de una clase determinada en el espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="d1880-144">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [ManagementClass](/dotnet/api/system.management.managementclass) object to retrieve a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains all instances of a given class in the WMI namespace.</span></span> <span data-ttu-id="d1880-145">Como alternativa, puede consultar WMI a través de un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) para obtener el mismo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="d1880-145">Alternately, you can query WMI through a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) to obtain the same set of objects.</span></span>

> [!Note]  
> <span data-ttu-id="d1880-146">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="d1880-146">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="d1880-147">En el procedimiento siguiente se describe cómo enumerar las instancias de una clase mediante C#.</span><span class="sxs-lookup"><span data-stu-id="d1880-147">The following procedure describes how to enumerate the instances of a class using C#.</span></span>

<span data-ttu-id="d1880-148">**Para enumerar las instancias de una clase mediante C #**</span><span class="sxs-lookup"><span data-stu-id="d1880-148">**To enumerate the instances of a class using C#**</span></span>

1.  <span data-ttu-id="d1880-149">Enumerar las instancias de con una llamada a [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span><span class="sxs-lookup"><span data-stu-id="d1880-149">Enumerate the instances with a call to [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span></span>

    <span data-ttu-id="d1880-150">El método [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) devuelve una colección o un conjunto de objetos a través de los cuales se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="d1880-150">The [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="d1880-151">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-151">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="d1880-152">La colección devuelta es realmente un objeto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) , por lo que se puede llamar a cualquiera de los métodos de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="d1880-152">The returned collection is actually an [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="d1880-153">Si desea recuperar una instancia de clase WMI en otro espacio de nombres o en un equipo diferente, especifique el equipo y el espacio de nombres en el parámetro *path* .</span><span class="sxs-lookup"><span data-stu-id="d1880-153">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *path* parameter.</span></span> <span data-ttu-id="d1880-154">Para obtener más información, vea [crear un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-154">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="d1880-155">Esto solo funciona si tiene los privilegios de acceso adecuados.</span><span class="sxs-lookup"><span data-stu-id="d1880-155">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="d1880-156">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md) y [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-156">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="d1880-157">Recupere todas las instancias individuales que desee mediante los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="d1880-157">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="d1880-158">En el ejemplo de código siguiente se recupera una colección de C# y, a continuación, se muestra la propiedad Size para todas las instancias de unidades lógicas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d1880-158">The following code example retrieves an C# collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a><span data-ttu-id="d1880-159">Enumerar WMI mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="d1880-159">Enumerating WMI Using VBScript</span></span>

<span data-ttu-id="d1880-160">Si no conoce la ruta de acceso del objeto para una instancia específica o desea recuperar todas las instancias de una clase concreta, use el método [**SWbemServices.**](swbemservices-instancesof.md) instanceof para devolver una enumeración [**SWbemObjectSet**](swbemobjectset.md) de todas las instancias de una clase.</span><span class="sxs-lookup"><span data-stu-id="d1880-160">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method to return an [**SWbemObjectSet**](swbemobjectset.md) enumeration of all the instances of a class.</span></span> <span data-ttu-id="d1880-161">También puede consultar WMI a través de [**SWbemServices.ExecQuery**](swbemservices-execquery.md) para obtener el mismo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="d1880-161">Alternatively you can query WMI through [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to obtain the same set of objects.</span></span>

<span data-ttu-id="d1880-162">En el procedimiento siguiente se describe cómo enumerar las instancias de una clase mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="d1880-162">The following procedure describes how to enumerate the instances of a class using VBScript.</span></span>

<span data-ttu-id="d1880-163">**Para enumerar las instancias de una clase mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="d1880-163">**To enumerate the instances of a class using VBScript**</span></span>

1.  <span data-ttu-id="d1880-164">Enumerar las instancias de con una llamada al método [**SWbemServices. instances**](swbemservices-instancesof.md) .</span><span class="sxs-lookup"><span data-stu-id="d1880-164">Enumerate the instances with a call to the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method.</span></span>

    <span data-ttu-id="d1880-165">El método [**instances**](swbemservices-instancesof.md) devuelve una colección o un conjunto de objetos a través de los cuales se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="d1880-165">The [**InstancesOf**](swbemservices-instancesof.md) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="d1880-166">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-166">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="d1880-167">La colección devuelta es realmente un objeto [**SWbemObjectSet**](swbemobjectset.md) , por lo que se puede llamar a cualquiera de los métodos de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="d1880-167">The returned collection is actually an [**SWbemObjectSet**](swbemobjectset.md) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="d1880-168">Si desea recuperar una instancia de clase WMI en otro espacio de nombres o en un equipo diferente, especifique el equipo y el espacio de nombres en el moniker.</span><span class="sxs-lookup"><span data-stu-id="d1880-168">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the moniker.</span></span> <span data-ttu-id="d1880-169">Para obtener más información, vea [crear un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-169">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="d1880-170">Esto solo funciona si tiene los privilegios de acceso adecuados.</span><span class="sxs-lookup"><span data-stu-id="d1880-170">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="d1880-171">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md) y [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-171">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="d1880-172">Recupere todas las instancias individuales que desee mediante los métodos de las colecciones.</span><span class="sxs-lookup"><span data-stu-id="d1880-172">Retrieve any individual instances you wish using the collections methods.</span></span>

<span data-ttu-id="d1880-173">En el ejemplo de código siguiente se recupera un objeto [**SWbemServices**](swbemservices.md) y, a continuación, se ejecuta el método [**instances**](swbemservices-instancesof.md) para mostrar la propiedad tamaño de todas las instancias de unidades lógicas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d1880-173">The following code example retrieves an [**SWbemServices**](swbemservices.md) object and then executes the [**InstancesOf**](swbemservices-instancesof.md) method to display the size property for all instances of logical drives on the local computer.</span></span>


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a><span data-ttu-id="d1880-174">Enumerar WMI mediante C++</span><span class="sxs-lookup"><span data-stu-id="d1880-174">Enumerating WMI Using C++</span></span>

<span data-ttu-id="d1880-175">Además de realizar la enumeración básica, puede establecer varias marcas y propiedades para aumentar el rendimiento de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d1880-175">In addition to performing basic enumeration, you can set several flags and properties to increase the performance of your enumeration.</span></span> <span data-ttu-id="d1880-176">Para obtener más información, vea mejorar el rendimiento de la [enumeración](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-176">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span>

<span data-ttu-id="d1880-177">**Para enumerar un conjunto de objetos en WMI**</span><span class="sxs-lookup"><span data-stu-id="d1880-177">**To enumerate an object set in WMI**</span></span>

1.  <span data-ttu-id="d1880-178">Cree una interfaz [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) que describa el conjunto de objetos que desea enumerar.</span><span class="sxs-lookup"><span data-stu-id="d1880-178">Create an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface describing the set of objects you wish to enumerate.</span></span>

    <span data-ttu-id="d1880-179">Un objeto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contiene una lista que describe un conjunto de objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="d1880-179">An [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object contains a list describing a set of WMI objects.</span></span> <span data-ttu-id="d1880-180">Puede usar los métodos **IEnumWbemClassObject** para enumerar los reenvíos, omitir objetos, comenzar al principio y copiar el enumerador.</span><span class="sxs-lookup"><span data-stu-id="d1880-180">You can use the **IEnumWbemClassObject** methods to enumerate forwards, skip objects, begin at the beginning, and copy the enumerator.</span></span> <span data-ttu-id="d1880-181">En la tabla siguiente se enumeran los métodos que se usan para crear enumeradores para diferentes tipos de objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="d1880-181">The following table lists the methods use to create enumerators for different types of WMI objects.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d1880-182">Object</span><span class="sxs-lookup"><span data-stu-id="d1880-182">Object</span></span></th>
    <th><span data-ttu-id="d1880-183">Método</span><span class="sxs-lookup"><span data-stu-id="d1880-183">Method</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d1880-184">Clase</span><span class="sxs-lookup"><span data-stu-id="d1880-184">Class</span></span></td>
    <td><dl><span data-ttu-id="d1880-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: CreateClassEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1880-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a></span></span><br />
<span data-ttu-id="d1880-186">[<strong>IWbemServices:: CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span><span class="sxs-lookup"><span data-stu-id="d1880-186">[<strong>IWbemServices::CreateClassEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d1880-187">Instancia</span><span class="sxs-lookup"><span data-stu-id="d1880-187">Instance</span></span></td>
    <td><dl><span data-ttu-id="d1880-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: CreateInstanceEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1880-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a></span></span><br />
<span data-ttu-id="d1880-189">[<strong>IWbemServices:: CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span><span class="sxs-lookup"><span data-stu-id="d1880-189">[<strong>IWbemServices::CreateInstanceEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d1880-190">Resultado de la consulta</span><span class="sxs-lookup"><span data-stu-id="d1880-190">Query result</span></span></td>
    <td><dl><span data-ttu-id="d1880-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1880-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a></span></span><br />
<span data-ttu-id="d1880-192">[<strong>IWbemServices:: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span><span class="sxs-lookup"><span data-stu-id="d1880-192">[<strong>IWbemServices::ExecQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d1880-193">Notificación de evento</span><span class="sxs-lookup"><span data-stu-id="d1880-193">Event notification</span></span></td>
    <td><dl><span data-ttu-id="d1880-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: ExecNotificationQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1880-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a></span></span><br />
<span data-ttu-id="d1880-195">[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span><span class="sxs-lookup"><span data-stu-id="d1880-195">[<strong>IWbemServices::ExecNotificationQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="d1880-196">Atravesar la enumeración devuelta mediante varias llamadas a [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span><span class="sxs-lookup"><span data-stu-id="d1880-196">Traverse through the returned enumeration using multiple calls to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span></span>

<span data-ttu-id="d1880-197">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="d1880-197">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 
