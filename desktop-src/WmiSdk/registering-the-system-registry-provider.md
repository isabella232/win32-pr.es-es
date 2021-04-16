---
description: El proveedor del registro del sistema se registra como parte del proceso de instalación de WMI en Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Registrar el proveedor del registro del sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706097"
---
# <a name="registering-the-system-registry-provider"></a>Registrar el proveedor del registro del sistema

El proveedor del registro del sistema se registra como parte del proceso de instalación de WMI en Windows. Si usa otra plataforma y desea utilizar el proveedor del registro del sistema, primero debe registrar el proveedor siguiendo los pasos que se describen a continuación.

En el procedimiento siguiente se describe cómo registrar el proveedor del registro del sistema.

**Para registrar el proveedor del registro del sistema**

1.  Registre el proveedor como un servidor COM.

    Si es necesario, puede que tenga que crear entradas del registro. Este proceso se aplica a todos los servidores COM y no está relacionado con WMI. Para obtener más información, vea la documentación de [com](https://msdn.microsoft.com/library/aa139695.aspx) en el kit de desarrollo de software (SDK) de Microsoft Windows.

2.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) para describir la implementación del proveedor del registro del sistema.

    La instancia de [**\_ \_ Win32Provider**](--win32provider.md) describe el nombre del proveedor y su identificador de clase (**CLSID**).

    En el ejemplo siguiente se describe cómo registrar [**\_ \_ Win32Provider**](--win32provider.md) como una propiedad de instancia, un evento o un proveedor de métodos.

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  Cree una o más instancias de clases derivadas de la clase [**\_ \_ ProviderRegistration**](--providerregistration.md) para describir la implementación lógica del proveedor del registro del sistema.

    Dependiendo del propósito para el que registre el proveedor del registro del sistema, puede crear una o varias de las siguientes clases.

    [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

    [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

    [**\_\_EventProviderRegistration**](--eventproviderregistration.md)

    [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

    En el siguiente ejemplo de código MOF se describe cómo se puede registrar el proveedor del registro del sistema como una instancia, una propiedad, un evento o un proveedor de métodos.

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  Compile el archivo MOF mediante el compilador MOF o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

El archivo RegEvent. mof proporcionado en la sección WMI del Windows SDK contiene las instancias [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necesarias para registrar el proveedor del registro del sistema como un proveedor de eventos. Para obtener más información acerca del registro de un proveedor, vea [registrar un proveedor](registering-a-provider.md) y [recibir un evento WMI](receiving-a-wmi-event.md).

 

 



