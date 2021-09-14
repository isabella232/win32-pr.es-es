---
description: Después de crear el consumidor de eventos lógicos y el filtro de eventos, debe vincularlos, lo que registra el consumidor lógico para recibir una notificación sobre los eventos especificados por el filtro.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Enlazar un filtro de eventos con un consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073068"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a>Enlazar un filtro de eventos con un consumidor lógico

Después de crear el consumidor de eventos lógicos y el filtro de eventos, debe vincularlos, lo que registra el consumidor lógico para recibir una notificación sobre los eventos especificados por el filtro.

En el procedimiento siguiente se describe cómo enlazar un filtro de eventos con un consumidor lógico.

**Para enlazar un filtro de eventos con un consumidor lógico**

1.  Cree una instancia de la clase del sistema [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) en el repositorio WMI.

    La [**\_ \_ clase FilterToConsumerBinding**](--filtertoconsumerbinding.md) es una clase de asociación que vincula la instancia de filtro de eventos y la instancia de consumidor lógico a través de las propiedades **de** referencia Filter y **Consumer.** Para obtener más información, vea [Declarar una clase de asociación](declaring-an-association-class.md).

2.  Establezca la **propiedad Filter** en la instancia del filtro.
3.  Establezca la **propiedad Consumer** en la instancia del consumidor lógico.
4.  Establezca la **propiedad DeliverSynchronously** para determinar el tipo de entrega que desea.

    La **propiedad DeliverSynchronously** determina cuándo WMI entrega notificaciones de eventos de forma sincrónica o asincrónica. Establecer esta propiedad en **TRUE solicita** una entrega sincrónica. Use la entrega sincrónica solo cuando el consumidor permanente pueda procesar eventos en aproximadamente 100 microsegundos.

    > [!Note]  
    > Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que el cliente requiere, se recomienda usar la comunicación semisincronosa en lugar de la asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

     

5.  Al anular el registro del consumidor de eventos lógicos, asegúrese de eliminar la [**\_ \_ instancia FilterToConsumerBinding.**](--filtertoconsumerbinding.md)

    Cada [**\_ \_ instancia de FilterToConsumerBinding**](--filtertoconsumerbinding.md) representa un registro para una notificación de eventos específica. Al eliminar un enlace, WMI desactiva el registro. Es posible que tenga que eliminar las instancias de filtro de eventos y consumidor lógico para desactivar el registro, en función de la implementación.

En el ejemplo de código siguiente se muestra una instancia [**\_ \_ filterToConsumerBinding**](--filtertoconsumerbinding.md) que asocia una instancia de una clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) a un filtro de eventos específico (la instancia del consumidor de eventos se creó en el tema Crear un consumidor lógico y el filtro de eventos se creó en el tema Crear un filtro [de](creating-an-event-filter.md) eventos). [](creating-a-logical-consumer.md)

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

Dos consumidores, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) y [**CommandLineEventConsumer,**](commandlineeventconsumer.md)no funcionarán a menos que su creador sea miembro del grupo de administradores local.

**:** Cuando un administrador crea una suscripción, su SID no se usa para la propiedad **CreatorSID,** pero en su lugar se usa el SID del grupo administradores local. Por lo tanto, diferentes administradores pueden crear instancias y la suscripción seguirá funcionando. Para obtener más información, vea [Recepción de eventos de forma segura.](receiving-events-securely.md)

Cuando un filtro está enlazado a un [](/windows/desktop/ETW/event-tracing-portal) consumidor lógico, el seguimiento de eventos registra el evento Windows (ETW). Para obtener más información, vea [Seguimiento de la actividad WMI.](tracing-wmi-activity.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> </dl>

 

 
