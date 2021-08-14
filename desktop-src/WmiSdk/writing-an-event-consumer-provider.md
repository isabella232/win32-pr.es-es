---
description: Un proveedor de consumidores de eventos es un componente de la arquitectura de consumidor permanente que determina qué consumidor de eventos permanente controla un evento determinado.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Escribir un proveedor de consumidores de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312e0c2ecbf02d8bb0a8f491339d191aadde41a66cd3e3228c3187d5dcf689e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553102"
---
# <a name="writing-an-event-consumer-provider"></a>Escribir un proveedor de consumidores de eventos

Un proveedor de consumidores de eventos es un componente de la arquitectura de consumidor permanente que determina qué consumidor de eventos permanente controla un evento determinado. Debe crear un proveedor de consumidores de eventos junto con los consumidores de eventos permanentes para enrutar los eventos correctamente desde WMI.

Un proveedor de consumidores de eventos vincula un proveedor de eventos con una lista de clases de consumidor. A continuación, las instancias de estas clases de consumidor reciben eventos de ese proveedor. WMI identifica a qué proveedor de consumidores se entregan los eventos, en función de la instancia [**\_ \_ eventConsumerProviderRegistration,**](--eventconsumerproviderregistration.md) que asocia la instancia [**\_ \_ de Win32Provider**](--win32provider.md) del proveedor de consumidores a una clase de consumidor lógica. Los usuarios crean instancias de la clase de consumidor como parte de una suscripción permanente. Si el proveedor de eventos no se está ejecutando cuando se produce un evento, WMI inicia el proveedor cuando necesita entregar eventos.

En el procedimiento siguiente se describe cómo implementar un proveedor de consumidores de eventos.

**Para implementar un proveedor de consumidores de eventos**

1.  Diseñe clases de consumidor Managed Object Format (MOF) y regístrelas con WMI. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes .](designing-managed-object-format--mof--classes.md)

    Los proveedores de clases se registran con WMI mediante la creación de una [**\_ \_ instancia de Win32Provider**](--win32provider.md) y una [**\_ \_ clase EventConsumerProviderRegistration.**](--eventconsumerproviderregistration.md) Para obtener más información, vea [Registrar un proveedor de consumidores de eventos.](registering-an-event-consumer-provider.md)

2.  Implemente [**la interfaz IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    WMI usa [**IWbemProviderInit para**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) cargar e inicializar un proveedor. Para obtener más información, [vea Inicializar un proveedor.](initializing-a-provider.md)

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de consumidores de eventos que usen el modelo multithreading "Both".

     

3.  Implemente [**la interfaz IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) para el proveedor.

    La [**interfaz IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) es la interfaz principal para un proveedor de consumidores de eventos.

4.  Proporcione uno o varios consumidores físicos para recibir los mensajes de evento de WMI.

    Un consumidor físico es un objeto COM que representa un consumidor de eventos permanente. Todos los consumidores físicos deben implementar la [**interfaz IWbemUnboundObjectSink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) Para obtener más información, [vea Implementar un consumidor físico.](implementing-a-physical-consumer.md)

 

 



