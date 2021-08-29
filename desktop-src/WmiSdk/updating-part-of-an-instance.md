---
description: En ocasiones, es posible que desee actualizar solo una parte de una instancia.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Actualizar parte de una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35be3e6b67380f8d41a8d789064d816d2c913ad22178897f9a0994a722a266c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049933"
---
# <a name="updating-part-of-an-instance"></a>Actualizar parte de una instancia

En ocasiones, es posible que desee actualizar solo una parte de una instancia. Por ejemplo, algunas instancias tienen un gran número de propiedades. Si tuviera que actualizar un gran número de estas instancias, puede reducir el rendimiento del sistema. Por lo tanto, puede optar por actualizar solo una parte de la instancia de y, por tanto, reducir la cantidad de información que debe enviar y recuperar hacia y desde WMI. Sin embargo, WMI no admite directamente operaciones de instancia parcial, ni la mayoría de los proveedores. Por lo tanto, si escribe una aplicación que usa operaciones de instancia parcial, prepárese para que las llamadas no se puedan realizar con el código de error **WBEM \_ E PROVIDER \_ NOT \_ \_ CAPABLE** o **WBEM E NOT \_ \_ \_ SUPPORTED** en C++. En lenguajes de scripting, los códigos de error **son wbemErrProviderNotCapable** o **wbemErrNotSupported.**

En el scripting, esta operación solo es necesaria para ayudar al rendimiento al actualizar una o dos propiedades que se pueden escribir en un número muy grande de objetos en una empresa. De lo contrario, las llamadas de VBScript normales a [**\_ SWbemObject.Put**](swbemobject-put-.md) o [**SWbemObject.PutAsync \_**](swbemobject-putasync-.md), aunque parezca que escriben todo el objeto, en realidad solo actualizan las propiedades que el proveedor ha habilitado para escritura.

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante PowerShell.

**Para solicitar una actualización de instancia parcial mediante PowerShell**

1.  Recupere la ruta de acceso del objeto que desea actualizar.

    Puede describir la ruta de acceso manualmente, o bien consultar el objeto y, a continuación, recuperar la **\_ \_ propiedad Path.**

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  Configure una tabla hash con los nombres de las propiedades que se actualizarán y use esta tabla hash en una llamada a [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante C#.

> [!Note]  
> **System.Management era el** espacio de nombres .NET original que se usaba para acceder a WMI; Sin embargo, las API de este espacio de nombres suelen ser más lentas y no escalan tan bien con respecto a sus homólogos **de Microsoft.Management.Infrastructure** más modernos.

 

**Para solicitar una actualización de instancia parcial mediante C #**

1.  Cree un nuevo [objeto ManagementObject](/dotnet/api/system.management.managementobject) que represente la instancia específica que se actualizará.

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  Establezca el valor de propiedad con una llamada a [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante VBScript.

**Para solicitar una actualización de instancia parcial mediante VBScript**

1.  Cree un [**objeto de contexto SWbemNamedValueSet.**](swbemnamedvalueset.md)

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  Agregue los valores de extensión Put "PUT EXTENSIONS" y "PUT EXT CLIENT REQUEST" al objeto de contexto mediante el método \_ \_ \_ \_ \_ \_ \_ \_ [**SWbemNamedValueSet.Add.**](swbemnamedvalueset-add.md)

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  Configure una matriz que enumera los nombres de las propiedades que se actualizarán y agregue esta matriz al objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) con el valor de extensión Put " \_ \_ PUT EXT \_ \_ PROPERTIES".

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  Establezca el *parámetro iFlags* de la [**llamada \_ SWbemObject.Put**](swbemobject-put-.md) a **wbemChangeFlagUpdateOnly**. Sin esta marca, se producirá un error en la llamada con un contexto no válido.

5.  Pase la marca y el objeto de contexto al proveedor en el parámetro *objwbemNamedValueSet* de [**SWbemObject.Put \_**](swbemobject-put-.md) o [**SWbemObject.PutAsync \_**](swbemobject-putasync-.md).

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante C++.

**Para solicitar una actualización de instancia parcial mediante C++**

1.  Cree un [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Un objeto de contexto es un objeto que WMI usa para pasar más información a un proveedor WMI. En este caso, usa el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para indicar al proveedor que acepte actualizaciones de instancias parciales.

2.  Agregue los valores con nombre "PUT EXTENSIONS" y "PUT EXT CLIENT REQUEST" al objeto IWbemContext con una llamada \_ \_ \_ \_ \_ a \_ \_ \_ [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue). [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)

    En la tabla siguiente se muestra el significado de \_ \_ "PUT \_ EXTENSIONS" y \_ \_ "PUT \_ EXT \_ CLIENT \_ REQUEST".

    

    | Valor con nombre                     | Descripción                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | "PUT \_ \_ \_ EXTENSIONS"           | **VT \_ BOOL establecido** en **VARIANT \_ TRUE**. Valor que indica que se han especificado uno o varios de los demás valores de contexto. Esto permite una comprobación rápida del objeto de contexto dentro del proveedor para determinar si se están utilizando actualizaciones de instancias parciales. |
    | "PUT \_ \_ EXT CLIENT \_ \_ \_ REQUEST" | **VT \_ BOOL establecido** en **VARIANT \_ TRUE**. Establecido por el cliente durante la solicitud inicial. Este valor se usa para evitar errores de reenentración.                                                                                                                   |

    

     

3.  Agregue PUT EXT STRICT NULLS, PUT EXT PROPERTIES o PUT EXT ATOMIC en cualquier combinación según sea necesario al objeto IWbemContext con otra llamada a \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue). [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)

    En la tabla siguiente se muestra el significado de los valores con nombre.

    

    | Valor con nombre                   | Descripción                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | "PUT \_ \_ EXT STRICT \_ \_ \_ NULLS" | **VT \_ BOOL establecido** en **VARIANT \_ TRUE**. Indica que el cliente ha establecido intencionadamente las propiedades en **VT \_ NULL** y espera que la operación de escritura se haga correctamente. Si el proveedor no puede establecer los valores **en NULL,** se debe notifica un error. |
    | "PUT \_ \_ \_ EXT \_ PROPERTIES"    | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadenas que contienen una lista de nombres de propiedad que se actualizarán. Se puede usar solo o en combinación con \_ \_ "PUT \_ EXT \_ PROPERTIES". Los valores están en la instancia de que se va a escribir.                           |
    | "PUT \_ \_ \_ EXT \_ ATOMIC"        | **VT \_ BOOL establecido** en **VARIANT \_ TRUE**. Indica que todas las actualizaciones deben realizarse correctamente simultáneamente (semántica atómica) o que el proveedor debe revertir. No puede haber ningún éxito parcial. Se puede usar solo o en combinación con otras marcas.     |

    

     

4.  Establezca el *parámetro iFlags* en **WBEM \_ FLAG UPDATE \_ \_ ONLY**. Sin esta marca, se producirá un error en la llamada con un contexto no válido.
5.  Pase el objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) a las llamadas [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) en el *parámetro pCtx.*

    Pasar el [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) indica al proveedor que permita actualizaciones de instancias parciales. En una actualización de instancia completa, establecería *pCtx en* **NULL.**

    El proveedor puede escribir las propiedades necesarias si el objeto de contexto presente en la llamada no contiene \_ \_ "PUT \_ EXTENSIONS". Si \_ "PUT EXTENSIONS" está presente en el objeto de contexto, WMI requiere que el proveedor obedezca exactamente la semántica de la operación o, de lo contrario, se producirá un error \_ \_ en la llamada. Para obtener más información, vea [Control de mensajes de acceso denegado en un proveedor](impersonating-a-client.md).

 

 
