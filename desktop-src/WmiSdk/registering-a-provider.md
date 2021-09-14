---
description: Antes de implementar el proveedor, primero debe registrar el proveedor con WMI. El registro del proveedor define el tipo del proveedor y las clases que admite el proveedor. WMI solo puede acceder a proveedores registrados.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registro de un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973752"
---
# <a name="registering-a-provider"></a>Registro de un proveedor

Antes de implementar el proveedor, primero debe registrar el proveedor con WMI. El registro del proveedor define el tipo del proveedor y las clases que admite el proveedor. WMI solo puede acceder a proveedores registrados.

> [!Note]  
> Para obtener más información sobre cómo registrar un proveedor de MI, [vea Cómo: Registrar un proveedor de MI.](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider)

 

Puede escribir el código del proveedor antes de registrar el proveedor. Sin embargo, es muy difícil depurar un proveedor que no está registrado con WMI. Determinar las interfaces del proveedor también ayuda a describir el propósito y la estructura de un proveedor. Por lo tanto, el registro del proveedor le ayuda a diseñar el proveedor.

Solo los administradores pueden registrar o eliminar un proveedor.

Un proveedor debe estar registrado para todos los distintos tipos de funciones de proveedor que realiza. Casi todos los proveedores proporcionan instancias de clases que definen, pero también pueden proporcionar datos de propiedad, métodos, eventos o clases. El proveedor también se puede registrar como proveedor de consumidores de eventos o como proveedor de contadores de rendimiento. Se recomienda combinar toda la funcionalidad del proveedor en un proveedor en lugar de tener muchos proveedores independientes para cada tipo. Un ejemplo es el proveedor [del Registro](/previous-versions/windows/desktop/regprov/system-registry-provider)del sistema , que proporciona métodos e instancias, y el proveedor [de](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)cuota de disco , que proporciona instancias, métodos y eventos.

Un proveedor debe estar registrado para todos los distintos tipos de funciones de proveedor que realiza. Casi todos los proveedores proporcionan instancias de clases que definen, pero también pueden proporcionar datos de propiedad, métodos, eventos o clases. El proveedor también se puede registrar como proveedor de consumidores de eventos o como proveedor de contadores de rendimiento.

Se usa la misma [**\_ \_ instancia de Win32Provider**](--win32provider.md) para cada tipo de registro:

-   [Registro de un proveedor de instancias](registering-an-instance-provider.md)
-   [Registro de un proveedor de clases](registering-a-class-provider.md)
-   [Registrar un proveedor de métodos](registering-a-method-provider.md)
-   [Registro de un proveedor de eventos](registering-an-event-provider.md)
-   [Registro de un proveedor de consumidores de eventos](registering-an-event-consumer-provider.md)
-   [Convertir un proveedor de instancias en un High-Performance de recursos](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Ejemplo: Crear y registrar una instancia de un proveedor

En el ejemplo siguiente se muestra un archivo MOF que crea y registra una instancia del proveedor del Registro del sistema en el espacio de nombres [](/previous-versions/windows/desktop/regprov/system-registry-provider) \\ cimv2 raíz. Asigna el alias $Reg al proveedor para evitar el nombre de ruta de acceso largo necesario en los registros de instancia y método. Para obtener más información, vea [Crear un alias](creating-an-alias.md).

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

## <a name="example-registering-a-provider"></a>Ejemplo: Registro de un proveedor

En el procedimiento siguiente se describe cómo registrar un proveedor.

**Para registrar un proveedor**

1.  Registre el proveedor como un servidor COM.

    Si es necesario, es posible que tenga que crear entradas del Registro. Este proceso se aplica a todos los servidores COM y no está relacionado con WMI. Para más información, consulte la sección COM de la documentación de Microsoft Windows Software Development Kit (SDK).

2.  Cree un archivo MOF que contenga instancias de [**\_ \_ Win32Provider**](--win32provider.md) y una instancia de una clase derivada directa o indirectamente de [**\_ \_ ProviderRegistration,**](--providerregistration.md)como [**\_ \_ InstanceProviderRegistration.**](--instanceproviderregistration.md) Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de instancias de clases derivadas de **\_ \_ Win32Provider** o [**\_ \_ ProviderRegistration**](--providerregistration.md).
3.  Establezca [**HostingModel en**](--win32provider.md) la instancia de **\_ \_ Win32Provider** según los valores de [Modelos de hospedaje.](provider-hosting-and-security.md)

    > [!Note]  
    > A menos que el proveedor requiera los privilegios elevados de la cuenta LocalSystem, la propiedad [**\_ \_ Win32Provider.HostingModel**](--win32provider.md) debe establecerse en "NetworkServiceHost". Para obtener más información, vea [Provider Hosting and Security](provider-hosting-and-security.md).

     

    En el siguiente ejemplo de MOF del ejemplo completo se muestra el código que crea una instancia de [**\_ \_ Win32Provider**](--win32provider.md).

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Instancia de una clase derivada directa o indirectamente de [**\_ \_ ProviderRegistration**](--providerregistration.md)para describir la implementación lógica del proveedor. Un proveedor se puede registrar para varios tipos diferentes de funcionalidad. En el ejemplo anterior se registra RegProv como proveedor de instancias y métodos. Pero si RegProv admite la funcionalidad, también se podría registrar como una propiedad o un proveedor de eventos. En la tabla siguiente se enumeran las clases que registran la funcionalidad del proveedor.

    

    | Clases de registro de proveedor                                                        | Descripción                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | Registra un proveedor [de instancias](registering-an-instance-provider.md).             |
    | [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | Registra un proveedor [de eventos](registering-an-event-provider.md).                   |
    | [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | Registra un proveedor [de consumidores de eventos](registering-an-event-consumer-provider.md). |
    | [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | Registra un proveedor [de métodos](registering-an-event-consumer-provider.md).          |
    | [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | Registra un proveedor [de propiedades](registering-a-property-provider.md).               |

    

     

5.  Coloque el archivo MOF en un directorio permanente.

    Normalmente, debe colocar el archivo en el directorio de instalación del proveedor.

6.  Compile el archivo MOF mediante [mofcomp](mofcomp.md) o la [**interfaz IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

    Para obtener más información, [vea Compilar archivos MOF](compiling-mof-files.md).

    **Windows 8 y Windows Server 2012:** Al instalar proveedores, [**tanto mofcomp**](mofcomp.md) como la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) tratan los calificadores Key y Static como true si están \[ \] \[ presentes, independientemente de sus \] valores reales. Otros calificadores se tratan como false si están presentes, pero no se establecen explícitamente en true.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Establecer descriptores de seguridad namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 
