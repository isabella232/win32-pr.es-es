---
title: Notificar el índice de cambios (características heredadas del entorno de Windows)
description: Con Microsoft Windows Desktop Search (WDS) 2,6, los controladores de protocolo para un almacén de datos determinado pueden indicar al indexador de WDS Cuándo han cambiado los datos de su almacén.
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021cfe5cd7061a3d3255e56d08e665a6caedf03
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104274506"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a>Notificar el índice de cambios (características heredadas del entorno de Windows)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Con Microsoft Windows Desktop Search (WDS) 2,6, los controladores de protocolo para un almacén de datos determinado pueden indicar al indexador de WDS Cuándo han cambiado los datos de su almacén. Esto mejora el rendimiento, ya que garantiza que el indexador no rastrea todo el almacén en los índices incrementales. Con las API de notificación, los controladores de protocolo pueden notificar al indizador que un elemento se ha cambiado o eliminado, y pueden agregar ámbitos a la cola de rastreo de las direcciones URL que requieren indexación. La notificación es útil para aplicaciones como el correo electrónico, donde el controlador de protocolo supervisa el almacén y notifica al indexador que los elementos han cambiado y requieren indexación.

## <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Los controladores de protocolo notifican al indexador los cambios a través de la interfaz [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) . La información sobre los cambios de datos se debe recopilar en los \_ \_ Structs de cambio de elementos de búsqueda y en el \_ tipo \_ de búsqueda de \_ tipos de enumeración de cambios y, a continuación, comunicarse con el indizador mediante el método **OnItemsChanged** de la interfaz **ISearchItemsChangedSink** .

Para tener acceso a esta interfaz, los controladores de protocolo personalizados primero deben crear instancias de un objeto [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) para obtener acceso al objeto [**ISearchCatalogManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) . Desde allí, se pueden crear instancias de un objeto [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) y notificar al indexador los cambios de los datos.

El método OnItemsChanged permite recopilar y comunicar los cambios de datos en el almacén de datos del cliente para iniciar la indexación.



| Dirección | Variable              | Descripción                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| En        | dwNumberofChanges     | Número total de cambios en la notificación.                             |
| En        | DataChangeEntries\[\] | Todas las notificaciones de cambios en una matriz de elementos de búsqueda \_ \_ cambian estructuras. |
| Fuera       | dwBatchId             | IDENTIFICADOR del lote que se devolverá con errores.                       |
| Fuera       | hrCompletionCodes\[\] | Indica si se aceptó cada dirección URL para la indización.                    |



 

La \_ \_ estructura de cambio del elemento de búsqueda identifica el tipo de cambio que se ha producido, así como la dirección URL actual del elemento y la dirección URL anterior, si procede. La estructura se define de la siguiente manera:



| Nombre de la propiedad | Tipo de propiedad                  | Descripción                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| Cambio        | \_tipo \_ de búsqueda de \_ cambio       | El tipo de cambio que se notifica.                                 |
| URL           | LPWSTR                         | Dirección URL del objeto que ha cambiado.                                   |
| OldURL        | LPWSTR                         | Si la notificación es un movimiento, se proporciona la dirección URL anterior y debe ser única. |
| Prioridad      | prioridad de la notificación de búsqueda \_ \_ | Prioridad del cambio.                                                |



 

El \_ tipo \_ de búsqueda de la \_ enumeración de cambios se define de la siguiente manera:



| Valor de enumeración                           | Value   | Descripción                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| BUSCAR \_ cambiar \_ Agregar                  | 0       | La notificación es para una dirección URL adicional.                                                      |
| BUSCAR \_ cambiar \_ eliminar               | 1       | La notificación es para la eliminación de una dirección URL.                                                  |
| BUSCAR \_ cambiar \_ modificar               | 2       | La notificación es que se ha modificado una dirección URL.                                               |
| \_cambiar nombre de cambio de búsqueda \_ \_         | 3       | La notificación es para el movimiento y el cambio de nombre de un objeto a una nueva dirección URL.                          |
| Buscar en el directorio de semántica de \_ cambios \_ \_ | 0x10000 | La notificación es para una dirección URL de contenedor.                                                        |
| semántica de cambio de búsqueda \_ \_ \_ superficial   | 0x20000 | La notificación es para una dirección URL de contenedor que solo debe tener indizadas sus propiedades de contenedor. |
| seguridad de la semántica de cambios de búsqueda \_ \_ \_  | 0x40000 | La notificación es para una dirección URL o un contenedor que ha cambiado sus propiedades de seguridad.    |



 

La \_ enumeración prioridad de notificación de búsqueda \_ se define de la siguiente manera:



| Valor de enumeración               | Value | Descripción                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_prioridad normal de búsqueda \_ | 0     | Solo se debe usar una prioridad normal al indizar la dirección URL. Estas notificaciones se procesan antes de la indización incremental en segundo plano normal de los archivos y almacenes de un usuario. |



 

 

 
