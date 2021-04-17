---
description: Las siguientes estructuras admiten las funciones de la API de la tabla de enrutamiento distribuida (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Estructuras de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667443"
---
# <a name="distributed-routing-table-structures"></a>Estructuras de tabla de enrutamiento distribuido

Las siguientes estructuras admiten las funciones de la API de la tabla de enrutamiento distribuida (DRT).



| Estructura                                                  | Descripción                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**datos de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Contiene un BLOB de datos. Varias funciones DRT utilizan esta estructura.                                                                                                                   |
| [**registro de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Contiene el registro de claves. Este es un miembro de la estructura del [**\_ \_ resultado**](/windows/desktop/api/drt/ns-drt-drt_search_result) de la búsqueda de DRT y es un argumento pasado a [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey). |
| [**Dirección de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Contiene información de extremo sobre un nodo DRT que participó en una búsqueda. Esta información está pensada para su uso en la depuración de problemas de conectividad.                                   |
| [**\_lista de direcciones de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Contiene un conjunto de estructuras de [**\_ direcciones de DRT**](/windows/desktop/api/drt/ns-drt-drt_address) que representan los nodos a los que se pone en contacto durante una búsqueda de una clave.                                                             |
| [**\_proveedor de seguridad de DRT \_**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Define la interfaz que debe ser implementada por un proveedor de seguridad.                                                                                                                   |
| [**\_proveedor de arranque de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Define la interfaz que debe ser implementada por un proveedor de arranque.                                                                                                                  |
| [**configuración de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Define la configuración de DRT en la inicialización. Esta estructura se pasa como argumento a [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).                                                                           |
| [**\_información de búsqueda de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Define una consulta de búsqueda. Esta estructura se pasa como argumento a [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).                                                                             |
| [**resultado de la búsqueda de DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Contiene un resultado de la búsqueda. [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)devuelve esta estructura.                                                                                |
| [**\_datos de eventos de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Contiene los datos de evento devueltos mediante una llamada a [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) después de que una aplicación reciba una señal de evento.                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeraciones de tabla de enrutamiento distribuido](distributed-routing-table-enumerations.md)
</dt> <dt>

[Funciones de tabla de enrutamiento distribuido](distributed-routing-table-functions.md)
</dt> <dt>

[Referencia de Table API de enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



