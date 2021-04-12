---
description: .
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Proceso de notificaciones en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7dd37979eab7ef32a5a8917ba6a3589e976105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153980"
---
# <a name="notifications-process-in-windows-search"></a>Proceso de notificaciones en Windows Search

Este tema se organiza de la siguiente manera:

-   [Información general del proceso de notificaciones](#overview-of-the-notifications-process)
-   [Los rastreos](#crawls)
-   [Notificaciones administradas por el indexador](#indexer-managed-notifications)
-   [Notificaciones administradas por el proveedor](#provider-managed-notifications)
-   [Notificaciones en conjuntos de filas](#notifications-on-rowsets)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Información general del proceso de notificaciones

Existen tres enfoques por los que se pueden indizar los datos del almacén de datos:

-   Los rastreos
-   Notificaciones administradas por el indexador
-   Notificaciones administradas por el proveedor

Las ventajas de cada enfoque se describen en las secciones siguientes.

## <a name="crawls"></a>Los rastreos

Los orígenes habilitados para notificaciones realizan un rastreo incremental al iniciarse y, a continuación, dependen de las notificaciones o un comando explícito para volver a rastrear. Esto sucede automáticamente en Windows Vista y versiones posteriores. En los sistemas operativos anteriores a Windows Vista, debe configurar un evento programado en el [programador de tareas](../taskschd/task-scheduler-start-page.md) que llama al código para iniciar un rastreo en las páginas de inicio. No es necesario implementar ninguna forma de notificaciones. Como proceso en segundo plano, el indexador atraviesa su ámbito de rastreo, buscando cambios y actualizando el catálogo. Esta opción se recomienda para casi todas las situaciones.

## <a name="indexer-managed-notifications"></a>Notificaciones de Indexer-Managed

Con las notificaciones administradas por indexador, se implementa una estrategia de notificación que notifica al indexador Cuándo han cambiado los datos en el almacén de datos y el indexador administra el seguimiento de las notificaciones y la indexación de los datos. En esta situación, el componente (que llamaremos un proveedor de notificaciones) supervisa el almacén de datos, recopila información sobre los cambios en el almacén y, a continuación, notifica periódicamente al indexador con una lista de elementos que necesitan indexación. El indexador es responsable de recuperar y resolver las notificaciones en caso de error. Esta opción, que puede considerar como la estrategia "enviarla y olvidarse", reduce la frecuencia de los rastreos del indexador.

## <a name="provider-managed-notifications"></a>Notificaciones de Provider-Managed

Con las notificaciones administradas por el proveedor, se implementa una estrategia de notificación similar al segundo enfoque, salvo que el proveedor de notificaciones debe realizar un seguimiento de las notificaciones y es responsable de recuperar y resolver las notificaciones en caso de error. En esta situación, el proveedor de notificaciones supervisa el almacén de datos, recopila y mantiene información sobre los cambios en el almacén, lo notifica periódicamente al indexador con una lista de elementos que necesitan indexación, recibe actualizaciones de estado del indexador y vuelve a enviar las notificaciones en caso de error.

> [!Note]  
> No se recomienda esta opción **a menos** que se espere que los rastreos incrementales del almacén de datos afecten significativamente al rendimiento, y se requiere un control granular sobre el estado de la indización o la información sobre él.

 

## <a name="notifications-on-rowsets"></a>Notificaciones en conjuntos de filas

En Windows 7 y versiones posteriores, la indización de eventos permite a los proveedores recibir notificaciones sobre sus conjuntos de filas. Los proveedores que utilizan los eventos de indización pueden mantener sus conjuntos de filas de forma similar al comportamiento de las ubicaciones reales del sistema de archivos. Las bibliotecas y las búsquedas son los principales ejemplos de ubicaciones que no son del sistema de archivos en Windows 7. Los eventos de indexador son las vistas de biblioteca, ya que las notificaciones son para las vistas de carpeta de archivos. La interfaz [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) se debe implementar para recibir notificaciones de eventos. El nivel de datos es el cliente principal de los eventos del indexador y decide qué hacer con los eventos en la interfaz de usuario de la vista elementos. Para obtener más información, consulte [Indexing Priority and Rowset Events in Windows 7](indexing-prioritization-and-rowset-events.md).

En cambio, en Windows Vista, las vistas basadas en consultas no tienen ningún evento asociado, salvo la caché de Shell para las ediciones de propiedades de archivo. Al realizar una búsqueda, los resultados que se devuelven son estáticos. Por lo tanto, si se agrega otro documento al sistema que coincida con el término de búsqueda, la vista no se actualiza para incluir la nueva adición. Este comportamiento es estándar para los resultados estáticos basados en Web. Sin embargo, los resultados estáticos son menos aceptables cuando se intenta proporcionar una vista basada en consultas a través de una ubicación de almacenamiento. Los usuarios esperan que el contenido del indexador sea el actual. Para obtener más información, consulte [notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md). Para obtener documentación de referencia, consulte [interfaces de notificaciones](-search-notifications-interfaces-entry-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexación, consulta y notificaciones en Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Qué se incluye en el índice](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de indexación en Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Consulta del proceso en Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Requisitos de formato de dirección URL](url-formatting-requirements.md)
</dt> </dl>

 

 
