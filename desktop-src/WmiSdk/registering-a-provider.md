---
description: Antes de implementar el proveedor, primero debe registrar el proveedor con WMI. Al registrar el proveedor se define el tipo del proveedor y las clases que admite el proveedor. WMI solo puede tener acceso a proveedores registrados.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706654"
---
# <a name="registering-a-provider"></a>Registrar un proveedor

Antes de implementar el proveedor, primero debe registrar el proveedor con WMI. Al registrar el proveedor se define el tipo del proveedor y las clases que admite el proveedor. WMI solo puede tener acceso a proveedores registrados.

> [!Note]  
> Para obtener más información sobre cómo registrar un proveedor de MI, consulte [Cómo: registrar un proveedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).

 

Puede escribir el código del proveedor antes de registrar el proveedor. Sin embargo, es muy difícil depurar un proveedor que no está registrado con WMI. La determinación de las interfaces del proveedor también ayuda a describir el propósito y la estructura de un proveedor. Por lo tanto, el registro del proveedor le ayudará a diseñar el proveedor.

Solo los administradores pueden registrar o eliminar un proveedor.

Un proveedor debe estar registrado para todos los distintos tipos de funciones de proveedor que realiza. Casi todos los proveedores proporcionan instancias de las clases que definen, pero también pueden proporcionar datos de propiedades, métodos, eventos o clases. El proveedor también puede registrarse como proveedor de consumidor de eventos o como proveedor de contadores de rendimiento. Se recomienda combinar toda la funcionalidad del proveedor en un proveedor, en lugar de tener muchos proveedores independientes para cada tipo. Un ejemplo es el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), que proporciona métodos e instancias, y el [proveedor de cuota de disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), que proporciona instancias, métodos y eventos.

Un proveedor debe estar registrado para todos los distintos tipos de funciones de proveedor que realiza. Casi todos los proveedores proporcionan instancias de las clases que definen, pero también pueden proporcionar datos de propiedades, métodos, eventos o clases. El proveedor también puede registrarse como proveedor de consumidor de eventos o como proveedor de contadores de rendimiento.

Se usa la misma instancia de [**\_ \_ Win32Provider**](--win32provider.md) para cada tipo de registro:

-   [Registrar un proveedor de instancias](registering-an-instance-provider.md)
-   [Registrar un proveedor de clases](registering-a-class-provider.md)
-   [Registrar un proveedor de métodos](registering-a-method-provider.md)
-   [Registrar un proveedor de eventos](registering-an-event-provider.md)
-   [Registrar un proveedor de consumidor de eventos](registering-an-event-consumer-provider.md)
-   [Crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Ejemplo: crear y registrar una instancia de un proveedor

En el ejemplo siguiente se muestra un archivo MOF que crea y registra una instancia del [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) en el \\ espacio de nombres root cimv2. Asigna el alias $Reg al proveedor para evitar la ruta de la longitud necesaria en los registros de instancias y métodos. Para obtener más información, vea [crear un alias](creating-an-alias.md).

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a>Ejemplo: registrar un proveedor

En el procedimiento siguiente se describe cómo registrar un proveedor.

**Para registrar un proveedor**

1.  Registre el proveedor como un servidor COM.

    Si es necesario, puede que tenga que crear entradas del registro. Este proceso se aplica a todos los servidores COM y no está relacionado con WMI. Para obtener más información, vea la sección COM en la documentación del kit de desarrollo de software (SDK) de Microsoft Windows.

2.  Cree un archivo MOF que contenga instancias de [**\_ \_ Win32Provider**](--win32provider.md) y una instancia de una clase derivada directa o indirectamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), como [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de instancias de clases derivadas de **\_ \_ Win32Provider** o [**\_ \_ ProviderRegistration**](--providerregistration.md).
3.  Establezca [**HostingModel**](--win32provider.md) en la instancia de **\_ \_ Win32Provider** según los valores de los [modelos de hospedaje](provider-hosting-and-security.md).

    > [!Note]  
    > A menos que el proveedor requiera los privilegios elevados de la cuenta LocalSystem, la propiedad [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) debe establecerse en "NetworkServiceHost". Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

     

    En el siguiente ejemplo de MOF del ejemplo completo se muestra el código que crea una instancia de [**\_ \_ Win32Provider**](--win32provider.md).

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Instancia de una clase derivada directa o indirectamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), para describir la implementación lógica del proveedor. Un proveedor se puede registrar para varios tipos diferentes de funcionalidad. En el ejemplo anterior se registra RegProv como proveedor de instancias y métodos. Pero si RegProv admite la funcionalidad, también podría registrarse como proveedor de propiedades o eventos. En la tabla siguiente se enumeran las clases que registran la funcionalidad del proveedor.

    

    | Clases de registro de proveedor                                                        | Descripción                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | Registra un [proveedor de instancias](registering-an-instance-provider.md).             |
    | [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | Registra un [proveedor de eventos](registering-an-event-provider.md).                   |
    | [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | Registra un [proveedor de consumidor de eventos](registering-an-event-consumer-provider.md). |
    | [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | Registra un [proveedor de métodos](registering-an-event-consumer-provider.md).          |
    | [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | Registra un [proveedor de propiedades](registering-a-property-provider.md).               |

    

     

5.  Coloque el archivo MOF en un directorio permanente.

    Normalmente, debe colocar el archivo en el directorio de instalación del proveedor.

6.  Compile el archivo MOF mediante [MOFCOMP](mofcomp.md) o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

    **Windows 8 y Windows Server 2012:** Al instalar proveedores, tanto [**MOFCOMP**](mofcomp.md) como la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) tratan los \[ \] calificadores de clave y \[ estáticos \] como true si están presentes, independientemente de sus valores reales. Otros calificadores se tratan como false si están presentes pero no se establecen explícitamente en true.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 
