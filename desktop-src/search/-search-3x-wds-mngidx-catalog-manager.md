---
description: Las interfaces ISearchCatalogManager e ISearchCatalogManager2 proporcionan métodos para administrar un catálogo de búsqueda, como provocar la nueva indexación o establecer tiempos de espera.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Uso del Administrador de catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deffc748c504b056e9d3f92dc8dcb127b835bec6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363299"
---
# <a name="using-the-catalog-manager"></a>Uso del Administrador de catálogos

Las [**interfaces ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) proporcionan métodos para administrar un catálogo de búsqueda, como provocar la nueva indexación o establecer tiempos de espera. Aunque Windows Search usa actualmente solo un catálogo, esta interfaz se diseñó para ofrecer un mayor control para administrar varios catálogos de forma independiente. La interfaz administra el catálogo de las maneras siguientes:

- Acceso a otras interfaces: recuperación de otras interfaces relacionadas con la búsqueda requeridas por el Administrador del ámbito de rastreo, las notificaciones de cambio de datos y la [**interfaz ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)
- Contenido del catálogo: garantiza que los nuevos datos se indexe y que otras aplicaciones y componentes funcionen correctamente forzando una nueva indexación de todo el catálogo o parte del mismo o restableciendo todo el catálogo.
- Propiedades del catálogo: establecimiento de propiedades que determinan cómo el catálogo administra los tiempos de espera al conectarse a controladores de protocolo y cómo se tratan las marcas diacríticas en las búsquedas.
- Estado del catálogo: obtener información sobre el catálogo, incluido el estado, el tamaño y el estado de actividad actual.

Este tema se organiza de la siguiente manera:

- [Acceso a interfaces relacionadas](#accessing-related-interfaces)
- [Administración del contenido del catálogo](#managing-the-catalog-contents)
- [Administración del estado del catálogo](#managing-catalog-status)
- [Administración de propiedades de catálogo](#managing-catalog-properties)
- [Ejecución en modo con privilegios elevados](#running-in-elevated-mode)
- [Temas relacionados](#related-topics)

## <a name="accessing-related-interfaces"></a>Acceso a interfaces relacionadas

Algunas interfaces útiles de la plataforma Windows Search requieren una instancia del Administrador de catálogos para poder usarse. Para crear un Administrador de catálogos para un catálogo especificado, llame al [**método ISearchManager::GetCatalog.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) A continuación, se pueden usar los métodos del Administrador de catálogos para crear instancias y devolver interfaces basadas en el catálogo especificado.

| Método                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Obtiene una instancia de la [**interfaz ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para el catálogo actual, lo que le permite crear consultas fácilmente.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Obtiene una instancia de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para este catálogo de búsqueda, con el fin de permitir a los desarrolladores modificar el ámbito de rastreo del Windows Search Indexer.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Obtiene una instancia de la interfaz [**ISearchItemsChangedSink,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) que las aplicaciones cliente usan para notificar al indexador los cambios cuando el cliente quiere información de estado de indexación sobre el elemento para admitir notificaciones administradas por el proveedor. Vea [Notifying the Index of Changes (Notificación](-search-3x-wds-notifyingofchanges.md) del índice de cambios) para obtener más información. |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Obtiene una instancia de [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink), que las aplicaciones cliente usan para notificar al indexador los cambios cuando el cliente no quiere información de estado de indexación (notificaciones administradas por el indexador). Vea [Notifying the Index of Changes (Notificación](-search-3x-wds-notifyingofchanges.md) del índice de cambios) para obtener más información.            |

## <a name="managing-the-catalog-contents"></a>Administración del contenido del catálogo

Hay dos tareas principales implicadas en la administración del catálogo: volver a indexar todas o algunas de las direcciones URL del ámbito de rastreo del indexador y restablecer todo el catálogo subyacente. Al volver a indexar las direcciones URL, los datos antiguos permanecen en el catálogo hasta o a menos que se reemplazan por datos nuevos. Al restablecer el catálogo, se vuelve a generar todo el catálogo y se indexa de nuevo todas las direcciones URL del ámbito de rastreo. Este proceso puede tardar mucho tiempo y solo debe usarse como último recurso para resolver problemas como un índice posiblemente dañado.

Al instalar una nueva aplicación, controlador de protocolo o filtro, la aplicación de instalación debe agregar su directorio o raíz al ámbito de rastreo para asegurarse de que el indexador incluye la ubicación de los datos de esa aplicación. Si los datos no aparecen en el catálogo después de que el indexador haya rastreado su ámbito de rastreo, primero debe asegurarse de que la ubicación de los datos se incluye en el ámbito de rastreo. Puede agregarlo mediante la interfaz de usuario para las Windows search o el [Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md). Si la ubicación parece estar en el ámbito de rastreo, puede forzar manualmente una nueva indexación de todas las direcciones URL del ámbito de rastreo del indexador o de un subconjunto, mediante los métodos siguientes de la interfaz [**ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

| Volver a indexar el método                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager::Reindex**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Vuelva a indexar todas las direcciones URL del catálogo. La información antigua permanecerá hasta que se reemplazó por información nueva.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Vuelva a indexar las direcciones URL que coincidan con el patrón o comiencen en una raíz determinada (por ejemplo, file:///C: \\ Foldername \\ Subfoldername \\ ). Esto resulta útil para volver a buscar todo en un directorio determinado o con una extensión determinada, como cuando se instala una aplicación. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Indica al indexador que dé prioridad a los elementos de indexación con direcciones URL que coincidan con un patrón especificado antes de completar otras tareas de indexación.                                                                                                                                    |

**Restablecer el índice.** Puede restablecer todo el índice con una llamada a [**ISearchCatalogManager::Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset). Esto restablece el catálogo subyacente recompilando las bases de datos y realizando un índice completo de todas las direcciones URL del ámbito de rastreo. Este proceso puede tardar mucho tiempo y solo debe usarse como último recurso para resolver problemas como un índice posiblemente dañado.

> [!IMPORTANT]
> Debido a la ralentización en la indexación que pueden provocar estos métodos, se deben usar con cuidado al intentar identificar problemas de indexación o catálogo. En primer lugar, asegúrese de que las raíces de búsqueda y las reglas de ámbito se agregan en el Administrador del ámbito de rastreo y, a continuación, asegúrese de que el bit FANCI (Atributo de archivo no indizado por contenido) está configurado correctamente para archivos y carpetas. Si ha confirmado que son correctas, pruebe ReindexSearchRoot primero y Reindex last. Si ninguno de estos trabajos funciona, pruebe Restablecer como último recurso.

Para obtener información relacionada, vea [Notificar al índice de cambios](-search-3x-wds-notifyingofchanges.md)y Consultar el índice con [ISearchQueryHelper.](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Administración del estado del catálogo

El Administrador de catálogos se puede usar para obtener el estado del catálogo para las aplicaciones que desean personalizar cómo se administra el catálogo (por ejemplo, una aplicación personalizada de supervisión "Estado del catálogo"). Pero el Administrador de catálogos no suele ser necesario para la mayoría de los escenarios de desarrollo relacionados con la búsqueda. Los usos comunes serían para una aplicación de supervisión "Estado del catálogo" o una Panel de control de estilo de catálogo.

En la tabla siguiente se describen los métodos de ISearchCatalogManager usados para administrar el estado del catálogo.


| Método | Descripción | 
|--------|-------------|
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a> | Obtiene la dirección URL que se está indexando actualmente. Este método sería útil si estuviera intentando identificar si el indexador estaba "atascado" en un elemento. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a> | Obtiene el número de elementos del catálogo. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a> | Recupera la siguiente información sobre los elementos que se indexarán:<ul><li>plIncrementalCount: el número de elementos que se van a indexar en el siguiente índice incremental</li><li>plNotificationQueue: el número de elementos de la cola de notificaciones. Esta información sería útil para una aplicación de notificación que necesitaba comprobar si el indexador recibe las notificaciones que envía la aplicación.</li><li>plHighPriorityQueue: el número de elementos de la cola de prioridad alta. Los elementos de plHighPriorityQueue se indexan primero.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a> | Obtiene el estado del catálogo y devuelve un valor de enumeración que proporciona el estado actual. Los siguientes son los posibles estados del catálogo:<ul><li>Inactivo: no se necesita indexación.</li><li>En pausa: la indexación está en pausa (debido a una batería baja o a un uso elevado de la CPU, por ejemplo).</li><li>Recuperación: la indexación se está recuperando.</li><li>Rastreo completo: el indexador está realizando un rastreo completo del ámbito de rastreo.</li><li>Rastreo incremental: el indexador está realizando un rastreo incremental.</li><li>Procesamiento de notificaciones: el indexador está procesando notificaciones.</li><li>Apagar: el indexador se está cerrando.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a> | Obtiene el nombre del catálogo actual especificado en el <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>método ISearchManager::GetCatalog.</strong></a> Actualmente, el único catálogo admitido es SystemIndex. | 


## <a name="managing-catalog-properties"></a>Administración de propiedades de catálogo

Hay tres propiedades de catálogo que puede administrar con el Administrador de catálogos:

- **Sensibilidad diacrítica.** Los signos diacríticos son marcas de acento agregadas a las letras para indicar el significado o la pronunciación de una palabra. Esta propiedad determina si el catálogo es sensible a los signos diacríticos y es importante cuando usted o los usuarios buscan e indexa texto en varios idiomas. Por ejemplo, con esta propiedad establecida en **FALSE,** el catálogo trataría "resume" y "resumé" como si fueran la misma palabra.
- **Tiempos de espera de conexión.** Esta propiedad representa la cantidad de tiempo de espera de una respuesta de conexión de un servidor o almacén de datos, tal como se representa en una estructura [**TIMEOUT \_ INFO.**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) Puede usar esta propiedad para ajustar el Windows Search.
- **Tiempos de espera de datos** Esta propiedad representa la cantidad de tiempo que se espera para una transacción de datos entre el indexador y un controlador o filtro de protocolo, tal como se representa en una estructura [**TIMEOUT \_ INFO.**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) Si ha transcurrido este tiempo, el proceso del demonio de filtro finaliza para evitar interbloqueos y otros problemas de recursos.

Las dos últimas propiedades están pensadas principalmente para su uso futuro. Cada una de estas propiedades tiene los `get` `put` métodos y .

| Método                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**put \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE si el catálogo debe diferenciar palabras con signos diacríticos. **FALSE** si el catálogo debe omitir los signos diacríticos. El cambio de esta propiedad requiere volver a generar el índice porque las claves del índice pueden no ser válidas.                       |
| [**get \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**put \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | Tiempo, en segundos, que el indexador debe esperar una respuesta de conexión de un servidor o almacén de datos. Si se establece este valor demasiado alto, se pueden producir retrasos si muchos sitios no responden. Si se establece en un nivel demasiado bajo, algunos sitios no se rastrearán. |
| [**get \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**put \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | Tiempo, en segundos, que el indexador debe esperar una transacción de datos.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Ejecución en modo con privilegios elevados

Cualquier llamada de método que actualice SystemIndex requiere que la aplicación se ejecute con privilegios elevados. De lo contrario, se producirá un error de acceso denegado en la aplicación.

## <a name="related-topics"></a>Temas relacionados


[Administración del índice](-search-3x-wds-mngidx-overview.md)

[Interfaces para administrar el índice](interfaces-for-managing-the-index.md)

[Uso del Administrador de búsqueda](-search-3x-wds-mngidx-searchmanager.md)

[Uso del Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md)
