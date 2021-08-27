---
description: Representa los tipos de direcciones de red. Use una o varias (como combinación bit a bit) de las constantes siguientes para crear una máscara de dirección de red que se usará con la macro NetAddr \_ SetAllowType.
title: NET_STRING (Iphlpapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4144dac9-772c-49cb-b924-e852fb4c81c7
api_name:
- NET_STRING_IPV4_ADDRESS
- NET_STRING_IPV4_SERVICE
- NET_STRING_IPV4_NETWORK
- NET_STRING_IPV6_ADDRESS
- NET_STRING_IPV6_ADDRESS_NO_SCOPE
- NET_STRING_IPV6_SERVICE
- NET_STRING_IPV6_SERVICE_NO_SCOPE
- NET_STRING_IPV6_NETWORK
- NET_STRING_NAMED_ADDRESS
- NET_STRING_NAMED_SERVICE
- NET_STRING_IP_ADDRESS
- NET_STRING_IP_ADDRESS_NO_SCOPE
- NET_STRING_IP_SERVICE
- NET_STRING_IP_SERVICE_NO_SCOPE
- NET_STRING_IP_NETWORK
- NET_STRING_ANY_ADDRESS
- NET_STRING_ANY_ADDRESS_NO_SCOPE
- NET_STRING_ANY_SERVICE
- NET_STRING_ANY_SERVICE_NO_SCOPE
api_type:
- HeaderDef
api_location:
- Iphlpapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a7d1a09e6165e77ee5419da47419a65e3995ce0ffedb8a6fb71f01fb9c63dde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111225"
---
# <a name="net_string"></a>CADENA \_ DE RED

Representa los tipos de direcciones de red. Use una o varias (como combinación bit a bit) de las constantes siguientes para crear una máscara de dirección de red que se usará con la macro [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Constante                                                                                                                                                                                                                   | Descripción                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**DIRECCIÓN \_ IPV4 DE CADENA \_ DE \_ NET**</dt> </dl>                              | La cadena identifica un host o enrutador IPv4 mediante una dirección literal (puerto o prefijo no permitido).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**SERVICIO NET \_ STRING \_ IPV4 \_**</dt> </dl>                              | La cadena identifica un servicio IPv4 mediante una dirección literal (puerto necesario; prefijo no permitido).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ NETWORK**</dt> </dl>                              | La cadena identifica una red IPv4 (prefijo necesario; puerto no permitido).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**DIRECCIÓN \_ \_ IPV6 DE CADENA \_ DE NET**</dt> </dl>                              | La cadena identifica un host o enrutador IPv6 mediante una dirección literal (puerto o prefijo no permitido; scope-id permitido).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl> | La cadena identifica un host o enrutador IPv6 mediante una dirección literal en la que el contexto de la interfaz ya se conoce (puerto o prefijo no permitido; scope-id no permitido).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**SERVICIO NET \_ STRING \_ \_ IPV6**</dt> </dl>                              | La cadena identifica un servicio IPv6 mediante una dirección literal (puerto necesario; prefijo no permitido; scope-id permitido).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ SERVICE \_ NO \_ SCOPE**</dt> </dl> | La cadena identifica un servicio IPv6 mediante una dirección literal en la que el contexto de la interfaz ya se conoce (puerto necesario; prefijo no permitido; scope-id no permitido).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ NETWORK**</dt> </dl>                              | La cadena identifica una red IPv6 (prefijo necesario; puerto o identificador de ámbito no permitido).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**DIRECCIÓN CON \_ NOMBRE DE CADENA DE \_ \_ NET**</dt> </dl>                           | La cadena identifica un host de Internet mediante el DNS (puerto o prefijo o identificador de ámbito no permitido).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ STRING \_ NAMED \_ SERVICE**</dt> </dl>                           | La cadena identifica un servicio de Internet mediante DNS (puerto necesario; prefijo o identificador de ámbito no permitido).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**DIRECCIÓN \_ \_ IP DE LA CADENA \_ DE RED**</dt> </dl>                                    | DIRECCIÓN \_ \_ IPV4 DE LA CADENA \_ NET DIRECCIÓN \| DIRECCIÓN \_ \_ IPV6 DE LA \_ CADENA DE RED.<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**DIRECCIÓN \_ \_ IP DE CADENA DE RED \_ SIN \_ \_ ÁMBITO**</dt> </dl>       | NET \_ STRING \_ IPV4 \_ ADDRESS NET STRING \| \_ \_ IPV6 ADDRESS NO SCOPE.NET STRING IPV6 \_ ADDRESS NO \_ SCOPE(DIRECCIÓN IPV4 \_ DE LA CADENA DE RED IPV6 NO TIENE ÁMBITO). <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE**</dt> </dl>                                    | SERVICIO NET \_ STRING \_ IPV4 \_ SERVICE NET STRING \| \_ \_ IPV6. \_<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>       | CADENA NET \_ DENOMINADA ADDRESS NET STRING IP ADDRESS \_ NO \_ \| \_ \_ \_ \_ \_ SCOPE.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**RED IP \_ DE \_ CADENA DE \_ RED**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ NETWORK \| NET \_ STRING \_ IPV6 \_ NETWORK.<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS**</dt> </dl>                                 | CADENA NET \_ DENOMINADA DIRECCIÓN DIRECCIÓN IP DE LA CADENA DE \_ \_ \| \_ \_ \_ RED.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl>    | CADENA NET \_ DENOMINADA ADDRESS NET STRING IP ADDRESS \_ NO \_ \| \_ \_ \_ \_ \_ SCOPE.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE**</dt> </dl>                                 | CADENA NET \_ DENOMINADA SERVICIO IP DE CADENA DE RED DE \_ \_ \| \_ \_ \_ SERVICIO.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>    | CADENA NET \_ DENOMINADA ADDRESS NET STRING IP ADDRESS \_ NO \_ \| \_ \_ \_ \_ \_ SCOPE.<br/>                                                                                                 |



## <a name="remarks"></a>Comentarios

Estos valores se definen en Iphlpapi.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Iphlpapi.h</dt> </dl> |



 

 




