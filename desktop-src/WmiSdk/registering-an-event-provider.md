---
description: Para crear un proveedor de eventos WMI, debe registrar la instancia de Win32Provider que representa al proveedor mediante una instancia \_ \_ \_ \_ de EventProviderRegistration.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registro de un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973743"
---
# <a name="registering-an-event-provider"></a>Registro de un proveedor de eventos

Para crear un proveedor [*de eventos*](gloss-e.md) WMI, debe registrar la instancia [**\_ \_ de Win32Provider**](--win32provider.md) que representa al proveedor mediante una instancia de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md). Como objeto COM, el proveedor debe registrarse con el sistema operativo y WMI. En el procedimiento siguiente se da por supuesto que ya ha implementado el proceso de registro como se describe [en Registro de un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de eventos.

**Para registrar un proveedor de eventos**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de [**\_ \_ la clase EventProviderRegistration**](--eventproviderregistration.md) que describa el conjunto de características del proveedor.

    La [**\_ \_ clase EventProviderRegistration**](--eventproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration.**](--objectproviderregistration.md) Las propiedades locales de **\_ \_ la clase EventProviderRegistration** son la ruta de acceso del objeto al proveedor y una lista de consultas que describen los eventos que admite el proveedor. Para obtener más información, vea [Consulta de WMI.](querying-wmi.md)

3.  Cargue la implementación de las [**\_ \_ clases Win32Provider**](--win32provider.md) [**\_ \_ y EventProviderRegistration**](--eventproviderregistration.md) en el repositorio WMI.

    WMI usa la definición de clase para registrar y acceder al proveedor de eventos. Para obtener más información, [vea Registrar un proveedor.](registering-a-provider.md)

En el ejemplo de código siguiente se describe una implementación de una [**\_ \_ clase Win32Provider**](--win32provider.md) y una [**\_ \_ clase EventProviderRegistration.**](--eventproviderregistration.md)

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

La primera consulta indica que el proveedor genera todas las notificaciones de eventos para la clase de eventos extrínsica FaxEvent. Dado que usa el operador ISA, la segunda consulta implica que el proveedor genera notificaciones para todos los eventos de creación de instancias para la clase [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) y todas sus subclases.

Cuando un proveedor se registra para proporcionar un evento intrínseco, el evento debe aplicarse a todas las instancias de una clase. En otras palabras, no se puede escribir una consulta para proporcionar eventos de creación de instancias solo para algunas de las unidades de disco que pertenecen a la [**clase \_ LogicalDisk win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

 

 
