---
description: Guía básica para usar WMI para obtener datos para scripts y aplicaciones cliente o para proporcionar datos a WMI desde una aplicación.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Uso de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d1556d321441c7e6a3191bf95e85db356e7ba9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475321"
---
# <a name="using-wmi"></a>Uso de WMI

Puede usar WMI desde aplicaciones cliente y scripts. Proporciona una infraestructura que facilita la de detectar y realizar tareas de administración. Además, puede agregar al conjunto de posibles tareas de administración mediante la creación de sus propios proveedores WMI.

> [!Note]  
> La versión de próxima generación de WMI para escribir aplicaciones y scripts está disponible a través de Windows Management Infrastructure (MI). Para obtener más información, vea [Proveedores y clientes de MI.](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page)

 

En esta sección se explican los temas siguientes:

-   [Obtener datos de WMI](#obtaining-data-from-wmi)
-   [Proporcionar datos a WMI](#providing-data-to-wmi)
-   [Tareas importantes para WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Obtener datos de WMI

En el procedimiento siguiente se describe cómo obtener datos de WMI escribiendo un script o una aplicación.

**Para obtener datos de WMI mediante la escritura de un script o una aplicación**

1.  Decida qué idioma se va a usar. Para obtener más información sobre el scripting, vea [Crear un script WMI.](creating-a-wmi-script.md) Para obtener más información sobre C++, vea [Crear una aplicación WMI mediante C++.](creating-a-wmi-application-using-c-.md) Para obtener más información sobre C# o WMI .NET, vea [Información general de .NET de WMI.](/previous-versions/)

    Puede ver o manipular datos WMI en muchos idiomas. En la tabla siguiente se enumeran los temas que describen cómo usar el scripting y los lenguajes de aplicación para obtener datos.

    

    
| Idioma de la aplicación | Tema | 
|----------------------|-------|
| Scripts escritos en el hospedaje ActiveX script de Microsoft, incluidos Visual Basic Scripting Edition (VBScript) y Perl<br /> | <a href="scripting-api-for-wmi.md">API de scripting para WMI.</a><br /> Comience por <a href="creating-a-wmi-script.md">Crear un script WMI</a>.<br /> Para obtener ejemplos de código de script, vea <a href="wmi-tasks-for-scripts-and-applications.md">Tareas wmi para scripts y</a> aplicaciones y el repositorio de scripts de TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter.</a><br /> | 
| Windows PowerShell<br /> | <a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Tareas iniciales con Windows PowerShell</a><br /> Cmdlets de PowerShell wmi, como <a href="/previous-versions//dd315295(v=technet.10)">Get-WmiObject</a>.<br /> | 
| Visual Basic aplicaciones<br /> | <a href="scripting-api-for-wmi.md">API de scripting para WMI.</a><br /> | 
| páginas Active Server<br /> | <a href="scripting-api-for-wmi.md">API de scripting para WMI.</a><br /> Comience por <a href="creating-active-server-pages-for-wmi.md">Crear Active Server para WMI.</a><br /> | 
| aplicaciones de C++<br /> | <a href="com-api-for-wmi.md">API COM para WMI.</a><br /> Empiece por <a href="creating-a-wmi-application-using-c-.md">crear una aplicación WMI mediante C++</a> y ejemplos de aplicación de <a href="wmi-c---application-examples.md">C++</a> WMI (contiene ejemplos).<br /> | 
| .NET Framework aplicaciones escritas en C#, Visual Basic .NET o J #<br /> | Clases del espacio <a href="/previous-versions//hh872326(v=vs.85)"><strong>de nombres Microsoft.Management.Infrastructure.</strong></a><br /><blockquote>    [!Note]<br /><strong>System.Management era el</strong> espacio de nombres original que abarcaba el código administrado para WMI. Sin embargo, la tecnología subyacente para <strong>System.Management</strong> suele ser más lenta que y no escala tan bien como <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft.Management.Infrastructure</strong></a>. Por lo tanto, no se recomienda usar <strong>System.Management</strong> para proyectos nuevos. (Para obtener más información sobre <strong>System.Management,</strong>vea <a href="/previous-versions/bb404655(v=vs.90)">Información general de .NET de WMI).</a>    </blockquote><br /> | 


    

     

2.  Asegúrese de que las conexiones a equipos remotos funcionan.

    Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

3.  La conexión a WMI en equipos remotos requiere la configuración de seguridad correcta, como se explica en [Mantenimiento de la seguridad wmi.](maintaining-wmi-security.md) En la tabla siguiente se enumeran los temas que describen cómo configurar las opciones de seguridad con el scripting y los lenguajes de aplicación.

    

    | Lenguaje                                                      | Tema                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Scripts en cualquier lenguaje, Visual Basic aplicaciones<br/> | [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | páginas Active Server<br/>                                | [Configuración de IIS 5 y versiones posteriores para el scripting ASP de WMI](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Establecer el nivel de seguridad de proceso predeterminado mediante C++](setting-the-default-process-security-level-using-c-.md) y [establecer la seguridad en IWbemServices y otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Después de conectarse a WMI, puede obtener datos a través de consultas y enumeraciones.

    Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) y [Querying with WQL](querying-with-wql.md).

5.  Los datos del Registro están disponibles a través de WMI y puede crear nuevas claves y valores o modificar las existentes.

    Para obtener más información, [vea Modificar el Registro del sistema](modifying-the-system-registry.md).

6.  Puede suscribirse a notificaciones de eventos a través de WMI, ya sea temporalmente entre reinicios del sistema o permanentemente.

    Para obtener más información, vea [Supervisar eventos y](monitoring-events.md) recibir un evento [WMI](receiving-a-wmi-event.md).

7.  Los datos del contador de rendimiento de un sistema están disponibles a través de WMI.

    Los contadores de la biblioteca de rendimiento del sistema se convierten en clases WMI. Para obtener más información, vea [Monitoring Performance Data](monitoring-performance-data.md).

8.  [Tareas de WMI para scripts y](wmi-tasks-for-scripts-and-applications.md) aplicaciones describe cómo realizar muchas tareas administrativas con WMI.

## <a name="providing-data-to-wmi"></a>Proporcionar datos a WMI

En el procedimiento siguiente se describe cómo proporcionar datos a WMI mediante la escritura de un proveedor.

**Para proporcionar datos a WMI mediante la escritura de un proveedor**

-   Decida el tipo de proveedor que se escribirá.

    No se puede escribir un proveedor WMI en VBScript. Sin embargo, puede tomar otros enfoques para escribir un proveedor COM wmi:

    -   Usar el Asistente ATL de WMI en Visual Studio.

        Este enfoque crea un proveedor COM no administrado. Para obtener más información, vea [Agregar un proveedor de instancias wmi y](./writing-an-instance-provider.md) Agregar un proveedor de eventos [WMI](./writing-an-event-provider.md).

    -   Usar COM directamente en cualquier entorno de desarrollo integrado.

        Este enfoque crea un proveedor COM no administrado.

    -   Usar WMI en el .NET Framework para crear un proveedor de código administrado.

        Este enfoque crea un proveedor de código administrado. Los proveedores de código administrado se pueden escribir en cualquier lenguaje .NET Framework, son más fáciles de escribir que los proveedores COM de WMI y pueden obtener datos de las clases basadas en [*CIM*](gloss-c.md)de WMI, como [Clases Win32](/windows/desktop/CIMWin32Prov/win32-provider). Sin embargo, el .NET Framework WMI tiene algunas limitaciones. Para obtener más información, vea [Administrar aplicaciones mediante WMI.](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))

    -   No se recomienda [usar las clases del marco](wmi-c-classes.md) de trabajo del proveedor.

        El marco de trabajo del proveedor se ha reemplazado por los asistentes ATL de WMI, mediante COM directamente o .NET Framework proveedores. Ya no se recomienda crear un proveedor COM WMI con las clases de marco de trabajo del proveedor. En la tabla siguiente se enumeran los temas que describen cómo usar proveedores de .NET Framework COM o .

    

    | Proveedor                                                      | Tema                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | Proveedor COM en el mismo proceso que WMI<br/>            | [Proporcionar datos a WMI](providing-data-to-wmi.md)<br/>                                           |
    | Proveedor desacoplado COM<br/>                             | [Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md)<br/> |
    | .NET Framework proveedor en C# o Visual Basic.NET<br/> | [Administración de aplicaciones mediante WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Tareas importantes para WMI

En los temas siguientes se proporciona información sobre el uso de WMI para supervisar y controlar componentes empresariales.



| Tema                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas wmi para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Describe cómo encontrar la clase WMI y los procedimientos correctos que se usan en scripts y aplicaciones que realizan tareas comunes de administración de equipos y redes, como agregar una nueva conexión de impresora para un equipo remoto o buscar todas las revisiones instaladas en un equipo.<br/>                                                                            |
| [Crear una aplicación WMI o un script](creating-a-wmi-application-or-script.md)<br/>                                                     | Cualquier lenguaje de scripting, como VBScript o Perl, que funcione con ActiveX objetos pueden acceder a datos WMI. Las aplicaciones pueden acceder a WMI en C++, mediante la [API COM](com-api-for-wmi.md) para WMI o en Visual Basic, mediante la biblioteca de tipos Wbemdisp.tlb y scripting API para [WMI.](scripting-api-for-wmi.md)[](using-the-wmi-scripting-type-library.md)<br/> |
| [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Describe cómo los scripts, las aplicaciones y los proveedores pueden establecer conexiones a WMI en equipos remotos para obtener datos o controlar hardware y software.<br/>                                                                                                                                                                                                   |
| [Conectarse a WMI en un equipo remoto mediante Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | Describe cómo usar Windows PowerShell establecer conexiones a WMI en equipos remotos para obtener datos o para controlar hardware y software.<br/>                                                                                                                                                                                                            |
| [Supervisión de eventos](monitoring-events.md)<br/>                                                                                           | Describe cómo obtener notificaciones de eventos mediante la creación de consumidores de eventos WMI temporales o permanentes.<br/>                                                                                                                                                                                                                                                           |
| [Proporcionar datos a WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI proporciona datos de administración dinámica a scripts de cliente y aplicaciones obteniendo datos de proveedores.<br/>                                                                                                                                                                                                                                                    |
| [Obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Describe cómo acceder a proveedores no predeterminados y consideraciones para los escritores de proveedores en sistemas de 64 bits.<br/>                                                                                                                                                                                                                                                    |



