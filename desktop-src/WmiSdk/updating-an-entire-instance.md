---
description: El medio más común de actualizar una instancia de clase WMI es actualizar toda la instancia a la vez.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Actualizar una instancia completa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cac29805eeff1f8c659c0bee6832eb65e9e6b5bdee8cd15bd0a052247a70e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995546"
---
# <a name="updating-an-entire-instance"></a>Actualizar una instancia completa

El medio más común de actualizar una instancia de clase WMI es actualizar toda la instancia a la vez. Al actualizar una instancia completa, WMI no tiene que analizar la instancia en propiedades individuales y enviarlas a la aplicación. En su lugar, WMI simplemente puede enviarle toda la instancia. Cuando termine, WMI podrá copiar toda la instancia modificada en la instancia original.

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia mediante PowerShell.

**Para modificar o actualizar una instancia mediante PowerShell**

1.  Recupere una copia local del objeto con una llamada a Get-WmiObject.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.

    Aunque no es necesario, es posible que quiera conocer el valor de la propiedad antes de cambiarla.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Realice cambios en las propiedades del objeto local.

    Al hacerlo, solo cambia la copia local. Para guardar los cambios en WMI, debe volver a colocar toda la copia en el repositorio WMI.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Vuelva a colocar el objeto en el repositorio WMI mediante una llamada al método Put.

    ```PowerShell
    $mySettings.Put()
    ```

    

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia mediante C#.

**Para modificar o actualizar una instancia mediante C# (Microsoft.Management.Infrastructure)**

1.  Recupere una copia local del objeto con una llamada a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), como se describe en [Recuperación de una instancia de WMI.](retrieving-an-instance.md)

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.

    Aunque no es necesario, es posible que quiera conocer el valor de la propiedad antes de cambiarla.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Realice cambios en las propiedades del objeto local.

    Al hacerlo, solo cambia la copia local. Para guardar los cambios en WMI, debe volver a colocar toda la copia en el repositorio WMI.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Vuelva a colocar el objeto en el repositorio WMI mediante una llamada a [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia mediante PowerShell.

> [!Note]  
> **System.Management era el** espacio de nombres original de .NET que se usaba para tener acceso a WMI; Sin embargo, las API de este espacio de nombres suelen ser más lentas y no escalan tan bien en relación con sus homólogos **microsoft.management.infrastructure** más modernos.

 

**Para modificar o actualizar una instancia mediante C# (Microsoft.Management)**

1.  Recupere una copia local del objeto con una llamada a [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.

    Aunque no es necesario, es posible que quiera conocer el valor de la propiedad antes de cambiarla.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Realice cambios en las propiedades del objeto local.

    Al hacerlo, solo cambia la copia local. Para guardar los cambios en WMI, debe volver a colocar toda la copia en el repositorio WMI.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Vuelva a colocar el objeto en el repositorio WMI mediante una llamada al [método ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) o .

    ```CSharp
    myDisk.Put();
    ```

    

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia mediante VBScript.

**Para modificar o actualizar una instancia mediante VBScript**

1.  Recupere una copia local del objeto con una llamada a **GetObject**.
2.  Si es necesario, vea las propiedades del objeto con una llamada al [**método Properties. \_**](swbemobject-properties-.md)

    Aunque no es necesario, es posible que quiera conocer el valor de la propiedad antes de cambiarla.

3.  Realice cualquier cambio en las propiedades del objeto con una llamada al [**método SWbemProperty.Value.**](swbemproperty-value.md)

    El **método Value** solo cambia la copia local. Para guardar los cambios en WMI, debe volver a colocar toda la copia en el repositorio WMI.

4.  Vuelva a colocar el objeto en el repositorio WMI con una llamada a los métodos [**\_ SWbemObject.Put**](swbemobject-put-.md) o [**SWbemObject.PutAsync. \_**](swbemobject-putasync-.md)

Como los nombres implican, [**coloque \_ las**](swbemobject-put-.md) actualizaciones de forma sincrónica mientras [**PutAsync \_**](swbemobject-putasync-.md) se actualiza de forma asincrónica. Cualquiera de los métodos copia la instancia original con la instancia modificada. Sin embargo, para aprovechar el procesamiento asincrónico, debe crear un [**objeto SWbemSink.**](swbemsink.md) Para obtener más información, vea [Llamar a un método](calling-a-method.md).

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia mediante C++.

**Para modificar o actualizar una instancia mediante C++**

1.  Recupere una copia local de la instancia con una llamada a [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).
2.  Si es necesario, vea las propiedades del objeto con una llamada a [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).

    Aunque no es necesario, es posible que quiera conocer el valor de la propiedad antes de cambiarla.

3.  Realice los cambios necesarios en la copia con una llamada a [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    El **método Put** solo cambia la copia local. Para guardar los cambios en WMI, debe volver a colocar toda la copia en el repositorio WMI.

4.  Vuelva a colocar la copia en el repositorio WMI con una llamada a los [**métodos IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

    Como los nombres implican, **PutInstance se** actualiza sincrónicamente mientras [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) se actualiza de forma asincrónica. Cualquiera de los métodos copia la instancia original con la instancia modificada. Sin embargo, para aprovechar el procesamiento asincrónico, debe implementar la [**interfaz IWbemObjectSink.**](iwbemobjectsink.md)

    Debe tener en cuenta que una operación de actualización en una instancia que pertenece a una jerarquía de clases podría no realizarse correctamente debido a un error relacionado con otra clase de la jerarquía. WMI llama al [**método PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) de cada uno de los proveedores responsables de las clases de las que deriva la clase propietaria de la instancia original. Si se produce un error en cualquiera de estos proveedores, se produce un error en la solicitud de actualización original. Para más información, consulte la sección Comentarios de [**PutInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Para obtener más información, vea [Llamar a un método de proveedor](calling-a-provider-method.md).

> [!Note]  
> Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que requiere el cliente, se recomienda usar la comunicación semisincronosa en lugar de la comunicación asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

 

 
