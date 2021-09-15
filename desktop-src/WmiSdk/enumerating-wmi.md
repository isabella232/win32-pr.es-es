---
description: La enumeración es el acto de desplazarse por un conjunto de objetos y, posiblemente, modificar cada objeto a medida que lo hace.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Enumeración de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575341"
---
# <a name="enumerating-wmi"></a>Enumeración de WMI

La enumeración es el acto de desplazarse por un conjunto de objetos y, posiblemente, modificar cada objeto a medida que lo hace. Por ejemplo, puede enumerar a través de un conjunto de objetos [**\_ de DiskDrive de Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) para buscar un número de serie determinado. Tenga en cuenta que, aunque puede enumerar cualquier objeto, WMI solo devuelve objetos a los que tiene acceso de seguridad.

Las enumeraciones de grandes conjuntos de datos pueden requerir una gran cantidad de recursos y degradar el rendimiento. Para obtener más información, vea [Improving Enumeration Performance](improving-enumeration-performance.md). También puede solicitar datos con una consulta más específica. Para obtener más información, vea [Consulta de WMI.](querying-wmi.md)

En este tema se de abordan las secciones siguientes:

-   [Enumeración de WMI mediante PowerShell](#enumerating-wmi-using-powershell)
-   [Enumerar WMI mediante C# (Microsoft.Management.Infrastructure)](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [Enumerar WMI mediante C# (System.Management)](#enumerating-wmi-using-c-systemmanagement)
-   [Enumeración de WMI mediante VBScript](#enumerating-wmi-using-vbscript)
-   [Enumeración de WMI mediante C++](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a>Enumeración de WMI mediante PowerShell

Si no conoce la ruta de acceso del objeto para una instancia específica o desea recuperar todas las instancias de una clase específica, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), con el nombre de la clase en el *parámetro -class.* Si desea usar una consulta, puede usar el *parámetro -query.*

En el procedimiento siguiente se describe cómo enumerar las instancias de una clase mediante PowerShell.

**Para enumerar las instancias de una clase mediante PowerShell**

1.  Enumerar las instancias con una llamada al cmdlet [Get-WmiObject.](https://technet.microsoft.com/library/dd315379.aspx)

    [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) devuelve una colección de uno o varios objetos WMI, a través de los cuales puede enumerar. Para obtener más información, vea [Accessing a Collection](accessing-a-collection.md).

    Si desea recuperar una instancia de clase WMI en otro espacio de nombres o en otro equipo, especifique el equipo y el espacio de nombres en los parámetros *-computer* y *-namespace,* respectivamente. Para obtener más información, vea [Crear un script WMI.](creating-a-wmi-script.md) Esto solo funciona si tiene los privilegios de acceso adecuados. Para obtener más información, vea [Mantenimiento de la seguridad WMI](maintaining-wmi-security.md) y Ejecución de operaciones con [privilegios.](executing-privileged-operations.md)

2.  Recupere las instancias individuales que quiera usar con los miembros de la colección.

En el ejemplo de código siguiente se recupera una colección de PowerShell y, a continuación, se muestra la propiedad size para todas las instancias de unidades lógicas en el equipo local.


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



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a>Enumerar WMI mediante C# (Microsoft.Management.Infrastructure)

1.  Agregue una referencia al ensamblado **de referencia Microsoft.Management.Infrastructure.** (Este ensamblado se incluye como parte del Kit [de desarrollo de software (SDK)](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)de Windows para Windows 8 ).
2.  Agregue una **instrucción using** para el espacio de **nombres Microsoft.Management.Infrastructure.**

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  Cree una instancia de un [objeto CimSession.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) El fragmento de código siguiente usa el valor "localhost" estándar para el [**método CimSession.Create.**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  Llame al [**método CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) pasando el espacio de nombres CIM deseado y WQL que se usará. El fragmento de código siguiente devolverá dos instancias que representan dos procesos Windows estándar en los que la propiedad de identificador (que representa un identificador de proceso o PID) tiene un valor de 0 o 4.

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  Recorrer en bucle los objetos [**CimInstance devueltos.**](https://www.bing.com/search?q=**CimInstance**)

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

En el ejemplo de código siguiente se enumeran todas las instancias de la clase Process de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) (que representa procesos activos) en el equipo local e imprime el nombre de cada proceso.

> [!Note]  
> En una aplicación real, definiría como parámetros el nombre del equipo ("localhost") y el espacio de nombres CIM ("root \\ cimv2"). Por motivos de simplicidad, se han codificado de forma rígida en este ejemplo.

 


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





## <a name="enumerating-wmi-using-c-systemmanagement"></a>Enumerar WMI mediante C# (System.Management)

Si no conoce la ruta de acceso del objeto para una instancia específica o desea recuperar todas las instancias de una clase específica, use el objeto [ManagementClass](/dotnet/api/system.management.managementclass) para recuperar una [clase ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) que contenga todas las instancias de una clase determinada en el espacio de nombres WMI. Como alternativa, puede consultar WMI a través de [managementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) para obtener el mismo conjunto de objetos.

> [!Note]  
> **System.Management era el** espacio de nombres .NET original que se usaba para acceder a WMI; Sin embargo, las API de este espacio de nombres suelen ser más lentas y no escalan tan bien con respecto a sus homólogos **de Microsoft.Management.Infrastructure** más modernos.

 

En el procedimiento siguiente se describe cómo enumerar las instancias de una clase mediante C#.

**Para enumerar las instancias de una clase mediante C #**

1.  Enumerar las instancias con una llamada a [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).

    El [método GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) devuelve una colección, o conjunto, de objetos a través del cual puede enumerar. Para obtener más información, vea [Accessing a Collection](accessing-a-collection.md). La colección devuelta es realmente un [objeto ManagementObjectCollection,](/dotnet/api/system.management.managementobjectcollection) por lo que se puede llamar a cualquiera de los métodos de ese objeto.

    Si desea recuperar una instancia de clase WMI en otro espacio de nombres o en otro equipo, especifique el equipo y el espacio de nombres en el parámetro *path.* Para obtener más información, vea [Crear un script WMI.](creating-a-wmi-script.md) Esto solo funciona si tiene los privilegios de acceso adecuados. Para obtener más información, vea [Mantenimiento de la seguridad WMI](maintaining-wmi-security.md) y Ejecución de operaciones con [privilegios.](executing-privileged-operations.md)

2.  Recupere las instancias individuales que quiera usar con los miembros de la colección.

En el ejemplo de código siguiente se recupera una colección de C# y, a continuación, se muestra la propiedad size para todas las instancias de unidades lógicas en el equipo local.


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



## <a name="enumerating-wmi-using-vbscript"></a>Enumeración de WMI mediante VBScript

Si no conoce la ruta de acceso del objeto para una instancia específica o desea recuperar todas las instancias de una clase específica, use el método [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) para devolver una enumeración [**SWbemObjectSet**](swbemobjectset.md) de todas las instancias de una clase. También puede consultar WMI a través [**de SWbemServices.ExecQuery**](swbemservices-execquery.md) para obtener el mismo conjunto de objetos.

En el procedimiento siguiente se describe cómo enumerar las instancias de una clase mediante VBScript.

**Para enumerar las instancias de una clase mediante VBScript**

1.  Enumerar las instancias con una llamada al [**método SWbemServices.InstancesOf.**](swbemservices-instancesof.md)

    El [**método InstancesOf**](swbemservices-instancesof.md) devuelve una colección o un conjunto de objetos a través de los cuales se puede enumerar. Para obtener más información, vea [Accessing a Collection](accessing-a-collection.md). La colección devuelta es realmente un [**objeto SWbemObjectSet,**](swbemobjectset.md) por lo que se puede llamar a cualquiera de los métodos de ese objeto.

    Si desea recuperar una instancia de clase WMI en otro espacio de nombres o en otro equipo, especifique el equipo y el espacio de nombres en el moniker. Para obtener más información, vea [Crear un script WMI.](creating-a-wmi-script.md) Esto solo funciona si tiene los privilegios de acceso adecuados. Para obtener más información, vea [Mantenimiento de la seguridad WMI](maintaining-wmi-security.md) y Ejecución de operaciones con [privilegios.](executing-privileged-operations.md)

2.  Recupere las instancias individuales que desee mediante los métodos de colecciones.

En el ejemplo de código siguiente se recupera un objeto [**SWbemServices**](swbemservices.md) y, a continuación, se ejecuta el método [**InstancesOf**](swbemservices-instancesof.md) para mostrar la propiedad size para todas las instancias de unidades lógicas en el equipo local.


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



## <a name="enumerating-wmi-using-c"></a>Enumeración de WMI mediante C++

Además de realizar la enumeración básica, puede establecer varias marcas y propiedades para aumentar el rendimiento de la enumeración. Para obtener más información, vea [Improving Enumeration Performance](improving-enumeration-performance.md).

**Para enumerar un conjunto de objetos en WMI**

1.  Cree una [**interfaz IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) que describa el conjunto de objetos que desea enumerar.

    Un [**objeto IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contiene una lista que describe un conjunto de objetos WMI. Puede usar los métodos **IEnumWbemClassObject** para enumerar reenvíos, omitir objetos, comenzar al principio y copiar el enumerador. En la tabla siguiente se enumeran los métodos que se usan para crear enumeradores para distintos tipos de objetos WMI.

    

    <table>
    <thead>
    <tr class="header">
    <th>Object</th>
    <th>Método</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Clase</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a><br />
[<strong>IWbemServices::CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Instancia</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a><br />
[<strong>IWbemServices::CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)<br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td>Resultado de la consulta</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a><br />
[<strong>IWbemServices::ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Notificación de evento</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a><br />
[<strong>IWbemServices::ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Recorrer la enumeración devuelta mediante varias llamadas a [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

 

 
