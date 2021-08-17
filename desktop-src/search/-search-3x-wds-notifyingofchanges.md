---
description: Mediante el uso de las API de notificación, los componentes pueden notificar al indexador que un elemento se ha cambiado, movido o eliminado, y puede agregar ámbitos de búsqueda a la cola de direcciones URL del indexador de Windows Search que requieren indexación.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: Notificación al índice de cambios (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb386763be5192851368b1f46b69f94576fbe261a57d215d649d38ac5a19ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052232"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>Notificación al índice de cambios (Windows Search)

Mediante el uso de las API de notificación, los componentes pueden notificar al indexador que un elemento se ha cambiado, movido o eliminado, y puede agregar ámbitos de búsqueda a la cola de direcciones URL del indexador de Windows Search que requieren indexación.

Los componentes pueden notificar al Windows Search que los datos de su almacén han cambiado. Normalmente, puede confiar en los rastreos programados del indexador. Sin embargo, proporcionar notificaciones al indexador puede mejorar el rendimiento asegurándose de que el indexador no rastrea todo el almacén en índices incrementales. Por ejemplo, esto podría recomendarse si espera que el almacén de datos sea excepcionalmente grande o excepcionalmente ocupado, como un almacén de datos de correo electrónico, por ejemplo.

-   [Implementación de notificaciones administradas por indexador](#implementing-indexer-managed-notifications)
    -   [Cola de notificaciones](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [Implementación de notificaciones administradas por el proveedor](#implementing-provider-managed-notifications)
    -   [Cola de notificaciones](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implementación de notificaciones administradas por indexador

Las notificaciones administradas por el indexador le permiten controlar el acceso al almacén de datos y, al mismo tiempo, liberar el mantenimiento de la cola de notificaciones a lo largo de todo el proceso de indexación. El proveedor de notificaciones debe supervisar los cambios en el almacén de datos y crear una cola de notificaciones. Periódicamente, el proveedor envía un lote de notificaciones de cambio al indexador. Cuando el indexador recibe las notificaciones, devuelve una confirmación y puede quitar los elementos de la cola. Si después de un período de tiempo no recibe una confirmación, puede volver a enviar las notificaciones. En caso de error, el indexador vuelve a generar su cola interna de elementos para rastrear o realiza un rastreo incremental del almacén.

Para implementar notificaciones administradas por el indexador, debe implementar lo siguiente:

-   Un mecanismo para supervisar los cambios en el almacén de datos.
-   Estructura de datos para poner en cola información (varias [**estructuras SEARCH ITEM PERSISTENT \_ \_ \_ CHANGE)**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) sobre esos cambios.
-   [**Interfaz ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) para enviar las notificaciones al indexador y obtener confirmaciones de notificación del indexador.

### <a name="notifications-queue"></a>Cola de notificaciones

Debe supervisar y poner en cola todos los cambios del almacén de datos para enviarlos al indexador como una notificación. El número de notificaciones que pone en cola y la frecuencia con la que las envía al indexador depende de sus circunstancias. Quizás envíe un lote de notificaciones por cada *n número* de cambios o después de algún intervalo de tiempo *t,* o una combinación de los dos.

El indexador espera que las notificaciones se incluyen en una matriz de estructuras [**SEARCH \_ ITEM PERSISTENT \_ \_ CHANGE,**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) por lo que puede optar por implementar la cola de forma similar.

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

Para acceder a esta interfaz, primero debe crear una instancia de un [**objeto ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) para obtener acceso a un [**objeto ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) A partir de ese objeto **ISearchCatalogManager,** se crea una instancia de un objeto [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) y se notifica al indexador los cambios de datos con una llamada al método **OnItemsChanged.**

En la llamada a este método, se incluye el número de cambios que se notifican y una matriz de [**estructuras SEARCH ITEM PERSISTENT \_ \_ \_ CHANGE.**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) Se obtiene una matriz de códigos de finalización de RR. UU. que indica si se aceptó cada dirección URL para la indexación. Esta es la confirmación del indexador.

## <a name="implementing-provider-managed-notifications"></a>Implementación de notificaciones administradas por el proveedor

Las notificaciones administradas por el proveedor le permiten controlar el acceso al almacén de datos y supervisar el progreso del indexador a medida que actualiza el catálogo Windows Search. El proveedor debe supervisar los cambios en el almacén de datos y crear una cola de notificaciones. Periódicamente, el proveedor envía un lote de notificaciones de cambio al indexador. Cuando el indexador recibe las notificaciones, devuelve una confirmación. Si después de un período de tiempo no recibe una confirmación, puede volver a enviar las notificaciones. A medida que el indexador rastrea el almacén de datos y actualiza el catálogo de Windows Search, notifica a su proveedor cada actualización del catálogo y puede quitar los elementos de la cola. El proveedor mantiene su cola de notificaciones a lo largo de este proceso para que, en caso de error, pueda volver a enviar notificaciones al indexador.

Para implementar notificaciones administradas por el proveedor, debe implementar lo siguiente:

-   Un mecanismo para supervisar los cambios en el almacén de datos.
-   Estructura de datos para poner en cola información (varias [**estructuras SEARCH \_ ITEM \_ CHANGE)**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) sobre esos cambios.
-   [**Interfaz ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) para enviar las notificaciones al indexador y obtener confirmaciones de notificación del indexador.
-   [**Interfaz ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) para recibir actualizaciones sobre el estado de la indexación.

### <a name="notifications-queue"></a>Cola de notificaciones

Debe supervisar y poner en cola todos los cambios del almacén de datos para enviarlos al indexador como una notificación. El número de notificaciones que pone en cola y la frecuencia con la que las envía al indexador depende de sus circunstancias. Quizás envíe un lote de notificaciones por cada *n número* de cambios o después de algún intervalo de tiempo *t,* o una combinación de los dos.

El indexador espera que las notificaciones se incluyen en una matriz de estructuras [**SEARCH \_ ITEM \_ CHANGE,**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) por lo que puede optar por almacenar información de cambios de forma similar. Sin embargo, también debe ser capaz de hacer coincidir las notificaciones que envía con las confirmaciones y actualizaciones devueltas por el indexador. Es posible que también quiera poder detectar cuánto tiempo se tarda en obtener confirmaciones, para que pueda decidir si desea volver a enviar notificaciones o cuándo.

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Para acceder a esta interfaz, primero debe crear una instancia de un [**objeto ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) para obtener acceso a un [**objeto ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) Desde ese **objeto ISearchCatalogManager,** se crea una instancia de un objeto [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) y se notifica al indexador los cambios de datos con una llamada al método **OnItemsChanged.**

En la llamada a este método, se incluye el número de cambios que se notifican y una matriz de [**estructuras SEARCH \_ ITEM \_ CHANGE.**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) Se obtiene una matriz de DocIds asignados por el indexador que representan cada cambio, así como una matriz de códigos de finalización de RECURSOS que indican si se aceptó cada dirección URL para la indexación. Esta es la confirmación del indexador de que ha recibido las notificaciones y se está preparando para indexar los elementos.

A partir de ese momento, el indexador envía actualizaciones mediante la [**interfaz ISearchNotifyInlineSite.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite)

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

Para obtener actualizaciones sobre el estado de los elementos y el catálogo, debe registrar la interfaz [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) con el indexador para que pueda enviarle devoluciones de llamada. Cada actualización enviada mediante [**ISearchNotifyInlineSite::OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) identifica los elementos por DocId, el estado de cada elemento ([**SEARCH ITEM \_ \_ INDEXING \_ STATUS**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) y la fase de indexación [**(SEARCH \_ INDEXING \_ PHASE**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)) en la que se encuentran los elementos.

No solo recibe actualizaciones sobre el estado de cada elemento, como se describió anteriormente, sino que también obtiene información importante sobre el estado del propio catálogo. El Windows servicio Search puede interrumpir o reiniciar el usuario final, una aplicación de terceros o algún otro error. Cuando esto sucede, necesita una manera de determinar qué notificaciones reprobar al indexador.

El [**método ISearchNotifyInlineSite::OnCatalogStatusChange,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) al que llama el Windows servicio Search, informa a los clientes sobre el estado del catálogo mediante los parámetros descritos en la tabla siguiente.



| Parámetro                 | Descripción                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | GUID que representa el restablecimiento del catálogo. Si este GUID cambia, se deben volver a enviar todas las notificaciones.                                                        |
| guidCheckPointSignature   | GUID que representa el último punto de control restaurado. Si este GUID cambia, se deben volver a enviar todas las notificaciones acumuladas desde el último punto de control guardado. |
| dwLastCheckPointNumber    | Número que indica el último punto de control guardado.                                                                                                        |



 

 

Cuando se produce un punto de control de catálogo, el servicio de búsqueda actualiza *dwLastCheckPointNumber* y todas las notificaciones enviadas antes de ese punto de control son seguras y recuperables en caso de error del servicio. Los proveedores de notificaciones solo deben realizar un seguimiento de las notificaciones enviadas entre puntos de control y rechazo en caso de restauración o restablecimiento del catálogo.

Si se produce una restauración de catálogo, el servicio de búsqueda revierte el catálogo al último punto de control guardado y actualiza *guidCheckPointSignature*. En esta situación, los proveedores de notificaciones deben reprobar todas las notificaciones acumuladas desde el punto de control guardado más reciente identificado por *dwLastCheckPointNumber*.

Si se produce un restablecimiento del catálogo, el servicio de búsqueda restablece todo el catálogo y actualiza *guidCatalogResetSignature*. El proveedor de notificaciones debe volver a reprobar todo su ámbito de rastreo.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
-   Para obtener información general sobre el Administrador de catálogos y el Administrador de búsqueda de catálogos (CSM), vea Uso del Administrador de catálogos y Uso [del Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md). [](-search-3x-wds-mngidx-catalog-manager.md)
-   Para obtener información sobre cómo crear un almacén de datos de Shell, vea [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Descripción de los controladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Ejemplo de código: Extensiones de shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalación y registro de controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Crear un conector de búsqueda para un controlador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Depuración de controladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
