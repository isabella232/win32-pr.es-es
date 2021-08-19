---
description: Es posible que quiera escribir una aplicación que pueda reaccionar a eventos en cualquier momento.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Recepción de eventos en todo momento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e049b7816e53439ede5edbc67c3bcdbaf6ed6e71accb8b3f994544cdd0efbd31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817451"
---
# <a name="receiving-events-at-all-times"></a>Recepción de eventos en todo momento

Es posible que quiera escribir una aplicación que pueda reaccionar a eventos en cualquier momento. Por ejemplo, es posible que un administrador quiera recibir un mensaje de correo electrónico cuando las medidas de rendimiento específicas se rechace en los servidores de red. En este caso, la aplicación debe ejecutarse en todo momento. Sin embargo, la ejecución continua de una aplicación no es un uso eficaz de los recursos del sistema. En su lugar, WMI permite crear un consumidor de eventos permanente. Los consumidores de eventos permanentes deben cumplir requisitos de seguridad especiales. Para obtener más información, [vea Securing WMI Events](securing-wmi-events.md).

Un consumidor de eventos permanente recibe eventos hasta que su registro se cancela explícitamente.

Un consumidor de eventos permanente es una combinación de las siguientes clases WMI, filtros y objetos COM que residen en el sistema:

-   Un objeto COM denominado consumidor físico. WMI proporciona varios consumidores permanentes estándar. Por ejemplo, el consumidor de eventos de script activo [ejecuta un script cuando se produce un evento](running-a-script-based-on-an-event.md).
-   Nueva clase de consumidor permanente.
-   Instancia de la clase de consumidor permanente denominada consumidor lógico.
-   Filtro que contiene la consulta de eventos.
-   Vinculación entre el consumidor y el filtro.

Las propiedades de un consumidor de eventos lógicos especifican las acciones que se deben realizar cuando se notifica un evento, pero no definen las consultas de eventos a las que están asociadas. Cuando se señala, WMI carga automáticamente el objeto COM que representa el consumidor de eventos permanente en la memoria activa. Normalmente, esto se produce durante el inicio o en respuesta a un evento desencadenante. Después de activarse, el consumidor de eventos permanente actúa como un consumidor de eventos normal, pero permanece hasta que el sistema operativo lo descargue específicamente.

Puede escribir su propio consumidor de eventos permanente o usar las clases de consumidor estándar preinstaladas de [WMI,](standard-consumer-classes.md)como [**ActiveScriptEventConsumer.**](activescripteventconsumer.md) Para obtener más información, [vea Clases de consumidor estándar](standard-consumer-classes.md), Supervisión y respuesta a eventos con [consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)y Eventos de [supervisión](monitoring-events.md).

En el procedimiento siguiente se describe cómo crear su propio consumidor de eventos permanente.

**Para crear su propio consumidor de eventos permanente**

1.  Determine qué tipo de eventos desea recibir.

    WMI admite eventos intrínsecos y extrínsecos. Un evento intrínseco es un evento predefinido por WMI, mientras que un evento extrínseco es un evento definido por un proveedor de terceros. Para obtener más información, [vea Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)

2.  [Implemente un consumidor físico.](implementing-a-physical-consumer.md)

    La principal diferencia entre una [](gloss-p.md) aplicación de administración y un consumidor físico es que un usuario carga y descarga una aplicación de administración, mientras que WMI carga y descarga un consumidor físico. La mayor parte de la codificación debe estar en el consumidor físico.

    > [!Note]  
    > Este paso es el primero en el procedimiento para facilitar la explicación. En términos de codificación, debe crear el último consumidor físico. De este modo, puede establecer los parámetros y la lógica para el proveedor de eventos permanente antes de comenzar la codificación larga. Sin embargo, no hay ninguna restricción para escribir primero el consumidor físico.

     

3.  [Cree una nueva clase de consumidor que describa el consumidor físico](creating-a-new-permanent-event-consumer-class.md).

    Al igual que cualquier clase, la clase de consumidor describe los parámetros generales de un consumidor de eventos permanente para WMI.

4.  [Cree una instancia de la clase de consumidor](creating-a-logical-consumer.md).

    Al igual que cualquier otra clase WMI, debe crear una instancia de la clase de consumidor si desea implementar la clase . Una instancia de una clase de consumidor también se conoce como [*consumidor lógico.*](gloss-l.md) El consumidor lógico representa el consumidor físico para WMI.

5.  [Cree un filtro de eventos](creating-an-event-filter.md).

    Las consultas de eventos que activan consumidores de eventos permanentes se denominan [*filtros de eventos*](gloss-e.md). Un único filtro de eventos se puede asociar a varios consumidores de eventos lógicos. Además, se pueden asociar varios filtros de eventos a un único consumidor de eventos lógicos. El filtro es una instancia de [**\_ \_ EventFilter.**](--eventfilter.md)

    Se genera un evento de registro NT cuando se produce un error en la consulta de un consumidor de eventos permanente. El origen del evento es WinMgmt, el identificador de evento es 10 y el tipo de evento es Error.

6.  [Vincule el filtro de eventos al consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

    Al vincular el filtro de eventos al consumidor lógico, se indica a WMI qué filtro de eventos pertenece a qué consumidor lógico. Los consumidores de eventos lógicos y los filtros de eventos están vinculados por una instancia de clase de asociación [**\_ \_ de FilterToConsumerBinding**](--filtertoconsumerbinding.md). Cuando se recibe un evento que coincide con una consulta de eventos descrita en un filtro de eventos, WMI busca el consumidor de eventos lógicos asociado consultando la instancia de clase de asociación. Una vez que se encuentra la instancia del consumidor de eventos lógicos, WMI usa una instancia de la clase [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) para buscar y ejecutar el consumidor de eventos físico asociado a esta instancia.

7.  [Escribir un proveedor de consumidores de eventos](writing-an-event-consumer-provider.md).

    El proveedor de consumidores de eventos es un objeto COM que busca el consumidor físico para WMI.

 

 



