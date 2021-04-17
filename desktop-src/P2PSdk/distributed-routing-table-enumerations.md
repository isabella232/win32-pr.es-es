---
description: Las enumeraciones siguientes admiten la API de tabla de enrutamiento distribuida (DRT).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumeraciones de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667446"
---
# <a name="distributed-routing-table-enumerations"></a>Enumeraciones de tabla de enrutamiento distribuido

Las enumeraciones siguientes admiten la API de tabla de enrutamiento distribuida (DRT).



| Enumeración                                                            | Descripción                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ámbito de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Define el conjunto de ámbitos IPv6 en el que la DRT funcionará cuando se use el transporte UDP de IPv6 creado por [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport). |
| [**\_marcas de dirección de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Define el conjunto de respuestas que puede devolver un nodo intermedio al realizar una búsqueda de una clave.                                                         |
| [**Estado de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Define los posibles estados de conectividad y error de un nodo local.                                                                                                   |
| [**\_tipo de coincidencia de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Define la exactitud de los resultados que se devuelven cuando se realiza una búsqueda.                                                                                                 |
| [**\_tipo de \_ cambio de clave de LEAFSET de DRT \_ \_**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Define el conjunto de tipos de cambios que se pueden realizar en un nodo de conjunto de hoja local en la caché de DRT local.                                                                |
| [**\_tipo de evento DRT \_**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Define el conjunto de eventos que puede generar la DRT.                                                                                                              |
| [**\_modo de seguridad de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Define los posibles modos de seguridad de DRT. Esta enumeración es un campo de la estructura de [**\_ configuración de DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .                                   |
| [**\_Estado de registro de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Define el estado de una clave registrada.                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estructuras de tabla de enrutamiento distribuido](distributed-routing-table-structures.md)
</dt> <dt>

[Funciones de tabla de enrutamiento distribuido](distributed-routing-table-functions.md)
</dt> <dt>

[Referencia de Table API de enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



