---
description: El proveedor del Registro del sistema se registra como parte del proceso de instalación de WMI en Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Registro del proveedor del Registro del sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973740"
---
# <a name="registering-the-system-registry-provider"></a>Registro del proveedor del Registro del sistema

El proveedor del Registro del sistema se registra como parte del proceso de instalación de WMI en Windows. Si usa otra plataforma y desea usar el proveedor del Registro del sistema, primero debe registrar el proveedor usted mismo siguiendo los pasos que se describen a continuación.

En el procedimiento siguiente se describe cómo registrar el proveedor del Registro del sistema.

**Para registrar el proveedor del Registro del sistema**

1.  Registre el proveedor como un servidor COM.

    Si es necesario, es posible que tenga que crear entradas del Registro. Este proceso se aplica a todos los servidores COM y no está relacionado con WMI. Para más información, consulte la [documentación de COM](https://msdn.microsoft.com/library/aa139695.aspx) en el Kit de desarrollo de software (SDK) de Microsoft Windows.

2.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) para describir la implementación del proveedor del Registro del sistema.

    La [**\_ \_ instancia de Win32Provider**](--win32provider.md) describe el nombre del proveedor y su identificador de clase **(CLSID).**

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

3.  Cree una o varias instancias de clases derivadas de la [**\_ \_ clase ProviderRegistration**](--providerregistration.md) para describir la implementación lógica del proveedor del Registro del sistema.

    En función del propósito para el que se registre el proveedor del Registro del sistema, puede crear una o varias de las clases siguientes.

    [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

    [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

    [**\_\_EventProviderRegistration**](--eventproviderregistration.md)

    [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

    En el ejemplo de código MOF siguiente se describe cómo puede registrar el proveedor del Registro del sistema como una instancia, propiedad, evento o proveedor de métodos.

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

4.  Compile el archivo MOF mediante el compilador MOF o la [**interfaz IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

El archivo RegEvent.mof proporcionado en la sección WMI del SDK de Windows contiene las instancias [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necesarias para registrar el proveedor del Registro del sistema como proveedor de eventos. Para obtener más información sobre cómo registrar un proveedor, vea [Registrar un proveedor](registering-a-provider.md) y Recibir un evento [WMI](receiving-a-wmi-event.md).

 

 



