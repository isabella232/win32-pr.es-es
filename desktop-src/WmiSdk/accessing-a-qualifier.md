---
description: Un calificador es una etiqueta que proporciona más información sobre un objeto, método o propiedad WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Acceso a un calificador WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465788"
---
# <a name="accessing-a-wmi-qualifier"></a>Acceso a un calificador WMI

Un calificador es una etiqueta que proporciona más información sobre un objeto, método o propiedad WMI. En ocasiones, es posible que tenga que acceder a los datos almacenados en un calificador. Por ejemplo, una tarea común consiste en determinar si un proveedor implementa un método intentando recuperar el calificador **Implementado** para ese método. Para obtener más información, vea [Calificadores WMI y](wmi-qualifiers.md) [Agregar un calificador](adding-a-qualifier.md).

Puede recuperar los calificadores de un objeto WMI en PowerShell recuperando primero el objeto y, a continuación, examinando los calificadores como lo haría con cualquier otra propiedad.

**Para recuperar un calificador mediante PowerShell**

-   Recupere el objeto cuyos calificadores desea ver mediante [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)y, a continuación, acceda a los calificadores a través de **la propiedad Qualifiers:**

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

    

    Para obtener más información, [vea Recuperar una instancia de WMI.](retrieving-an-instance.md)

Puede recuperar los calificadores en una instancia de WMI en C# recuperando primero el objeto y, a continuación, examinando los calificadores como una colección.

**Para recuperar un calificador mediante C# (Microsoft.System.Management)**

1.  Recupere la clase cuyos calificadores desea ver mediante la creación de un objeto CimInstance, utilizando el nombre de clase y el espacio de nombres especificados.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Para obtener más información, [vea Recuperar una instancia de WMI.](retrieving-an-instance.md)

2.  Puede recuperar los calificadores de clase de [CimInstance.CimClass.CimClass.CimClassQualifiers,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85))los calificadores de propiedad de [CimInstance.CimClass.CimClassProperties y](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))los calificadores de método de [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).

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

    

    Para obtener más información, [vea Recuperar una instancia de WMI.](retrieving-an-instance.md)

Puede recuperar los calificadores de un objeto WMI en C# recuperando primero el objeto y examinando los calificadores como una colección.

> [!Note]  
> **System.Management era el** espacio de nombres .NET original que se usaba para acceder a WMI; Sin embargo, las API de este espacio de nombres suelen ser más lentas y no escalan tan bien con respecto a sus homólogos **de Microsoft.Management.Infrastructure** más modernos.

 

**Para recuperar un calificador mediante C# (System.Management)**

1.  Recupere el objeto cuyos calificadores desea ver mediante [ManagementObject](/dotnet/api/system.management.managementobject).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Para obtener más información, [vea Recuperar una instancia de WMI.](retrieving-an-instance.md)

2.  Coloque los calificadores en [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)y enumere a través de los [valores QualifierData.](/dotnet/api/system.management.qualifierdata)

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Para obtener más información, [vea Recuperar una instancia de WMI.](retrieving-an-instance.md)

En el procedimiento siguiente se describe cómo recuperar un calificador mediante VBScript.

**Para recuperar un calificador mediante VBScript**

1.  Recupere el objeto cuyos calificadores desea ver, como se muestra en el ejemplo siguiente:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    La manera más común de recuperar un objeto es mediante el [**método GetObject.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) Para obtener más información, [vea Recuperar una instancia de WMI.](retrieving-an-instance.md)

2.  Acceda a los calificadores del objeto a través de la propiedad [**SWbemObject.Qualifiers, \_**](swbemobject-qualifiers-.md) como se muestra en el ejemplo siguiente:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

En el ejemplo de código siguiente se describe cómo tener acceso a todos los calificadores de un [**objeto Proceso \_ de Win32.**](/windows/desktop/CIMWin32Prov/win32-process)


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

    La manera más común de recuperar un objeto es mediante una llamada a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) Para obtener más información, vea [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).

2.  Recupere el calificador establecido para una propiedad determinada con una llamada a los métodos [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) [**o IWbemClassObject::GetMethodQualifierSet.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)

3.  Acceda a los calificadores del objeto a través de la [**interfaz IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) devuelta.

## <a name="examples"></a>Ejemplos

Para obtener más información sobre cómo recuperar calificadores, vea el ejemplo de código de PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) en la Galería de TechNet.

 

 
