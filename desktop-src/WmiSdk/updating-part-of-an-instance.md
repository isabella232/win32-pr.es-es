---
description: En ocasiones, puede que desee actualizar solo parte de una instancia.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Actualizar parte de una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706028"
---
# <a name="updating-part-of-an-instance"></a>Actualizar parte de una instancia

En ocasiones, puede que desee actualizar solo parte de una instancia. Por ejemplo, algunas instancias tienen un gran número de propiedades. Si tuviera que actualizar un gran número de estas instancias, puede reducir el rendimiento del sistema. Por lo tanto, puede optar por actualizar solo parte de la instancia y, por tanto, reducir la cantidad de información que debe enviar y recuperar en WMI. Sin embargo, WMI no admite directamente las operaciones de instancia parcial ni la mayoría de los proveedores. Por lo tanto, si escribe una aplicación que utiliza operaciones de instancia parcial, debe estar preparado para que las llamadas produzcan un error con el **proveedor de WBEM \_ e \_ \_ \_** no compatible o el código de error **WBEM \_ e \_ no \_ admitido** en C++. En los lenguajes de scripting, los códigos de error son **wbemErrProviderNotCapable** o **wbemErrNotSupported**.

En el scripting, esta operación solo es necesaria para ayudar al rendimiento al actualizar una o dos propiedades que se deben escribir en un gran número de objetos en una empresa. De lo contrario, las llamadas normales de VBScript a [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md), mientras que parece que escriben todo el objeto, en realidad solo están actualizando las propiedades en las que el proveedor tiene habilitada la escritura.

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante PowerShell.

**Para solicitar una actualización de instancia parcial mediante PowerShell**

1.  Recupere la ruta de acceso del objeto que desea actualizar.

    Puede describir la ruta de acceso manualmente, o bien consultar el objeto y, a continuación, recuperar la propiedad **\_ \_ path** .

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  Configure una tabla hash que Enumere los nombres de las propiedades que se van a actualizar y use esta tabla hash en una llamada a [set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante C#.

> [!Note]  
> **System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.

 

**Para solicitar una actualización de instancia parcial mediante C #**

1.  Cree un nuevo objeto [ManagementObject](/dotnet/api/system.management.managementobject) que represente la instancia específica que se va a actualizar.

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  Establezca el valor de propiedad con una llamada a [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante VBScript.

**Para solicitar una actualización de instancia parcial mediante VBScript**

1.  Cree un objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  Agregue los valores de la extensión put " \_ \_ Put \_ Extensions" y " \_ \_ Put \_ ext \_ Client \_ Request" al objeto de contexto mediante el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  Configure una matriz que Enumere los nombres de las propiedades que se van a actualizar y agregue esta matriz al objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) con el valor de la extensión put " \_ \_ Put \_ ext \_ Properties".

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  Establezca el parámetro *iFlags* de la llamada a [**SWbemObject \_ . put**](swbemobject-put-.md) en **wbemChangeFlagUpdateOnly**. Sin este marcador, se producirá un error en la llamada con un contexto no válido.

5.  Pase la marca y el objeto de contexto al proveedor en el parámetro *objwbemNamedValueSet* de [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md).

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante C++.

**Para solicitar una actualización de instancia parcial mediante C++**

1.  Cree un objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Un objeto de contexto es un objeto que WMI utiliza para pasar más información a un proveedor WMI. En este caso, se usa el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para indicar al proveedor que acepte actualizaciones parciales de la instancia.

2.  Agregue los \_ \_ valores "Put \_ Extensions" y " \_ \_ Put \_ ext \_ Client \_ Request" con nombre al objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una llamada a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    En la tabla siguiente se muestra el significado de " \_ \_ Put \_ Extensions" y " \_ \_ Put \_ ext \_ Client \_ Request".

    

    | Valor con nombre                     | Descripción                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ Put \_ Extensions"           | **VT \_ BOOL** se establece en **Variant \_ true**. Valor que indica que se han especificado uno o varios de los demás valores de contexto. Esto permite realizar una comprobación rápida del objeto de contexto dentro del proveedor para determinar si se están usando actualizaciones parciales de instancia. |
    | " \_ \_ Put \_ ext \_ Client \_ Request" | **VT \_ BOOL** se establece en **Variant \_ true**. Establecido por el cliente durante la solicitud inicial. Este valor se usa para evitar errores de reentrada.                                                                                                                   |

    

     

3.  Agregue las \_ \_ \_ propiedades Put ext \_ Strict, Put ext o Put ext \_ \_ \_ \_ \_ \_ \_ \_ \_ Atomic en cualquier combinación según sea necesario para el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con otra llamada a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    En la tabla siguiente se muestra el significado de los valores con nombre.

    

    | Valor con nombre                   | Descripción                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ Put \_ ext \_ STRICT \_ Nulls" | **VT \_ BOOL** se establece en **Variant \_ true**. Indica que el cliente ha establecido intencionadamente las propiedades en **VT \_ null** y espera que la operación de escritura se realice correctamente. Si el proveedor no puede establecer los valores en **null**, se debe informar de un error. |
    | " \_ \_ Put \_ ext \_ Properties"    | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadenas que contiene una lista de nombres de propiedad que se van a actualizar. Se puede usar por sí solo o en combinación con " \_ \_ Put \_ ext \_ Properties". Los valores se encuentran en la instancia que se está escribiendo.                           |
    | " \_ \_ Put \_ ext \_ Atomic"        | **VT \_ BOOL** se establece en **Variant \_ true**. Indica que todas las actualizaciones deben realizarse de forma simultánea (semántica atómica) o el proveedor debe revertirse. No puede haber ningún éxito parcial. Se puede usar por sí solo o en combinación con otras marcas.     |

    

     

4.  Establezca el parámetro *iFlags* en **WBEM \_ marcar \_ \_ solo actualizar**. Sin este marcador, se producirá un error en la llamada con un contexto no válido.
5.  Pase el objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) a las llamadas [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) en el parámetro *pCtx* .

    Al pasar el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) se indica al proveedor que permita las actualizaciones parciales de la instancia. En una actualización de instancia completa, establecería *pCtx* en **null**.

    El proveedor puede escribir las propiedades necesarias si el objeto de contexto presente en la llamada no contiene " \_ \_ Put \_ Extensions". Si " \_ \_ Put \_ Extensions" está presente en el objeto de contexto, WMI requiere que el proveedor cumpla la semántica de la operación exactamente o que se produzca un error en la llamada. Para obtener más información, vea [controlar los mensajes de acceso denegado en un proveedor](impersonating-a-client.md).

 

 
