---
description: Las interfaces ISearchCatalogManager y ISearchCatalogManager2 proporcionan métodos para administrar un catálogo de búsqueda, como hacer que se vuelvan a indexar o establecer tiempos de espera.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Usar el administrador de catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1295cc9cc76fb334b4687b876fa1959a22e33235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677307"
---
# <a name="using-the-catalog-manager"></a>Usar el administrador de catálogos

Las interfaces [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) y [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) proporcionan métodos para administrar un catálogo de búsqueda, como hacer que se vuelvan a indexar o establecer tiempos de espera. Aunque Windows Search solo usa un catálogo, esta interfaz se diseñó para proporcionar un mayor control sobre la administración de varios catálogos de forma independiente. La interfaz administra el catálogo de las maneras siguientes:

- Acceso a otras interfaces: recuperación de otras interfaces relacionadas con la búsqueda requeridas por el administrador de ámbito de rastreo, las notificaciones de cambio de datos y la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .
- Contenido del catálogo: asegurarse de que los nuevos datos se indizan y que otras aplicaciones y componentes funcionan correctamente forzando una reindexación de todo o parte del catálogo o restableciendo todo el catálogo.
- Propiedades del catálogo: establecer propiedades que determinan cómo administra el catálogo los tiempos de espera al conectarse a los controladores de protocolo y cómo se tratan las marcas diacríticas en las búsquedas.
- Estado del catálogo: obtener información sobre el catálogo, incluidos el estado, el tamaño y el estado de la actividad actual.

Este tema se organiza de la siguiente manera:

- [Acceso a interfaces relacionadas](#accessing-related-interfaces)
- [Administrar el contenido del catálogo](#managing-the-catalog-contents)
- [Administrar el estado del catálogo](#managing-catalog-status)
- [Administrar propiedades del catálogo](#managing-catalog-properties)
- [Ejecutar en modo elevado](#running-in-elevated-mode)
- [Temas relacionados](#related-topics)

## <a name="accessing-related-interfaces"></a>Acceso a interfaces relacionadas

Algunas interfaces útiles en la plataforma de Windows Search requieren una instancia del administrador de catálogos para poder usarse. Para crear un administrador de catálogo para un catálogo especificado, llame al método [**ISearchManager:: GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) . Los métodos del administrador de catálogo se pueden usar para crear instancias y devolver interfaces basadas en el catálogo especificado.

| Método                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Obtiene una instancia de la interfaz [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para el catálogo actual, para permitirle crear consultas fácilmente.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Obtiene una instancia de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para este catálogo de búsqueda, para permitir que los desarrolladores modifiquen el ámbito de rastreo del indizador de Windows Search.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Obtiene una instancia de la interfaz [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) , que las aplicaciones cliente utilizan para notificar a los cambios del indexador cuando el cliente desea información de estado de la indización sobre el elemento para admitir las notificaciones administradas por el proveedor. Consulte [notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md) para obtener más información. |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Obtiene una instancia de [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink), que las aplicaciones cliente utilizan para notificar a los cambios del indexador cuando el cliente no desea información de estado de la indización (notificaciones administradas por el indizador). Consulte [notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md) para obtener más información.            |

## <a name="managing-the-catalog-contents"></a>Administrar el contenido del catálogo

Hay dos tareas principales relacionadas con la administración del catálogo: volver a indexar todas o algunas de las direcciones URL en el ámbito de rastreo del indexador y restablecer todo el catálogo subyacente. Cuando se vuelven a indizar las direcciones URL, los datos antiguos permanecen en el catálogo hasta que se reemplazan por los nuevos datos. Al restablecer el catálogo, se vuelve a generar todo el catálogo y todas las direcciones URL del ámbito de rastreo se vuelven a indizar. Este proceso puede tardar mucho tiempo y solo debe usarse como último recurso para solucionar problemas, como un índice posiblemente dañado.

Al instalar una nueva aplicación, controlador de protocolo o filtro, la aplicación de instalación debe agregar su directorio o raíz al ámbito de rastreo para asegurarse de que el indexador incluye la ubicación de los datos de la aplicación. Si los datos no aparecen en el catálogo después de que el indizador haya rastreado su ámbito de rastreo, primero debe asegurarse de que la ubicación de los datos está incluida en el ámbito de rastreo. Puede agregarlo mediante la interfaz de usuario para las opciones de búsqueda de Windows o el [Administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md). Si la ubicación parece estar en el ámbito de rastreo, puede forzar manualmente una reindización de todas las direcciones URL en el ámbito de rastreo del indexador o en un subconjunto, mediante los siguientes métodos de la interfaz [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .

| Volver a indizar el método                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager:: REINDEX**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Vuelve a indexar todas las direcciones URL en el catálogo. La información anterior se conservará hasta que se reemplace por nueva información.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Vuelve a indexar las direcciones URL que coinciden con el patrón o se inician en una raíz determinada (por ejemplo, file:///C: \\ nombreDeCarpeta \\ Subfoldername \\ ). Esto resulta útil para volver a rastrear todo en un directorio determinado o con una extensión determinada, como cuando se instala una aplicación. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Indica al indizador que dé prioridad a los elementos de indización con direcciones URL que coincidan con un patrón especificado sobre la finalización de otras tareas de indización.                                                                                                                                    |

**Restableciendo el índice.** Puede restablecer todo el índice con una llamada a [**ISearchCatalogManager:: RESET**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset). Esto restablece el catálogo subyacente mediante la regeneración de las bases de datos y la realización de un índice completo de todas las direcciones URL en el ámbito de rastreo. Este proceso puede tardar mucho tiempo y solo debe usarse como último recurso para solucionar problemas, como un índice posiblemente dañado.

> [!IMPORTANT]
> Debido a la ralentización de la indización que pueden causar estos métodos, deben usarse con cuidado cuando intente identificar problemas de catálogo o de indexación. En primer lugar, asegúrese de que las reglas de ámbito y las raíces de búsqueda se han agregado en el administrador de ámbito de rastreo y, a continuación, asegúrese de que el bit FANCI (atributo de archivo no indizado de contenido) está establecido correctamente para los archivos y las carpetas. Si ha confirmado que son correctos, pruebe ReindexSearchRoot primero y vuelva a indexar en último lugar. Si ninguno de estos trabajos, intente restablecer como último recurso.

Para obtener información relacionada, vea [notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md)y [consultar el índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Administrar el estado del catálogo

El administrador de catálogos se puede usar para obtener el estado del catálogo de las aplicaciones que quieren personalizar cómo se administra el catálogo (por ejemplo, una aplicación de supervisión "estado del catálogo" personalizada). Pero el administrador de catálogos no suele ser necesario para la mayoría de los escenarios de desarrollo relacionados con búsquedas. Los usos comunes serían una aplicación de supervisión de "estado del catálogo" o una aplicación de estilo del panel de control.

En la tabla siguiente se describen los métodos de ISearchCatalogManager que se usan para administrar el estado del catálogo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a></td>
<td>Obtiene la dirección URL que se está indizando actualmente. Este método sería útil si intentara identificar si el indexador estaba &quot; atascado &quot; en un elemento.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>Númerodeelementos</strong></a></td>
<td>Obtiene el número de elementos del catálogo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a></td>
<td>Recupera la siguiente información acerca de los elementos que se van a indizar:
<ul>
<li>plIncrementalCount: número de elementos que se van a indizar en el siguiente Índice incremental</li>
<li>plNotificationQueue: el número de elementos de la cola de notificaciones. Esta información sería útil para una aplicación de notificación que necesitaba comprobar si el indexador está recibiendo las notificaciones que la aplicación está enviando.</li>
<li>plHighPriorityQueue: el número de elementos de la cola de prioridad alta. Los elementos de plHighPriorityQueue se indexan en primer lugar.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a></td>
<td>Obtiene el estado del catálogo y devuelve un valor de enumeración que proporciona el estado actual. A continuación se indican los posibles estados del catálogo:
<ul>
<li>Idle: no se necesita ninguna indexación.</li>
<li>En pausa: la indexación está en pausa (por ejemplo, debido a una batería baja o un uso elevado de la CPU).</li>
<li>Recuperación: la indexación se está recuperando.</li>
<li>Rastreo completo: Indexer está realizando un rastreo completo del ámbito de rastreo.</li>
<li>Rastreo incremental: Indexer realiza un rastreo incremental.</li>
<li>Procesando notificaciones: indexador está procesando notificaciones.</li>
<li>Cerrando: el indexador se está cerrando.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a></td>
<td>Obtiene el nombre del catálogo actual que se especifica en el método <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>ISearchManager:: GetCatalog</strong></a> . Actualmente, el único Catálogo admitido es SystemIndex.</td>
</tr>
</tbody>
</table>

## <a name="managing-catalog-properties"></a>Administrar propiedades del catálogo

Existen tres propiedades de catálogo que se pueden administrar con el administrador de catálogos:

- **Sensibilidad diacrítica.** Los signos diacríticos son signos de acento agregados a las letras para indicar el significado o la Pronunciación de una palabra. Esta propiedad determina si el catálogo es sensible a los signos diacríticos y es importante cuando usted o sus usuarios buscan e indexan texto en varios idiomas. Por ejemplo, con esta propiedad establecida en **false**, el catálogo trataría "resume" y "resumé" como si fueran la misma palabra.
- **Tiempos de espera de conexión.** Esta propiedad representa la cantidad de tiempo de espera para una respuesta de conexión de un servidor o un almacén de datos, como se representa en una estructura de [**\_ información de tiempo de espera**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . Puede usar esta propiedad para ajustar la búsqueda de Windows.
- **Tiempos de espera de datos** Esta propiedad representa la cantidad de tiempo de espera para una transacción de datos entre el indexador y un controlador o filtro de protocolo, como se representa en una estructura de [**\_ información de tiempo de espera**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . Si este tiempo ha transcurrido, el proceso del demonio de filtro se termina para evitar el interbloqueo y otros problemas de recursos.

Las dos últimas propiedades están pensadas principalmente para un uso futuro. Cada una de estas propiedades `get` tiene `put` métodos y.

| Método                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**Put \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE si el catálogo debe diferenciar las palabras con signos diacríticos. **False** si el catálogo debe omitir los signos diacríticos. Para cambiar esta propiedad, es necesario volver a generar el índice porque es posible que las claves del índice dejen de ser válidas.                       |
| [**obtener \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**Put \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | Tiempo, en segundos, que el indizador debe esperar una respuesta de conexión de un servidor o un almacén de datos. Si se establece en un valor demasiado alto, se pueden producir retrasos si muchos sitios no responden. Si se establece en un valor demasiado bajo, es posible que algunos sitios no se rastreen. |
| [**obtener \_ tiempo de espera**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**poner \_ tiempo de espera**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | Tiempo, en segundos, que el indizador debe esperar una transacción de datos.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Ejecutar en modo elevado

Cualquier llamada al método que actualice SystemIndex requiere que la aplicación se ejecute con privilegios elevados. De lo contrario, se producirá un error de acceso denegado en la aplicación.

## <a name="related-topics"></a>Temas relacionados


[Administración del índice](-search-3x-wds-mngidx-overview.md)

[Interfaces para administrar el índice](interfaces-for-managing-the-index.md)

[Usar el administrador de búsqueda](-search-3x-wds-mngidx-searchmanager.md)

[Usar el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md)
