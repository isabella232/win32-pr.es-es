---
description: El primer tipo de objeto que se puede recuperar es una clase WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Recuperar una clase WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2695a934436e6e53fe84ee11c6008615b3d6f5d1807039d76b72fa704a2cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739884"
---
# <a name="retrieving-a-wmi-class"></a>Recuperar una clase WMI

El primer tipo de objeto que se puede recuperar es una clase WMI. Al recuperar una clase WMI, realmente se recupera una definición de clase, que es una lista de las propiedades, calificadores y métodos que describen completamente la clase. Sin embargo, una definición de clase es básicamente la propia clase.

PowerShell usa una consulta estándar para recuperar definiciones de clase mediante la **clase meta \_ class.**

**Para recuperar una definición de clase en PowerShell**

-   Use [Get-WmiObject con una](https://technet.microsoft.com/library/dd315379.aspx) consulta a la meta class , con la cláusula WHERE que contiene el nombre de la clase con la que se va a recuperar. **\_**

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WmiObject es](https://technet.microsoft.com/library/dd315379.aspx) el cmdlet estándar que PowerShell usa para recuperar información de clase e instancia de WMI. La **clase \_ meta class** define la consulta como una consulta de esquema. Sin la **clase \_ meta** class, esta consulta devolvería todas las instancias de Win32 \_ LogicalDisk. Para obtener más información sobre cómo consultar WMI, vea [Instrucción SELECT para consultas de esquema.](select-statement-for-schema-queries.md)

El proceso actual para recuperar una definición de WMI en C# es usar **la clase CIMInstance.**

**Para recuperar una definición de clase en C# (Microsoft.Management.Infrastructure)**

1.  Con el espacio **de nombres Microsoft.Management.Infrastructure,** cree una **clase CIMInstance** con el espacio de nombres y el nombre de clase especificados.

    La clase creada contendrá toda la información de clase, pero no datos de instancia.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Como alternativa, al igual que con PowerShell, también podría realizar una consulta mediante la **etiqueta de meta \_** class como parte de la consulta.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Al igual que con PowerShell, C# usa una **consulta de meta \_ class** para recuperar definiciones de clase. Como alternativa, puede crear un objeto **ManagementClass** para acceder directamente a la definición de clase.

> [!Note]  
> **System.Management era el** espacio de nombres .NET original que se usaba para acceder a WMI; Sin embargo, las API de este espacio de nombres suelen ser más lentas y no escalan tan bien con respecto a sus homólogos **de Microsoft.Management.Infrastructure** más modernos.

 

**Para recuperar una definición de clase en C# (System.Management)**

1.  Puede usar [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) con una consulta a la meta class , con la cláusula WHERE que contiene el nombre de la clase con la que se va a recuperar. **\_**

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher es](/dotnet/api/system.management.managementobjectsearcher) la clase estándar que .NET usa para recuperar información de clase e instancia de WMI. [ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) devuelve [managementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contiene la clase de definición de esquema. La **clase \_ meta class** define la consulta como una consulta de esquema. Sin la **clase meta \_** class, esta consulta devolvería todas las instancias de [**\_ LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Para obtener más información sobre cómo consultar WMI, vea [Instrucción SELECT para consultas de esquema.](select-statement-for-schema-queries.md)

2.  Como alternativa, cree un nuevo [objeto ManagementClass,](/dotnet/api/system.management.managementclass) con el nombre como ruta de acceso, para recuperar la clase.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Puede recuperar una definición de clase en VBScript de forma similar a la recuperación de una instancia específica.

**Para recuperar una definición de clase en VBScript**

1.  Llame [**a SWbemServices.Get,**](swbemservices-get.md) pero no identifique una instancia específica en la ruta de acceso del objeto para la clase .
2.  En el ejemplo de código siguiente se recupera la definición de clase para la clase que describe las unidades lógicas en el equipo.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows El host de script (WSH) también admite lo siguiente.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    En Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) o [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) en el script del lado servidor. Para obtener más información, [vea Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).

3.  También se puede especificar una clase o instancia, en cuyo caso el objeto devuelto es un objeto WMI, por ejemplo, una instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), en lugar de un objeto de servicios. Tenga en cuenta que no se pueden usar las funciones [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) de VBScript para crear una instancia del objeto [**genérico SWbemObject**](swbemobject.md).
4.  En las páginas HTML que se ejecutan en Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) y [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) pueden producir un error porque los objetos de scripting WMI, como los controles ActiveX, no están marcados como seguros para el scripting. La única excepción es [**el objeto SWbemDateTime.**](swbemdatetime.md) La única manera de que estas llamadas se puedan realizar correctamente es cuando se reduce la configuración de seguridad de IE, lo que no se recomienda.

Al recuperar una clase en C++, llame a la [**versión IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) [**de GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Para recuperar una definición de clase en C++**

1.  Llame a [**los métodos IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para recuperar la definición de una clase.
2.  Una clase puede tener varias definiciones de clase, lo que suele ocurrir cuando hay más de un proveedor de clases cargado en un espacio de nombres. Cuando una clase tiene varias definiciones de clase, WMI devuelve la primera definición detectada y el código **de estado WBEM \_ S DUPLICATE \_ \_ OBJECTS.**

Dado [**que GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) devuelve una definición de clase, se usa normalmente como primer paso para crear una instancia. Para obtener más información sobre cómo usar **GetObject**, vea [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).

 

 
