---
description: 'Los datos de la suscripción residen en el catálogo COM+ de la suscripción. Una suscripción se puede crear mediante la herramienta administrativa Servicios de componentes o mediante programación con la interfaz ICOMAdminCatalog:: InstallComponent.'
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Suscripciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274944"
---
# <a name="subscriptions"></a>Suscripciones

Los datos de la suscripción residen en el catálogo COM+ de la suscripción. Una suscripción se puede crear mediante la herramienta administrativa Servicios de componentes o mediante programación con la interfaz [**ICOMAdminCatalog:: InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) .

La colección [**SubscriptionsForComponent**](subscriptionsforcomponent.md) se usa para agregar, eliminar o cambiar la información relativa a las suscripciones. La colección **SubscriptionsForComponent** es una colección secundaria de un componente. Para agregar una suscripción, obtenga la colección **SubscriptionsForComponent** del componente y use el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) para agregar una entrada a la colección. Para configurar las distintas propiedades del objeto de suscripción, utilice la propiedad [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) . Para guardar los cambios, use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto de colección **SubscriptionsForComponent** .

También puede usar la herramienta de administración de servicios de componentes para modificar algunas de las propiedades de la suscripción, pero no todas. Las suscripciones especifican la siguiente información:

-   Identidad y ubicación del suscriptor
-   Método de entrega
-   Métodos de evento que se van a proporcionar
-   Objeto de clase de eventos y propiedad PublisherID de un componente de clase de evento del que el suscriptor desea recibir eventos

Las suscripciones existen de forma independiente de los objetos de la clase de eventos. Puede deshabilitar una suscripción estableciendo la propiedad Enabled en false. Los eventos COM+ no llaman a una suscripción deshabilitada.

Los tres tipos de suscripciones son los siguientes:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Permanentes
</dt> <dd>

Las suscripciones persistentes residen en el catálogo de COM+ y son independientes de la duración del suscriptor. Las suscripciones persistentes sobreviven a un reinicio del sistema. Por lo general, una suscripción persistente se crea cuando se instala una aplicación en el equipo de un suscriptor y se quita cuando se quita la aplicación. Una vez creada una suscripción persistente, los eventos COM+ activan el suscriptor cada vez que se le debe entregar un evento.

Cuando un publicador crea una instancia de y realiza una llamada en un objeto de [clase de evento](the-com--event-class-object.md) , el objeto busca todas las suscripciones persistentes en el catálogo de com+ y crea una nueva instancia de cada objeto. El proceso de creación puede ser directo o a través de un moniker para los componentes en cola. Especifique el objeto de suscriptor mediante la propiedad [**SubscriberMoniker**](subscriptionsforcomponent.md) de la suscripción. Los objetos de suscriptor creados por una suscripción persistente siempre se liberan después de cada llamada de evento.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Temporal
</dt> <dd>

En el caso de las suscripciones transitorias, puede utilizar la colección [**TransientSubscriptions**](transientsubscriptions.md) , cuyo objeto primario es el objeto de catálogo raíz. Las suscripciones transitorias solicitan un evento para un objeto de suscriptor específico que ya existe. Las suscripciones transitorias se almacenan en el catálogo de COM+, pero la suscripción se elimina si se detiene el sistema operativo o el sistema de eventos. A diferencia de las suscripciones persistentes, las suscripciones transitorias se asocian a un objeto determinado y solo se almacenan en el sistema de eventos. Las suscripciones transitorias pueden ser más eficaces que las suscripciones persistentes, pero debe administrar los ciclos de vida de los objetos. Para obtener información sobre cómo registrar una suscripción transitoria, consulte [registrar una suscripción transitoria](registering-a-transient-subscription.md).

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Por usuario
</dt> <dd>

Las suscripciones por usuario solo pueden enviar eventos cuando el suscriptor inicia sesión en el equipo del sistema de eventos. Cuando el suscriptor inicia sesión, el sistema de eventos habilita todas las suscripciones en las que la marca *peruser* está establecida en **true** y *username* está establecido en el nombre del usuario que ha iniciado sesión. Cuando el suscriptor cierra la sesión, se deshabilitan las suscripciones.

Las suscripciones por usuario solo son efectivas cuando el publicador y el suscriptor se encuentran en el mismo equipo. Logon y Logoff solo se detectan en el equipo del publicador, no en el equipo en el que reside el objeto de suscriptor.

</dd> </dl>

El sistema de eventos utiliza metaeventos para notificar a los suscriptores interesados cada vez que se crean, modifican o quitan suscripciones o objetos de clase de eventos. Para recibir los metaeventos del sistema de eventos, las aplicaciones deben crear una suscripción que resida en el equipo del sistema de eventos y que especifique el identificador de la interfaz de activación (IID \_ IEventObjectChange).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicar y entregar eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Objeto de la clase de eventos COM+](the-com--event-class-object.md)
</dt> <dt>

[Usar eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



