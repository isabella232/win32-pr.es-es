---
description: WMI proporciona una infraestructura de administración del sistema estandarizada que pueden aprovechar varios clientes diferentes.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Creación de clientes WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95123d4462408a25591df2babb8b1ddd83942e5e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883069"
---
# <a name="creating-wmi-clients"></a>Creación de clientes WMI

WMI proporciona una infraestructura de administración del sistema estandarizada que pueden aprovechar varios clientes diferentes. Estos clientes van desde la herramienta wmic.exe línea de comandos hasta System Center Operations Manager. Puede escribir sus propios clientes WMI mediante wmi scripting API, la API nativa de C++ o mediante los tipos del espacio de nombres de la biblioteca de clases System.Management .NET Framework.

## <a name="how-to-create-a-wmi-client"></a>Cómo crear un cliente WMI

La funcionalidad básica de WMI consiste en recuperar objetos del repositorio WMI y examinar las propiedades de esos objetos. También puede optar por actualizar esas propiedades o llamar a métodos en esas propiedades. En los ejemplos siguientes se muestra cómo realizar una tarea básica de administración de WMI: recuperar el nombre del equipo local.



<table>
<colgroup>
<col  />
<col  />
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
<td>WMI y PowerShell están estrechamente integrados; por lo tanto, la recuperación de objetos WMI con PowerShell es simplemente una cuestión de llamar al cmdlet Get-WmiObject. Tenga en cuenta que, por coherencia, el primer fragmento de código indica explícitamente muchos de los valores predeterminados; el segundo supone que los valores predeterminados son correctos.<br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
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
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creación de un cliente con VBScript</p></td>
<td><p>VBScript era el lenguaje de scripting original que tenía un uso común con WMI. Aunque PowerShell se ha vuelto más popular, muchos de los ejemplos de código existentes en esta documentación se escriben en VBScript. Tenga en cuenta que este ejemplo de VBScript concreto indica explícitamente tanto la ruta de acceso del equipo local como el nivel de suplantación; esto no es necesario, pero suele ser un procedimiento recomendado.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creación de un cliente con C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</p></td>
<td><p>Este espacio de nombres contiene la solución actual para acceder a WMI con código administrado y se conoce como infraestructura de administración de Windows (MI o WMIv2). Actualmente, MI es la tecnología admitida para crear clientes de administración administrada. Para obtener más información, vea How to Implement a Managed MI Client (Cómo implementar un cliente <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">de MI administrado)</a> y How to Implement a Native MI Client (Cómo <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">implementar un cliente de MI nativo).</a></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
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
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creación de un cliente con C# (<a href="/dotnet/api/system.management">System.Management</a>)</p></td>
<td><p>Este espacio de nombres contiene la solución original para acceder a WMI con código administrado. Aunque las <a href="/dotnet/api/system.management">clases System.Management</a> siguen estando disponibles, las clases <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> suelen ser más eficaces y escalan mejor. Por lo tanto, se recomienda usar las clases de MI, en lugar de las clases WMI originales.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
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
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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
| [Tareas wmi para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)                         | Muestra código de cliente WMI de ejemplo.                                                                                                                                                                 |
| [Crear una aplicación WMI o un script](creating-a-wmi-application-or-script.md)                             | Proporciona información sobre cómo crear varios clientes WMI.                                                                                                                                       |
| [Supervisión de datos de rendimiento](monitoring-performance-data.md)                                               | Describe cómo usar WMI para supervisar los datos de rendimiento.                                                                                                                                          |
| [Recepción de un evento WMI](receiving-a-wmi-event.md)                                                           | Describe cómo ver eventos WMI.                                                                                                                                                              |
| [Supervisión de eventos](monitoring-events.md)                                                                   | Describe cómo supervisar eventos WMI.                                                                                                                                                           |
| [Consulta con WQL](querying-with-wql.md)                                                                   | Presenta el lenguaje de consulta de WMI (WQL).                                                                                                                                                       |
| [Consultar el estado de las características opcionales](querying-the-status-of-optional-features.md)                     | En Windows 7, WMI implementó la [**clase \_ OptionalFeature de Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Esta clase recupera el estado de las características opcionales que están presentes en un equipo. |
| [Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md)                       | Se centra en la sintaxis para describir la ubicación de una entidad administrada de WMI.                                                                                                                     |
| [Acceso a otras características del sistema operativo con WMI](accessing-other-operating-system-features-with-wmi.md) | Describe cómo escribir clientes WMI que acceden a controladores de dispositivo, Active Directory y dispositivos SNMP.                                                                                             |
| [Acceso a datos en el espacio de nombres Interop](accessing-data-in-the-interop-namespace.md)                       | Los proveedores de asociación permiten Windows de Instrumental de administración de recursos (WMI) recorrer y recuperar perfiles e instancias de clase asociadas de distintos espacios de nombres.                      |
| [Manipulación de información de clase e instancia](manipulating-class-and-instance-information.md)               | Describe las tareas comunes que deben realizar los clientes WMI.                                                                                                                                      |
| [Vincular clases juntas](linking-classes-together.md)                                                     | Describe el proveedor de vistas y cómo se puede usar para reunir información de varias clases WMI.                                                                                    |
| [Modificar el Registro del sistema](modifying-the-system-registry.md)                                           | Describe cómo los clientes WMI pueden usar WMI para administrar la información del Registro del sistema.                                                                                                                   |



 

