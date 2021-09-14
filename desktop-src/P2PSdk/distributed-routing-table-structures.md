---
description: Las estructuras siguientes admiten las funciones de API de tabla de enrutamiento distribuido (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Estructuras de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073928"
---
# <a name="distributed-routing-table-structures"></a>Estructuras de tabla de enrutamiento distribuido

Las estructuras siguientes admiten las funciones de API de tabla de enrutamiento distribuido (DRT).



| Estructura                                                  | Descripción                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRT \_ DATA**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Contiene un blob de datos. Varias funciones drt usan esta estructura.                                                                                                                   |
| [**REGISTRO \_ DE DRT**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Contiene el registro de claves. Se trata de un miembro de la estructura [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) y es un argumento pasado a [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey). |
| [**DIRECCIÓN \_ DE DRT**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Contiene información de punto de conexión sobre un nodo DRT que participó en una búsqueda. Esta información está pensada para su uso en la depuración de problemas de conectividad.                                   |
| [**LISTA DE DIRECCIONES DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Contiene un conjunto de estructuras [**DRT \_ ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) que representan los nodos a los que se ha contactado durante una búsqueda de una clave.                                                             |
| [**PROVEEDOR DE SEGURIDAD DE DRT \_ \_**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Define la interfaz que debe implementar un proveedor de seguridad.                                                                                                                   |
| [**PROVEEDOR DE ARRANQUE DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Define la interfaz que debe implementar un proveedor de arranque.                                                                                                                  |
| [**CONFIGURACIÓN \_ DE DRT**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Define la configuración de DRT durante la inicialización. Esta estructura se pasa como argumento a [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).                                                                           |
| [**INFORMACIÓN DE BÚSQUEDA DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Define una consulta de búsqueda. Esta estructura se pasa como argumento a [**DrtStartSearch.**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                                                                             |
| [**RESULTADO DE LA BÚSQUEDA DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Contiene un resultado de búsqueda. [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)devuelve esta estructura.                                                                                |
| [**DATOS DE EVENTOS DE DRT \_ \_**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Contiene los datos de evento devueltos mediante una llamada [**a DrtGetEventData después**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) de que una aplicación reciba una señal de evento.                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeraciones de tablas de enrutamiento distribuido](distributed-routing-table-enumerations.md)
</dt> <dt>

[Funciones de tabla de enrutamiento distribuido](distributed-routing-table-functions.md)
</dt> <dt>

[Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



