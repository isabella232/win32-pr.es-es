---
description: Un calificador es una etiqueta que proporciona más información sobre un objeto, un método o una propiedad de WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Obtener acceso a un calificador de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707102"
---
# <a name="accessing-a-wmi-qualifier"></a>Obtener acceso a un calificador de WMI

Un calificador es una etiqueta que proporciona más información sobre un objeto, un método o una propiedad de WMI. En ocasiones, puede que necesite tener acceso a los datos almacenados en un calificador. Por ejemplo, una tarea común es determinar si un proveedor implementa un método intentando recuperar el calificador **implementado** para ese método. Para obtener más información, vea [calificadores de WMI](wmi-qualifiers.md) y [Agregar un calificador](adding-a-qualifier.md).

Puede recuperar los calificadores de un objeto WMI en PowerShell; para ello, recupere primero el objeto y, a continuación, examine los calificadores como lo haría con cualquier otra propiedad.

**Para recuperar un calificador mediante PowerShell**

-   Recupere el objeto cuyos calificadores desea ver mediante [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx)y, a continuación, acceda a los calificadores a través de la propiedad **Qualifiers** :

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).

Puede recuperar los calificadores de una instancia de WMI en C#; para ello, recupere primero el objeto y, a continuación, examine los calificadores como una colección.

**Para recuperar un calificador mediante C# (Microsoft.SysTEM. Administración**

1.  Recupere la clase cuyos calificadores desea ver creando un objeto CimInstance con el nombre de clase y el espacio de nombres especificados.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).

2.  Puede recuperar los calificadores de clase de [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), los calificadores de propiedad de [CimInstance. CimClass. CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))y los calificadores de método de [CimInstance. CimClass. CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).

Puede recuperar los calificadores de un objeto WMI en C#; para ello, recupere primero el objeto y, a continuación, examine los calificadores como una colección.

> [!Note]  
> **System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.

 

**Para recuperar un calificador mediante C# (System. Management)**

1.  Recupere el objeto cuyos calificadores desea ver mediante [ManagementObject](/dotnet/api/system.management.managementobject).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).

2.  Coloque los calificadores en un [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)y enumere los valores de [QualifierData](/dotnet/api/system.management.qualifierdata) .

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).

En el procedimiento siguiente se describe cómo recuperar un calificador mediante VBScript.

**Para recuperar un calificador mediante VBScript**

1.  Recupere el objeto cuyos calificadores desea ver, tal como se muestra en el ejemplo siguiente:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    La forma más común de recuperar un objeto es mediante el método [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) . Para obtener más información, consulte [recuperar una instancia de WMI](retrieving-an-instance.md).

2.  Obtenga acceso a los calificadores del objeto a través de la propiedad [**SWbemObject. Qualifiers \_**](swbemobject-qualifiers-.md) , como se muestra en el ejemplo siguiente:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

En el ejemplo de código siguiente se describe cómo obtener acceso a todos los calificadores de un objeto de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) .


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



En el procedimiento siguiente se describe cómo recuperar un calificador mediante C++.

**Para recuperar un calificador mediante C++**

1.  Recupere el objeto cuyos calificadores desea ver.

    La forma más común de recuperar un objeto es mediante una llamada a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Para obtener más información, consulte [recuperar datos de clase o instancia de WMI](retrieving-class-or-instance-data.md).

2.  Recupera el conjunto de calificador para una propiedad determinada con una llamada a los métodos [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) o [**IWbemClassObject:: GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) .

3.  Obtenga acceso a los calificadores del objeto a través de la interfaz [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) devuelta.

## <a name="examples"></a>Ejemplos

Para obtener más información sobre cómo recuperar calificadores, vea el ejemplo de código de PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) en la galería de TechNet.

 

 
