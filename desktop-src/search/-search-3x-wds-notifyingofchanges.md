---
description: Mediante el uso de los componentes de las API de notificación, se puede notificar al indexador que un elemento se ha cambiado, se ha migrado o eliminado, y puede Agregar ámbitos de búsqueda a la cola de direcciones URL del indexador de Windows Search que requieren indexación.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: Notificar el índice de cambios (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a89112da20c4010e1fc23fab16778309195d20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153988"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>Notificar el índice de cambios (búsqueda de Windows)

Mediante el uso de los componentes de las API de notificación, se puede notificar al indexador que un elemento se ha cambiado, se ha migrado o eliminado, y puede Agregar ámbitos de búsqueda a la cola de direcciones URL del indexador de Windows Search que requieren indexación.

Los componentes pueden notificar al indizador de Windows Search que han cambiado los datos de su almacén. Normalmente, puede confiar en los rastreos programados del indexador. Sin embargo, proporcionar notificaciones al indexador puede mejorar el rendimiento asegurándose de que el indexador no rastrea todo el almacén en los índices incrementales. Por ejemplo, esto podría recomendarse si se espera que el almacén de datos sea excepcionalmente grande o que esté disponible de forma excepcional, como por ejemplo, un almacén de datos de correo electrónico.

-   [Implementación de notificaciones administradas por el indexador](#implementing-indexer-managed-notifications)
    -   [Cola de notificaciones](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [Implementación de notificaciones administradas por el proveedor](#implementing-provider-managed-notifications)
    -   [Cola de notificaciones](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implementación de notificaciones administradas por el indexador

Las notificaciones administradas por indexador le permiten controlar el acceso a su almacén de datos a la vez que se le libera de mantener la cola de notificaciones en todo el proceso de indexación. El proveedor de notificaciones debe supervisar los cambios en el almacén de datos y crear una cola de notificaciones. Periódicamente, el proveedor envía un lote de notificaciones de cambio al indexador. Cuando el indexador recibe las notificaciones, devuelve una confirmación y puede quitar los elementos de la cola. Si después de un período de tiempo no recibe un reconocimiento, puede volver a enviar las notificaciones. En caso de error, el indizador vuelve a generar su cola interna de elementos para rastrear o realiza un rastreo incremental del almacén.

Para implementar notificaciones administradas por el indexador, debe implementar lo siguiente:

-   Mecanismo para supervisar los cambios en el almacén de datos.
-   Una estructura de datos para poner en cola información (varias estructuras de [**\_ \_ \_ cambio persistentes de elementos de búsqueda**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) ) sobre esos cambios.
-   La interfaz [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) para enviar las notificaciones al indexador y para obtener confirmaciones de notificación del indexador.

### <a name="notifications-queue"></a>Cola de notificaciones

Debe supervisar y poner en cola todos los cambios en el almacén de datos para enviarlos al indexador como una notificación. El número de notificaciones que se ponen en cola y la frecuencia con que se envían al indexador depende de su circunstancia. Es posible que se envíe un lote de notificaciones por cada *n* cambios o después de algún intervalo de tiempo *t* o de una combinación de ambos.

El indexador espera que las notificaciones se incluyan en una matriz de estructuras de [**\_ \_ \_ cambio persistentes de elementos de búsqueda**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) , por lo que puede optar por implementar la cola de forma similar.

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

Para tener acceso a esta interfaz, primero cree una instancia de un objeto [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) para obtener acceso a un objeto [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . Desde ese objeto **ISearchCatalogManager** , crea una instancia de un objeto [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) y notifica al indexador de los cambios de datos con una llamada al método **OnItemsChanged** .

En la llamada a este método, se incluye el número de cambios que se están informando y una matriz de estructuras de [**\_ \_ \_ cambio persistente del elemento de búsqueda**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) . Obtiene una matriz de códigos de finalización de recursos humanos que indican si se aceptó cada dirección URL para la indexación. Esta es la confirmación del indexador.

## <a name="implementing-provider-managed-notifications"></a>Implementación de notificaciones administradas por el proveedor

Las notificaciones administradas por el proveedor permiten controlar el acceso al almacén de datos y supervisar el progreso del indexador mientras actualiza el catálogo de Windows Search. El proveedor debe supervisar los cambios en el almacén de datos y crear una cola de notificaciones. Periódicamente, el proveedor envía un lote de notificaciones de cambio al indexador. Cuando el indexador recibe las notificaciones, devuelve una confirmación. Si después de un período de tiempo no recibe un reconocimiento, puede volver a enviar las notificaciones. A medida que el indexador rastrea el almacén de datos y actualiza el catálogo de Windows Search, notifica al proveedor de cada actualización del catálogo y puede quitar los elementos de la cola. El proveedor mantiene su cola de notificación a lo largo de este proceso, de modo que, en caso de error, pueda volver a enviar las notificaciones al indexador.

Para implementar notificaciones administradas por el proveedor, debe implementar lo siguiente:

-   Mecanismo para supervisar los cambios en el almacén de datos.
-   Una estructura de datos para poner en cola la información (varias estructuras de [**\_ \_ cambio de elementos de búsqueda**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) ) sobre esos cambios.
-   La interfaz [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) para enviar las notificaciones al indexador y para obtener confirmaciones de notificación del indexador.
-   Interfaz [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) para recibir actualizaciones sobre el estado de la indización.

### <a name="notifications-queue"></a>Cola de notificaciones

Debe supervisar y poner en cola todos los cambios en el almacén de datos para enviarlos al indexador como una notificación. El número de notificaciones que se ponen en cola y la frecuencia con que se envían al indexador depende de su circunstancia. Es posible que se envíe un lote de notificaciones por cada *n* cambios o después de algún intervalo de tiempo *t* o de una combinación de ambos.

El indexador espera que las notificaciones aparezcan en una matriz de estructuras de [**\_ \_ cambio de elementos de búsqueda**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) , por lo que puede optar por almacenar la información de los cambios de forma similar. Sin embargo, también debe poder hacer coincidir las notificaciones que envíe con las confirmaciones y las actualizaciones devueltas por el indexador. Es posible que también desee poder detectar el tiempo necesario para obtener confirmaciones, de modo que pueda decidir si desea volver a enviar las notificaciones.

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Para tener acceso a esta interfaz, primero cree una instancia de un objeto [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) para obtener acceso a un objeto [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . Desde ese objeto **ISearchCatalogManager** , crea una instancia de un objeto [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) y notifica al indexador de los cambios de datos con una llamada al método **OnItemsChanged** .

En la llamada a este método, se incluye el número de cambios que se van a informar y una matriz de estructuras de [**\_ \_ cambio de elementos de búsqueda**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) . Obtiene una matriz de DocIds asignados por indexador que representan cada cambio, así como una matriz de códigos de finalización de recursos humanos que indican si se aceptó la indexación de cada dirección URL. Esta es la confirmación del indexador de que ha recibido las notificaciones y se está preparando para indexar los elementos.

A partir de ese punto, el indexador envía las actualizaciones mediante la interfaz [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) .

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

Para obtener actualizaciones sobre el estado de los elementos y el catálogo, debe registrar la interfaz [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) con el indizador para que pueda enviarle devoluciones de llamada. Cada actualización enviada mediante [**ISearchNotifyInlineSite:: OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) identifica los elementos por DocId, el estado de cada elemento ([**\_ Estado de \_ indización \_ de elementos de búsqueda**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) y la fase de indización ([**\_ \_ fase de indización de búsqueda**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)) en la que se encuentran los elementos.

No solo recibirá actualizaciones sobre el estado de cada elemento, tal y como se describió anteriormente, también obtendrá información importante sobre el estado del catálogo. El servicio Windows Search puede ser interrumpido o reiniciado por el usuario final, una aplicación de terceros o algún otro error. Cuando esto sucede, necesita una manera de determinar qué notificaciones se reenvían al indexador.

El método [**ISearchNotifyInlineSite:: OnCatalogStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) , al que llama el servicio Windows Search, informa a los clientes sobre el estado del catálogo mediante los parámetros que se describen en la tabla siguiente.



| Parámetro                 | Descripción                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | Un GUID que representa el restablecimiento del catálogo. Si este GUID cambia, se deben reenviar todas las notificaciones.                                                        |
| guidCheckPointSignature   | Un GUID que representa el último punto de control restaurado. Si este GUID cambia, se deben reenviar todas las notificaciones acumuladas desde el último punto de control guardado. |
| dwLastCheckPointNumber    | Número que indica el último punto de control guardado.                                                                                                        |



 

 

Cuando se produce un punto de comprobación del catálogo, el servicio de búsqueda actualiza el *dwLastCheckPointNumber* y todas las notificaciones enviadas antes de ese punto de control son seguras y recuperables en caso de que se produzca un error en el servicio. Los proveedores de notificaciones solo tienen que realizar el seguimiento de las notificaciones enviadas entre los puntos de comprobación y reenviar en caso de que se restaure o restablezca el catálogo.

Si se realiza una restauración de catálogo, el servicio de búsqueda revierte el catálogo al último punto de comprobación guardado y actualiza el *guidCheckPointSignature*. En esta situación, los proveedores de notificaciones deben reenviar todas las notificaciones acumuladas desde el último punto de control guardado, tal y como se identifica en el *dwLastCheckPointNumber*.

Si se debe restablecer el catálogo, el servicio de búsqueda restablece todo el catálogo y actualiza el *guidCatalogResetSignature*. El proveedor de notificaciones debe volver a enviar todo el ámbito de rastreo.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
-   Para obtener información general del administrador de catálogos y del administrador de búsqueda de catálogos (CSM), consulte [usar el administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) y [el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md).
-   Para obtener información sobre cómo crear un almacén de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Descripción de los controladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Código de ejemplo: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Crear un conector de búsqueda para un controlador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Controladores de protocolo de depuración](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
