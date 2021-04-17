---
description: Un proveedor de consumidores de eventos es un componente de la arquitectura de consumidor permanente que determina qué consumidor de eventos permanente controla un evento determinado.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Escribir un proveedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706557"
---
# <a name="writing-an-event-consumer-provider"></a>Escribir un proveedor de consumidor de eventos

Un proveedor de consumidores de eventos es un componente de la arquitectura de consumidor permanente que determina qué consumidor de eventos permanente controla un evento determinado. Debe crear un proveedor de consumidor de eventos junto con los consumidores de eventos permanentes para enrutar los eventos correctamente desde WMI.

Un proveedor de consumidor de eventos vincula un proveedor de eventos con una lista de clases de consumidor. Las instancias de estas clases de consumidor reciben los eventos de ese proveedor. WMI identifica el proveedor de consumidores en el que se entregan los eventos, en función de la instancia de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , que asocia la instancia del proveedor de consumidores [**\_ \_ Win32Provider**](--win32provider.md) a una clase de consumidor lógico. Los usuarios crean instancias de la clase Consumer como parte de una suscripción permanente. Si el proveedor de eventos no se está ejecutando cuando se produce un evento, WMI inicia el proveedor cuando necesita proporcionar eventos.

En el procedimiento siguiente se describe cómo implementar un proveedor de consumidor de eventos.

**Para implementar un proveedor de consumidor de eventos**

1.  Diseñe clases de consumidor en Managed Object Format (MOF) y regístrela en WMI. Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

    Los proveedores de clases se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) . Para obtener más información, vea [registrar un proveedor de consumidor de eventos](registering-an-event-consumer-provider.md).

2.  Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor. Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de consumidores de eventos que utilicen el modelo de multithreading "both".

     

3.  Implemente la interfaz [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) para el proveedor.

    La interfaz [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) es la interfaz principal para un proveedor de consumidor de eventos.

4.  Proporcione uno o más consumidores físicos para recibir los mensajes de eventos de WMI.

    Un consumidor físico es un objeto COM que representa un consumidor de eventos permanente. Todos los consumidores físicos deben implementar la interfaz [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Para obtener más información, consulte [implementación de un consumidor físico](implementing-a-physical-consumer.md).

 

 



