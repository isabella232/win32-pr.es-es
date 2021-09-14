---
description: Las enumeraciones siguientes admiten la API de tabla de enrutamiento distribuido (DRT).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumeraciones de tablas de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073941"
---
# <a name="distributed-routing-table-enumerations"></a>Enumeraciones de tablas de enrutamiento distribuido

Las enumeraciones siguientes admiten la API de tabla de enrutamiento distribuido (DRT).



| Enumeración                                                            | Descripción                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ÁMBITO \_ DE DRT**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Define el conjunto de ámbitos IPv6 en los que drt funcionará cuando se use el transporte UDP de IPv6 creado por [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport). |
| [**MARCAS DE DIRECCIONES DE DRT \_ \_**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Define el conjunto de respuestas que puede devolver un nodo intermedio al realizar una búsqueda de una clave.                                                         |
| [**ESTADO \_ DE DRT**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Define los posibles estados de conectividad y error de un nodo local.                                                                                                   |
| [**TIPO DE COINCIDENCIA DE DRT \_ \_**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Define la exactitud de los resultados devueltos cuando se realiza una búsqueda.                                                                                                 |
| [**DRT \_ LEAFSET \_ KEY \_ CHANGE \_ TYPE**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Define el conjunto de tipos de cambio que se pueden realizar en un nodo de conjunto hoja local en la caché de DRT local.                                                                |
| [**TIPO DE EVENTO DRT \_ \_**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Define el conjunto de eventos que puede generar el DRT.                                                                                                              |
| [**MODO DE SEGURIDAD DE DRT \_ \_**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Define los posibles modos de seguridad del DRT. Esta enumeración es un campo de la [**estructura SETTINGS \_ de DRT.**](/windows/desktop/api/drt/ns-drt-drt_settings)                                   |
| [**ESTADO DE REGISTRO DE DRT \_ \_**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Define el estado de una clave registrada.                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estructuras de tabla de enrutamiento distribuido](distributed-routing-table-structures.md)
</dt> <dt>

[Funciones de tabla de enrutamiento distribuido](distributed-routing-table-functions.md)
</dt> <dt>

[Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



