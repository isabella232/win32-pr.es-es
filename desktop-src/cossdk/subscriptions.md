---
description: Los datos de suscripción residen en el catálogo com+ de la suscripción. Una suscripción se puede crear mediante la herramienta administrativa Servicios de componentes o mediante programación mediante la interfaz ICOMAdminCatalog::InstallComponent.
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Suscripciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48810ae90f3507ea7afb661b106c4d05f8cc5b9a4f1b09aafdfb26d9fdb03a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546177"
---
# <a name="subscriptions"></a>Suscripciones

Los datos de suscripción residen en el catálogo com+ de la suscripción. Una suscripción se puede crear mediante la herramienta administrativa Servicios de componentes o mediante programación mediante la [**interfaz ICOMAdminCatalog::InstallComponent.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)

La [**colección SubscriptionsForComponent**](subscriptionsforcomponent.md) se usa para agregar, eliminar o cambiar información relativa a las suscripciones. La **colección SubscriptionsForComponent** es una colección secundaria de un componente. Para agregar una suscripción, obtenga la colección **SubscriptionsForComponent** del componente y use el [**método Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) para agregar una entrada a la colección. Para configurar las distintas propiedades del objeto de suscripción, use la [**propiedad**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) Value. Para guardar los cambios, use [**SaveChanges en**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) el **objeto de colección SubscriptionsForComponent.**

También puede usar la herramienta de administración Servicios de componentes para modificar algunas de las propiedades de la suscripción, pero no todas. Las suscripciones especifican la siguiente información:

-   Identidad y ubicación del suscriptor
-   Método de entrega
-   Métodos de eventos que se entregan
-   Objeto de clase de evento y propiedad PublisherID de un componente de clase de eventos del que el suscriptor desea recibir eventos

Las suscripciones existen independientemente de los objetos de clase de eventos. Puede deshabilitar una suscripción estableciendo la propiedad Enabled en False. Eventos COM+ no llama a una suscripción deshabilitada.

Los tres tipos de suscripciones son los siguientes:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistente
</dt> <dd>

Las suscripciones persistentes residen en el catálogo de COM+ y son independientes de la duración del suscriptor. Las suscripciones persistentes sobreviven a un reinicio del sistema. Por lo general, se crea una suscripción persistente cuando se instala una aplicación en el equipo de un suscriptor y se quita cuando se quita la aplicación. Después de crear una suscripción persistente, EVENTOS COM+ activa al suscriptor cada vez que se le debe entregar un evento.

Cuando un publicador crea instancias y [](the-com--event-class-object.md) realiza una llamada en un objeto de clase de eventos, el objeto busca todas las suscripciones persistentes en el catálogo de COM+ y crea una nueva instancia de cada objeto. El proceso de creación puede ser directo o a través de un moniker para los componentes en cola. Especifique el objeto de suscriptor mediante la [**propiedad SubscriberMoniker**](subscriptionsforcomponent.md) de la suscripción. Los objetos de suscriptor creados por una suscripción persistente siempre se liberan después de cada llamada de evento.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transitoria
</dt> <dd>

Para las suscripciones transitorias, puede usar la [**colección TransientSubscriptions,**](transientsubscriptions.md) cuyo objeto primario es el objeto de catálogo raíz. Las suscripciones transitorias solicitan un evento para un objeto de suscriptor específico que ya existe. Las suscripciones transitorias se almacenan en el catálogo de COM+, pero la suscripción se elimina si se detiene el sistema operativo o el sistema operativo. A diferencia de las suscripciones persistentes, las suscripciones transitorias están vinculadas a un objeto determinado y solo se almacenan en el sistema de eventos. Las suscripciones transitorias pueden ser más eficaces que las suscripciones persistentes, pero debe administrar sus ciclos de vida de objetos. Para obtener información sobre cómo registrar una suscripción transitoria, vea [Registrar una suscripción transitoria.](registering-a-transient-subscription.md)

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Por usuario
</dt> <dd>

Las suscripciones por usuario solo pueden entregar eventos cuando el suscriptor ha iniciado sesión en el equipo del sistema de eventos. Cuando el suscriptor inicia sesión, el sistema de eventos habilita todas las suscripciones en las que la marca *PerUser* está establecida en **TRUE** y *UserName* se establece en el nombre del usuario que ha iniciado sesión. Cuando el suscriptor cierra la sesión, las suscripciones se deshabilitan.

Las suscripciones por usuario solo son efectivas cuando el publicador y el suscriptor están en el mismo equipo. El inicio de sesión y la cierre de sesión solo se detectan en el equipo del publicador, no en el equipo en el que reside el objeto de suscriptor.

</dd> </dl>

El sistema de eventos usa metadatos para notificar a los suscriptores interesados cada vez que se crean, modifican o quitan objetos o suscripciones de clase de eventos. Para recibir metadatos del sistema de eventos, las aplicaciones deben crear una suscripción que resida en el equipo del sistema de eventos y que especifique el identificador de interfaz de activación (IID \_ IEventObjectChange).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicación y entrega de eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[El objeto de clase de eventos COM+](the-com--event-class-object.md)
</dt> <dt>

[Uso de eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



