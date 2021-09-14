---
description: Para crear un proveedor de consumidores de eventos WMI, debe registrar la instancia de Win32Provider que representa al proveedor mediante una instancia de \_ \_ \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registro de un proveedor de consumidores de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973747"
---
# <a name="registering-an-event-consumer-provider"></a>Registro de un proveedor de consumidores de eventos

Para crear un [*proveedor*](gloss-e.md) de consumidores de eventos WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa al proveedor mediante una instancia de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md). Como objeto COM, el proveedor debe registrarse con el sistema operativo y WMI. En el procedimiento siguiente se da por supuesto que ya ha implementado el proceso de registro como se describe [en Registro de un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de consumidores de eventos.

**Para registrar un proveedor de consumidores de eventos**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de [**\_ \_ la clase EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) que describa el conjunto de características del proveedor.

    Las propiedades definidas por [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) incluyen la ruta de acceso del objeto al proveedor y los nombres de las clases de consumidor lógico que admite el proveedor de consumidores de eventos.

    Asegúrese de etiquetar la clase con los calificadores **Dynamic** [**y Provider.**](/windows/desktop/api/Provider/nl-provider-provider) El **calificador** Dinámico indica que WMI debe usar un proveedor para recuperar las instancias de clase. El **calificador** Provider especifica el nombre del proveedor que WMI debe usar.

En el ejemplo de código siguiente se muestra cómo registrar un proveedor de consumidores de eventos.

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

 

 



