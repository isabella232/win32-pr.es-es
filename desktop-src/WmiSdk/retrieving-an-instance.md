---
description: La recuperación de una instancia de es uno de los procedimientos de recuperación más comunes que es probable que se realice en WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Recuperación de una instancia de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083384"
---
# <a name="retrieving-a-wmi-instance"></a>Recuperación de una instancia de WMI

La recuperación de una instancia de es uno de los procedimientos de recuperación más comunes que es probable que se realice en WMI. Puede recuperar una instancia existente o crear una nueva instancia sin nombre. La ruta de acceso WMI a la instancia existente es un parámetro necesario. Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

> [!Note]  
> Al proporcionar una instancia, es posible que un proveedor no pueda proporcionar un valor para ciertas propiedades. A menos que se indique lo contrario en la descripción de la propiedad, no se puede inferir ningún significado de un valor vacío. No se debe confundir con una cadena que tiene un valor **null** . En este caso, el valor se rellena. Está vacía pero tiene un valor: **null**.

 

Recupere una copia local de la instancia con una llamada al cmdlet [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx) de PowerShell.

**Para recuperar una instancia de una clase WMI mediante PowerShell**

-   Puede recuperar instancias específicas mediante los parámetros *-Class* y *-Filter* .

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Puede recuperar una instancia de WMI mediante C# si crea un objeto de búsqueda mediante [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))y, a continuación, lo rellena con los valores de clave pertinentes y, a continuación, busca ese objeto con una llamada a [CimSession. getInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

**Para recuperar una instancia de una clase WMI mediante C# (Microsoft. Management. Infrastructure)**

1.  Con el espacio de nombres [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , cree un nuevo objeto [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) con el nombre de clase y el espacio de nombres pertinentes.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  Cree un [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) que contenga el nombre y el valor de la propiedad clave de la instancia que desea buscar y agregue esa propiedad al objeto de clase.

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  Recupere el objeto de WMI con una llamada a [CimSession. getInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

Puede recuperar una instancia de clase WMI específica, o una colección de instancias de clase WMI, mediante clases en el espacio de nombres [System. Management](/dotnet/api/system.management) .

> [!Note]  
> **System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.

 

**Para recuperar una instancia de una clase WMI mediante C# (System. Management)**

1.  Recuperar una copia local de una instancia específica creando una nueva [ManagementObject](/dotnet/api/system.management.managementobject), con el nombre y el valor de instancia específico pasados a través del parámetro *ManagementPath* . A continuación, puede recuperar los datos de instancia llamando explícitamente a [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  Como alternativa, puede recuperar todas las instancias de una clase WMI buscándolas con un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)y, a continuación, enumerando el [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)devuelto.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    Puede llamar implícitamente al método **Get** accediendo a la instancia. Para obtener más información, consulte [recuperar parte de una instancia de WMI](retrieving-part-of-an-instance.md).

Recuperar una copia local de la instancia con una llamada al método [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) de VBScript.

**Para recuperar una instancia de una clase WMI mediante VBScript**

-   Llame a [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) con la ruta de acceso del objeto de la instancia, tal y como se muestra en el ejemplo siguiente.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    Para recuperar una instancia concreta, es necesario asignar un nombre como parte de la ruta de acceso del objeto.

En C++, llame a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Para recuperar una instancia de una clase WMI mediante C++**

-   Recupere una copia local de la instancia de con una llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Se debe incluir la ruta de acceso WMI al objeto.

    Como su nombre implica, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) recupera la instancia de forma asincrónica, mientras que [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) recupera la instancia de forma sincrónica. Si desea usar la recuperación asincrónica, debe implementar la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .

## <a name="examples"></a>Ejemplos

Para ver un ejemplo de VBScript que se utiliza como plantilla para recuperar información de clase e instancia, vea el ejemplo de [script de plantilla WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) en la galería de TechNet. En este ejemplo concreto se usa GetObject para recuperar el servicio WMI.

 

 
