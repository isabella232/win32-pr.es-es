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
# <a name="creating-wmi-clients"></a>Creación de clientes WMI

WMI proporciona una infraestructura de administración de sistema estandarizada que puede ser aprovechada por varios clientes diferentes. Estos clientes van desde la herramienta de línea de comandos wmic.exe a System Center Operations Manager. Puede escribir sus propios clientes WMI mediante la API de scripting de WMI, la API de C++ nativa o los tipos del espacio de nombres de la biblioteca de clases System. Management .NET Framework.

## <a name="how-to-create-a-wmi-client"></a>Cómo crear un cliente WMI

La funcionalidad básica de WMI consiste en recuperar objetos del repositorio WMI y examinar las propiedades de dichos objetos. También puede optar por actualizar esas propiedades o llamar a métodos en esas propiedades. En los siguientes ejemplos se muestra cómo realizar una tarea de administración de WMI básica: recuperar el nombre del equipo local.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Término</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creación de un cliente con PowerShell<br/></td>
<td>WMI y PowerShell están estrechamente integrados; como tal, la recuperación de objetos WMI con PowerShell es simplemente cuestión de llamar al cmdlet Get-WmiObject. Tenga en cuenta que, por coherencia, el primer fragmento de código dice explícitamente muchos de los valores predeterminados. en el segundo se supone que los valores predeterminados son correctos.<br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Crear un cliente con VBScript</p></td>
<td><p>VBScript era el lenguaje de scripting original que tenía un uso común con WMI. Aunque PowerShell se ha vuelto más popular, muchos de los ejemplos de código existentes en esta documentación se escriben en VBScript. Tenga en cuenta que este ejemplo de VBScript concreto indica explícitamente la ruta de acceso al equipo local, así como el nivel de suplantación; Esto no es necesario, pero suele ser un procedimiento recomendado.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Crear un cliente con C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</p></td>
<td><p>Este espacio de nombres contiene la solución actual para tener acceso a WMI con código administrado y se conoce como Windows Management Infrastructure (MI o WMIv2). Actualmente, MI es la tecnología admitida para la creación de clientes de administración administrados. Para obtener más información, vea <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">cómo implementar un cliente de mi administrado</a> y <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">cómo implementar un cliente de mi nativo</a>.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Crear un cliente con C# (<a href="/dotnet/api/system.management">System. Management</a>)</p></td>
<td><p>Este espacio de nombres contiene la solución original para tener acceso a WMI con código administrado. Aunque las clases <a href="/dotnet/api/system.management">System. Management</a> siguen estando disponibles, las clases <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> suelen ser más eficaces y escalables mejor. Como tal, se recomienda usar las clases de MI, en lugar de las clases de WMI originales.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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



 

En la siguiente tabla se enumeran los temas incluidos en esta sección.



| Tema                                                                                                        | Descripción                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)                         | Describe una serie de problemas que surgen cuando los clientes usan la infraestructura WMI en un equipo remoto.                                                                                          |
| [Tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)                         | Muestra el código de cliente WMI de ejemplo.                                                                                                                                                                 |
| [Crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md)                             | Proporciona información acerca de la creación de varios clientes WMI.                                                                                                                                       |
| [Supervisión de datos de rendimiento](monitoring-performance-data.md)                                               | Describe cómo utilizar WMI para supervisar los datos de rendimiento.                                                                                                                                          |
| [Recibir un evento de WMI](receiving-a-wmi-event.md)                                                           | Describe cómo ver los eventos de WMI.                                                                                                                                                              |
| [Supervisión de eventos](monitoring-events.md)                                                                   | Describe cómo supervisar los eventos de WMI.                                                                                                                                                           |
| [Realizar consultas con WQL](querying-with-wql.md)                                                                   | Presenta el lenguaje de consulta de WMI (WQL).                                                                                                                                                       |
| [Consultar el estado de las características opcionales](querying-the-status-of-optional-features.md)                     | En Windows 7, WMI implementó la clase [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Esta clase recupera el estado de las características opcionales que están presentes en un equipo. |
| [Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md)                       | Se centra en la sintaxis para describir la ubicación de una entidad administrada de WMI.                                                                                                                     |
| [Obtener acceso a otras características del sistema operativo con WMI](accessing-other-operating-system-features-with-wmi.md) | Describe cómo escribir clientes WMI que tengan acceso a controladores de dispositivos, Active Directory y dispositivos SNMP.                                                                                             |
| [Obtener acceso a los datos en el espacio de nombres Interop](accessing-data-in-the-interop-namespace.md)                       | Los proveedores de asociación permiten a los clientes de Instrumental de administración de Windows (WMI) atravesar y recuperar perfiles y las instancias de clase asociadas de distintos espacios de nombres.                      |
| [Manipular información de clase e instancia](manipulating-class-and-instance-information.md)               | Describe las tareas comunes que los clientes WMI deben realizar.                                                                                                                                      |
| [Vincular clases juntas](linking-classes-together.md)                                                     | Describe el proveedor de vistas y cómo se puede usar para reunir información de varias clases WMI.                                                                                    |
| [Modificar el registro del sistema](modifying-the-system-registry.md)                                           | Describe cómo los clientes WMI pueden utilizar WMI para administrar la información del registro del sistema.                                                                                                                   |



 

