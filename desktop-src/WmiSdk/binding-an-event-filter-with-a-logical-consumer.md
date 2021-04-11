---
description: Después de crear el consumidor de eventos lógicos y el filtro de eventos, debe vincularlos, lo que registra el consumidor lógico para recibir notificaciones sobre los eventos especificados por el filtro.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Enlazar un filtro de eventos con un consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912406"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a>Enlazar un filtro de eventos con un consumidor lógico

Después de crear el consumidor de eventos lógicos y el filtro de eventos, debe vincularlos, lo que registra el consumidor lógico para recibir notificaciones sobre los eventos especificados por el filtro.

En el procedimiento siguiente se describe cómo enlazar un filtro de eventos con un consumidor lógico.

**Para enlazar un filtro de eventos con un consumidor lógico**

1.  Cree una instancia de la clase del sistema [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) en el repositorio WMI.

    La clase [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) es una clase de asociación que vincula la instancia de filtro de eventos y la instancia de consumidor lógico a la vez a través de las propiedades de **filtro** y referencia de **consumidor** . Para obtener más información, vea [declarar una clase de asociación](declaring-an-association-class.md).

2.  Establezca la propiedad **filtro** en la instancia del filtro.
3.  Establezca la propiedad **Consumer** en la instancia del consumidor lógico.
4.  Establezca la propiedad **DeliverSynchronously** para determinar el tipo de entrega que desea.

    La propiedad **DeliverSynchronously** determina cuándo WMI envía notificaciones de eventos de forma sincrónica o asincrónica. Al establecer esta propiedad en **true** , se solicita una entrega sincrónica. Use la entrega sincrónica solo cuando el consumidor permanente pueda procesar eventos en unos 100 microsegundos aproximadamente.

    > [!Note]  
    > Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

     

5.  Al anular el registro del consumidor de eventos lógicos, asegúrese de eliminar la instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .

    Cada instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) representa un registro para una notificación de eventos específica. Cuando se elimina un enlace, WMI desactiva el registro. Es posible que tenga que eliminar las instancias del consumidor lógico y del filtro de eventos para desactivar el registro, en función de la implementación.

En el ejemplo de código siguiente se muestra una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) que asocia una instancia de una clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) con un filtro de eventos específico (la instancia del consumidor de eventos se creó en el tema [crear un consumidor lógico](creating-a-logical-consumer.md) y el filtro de eventos se creó en el tema [crear un filtro de eventos](creating-an-event-filter.md) ).

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Dos consumidores, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) y [**CommandLineEventConsumer**](commandlineeventconsumer.md), no funcionarán a menos que su creador sea miembro del grupo de administradores local.

**:** Cuando un administrador crea una suscripción, su SID no se utiliza para la propiedad **CreatorSID** , pero en su lugar se usa el SID del grupo de administradores locales. Por lo tanto, los administradores pueden crear las instancias y la suscripción seguirá funcionando. Para obtener más información, consulte [recepción de eventos de forma segura](receiving-events-securely.md).

Cuando un filtro se enlaza a un consumidor lógico, el evento se registra mediante el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) para Windows (ETW). Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> </dl>

 

 
