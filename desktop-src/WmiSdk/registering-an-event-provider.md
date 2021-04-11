---
description: Para crear un proveedor de eventos WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ EventProviderRegistration.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrar un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156764"
---
# <a name="registering-an-event-provider"></a>Registrar un proveedor de eventos

Para crear un [*proveedor de eventos*](gloss-e.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md). Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI. En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de eventos.

**Para registrar un proveedor de eventos**

1.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de la clase [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) que describa el conjunto de características del proveedor.

    La clase [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . Las propiedades locales de la clase **\_ \_ EventProviderRegistration** son la ruta de acceso del objeto al proveedor y una lista de consultas que describen los eventos que admite el proveedor. Para obtener más información, consulte [consultar WMI](querying-wmi.md).

3.  Cargue la implementación de las clases [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) en el repositorio WMI.

    WMI utiliza la definición de clase para registrar y tener acceso al proveedor de eventos. Para obtener más información, vea [registrar un proveedor](registering-a-provider.md).

En el ejemplo de código siguiente se describe una implementación de una clase [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .

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

La primera consulta indica que el proveedor genera todas las notificaciones de eventos para la clase de evento extrínseco FaxEvent. Dado que utiliza el operador ISA, la segunda consulta implica que el proveedor genera notificaciones para todos los eventos de creación de instancia para la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) y todas sus subclases.

Cuando un proveedor se registra para proporcionar un evento intrínseco, el evento se debe aplicar a todas las instancias de una clase. En otras palabras, no se puede escribir una consulta para proporcionar eventos de creación de instancias solo para algunas de las unidades de disco que pertenecen a la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

 

 
