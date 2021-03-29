---
description: Es posible que desee escribir una aplicación que pueda reaccionar a los eventos en cualquier momento.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Recepción de eventos en todo momento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5559068e1e108c6f4185c31f8858a9e4169c50c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360545"
---
# <a name="receiving-events-at-all-times"></a>Recepción de eventos en todo momento

Es posible que desee escribir una aplicación que pueda reaccionar a los eventos en cualquier momento. Por ejemplo, es posible que un administrador desee recibir un mensaje de correo electrónico cuando las medidas de rendimiento específicas disminuyan en los servidores de red. En este caso, la aplicación debe ejecutarse en todo momento. Sin embargo, la ejecución continua de una aplicación no es un uso eficaz de los recursos del sistema. En su lugar, WMI le permite crear un consumidor de eventos permanente. Los consumidores de eventos permanentes deben cumplir requisitos de seguridad especiales. Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).

Un consumidor de eventos permanente recibe eventos hasta que su registro se cancela explícitamente.

Un consumidor de eventos permanente es una combinación de las siguientes clases, filtros y objetos COM de WMI que residen en el sistema:

-   Objeto COM denominado consumidor físico. WMI proporciona varios consumidores permanentes estándar. Por ejemplo, el consumidor de eventos Active script [ejecuta un script cuando se produce un evento](running-a-script-based-on-an-event.md).
-   Nueva clase de consumidor permanente.
-   Instancia de la clase de consumidor permanente denominada consumidor lógico.
-   Filtro que contiene la consulta de eventos.
-   Una vinculación entre el consumidor y el filtro.

Las propiedades de un consumidor de eventos lógicos especifican las acciones que se deben realizar cuando se notifica un evento, pero no definen las consultas de eventos con las que están asociadas. Cuando se señala, WMI carga automáticamente el objeto COM que representa el consumidor de eventos permanente en la memoria activa. Normalmente, esto sucede durante el inicio o en respuesta a un evento desencadenador. Tras su activación, el consumidor de eventos permanente actúa como un consumidor de eventos normal, pero permanece hasta que el sistema operativo ha descargado de forma específica.

Puede escribir su propio consumidor de eventos permanente o usar las [clases de consumidor estándar](standard-consumer-classes.md)preinstaladas de WMI, como [**ActiveScriptEventConsumer**](activescripteventconsumer.md). Para obtener más información, vea [clases de consumidor estándar](standard-consumer-classes.md), [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)y [eventos de supervisión](monitoring-events.md).

En el procedimiento siguiente se describe cómo crear su propio consumidor de eventos permanente.

**Para crear su propio consumidor de eventos permanente**

1.  Determine qué tipo de eventos desea recibir.

    WMI admite eventos intrínsecos y extrínsecos. Un evento intrínseco es un evento predefinido por WMI, mientras que un evento extrínseco es un evento definido por un proveedor de terceros. Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).

2.  [Implemente un consumidor físico](implementing-a-physical-consumer.md).

    La diferencia principal entre una aplicación de administración y un [*consumidor físico*](gloss-p.md) es que un usuario carga y descarga una aplicación de administración, mientras que WMI carga y descarga un consumidor físico. La mayor parte del código debe estar en el consumidor físico.

    > [!Note]  
    > Este paso es el primero en el procedimiento para facilitar la explicación. En cuanto a la codificación, debe crear el consumidor físico en último lugar. De este modo, puede diseñar los parámetros y la lógica para su proveedor de eventos permanente antes de comenzar la codificación larga. Sin embargo, no hay ninguna restricción sobre la escritura del consumidor físico en primer lugar.

     

3.  [Cree una nueva clase de consumidor que describa el consumidor físico](creating-a-new-permanent-event-consumer-class.md).

    Como cualquier clase, la clase de consumidor describe los parámetros generales de un consumidor de eventos permanente en WMI.

4.  [Cree una instancia de la clase Consumer](creating-a-logical-consumer.md).

    Al igual que cualquier otra clase WMI, debe crear una instancia de la clase Consumer si desea implementar la clase. Una instancia de una clase de consumidor también se conoce como [*consumidor lógico*](gloss-l.md). El consumidor lógico representa al consumidor físico en WMI.

5.  [Cree un filtro de eventos](creating-an-event-filter.md).

    Las consultas de eventos que activan consumidores de eventos permanentes se denominan [*filtros de eventos*](gloss-e.md). Un filtro de evento único se puede asociar a varios consumidores de eventos lógicos. Además, se pueden asociar varios filtros de eventos a un único consumidor de eventos lógicos. El filtro es una instancia de [**\_ \_ EventFilter**](--eventfilter.md).

    Un evento de registro NT se genera cuando se produce un error en la consulta del consumidor de eventos permanente. El origen del evento es WinMgmt, el ID. de evento es 10 y el tipo de evento es error.

6.  [Vincule el filtro de eventos al consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

    Al vincular el filtro de eventos al consumidor lógico, se indica a WMI sobre qué filtro de eventos pertenece al consumidor lógico. Los consumidores de eventos lógicos y los filtros de eventos están vinculados por una instancia de clase de Asociación de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md). Cuando se recibe un evento que coincide con una consulta de evento descrita en un filtro de eventos, WMI busca el consumidor de eventos lógicos asociado examinando la instancia de la clase de asociación. Una vez que se encuentra la instancia del consumidor de eventos lógicos, WMI utiliza una instancia de la clase [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) para buscar y ejecutar el consumidor de eventos físicos asociado a esta instancia.

7.  [Escribir un proveedor de consumidor de eventos](writing-an-event-consumer-provider.md).

    El proveedor del consumidor de eventos es un objeto COM que busca el consumidor físico para WMI.

 

 



