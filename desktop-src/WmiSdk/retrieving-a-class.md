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
# <a name="retrieving-a-wmi-class"></a>Recuperación de una clase WMI

El primer tipo de objeto que se puede recuperar es una clase WMI. Al recuperar una clase WMI, en realidad se recupera una definición de clase, que es una lista de las propiedades, calificadores y métodos que describen la clase por completo. Sin embargo, una definición de clase es básicamente la propia clase.

PowerShell usa una consulta estándar para recuperar definiciones de clase, mediante la clase **meta \_ Class** .

**Para recuperar una definición de clase en PowerShell**

-   Use [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) con una consulta para la **\_ clase meta**, con la cláusula WHERE que contiene el nombre de la clase con la que se va a recuperar.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) es el cmdlet estándar que PowerShell usa para recuperar información de clase e instancia de WMI. La clase **meta \_ Class** define la consulta como una consulta de esquema. Sin la clase **meta \_ Class** , esta consulta devolvería todas las instancias de Win32 \_ LogicalDisk. Para obtener más información sobre cómo consultar WMI, vea [instrucción SELECT para consultas de esquema](select-statement-for-schema-queries.md).

El proceso actual para recuperar una definición de WMI en C# es usar la clase **CIMInstance** .

**Para recuperar una definición de clase en C# (Microsoft. Management. Infrastructure)**

1.  Con el espacio de nombres **Microsoft. Management. Infrastructure** , cree una clase **CIMInstance** con el espacio de nombres y el nombre de clase especificados.

    La clase creada contendrá toda la información de la clase, pero no los datos de la instancia.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Como alternativa, como con PowerShell, también puede realizar una consulta mediante la etiqueta **meta \_ Class** como parte de la consulta.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Al igual que con PowerShell, C# usa una consulta de **\_ metaclase** para recuperar definiciones de clase. Como alternativa, puede crear un objeto **ManagementClass** para tener acceso directamente a la definición de clase.

> [!Note]  
> **System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.

 

**Para recuperar una definición de clase en C# (System. Management)**

1.  Puede usar [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) con una consulta a **meta \_ Class**, con la cláusula WHERE que contiene el nombre de la clase con la que se va a recuperar.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) es la clase estándar que usa .net para recuperar información de clase e instancia de WMI. [ManagementObjectSerarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) devuelve un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contiene la clase de definición de esquema. La clase **meta \_ Class** define la consulta como una consulta de esquema. Sin la clase **meta \_ Class** , esta consulta devolvería todas las instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Para obtener más información sobre cómo consultar WMI, vea [instrucción SELECT para consultas de esquema](select-statement-for-schema-queries.md).

2.  Como alternativa, cree un nuevo objeto [ManagementClass](/dotnet/api/system.management.managementclass) , con el nombre de la ruta de acceso, para recuperar la clase.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Puede recuperar una definición de clase en VBScript de una manera similar a la recuperación de una instancia específica.

**Para recuperar una definición de clase en VBScript**

1.  Llame a [**SWbemServices. Get**](swbemservices-get.md) pero no identifique una instancia específica en la ruta de acceso del objeto para la clase.
2.  En el ejemplo de código siguiente se recupera la definición de clase para la clase que describe las unidades lógicas del equipo.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows Script Host (WSH) también admite lo siguiente.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    En Active Server páginas (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) o [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) en el script del lado servidor. Para obtener más información, consulte [crear páginas Active Server para WMI](creating-active-server-pages-for-wmi.md).

3.  También se puede especificar una clase o una instancia, en cuyo caso el objeto devuelto es un objeto WMI, por ejemplo, una instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), en lugar de un objeto Services. Tenga en cuenta que no puede utilizar las funciones [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) de VBScript para crear una instancia del objeto genérico [**SWbemObject**](swbemobject.md).
4.  En las páginas HTML que se ejecutan en Microsoft Internet Explorer (IE), se puede producir un error en [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) y [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) , ya que los objetos de scripting de WMI, como los controles ActiveX, no se marcan como seguros para el scripting. La única excepción es el objeto [**SWbemDateTime**](swbemdatetime.md) . La única manera en que estas llamadas se pueden realizar es cuando se reduce la configuración de seguridad de Internet Explorer, lo que no se recomienda.

Al recuperar una clase en C++, llame a la versión [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Para recuperar una definición de clase en C++**

1.  Llame a los métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para recuperar la definición de una clase.
2.  Una clase puede tener varias definiciones de clase, lo que suele ocurrir cuando se tiene más de un proveedor de clases cargado en un espacio de nombres. Cuando una clase tiene varias definiciones de clase, WMI devuelve la primera definición detectada y el código de estado de **\_ objetos WBEM S \_ duplicados \_** .

Dado que [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) devuelve una definición de clase, se utiliza normalmente como primer paso para crear una instancia. Para obtener más información sobre cómo usar **GetObject**, vea [crear y declarar una instancia de mediante C++](creating-and-declaring-an-instance-using-c-.md).

 

 
