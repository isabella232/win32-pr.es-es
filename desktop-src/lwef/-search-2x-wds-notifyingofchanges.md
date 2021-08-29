---
title: Notificar al índice de cambios (características heredadas Windows entorno)
description: Con Microsoft Windows Desktop Search (WDS) 2.6, los controladores de protocolo de un almacén de datos determinado pueden decir al indexador WDS cuándo han cambiado los datos de su almacén.
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b52f192f8ee943ef3378e4a21a62702f4e12bc7bf5dfbd07ccc8a1093aab3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601765"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a>Notificar al índice de cambios (características heredadas Windows entorno)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Con Microsoft Windows Desktop Search (WDS) 2.6, los controladores de protocolo de un almacén de datos determinado pueden decir al indexador WDS cuándo han cambiado los datos de su almacén. Esto mejora el rendimiento al garantizar que el indexador no rastree todo el almacén en índices incrementales. Mediante las API de notificación, los controladores de protocolo pueden notificar al indexador que un elemento se ha movido o eliminado, y pueden agregar ámbitos a la cola de rastreo del indexador de WDS de direcciones URL que requieren indexación. La notificación es útil para aplicaciones como el correo electrónico, donde el controlador de protocolo supervisa el almacén y notifica al indexador que los elementos han cambiado y requieren indexación.

## <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Los controladores de protocolo notifican al indexador los cambios a través de [**la interfaz ISearchItemsChangedSink.**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) La información sobre los cambios de datos debe recopilarse en los structs SEARCH ITEM CHANGE y SEARCH KIND OF CHANGE enumeration types y, a continuación, comunicarse con el indexador a través del método OnItemsChanged de la interfaz \_ \_ \_ \_ \_ **ISearchItemsChangedSink.** 

Para acceder a esta interfaz, los controladores de protocolo personalizados deben crear primero una instancia de un objeto [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) para obtener acceso al [**objeto ISearchCatalogManager.**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) Desde allí, se puede crear una instancia de un [**objeto ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) y notificar al indexador los cambios de datos.

El método OnItemsChanged permite recopilar y comunicar los cambios de datos en el almacén de datos del cliente para iniciar la indexación.



| Dirección | Variable              | Descripción                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| En        | dwNumberofChanges     | Número total de cambios en la notificación.                             |
| En        | DataChangeEntries\[\] | Todas las notificaciones de cambios de una matriz de estructuras SEARCH \_ ITEM \_ CHANGE. |
| Fuera       | dwBatchId             | Identificador de lote que se pasará con errores.                       |
| Fuera       | hrCompletionCodes\[\] | Indica si se aceptó cada dirección URL para la indexación.                    |



 

La estructura SEARCH ITEM CHANGE identifica el tipo de cambio que se produjo, así como la dirección URL actual del elemento y la dirección \_ \_ URL anterior, si procede. La estructura se define de la siguiente manera:



| Nombre de la propiedad | Tipo de propiedad                  | Descripción                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| Change        | TIPO \_ DE CAMBIO DE \_ \_ BÚSQUEDA       | Tipo de cambio que se notifica.                                 |
| URL           | LPWSTR                         | Dirección URL del objeto que ha cambiado.                                   |
| OldURL        | LPWSTR                         | Si la notificación es un traslado, se proporciona la dirección URL anterior y debe ser única. |
| Prioridad      | PRIORIDAD \_ DE NOTIFICACIÓN DE \_ BÚSQUEDA | Prioridad del cambio.                                                |



 

La \_ enumeración SEARCH KIND \_ OF CHANGE se define de la siguiente \_ manera:



| Valor de enumeración                           | Valor   | Descripción                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| BUSCAR \_ CAMBIO \_ AGREGAR                  | 0       | La notificación es para una dirección URL adicional.                                                      |
| SEARCH \_ CHANGE \_ DELETE               | 1       | La notificación es para la eliminación de una dirección URL.                                                  |
| MODIFICAR \_ CAMBIO DE \_ BÚSQUEDA               | 2       | La notificación es que se ha modificado una dirección URL.                                               |
| CAMBIAR NOMBRE \_ DE CAMBIO \_ DE \_ BÚSQUEDA         | 3       | La notificación es para mover y cambiar el nombre de un objeto a una nueva dirección URL.                          |
| DIRECTORIO \_ DE SEMÁNTICA DE CAMBIO DE \_ \_ BÚSQUEDA | 0x10000 | La notificación es para una dirección URL de contenedor.                                                        |
| SEMÁNTICA \_ DE CAMBIO DE BÚSQUEDA \_ SUPERFICIAL \_   | 0x20000 | La notificación es para una dirección URL de contenedor que solo debe tener indexadas sus propiedades de contenedor. |
| SEGURIDAD \_ DE SEMÁNTICA DE CAMBIO DE \_ \_ BÚSQUEDA  | 0x40000 | La notificación es para una dirección URL o dirección URL de contenedor que ha cambiado sus propiedades de seguridad.    |



 

La \_ enumeración SEARCH NOTIFICATION PRIORITY se define de la siguiente \_ manera:



| Valor de enumeración               | Value | Descripción                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BUSCAR \_ PRIORIDAD NORMAL \_ | 0     | Solo se debe usar una prioridad normal al indexar la dirección URL. Estas notificaciones se procesan antes de la indexación incremental en segundo plano normal de los archivos y almacenes de un usuario. |



 

 

 
