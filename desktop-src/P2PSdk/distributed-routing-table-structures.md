---
description: Las estructuras siguientes admiten las funciones de API de tabla de enrutamiento distribuido (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Estructuras de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7613b63559eadd2b19229228b9d57fb438b6bd2bbb1b5a9d335a6513c1e8bfee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978945"
---
# <a name="distributed-routing-table-structures"></a>Estructuras de tabla de enrutamiento distribuido

Las estructuras siguientes admiten las funciones de API de tabla de enrutamiento distribuido (DRT).



| Estructura                                                  | Descripción                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATOS DE \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Contiene un blob de datos. Varias funciones de DRT usan esta estructura.                                                                                                                   |
| [**REGISTRO DE \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Contiene el registro de claves. Este es un miembro de la estructura [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) y es un argumento pasado a [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey). |
| [**DIRECCIÓN DE \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Contiene información de punto de conexión sobre un nodo DRT que participó en una búsqueda. Esta información está pensada para su uso en la depuración de problemas de conectividad.                                   |
| [**LISTA DE DIRECCIONES \_ DE \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Contiene un conjunto de estructuras [**DRT \_ ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) que representan los nodos con los que se ha contactado durante una búsqueda de una clave.                                                             |
| [**PROVEEDOR DE SEGURIDAD \_ DE \_ DRT**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Define la interfaz que debe implementar un proveedor de seguridad.                                                                                                                   |
| [**PROVEEDOR DE ARRANQUE DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Define la interfaz que debe implementar un proveedor de arranque.                                                                                                                  |
| [**CONFIGURACIÓN DE \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Define la configuración de DRT durante la inicialización. Esta estructura se pasa como argumento a [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).                                                                           |
| [**INFORMACIÓN DE BÚSQUEDA DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Define una consulta de búsqueda. Esta estructura se pasa como argumento a [**DrtStartSearch.**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                                                                             |
| [**RESULTADO DE LA BÚSQUEDA DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Contiene un resultado de búsqueda. [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)devuelve esta estructura.                                                                                |
| [**DATOS DE EVENTOS DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Contiene los datos de evento devueltos mediante una llamada [**a DrtGetEventData después**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) de que una aplicación reciba una señal de evento.                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeraciones de tabla de enrutamiento distribuido](distributed-routing-table-enumerations.md)
</dt> <dt>

[Funciones de tabla de enrutamiento distribuido](distributed-routing-table-functions.md)
</dt> <dt>

[Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



