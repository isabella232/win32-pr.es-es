---
description: Guía básica para el uso de WMI para obtener datos para aplicaciones y scripts de cliente, o para proporcionar datos a WMI desde una aplicación.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Usar WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31878b41de0f44a70c31c2134f0a611a9309a321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156817"
---
# <a name="using-wmi"></a>Usar WMI

Puede usar WMI desde aplicaciones cliente y scripts. Proporciona una infraestructura que facilita la detección y la realización de tareas de administración. Además, puede Agregar al conjunto de posibles tareas de administración mediante la creación de sus propios proveedores de WMI.

> [!Note]  
> La versión de próxima generación de WMI para escribir aplicaciones y scripts está disponible a través de Windows Management Infrastructure (MI). Para obtener más información, vea [proveedores y clientes de mi](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

En esta sección se explican los temas siguientes:

-   [Obtención de datos de WMI](#obtaining-data-from-wmi)
-   [Proporcionar datos a WMI](#providing-data-to-wmi)
-   [Tareas importantes para WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Obtención de datos de WMI

En el procedimiento siguiente se describe cómo obtener datos de WMI escribiendo un script o una aplicación.

**Para obtener datos de WMI escribiendo un script o una aplicación**

1.  Decida qué idioma desea usar. Para obtener más información sobre la creación de scripts, vea [crear un script WMI](creating-a-wmi-script.md). Para obtener más información sobre C++, vea [crear una aplicación WMI con c++](creating-a-wmi-application-using-c-.md). Para obtener más información acerca de C# o WMI .NET, consulte [información general sobre WMI .net](/previous-versions/).

    Puede ver o manipular los datos de WMI en muchos idiomas. En la tabla siguiente se enumeran los temas en los que se describe cómo usar los lenguajes de scripting y de aplicación para obtener datos.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Idioma de la aplicación</th>
    <th>Tema</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Scripts escritos en Microsoft ActiveX script Hosting, incluido Visual Basic Scripting Edition (VBScript) y Perl<br/></td>
    <td><a href="scripting-api-for-wmi.md">API de scripting para WMI</a>.<br/> Comience con <a href="creating-a-wmi-script.md">la creación de un script de WMI</a>.<br/> Para obtener ejemplos de código de script, vea <a href="wmi-tasks-for-scripts-and-applications.md">tareas de WMI para scripts y aplicaciones</a> y el repositorio de scripts de TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Windows PowerShell<br/></td>
    <td><a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Introducción con Windows PowerShell</a><br/> Cmdlets de WMI PowerShell, como <a href="/previous-versions//dd315295(v=technet.10)">Get-WMIObject</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>Aplicaciones Visual Basic<br/></td>
    <td><a href="scripting-api-for-wmi.md">API de scripting para WMI</a>.<br/></td>
    </tr>
    <tr class="even">
    <td>páginas Active Server<br/></td>
    <td><a href="scripting-api-for-wmi.md">API de scripting para WMI</a>.<br/> Comience con la <a href="creating-active-server-pages-for-wmi.md">creación de páginas de Active Server para WMI</a>.<br/></td>
    </tr>
    <tr class="odd">
    <td>aplicaciones de C++<br/></td>
    <td><a href="com-api-for-wmi.md">API com para WMI</a>.<br/> Comience con <a href="creating-a-wmi-application-using-c-.md">la creación de una aplicación WMI mediante</a> los <a href="wmi-c---application-examples.md">ejemplos de aplicación</a> de c++ y WMI de c++ (contiene ejemplos).<br/></td>
    </tr>
    <tr class="even">
    <td>.NET Framework aplicaciones escritas en C#, Visual Basic .NET o J #<br/></td>
    <td>Clases del espacio de nombres <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a> .<br/>
    <blockquote>
    [!Note]<br />
    <strong>System. Management</strong> era el espacio de nombres original que incluía el código administrado para WMI. Sin embargo, la tecnología subyacente de <strong>System. Management</strong> es generalmente más lenta que y no escala, sino también <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. Infrastructure</strong></a>. Como tal, no se recomienda usar <strong>System. Management</strong> para los proyectos nuevos. (Para obtener más información sobre <strong>System. Management</strong>, vea <a href="/previous-versions/bb404655(v=vs.90)">información general sobre WMI .net</a>). </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Asegúrese de que las conexiones a los equipos remotos funcionan.

    Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

3.  La conexión a WMI en equipos remotos requiere la configuración de seguridad correcta, como se explica en [mantener la seguridad de WMI](maintaining-wmi-security.md). En la tabla siguiente se enumeran los temas en los que se describe cómo configurar las opciones de seguridad con los lenguajes de scripting y aplicación.

    

    | Lenguaje                                                      | Tema                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Scripts en cualquier lenguaje, Visual Basic aplicaciones<br/> | [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | páginas Active Server<br/>                                | [Configuración de IIS 5 y versiones posteriores para el scripting de ASP de WMI](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Establecer el nivel de seguridad de proceso predeterminado mediante C++](setting-the-default-process-security-level-using-c-.md) y [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Después de conectarse a WMI, puede obtener datos a través de consultas y enumeraciones.

    Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md) y [realizar consultas con WQL](querying-with-wql.md).

5.  Los datos del registro están disponibles a través de WMI, y puede crear nuevas claves y valores o modificar los existentes.

    Para obtener más información, vea [modificar el registro del sistema](modifying-the-system-registry.md).

6.  Puede suscribirse a notificaciones de eventos a través de WMI, ya sea temporalmente entre los reinicios del sistema o de forma permanente.

    Para obtener más información, vea [supervisar eventos](monitoring-events.md) y [recibir un evento WMI](receiving-a-wmi-event.md).

7.  Los datos del contador de rendimiento de un sistema están disponibles a través de WMI.

    Los contadores de la biblioteca de rendimiento del sistema se convierten en clases WMI. Para obtener más información, vea [supervisar datos de rendimiento](monitoring-performance-data.md).

8.  [Tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md) describe cómo realizar muchas tareas administrativas con WMI.

## <a name="providing-data-to-wmi"></a>Proporcionar datos a WMI

En el procedimiento siguiente se describe cómo proporcionar datos a WMI escribiendo un proveedor.

**Para proporcionar datos a WMI escribiendo un proveedor**

-   Decida el tipo de proveedor que se va a escribir.

    No se puede escribir un proveedor WMI en VBScript. Sin embargo, puede adoptar varios enfoques para escribir un proveedor COM de WMI:

    -   Usar el Asistente para ATL de WMI en Visual Studio.

        Este enfoque crea un proveedor COM no administrado. Para obtener más información, vea [Agregar un proveedor de instancias WMI](./writing-an-instance-provider.md) y [Agregar un proveedor de eventos WMI](./writing-an-event-provider.md).

    -   Usar COM directamente en cualquier entorno de desarrollo integrado.

        Este enfoque crea un proveedor COM no administrado.

    -   Usar WMI en el .NET Framework para crear un proveedor de código administrado.

        Este enfoque crea un proveedor de código administrado. Los proveedores de código administrado se pueden escribir en cualquier lenguaje .NET Framework, son más fáciles de escribir que los proveedores COM WMI y pueden obtener datos de las clases basadas en WMI [*CIM*](gloss-c.md), como [las clases Win32](/windows/desktop/CIMWin32Prov/win32-provider). Sin embargo, el proveedor WMI de .NET Framework tiene algunas limitaciones. Para obtener más información, vea [Administrar aplicaciones mediante WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

    -   No se recomienda el uso de las [clases de Framework de proveedor](wmi-c-classes.md) .

        El marco de trabajo del proveedor se ha sustituido por los asistentes ATL de WMI, utilizando directamente COM o proveedores de .NET Framework. Ya no se recomienda crear un proveedor COM WMI con las clases de marco de trabajo del proveedor. En la tabla siguiente se enumeran los temas en los que se describe cómo utilizar los proveedores COM o .NET Framework.

    

    | Proveedor                                                      | Tema                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | Proveedor COM en el mismo proceso que WMI<br/>            | [Proporcionar datos a WMI](providing-data-to-wmi.md)<br/>                                           |
    | Proveedor desacoplado COM<br/>                             | [Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md)<br/> |
    | .NET Framework proveedor en C# o Visual Basic.NET<br/> | [Administrar aplicaciones mediante WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Tareas importantes para WMI

En los temas siguientes se proporciona información acerca del uso de WMI para supervisar y controlar los componentes de la empresa.



| Tema                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Describe cómo buscar la clase y los procedimientos de WMI correctos para usar en scripts y aplicaciones que realizan tareas comunes de administración de equipos y redes, como agregar una nueva conexión de impresora para un equipo remoto o buscar todas las revisiones instaladas en un equipo.<br/>                                                                            |
| [Crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md)<br/>                                                     | Cualquier lenguaje de scripting, como VBScript o Perl, que funciona con objetos ActiveX puede tener acceso a los datos de WMI. Las aplicaciones pueden tener acceso a WMI en C++, mediante la [API com para WMI](com-api-for-wmi.md) o en Visual Basic, mediante la[biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb y la [API de scripting para WMI](scripting-api-for-wmi.md).<br/> |
| [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Describe cómo los scripts, las aplicaciones y los proveedores pueden establecer conexiones a WMI en equipos remotos para obtener datos o controlar el hardware y el software.<br/>                                                                                                                                                                                                   |
| [Conexión a WMI en un equipo remoto mediante Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | Describe cómo usar Windows PowerShell para establecer conexiones a WMI en equipos remotos con el fin de obtener datos o controlar el hardware y el software.<br/>                                                                                                                                                                                                            |
| [Supervisión de eventos](monitoring-events.md)<br/>                                                                                           | Describe cómo obtener notificaciones de eventos mediante la creación de consumidores de eventos de WMI temporales o permanentes.<br/>                                                                                                                                                                                                                                                           |
| [Proporcionar datos a WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI proporciona datos de administración dinámica a las aplicaciones y los scripts de cliente al obtenerlos de los proveedores.<br/>                                                                                                                                                                                                                                                    |
| [Obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Describe cómo obtener acceso a proveedores y consideraciones no predeterminados para escritores de proveedores en sistemas de 64 bits.<br/>                                                                                                                                                                                                                                                    |



