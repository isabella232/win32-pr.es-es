---
description: Proceso de notificaciones en Windows Search
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Proceso de notificaciones en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b37747d1ec13c3a4a865e16721c64d4a0186dbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089823"
---
# <a name="notifications-process-in-windows-search"></a>Proceso de notificaciones en Windows Search

Este tema se organiza de la siguiente manera:

-   [Información general del proceso de notificaciones](#overview-of-the-notifications-process)
-   [Arrastra](#crawls)
-   [Notificaciones administradas por indexador](#indexer-managed-notifications)
-   [Notificaciones administradas por el proveedor](#provider-managed-notifications)
-   [Notificaciones en conjuntos de filas](#notifications-on-rowsets)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Información general del proceso de notificaciones

Hay tres enfoques por los que se pueden indexar los datos del almacén de datos:

-   Arrastra
-   Notificaciones administradas por el indexador
-   Notificaciones administradas por el proveedor

Los fundamentos de cada enfoque se describen en las secciones siguientes.

## <a name="crawls"></a>Arrastra

Los orígenes habilitados para notificaciones hacen un rastreo incremental en el inicio y, a continuación, se basan en notificaciones o en un comando explícito para rastrear de nuevo. Esto sucede automáticamente en Windows Vista y versiones posteriores. En sistemas operativos anteriores a Windows Vista, debe configurar [](../taskschd/task-scheduler-start-page.md) un evento programado en el Programador de tareas que llame al código para iniciar un rastreo a través de las páginas de inicio. No es necesario implementar ningún tipo de notificación. Como proceso en segundo plano, el indexador recorre su ámbito de rastreo, buscando cambios y actualizando el catálogo. Esta opción se recomienda para casi todas las situaciones.

## <a name="indexer-managed-notifications"></a>Indexer-Managed notificaciones

Con las notificaciones administradas por el indexador, implementa una estrategia de notificación que notifica al indexador cuándo han cambiado los datos del almacén de datos y el indexador administra el seguimiento de las notificaciones y la indexación de los datos. En esta situación, el componente (al que llamaremos proveedor de notificaciones) supervisa el almacén de datos, recopila información sobre los cambios en el almacén y, a continuación, notifica periódicamente al indexador una lista de elementos que necesitan indexación. El indexador es responsable de recuperar y resolver las notificaciones en caso de error. Esta opción, que se puede pensar como la estrategia "enviarla y olvidarla", reduce la frecuencia de rastreos del indexador.

## <a name="provider-managed-notifications"></a>Provider-Managed notificaciones

Con las notificaciones administradas por el proveedor, implementa una estrategia de notificación similar al segundo enfoque, salvo que el proveedor de notificaciones debe realizar un seguimiento de las notificaciones y es responsable de recuperar y resolver las notificaciones en caso de error. En esta situación, el proveedor de notificaciones supervisa el almacén de datos, recopila y mantiene información sobre los cambios en el almacén, notifica periódicamente al indexador con una lista de elementos que necesitan indexación, recibe actualizaciones de estado del indexador y vuelve a enviar notificaciones en caso de error.

> [!Note]  
> Esta opción no **se** recomienda a menos que espere que los rastreos incrementales del almacén de datos dificulten significativamente el rendimiento y requiera un control granular sobre el estado de indexación o una visión detallada del estado de indexación.

 

## <a name="notifications-on-rowsets"></a>Notificaciones en conjuntos de filas

En Windows 7 y versiones posteriores, la indexación de eventos permite a los proveedores recibir notificaciones sobre sus conjuntos de filas. Los proveedores que usan la indexación de eventos pueden mantener sus conjuntos de filas de una manera similar al comportamiento de las ubicaciones reales del sistema de archivos. Las bibliotecas y las búsquedas son los ejemplos principales de ubicaciones que no son del sistema de archivos en Windows 7. Los eventos de indexador son para las vistas de biblioteca, ya que las notificaciones son para vistas de carpeta de archivos. La [**interfaz IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) debe implementarse para recibir notificaciones de eventos. La capa de datos es el cliente principal de los eventos del indexador y decide qué hacer con los eventos en la interfaz de usuario de la vista elementos. Para obtener más información, [vea Indexing Prioritization and Rowset Events in Windows 7](indexing-prioritization-and-rowset-events.md).

Por el contrario, en Windows Vista, las vistas basadas en consultas no tienen eventos asociados, excepto para la caché de Shell para las ediciones de propiedades de archivo. Al realizar una búsqueda, los resultados que se devuelven son estáticos. Por lo tanto, si se agrega otro documento al sistema que coincida con el término de búsqueda, la vista no se actualiza para incluir la nueva adición. Este comportamiento es estándar para los resultados estáticos basados en web. Sin embargo, los resultados estáticos son menos aceptables cuando se intenta proporcionar una vista basada en consultas sobre una ubicación de almacenamiento. Los usuarios esperan que el contenido del indexador esté actual. Para obtener más información, vea [Notifying the Index of Changes](-search-3x-wds-notifyingofchanges.md). Para obtener documentación de referencia, vea [Interfaces de notificaciones](-search-notifications-interfaces-entry-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexación, consulta y notificaciones en Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Qué se incluye en el índice](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de indexación en Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Proceso de consulta en Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Requisitos de formato de dirección URL](url-formatting-requirements.md)
</dt> </dl>

 

 
