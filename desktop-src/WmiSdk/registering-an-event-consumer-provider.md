---
description: Para crear un proveedor de consumidor de eventos WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrar un proveedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812434"
---
# <a name="registering-an-event-consumer-provider"></a>Registrar un proveedor de consumidor de eventos

Para crear un [*proveedor de consumidor de eventos*](gloss-e.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md). Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI. En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de consumidor de eventos.

**Para registrar un proveedor de consumidores de eventos**

1.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de la clase [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) que describa el conjunto de características del proveedor.

    Las propiedades definidas por [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) incluyen la ruta de acceso del objeto al proveedor y los nombres de las clases de consumidor lógicas que admite el proveedor del consumidor de eventos.

    Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y **dinámicos** . El calificador **dinámico** indica que WMI debe utilizar un proveedor para recuperar las instancias de clase. El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.

En el ejemplo de código siguiente se muestra cómo registrar un proveedor de consumidor de eventos.

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



