---
description: WMI proporciona una infraestructura de administración de sistema estandarizada que puede ser aprovechada por varios clientes diferentes.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Creación de clientes WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd6d89c63218ffd20ef66b2115e581bdb9c4373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715837"
---
# <a name="creating-wmi-clients"></a><span data-ttu-id="ce6c9-103">Creación de clientes WMI</span><span class="sxs-lookup"><span data-stu-id="ce6c9-103">Creating WMI Clients</span></span>

<span data-ttu-id="ce6c9-104">WMI proporciona una infraestructura de administración de sistema estandarizada que puede ser aprovechada por varios clientes diferentes.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-104">WMI provides a standardized system management infrastructure that can be leveraged by a number of different clients.</span></span> <span data-ttu-id="ce6c9-105">Estos clientes van desde la herramienta de línea de comandos wmic.exe a System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-105">These clients range from the wmic.exe command line tool to System Center Operations Manager.</span></span> <span data-ttu-id="ce6c9-106">Puede escribir sus propios clientes WMI mediante la API de scripting de WMI, la API de C++ nativa o los tipos del espacio de nombres de la biblioteca de clases System. Management .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-106">You can write your own WMI clients by using either the WMI Scripting API, the native C++ API or by using the types in the System.Management .NET Framework class library namespace.</span></span>

## <a name="how-to-create-a-wmi-client"></a><span data-ttu-id="ce6c9-107">Cómo crear un cliente WMI</span><span class="sxs-lookup"><span data-stu-id="ce6c9-107">How to create a WMI client</span></span>

<span data-ttu-id="ce6c9-108">La funcionalidad básica de WMI consiste en recuperar objetos del repositorio WMI y examinar las propiedades de dichos objetos.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-108">The core functionality of WMI consists of retrieving objects from the WMI repository and examining the properties of those objects.</span></span> <span data-ttu-id="ce6c9-109">También puede optar por actualizar esas propiedades o llamar a métodos en esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-109">You can also choose to update those properties, or call methods on those properties.</span></span> <span data-ttu-id="ce6c9-110">En los siguientes ejemplos se muestra cómo realizar una tarea de administración de WMI básica: recuperar el nombre del equipo local.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-110">The following examples show how to perform a basic WMI administration task: retrieving the name of the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce6c9-111">Término</span><span class="sxs-lookup"><span data-stu-id="ce6c9-111">Term</span></span></th>
<th><span data-ttu-id="ce6c9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce6c9-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce6c9-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creación de un cliente con PowerShell</span><span class="sxs-lookup"><span data-stu-id="ce6c9-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creating a client with PowerShell</span></span><br/></td>
<td><span data-ttu-id="ce6c9-114">WMI y PowerShell están estrechamente integrados; como tal, la recuperación de objetos WMI con PowerShell es simplemente cuestión de llamar al cmdlet Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-114">WMI and PowerShell are tightly integrated; as such, retrieving WMI objects with PowerShell is simply a matter of calling the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="ce6c9-115">Tenga en cuenta que, por coherencia, el primer fragmento de código dice explícitamente muchos de los valores predeterminados. en el segundo se supone que los valores predeterminados son correctos.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-115">Note that for consistency, the first code snippet explicitly states many of the default values; the second assumes that the default values are correct.</span></span><br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce6c9-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ce6c9-116">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#explicitly states many of the default parameters
$myComputer = Get-WmiObject -ComputerName &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Query &quot;SELECT * FROM Win32_ComputerSystem&quot;
foreach ($computer in $myComputer)
{ &quot;System Name: &quot; + $computer.name }

#assumes the default values are correct
Get-WmiObject Win32_ComputerSystem | Format-Table &quot;Name&quot;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce6c9-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Crear un cliente con VBScript</span><span class="sxs-lookup"><span data-stu-id="ce6c9-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creating a client with VBScript</span></span></p></td>
<td><p><span data-ttu-id="ce6c9-118">VBScript era el lenguaje de scripting original que tenía un uso común con WMI.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-118">VBScript was the original scripting language that had common use with WMI.</span></span> <span data-ttu-id="ce6c9-119">Aunque PowerShell se ha vuelto más popular, muchos de los ejemplos de código existentes en esta documentación se escriben en VBScript.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-119">While PowerShell has become more popular, many of the existing code samples in this documentation are written in VBScript.</span></span> <span data-ttu-id="ce6c9-120">Tenga en cuenta que este ejemplo de VBScript concreto indica explícitamente la ruta de acceso al equipo local, así como el nivel de suplantación; Esto no es necesario, pero suele ser un procedimiento recomendado.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-120">Note that this particular VBScript sample explicitly states both the local machine path as well as the impersonation level; this is not required, but is often a best practice.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce6c9-121">VB</span><span class="sxs-lookup"><span data-stu-id="ce6c9-121">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce6c9-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Crear un cliente con C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</span><span class="sxs-lookup"><span data-stu-id="ce6c9-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creating a client with C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</span></span></p></td>
<td><p><span data-ttu-id="ce6c9-123">Este espacio de nombres contiene la solución actual para tener acceso a WMI con código administrado y se conoce como Windows Management Infrastructure (MI o WMIv2).</span><span class="sxs-lookup"><span data-stu-id="ce6c9-123">This namespace contains the current solution for accessing WMI with managed code, and is known as the Windows Management Infrastructure (MI, or WMIv2).</span></span> <span data-ttu-id="ce6c9-124">Actualmente, MI es la tecnología admitida para la creación de clientes de administración administrados.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-124">Currently, MI is the supported technology for creating managed management clients.</span></span> <span data-ttu-id="ce6c9-125">Para obtener más información, vea <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">cómo implementar un cliente de mi administrado</a> y <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">cómo implementar un cliente de mi nativo</a>.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-125">For more information, see <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client</a> and <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">How to Implement a Native MI Client</a>.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce6c9-126">C#</span><span class="sxs-lookup"><span data-stu-id="ce6c9-126">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce6c9-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Crear un cliente con C# (<a href="/dotnet/api/system.management">System. Management</a>)</span><span class="sxs-lookup"><span data-stu-id="ce6c9-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creating a client with C# (<a href="/dotnet/api/system.management">System.Management</a>)</span></span></p></td>
<td><p><span data-ttu-id="ce6c9-128">Este espacio de nombres contiene la solución original para tener acceso a WMI con código administrado.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-128">This namespace contains the original solution for accessing WMI with managed code.</span></span> <span data-ttu-id="ce6c9-129">Aunque las clases <a href="/dotnet/api/system.management">System. Management</a> siguen estando disponibles, las clases <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> suelen ser más eficaces y escalables mejor.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-129">While the <a href="/dotnet/api/system.management">System.Management</a> classes are still available, the <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> classes are generally more efficient and scale better.</span></span> <span data-ttu-id="ce6c9-130">Como tal, se recomienda usar las clases de MI, en lugar de las clases de WMI originales.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-130">As such, it is recommended that you use the MI classes, rather than the original WMI classes.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce6c9-131">C#</span><span class="sxs-lookup"><span data-stu-id="ce6c9-131">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce6c9-132">En la siguiente tabla se enumeran los temas incluidos en esta sección.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-132">The following table lists the topics covered in this section.</span></span>



| <span data-ttu-id="ce6c9-133">Tema</span><span class="sxs-lookup"><span data-stu-id="ce6c9-133">Topic</span></span>                                                                                                        | <span data-ttu-id="ce6c9-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce6c9-134">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce6c9-135">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="ce6c9-135">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)                         | <span data-ttu-id="ce6c9-136">Describe una serie de problemas que surgen cuando los clientes usan la infraestructura WMI en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-136">Describes a number of issues that arise when clients use the WMI infrastructure on a remote computer.</span></span>                                                                                          |
| [<span data-ttu-id="ce6c9-137">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ce6c9-137">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)                         | <span data-ttu-id="ce6c9-138">Muestra el código de cliente WMI de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-138">Shows example WMI client code.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="ce6c9-139">Crear una aplicación o un script WMI</span><span class="sxs-lookup"><span data-stu-id="ce6c9-139">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)                             | <span data-ttu-id="ce6c9-140">Proporciona información acerca de la creación de varios clientes WMI.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-140">Provides information about creating various WMI clients.</span></span>                                                                                                                                       |
| [<span data-ttu-id="ce6c9-141">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="ce6c9-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)                                               | <span data-ttu-id="ce6c9-142">Describe cómo utilizar WMI para supervisar los datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-142">Describes how to use WMI to monitor performance data.</span></span>                                                                                                                                          |
| [<span data-ttu-id="ce6c9-143">Recibir un evento de WMI</span><span class="sxs-lookup"><span data-stu-id="ce6c9-143">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)                                                           | <span data-ttu-id="ce6c9-144">Describe cómo ver los eventos de WMI.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-144">Describes how to view WMI events.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="ce6c9-145">Supervisión de eventos</span><span class="sxs-lookup"><span data-stu-id="ce6c9-145">Monitoring Events</span></span>](monitoring-events.md)                                                                   | <span data-ttu-id="ce6c9-146">Describe cómo supervisar los eventos de WMI.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-146">Describes how to monitor WMI events.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="ce6c9-147">Realizar consultas con WQL</span><span class="sxs-lookup"><span data-stu-id="ce6c9-147">Querying with WQL</span></span>](querying-with-wql.md)                                                                   | <span data-ttu-id="ce6c9-148">Presenta el lenguaje de consulta de WMI (WQL).</span><span class="sxs-lookup"><span data-stu-id="ce6c9-148">Introduces the WMI Query Language (WQL).</span></span>                                                                                                                                                       |
| [<span data-ttu-id="ce6c9-149">Consultar el estado de las características opcionales</span><span class="sxs-lookup"><span data-stu-id="ce6c9-149">Querying the Status of Optional Features</span></span>](querying-the-status-of-optional-features.md)                     | <span data-ttu-id="ce6c9-150">En Windows 7, WMI implementó la clase [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="ce6c9-150">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="ce6c9-151">Esta clase recupera el estado de las características opcionales que están presentes en un equipo.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-151">This class retrieves the status of the optional features that are present on a computer.</span></span> |
| [<span data-ttu-id="ce6c9-152">Describir la ubicación de un objeto WMI</span><span class="sxs-lookup"><span data-stu-id="ce6c9-152">Describing the Location of a WMI Object</span></span>](describing-the-location-of-a-wmi-object.md)                       | <span data-ttu-id="ce6c9-153">Se centra en la sintaxis para describir la ubicación de una entidad administrada de WMI.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-153">Focuses on the syntax for describing the location of a WMI managed entity.</span></span>                                                                                                                     |
| [<span data-ttu-id="ce6c9-154">Obtener acceso a otras características del sistema operativo con WMI</span><span class="sxs-lookup"><span data-stu-id="ce6c9-154">Accessing Other Operating System Features with WMI</span></span>](accessing-other-operating-system-features-with-wmi.md) | <span data-ttu-id="ce6c9-155">Describe cómo escribir clientes WMI que tengan acceso a controladores de dispositivos, Active Directory y dispositivos SNMP.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-155">Describes how to write WMI clients that access device drivers, Active Directory, and SNMP devices.</span></span>                                                                                             |
| [<span data-ttu-id="ce6c9-156">Obtener acceso a los datos en el espacio de nombres Interop</span><span class="sxs-lookup"><span data-stu-id="ce6c9-156">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)                       | <span data-ttu-id="ce6c9-157">Los proveedores de asociación permiten a los clientes de Instrumental de administración de Windows (WMI) atravesar y recuperar perfiles y las instancias de clase asociadas de distintos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-157">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>                      |
| [<span data-ttu-id="ce6c9-158">Manipular información de clase e instancia</span><span class="sxs-lookup"><span data-stu-id="ce6c9-158">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)               | <span data-ttu-id="ce6c9-159">Describe las tareas comunes que los clientes WMI deben realizar.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-159">Describes the common tasks that WMI clients must perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="ce6c9-160">Vincular clases juntas</span><span class="sxs-lookup"><span data-stu-id="ce6c9-160">Linking Classes Together</span></span>](linking-classes-together.md)                                                     | <span data-ttu-id="ce6c9-161">Describe el proveedor de vistas y cómo se puede usar para reunir información de varias clases WMI.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-161">Discusses the view provider and how it can be used to bring together information from multiple WMI classes.</span></span>                                                                                    |
| [<span data-ttu-id="ce6c9-162">Modificar el registro del sistema</span><span class="sxs-lookup"><span data-stu-id="ce6c9-162">Modifying the System Registry</span></span>](modifying-the-system-registry.md)                                           | <span data-ttu-id="ce6c9-163">Describe cómo los clientes WMI pueden utilizar WMI para administrar la información del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="ce6c9-163">Describes how WMI clients can use WMI to manage system registry information.</span></span>                                                                                                                   |



 

