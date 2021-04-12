---
description: La forma más común de actualizar una instancia de clase WMI es actualizar toda la instancia a la vez.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Actualizar una instancia completa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277921"
---
# <a name="updating-an-entire-instance"></a>Actualizar una instancia completa

La forma más común de actualizar una instancia de clase WMI es actualizar toda la instancia a la vez. Al actualizar una instancia completa, WMI no tiene que analizar la instancia en propiedades individuales y enviarlas a la aplicación. En su lugar, WMI simplemente le puede enviar toda la instancia. Cuando termine, WMI podrá copiar toda la instancia modificada en la instancia original.

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante PowerShell.

**Para modificar o actualizar una instancia mediante PowerShell**

1.  Recupere una copia local del objeto con una llamada a get-WmiObject.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.

    Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Realice los cambios en las propiedades del objeto local.

    Si lo hace, solo cambiará la copia local. Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Vuelva a colocar el objeto en el repositorio WMI mediante una llamada al método put.

    ```PowerShell
    $mySettings.Put()
    ```

    

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante C#.

**Para modificar o actualizar una instancia mediante C# (Microsoft. Management. Infrastructure)**

1.  Recupere una copia local del objeto con una llamada a [CimSession. getInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), tal y como se describe en [recuperar una instancia de WMI](retrieving-an-instance.md).

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

    Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Realice los cambios en las propiedades del objeto local.

    Si lo hace, solo cambiará la copia local. Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Vuelva a colocar el objeto en el repositorio WMI mediante una llamada a [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante PowerShell.

> [!Note]  
> **System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.

 

**Para modificar o actualizar una instancia de mediante C# (Microsoft. Management)**

1.  Recupere una copia local del objeto con una llamada a [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.

    Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Realice los cambios en las propiedades del objeto local.

    Si lo hace, solo cambiará la copia local. Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Vuelva a colocar el objeto en el repositorio WMI mediante una llamada al método [ManagementObject. put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) o.

    ```CSharp
    myDisk.Put();
    ```

    

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante VBScript.

**Para modificar o actualizar una instancia de mediante VBScript**

1.  Recupere una copia local del objeto con una llamada a **GetObject**.
2.  Si es necesario, vea las propiedades del objeto con una llamada al método [**Properties \_**](swbemobject-properties-.md) .

    Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.

3.  Realice cualquier cambio en las propiedades del objeto con una llamada al método [**SWbemProperty. Value**](swbemproperty-value.md) .

    El método **Value** solo cambia la copia local. Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.

4.  Vuelva a colocar el objeto en el repositorio WMI con una llamada a los métodos [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md) .

Como los nombres implican [**, \_ ponga**](swbemobject-put-.md) las actualizaciones sincrónicamente mientras el [**PutAsync \_**](swbemobject-putasync-.md) se actualiza de forma asincrónica. Cualquiera de los métodos copia la instancia original con la instancia modificada. Sin embargo, para aprovechar el procesamiento asincrónico, debe crear un objeto [**SWbemSink**](swbemsink.md) . Para obtener más información, consulte [llamar a un método](calling-a-method.md).

En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante C++.

**Para modificar o actualizar una instancia de mediante C++**

1.  Recupere una copia local de la instancia de con una llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).
2.  Si es necesario, vea las propiedades del objeto con una llamada a [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).

    Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.

3.  Realice los cambios necesarios en la copia con una llamada a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    El método **Put** cambia solo la copia local. Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.

4.  Vuelva a colocar la copia en el repositorio WMI con una llamada a los métodos [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    Como los nombres implican, **PutInstance** se actualiza sincrónicamente mientras [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) actualiza de forma asincrónica. Cualquiera de los métodos copia la instancia original con la instancia modificada. Sin embargo, para aprovechar el procesamiento asincrónico, debe implementar la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .

    Debe tener en cuenta que una operación de actualización en una instancia que pertenece a una jerarquía de clases podría no realizarse correctamente debido a un error relacionado con otra clase de la jerarquía. WMI llama al método [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) de cada uno de los proveedores responsables de las clases de las que se deriva la clase propietaria de la instancia original. Si se produce un error en cualquiera de estos proveedores, se produce un error en la solicitud de actualización original. Para obtener más información, vea la sección Comentarios de [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

Para obtener más información, consulte [llamar a un método de proveedor](calling-a-provider-method.md).

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

 

 
