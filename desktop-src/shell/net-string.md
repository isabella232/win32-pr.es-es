---
description: Representan los tipos de dirección de red. Use una o varias (como una combinación bit a bit) de las constantes siguientes para crear una máscara de dirección de red que se usará con la macro NetAddr \_ SetAllowType.
title: NET_STRING (iphlpapi. h)
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
ms.openlocfilehash: 41ebe1cb844ec36ef13c8f8fe143d46dd9ac51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997253"
---
# <a name="net_string"></a>cadena de red \_

Representan los tipos de dirección de red. Use una o varias (como una combinación bit a bit) de las constantes siguientes para crear una máscara de dirección de red que se usará con la macro [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Constante                                                                                                                                                                                                                   | Descripción                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**\_ \_ Dirección IPv4 de cadena de red \_**</dt> </dl>                              | La cadena identifica un host o enrutador IPv4 mediante la dirección literal (no se permite el puerto o el prefijo).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**\_ \_ Servicio IPv4 de cadena de red \_**</dt> </dl>                              | La cadena identifica un servicio IPv4 mediante una dirección literal (puerto requerido; no se permite el prefijo).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**\_Red IPv4 de cadena de \_ \_ red**</dt> </dl>                              | La cadena identifica una red IPv4 (prefijo necesario; puerto no permitido).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**\_ \_ Dirección IPv6 de la cadena de red \_**</dt> </dl>                              | La cadena identifica un host o un enrutador IPv6 con una dirección literal (no se permite el puerto o el prefijo; identificador de ámbito permitido).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**\_Dirección IPv6 de cadena de red \_ \_ \_ sin \_ ámbito**</dt> </dl> | La cadena identifica un host o un enrutador IPv6 con una dirección literal en la que ya se conoce el contexto de la interfaz (no se permite el puerto o el prefijo; no se permite el identificador de ámbito).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**\_ \_ Servicio IPv6 de cadena de red \_**</dt> </dl>                              | La cadena identifica un servicio IPv6 mediante una dirección literal (puerto requerido; no se permite el prefijo; identificador de ámbito permitido).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**El \_ servicio IPv6 de la cadena de red \_ \_ \_ no tiene \_ ámbito**</dt> </dl> | La cadena identifica un servicio IPv6 mediante una dirección literal en la que ya se conoce el contexto de la interfaz (puerto requerido; no se permite el prefijo; no se permite el identificador de ámbito).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**\_Red IPv6 de cadena de \_ \_ red**</dt> </dl>                              | La cadena identifica una red IPv6 (prefijo obligatorio; no se permite el puerto o el identificador de ámbito).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**NET \_ String \_ denominada \_ Address**</dt> </dl>                           | La cadena identifica un host de Internet que usa el DNS (puerto o prefijo o identificador de ámbito no permitido).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ String \_ denominado \_ Service**</dt> </dl>                           | La cadena identifica un servicio de Internet mediante DNS (puerto requerido; prefijo o identificador de ámbito no permitido).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**\_ \_ dirección IP de cadena de red \_**</dt> </dl>                                    | Dirección IPv4 de la cadena de red dirección \_ \_ IPv6 de cadena de \_ \| red \_ \_ \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**\_dirección IP de cadena de red \_ \_ \_ sin \_ ámbito**</dt> </dl>       | Dirección IPv4 de la cadena de red \_ IPv4 dirección \_ \_ \| \_ \_ IPv6 \_ \_ no \_ ámbito. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**\_ \_ servicio IP de cadena de red \_**</dt> </dl>                                    | NET \_ String \_ IPv4 \_ Service \| red \_ \_ IPv6 \_ Service.<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**el \_ servicio IP de cadena de red \_ \_ \_ no tiene \_ ámbito**</dt> </dl>       | la \_ cadena de red \_ denominada \_ dirección \| IP de cadena de red \_ \_ \_ \_ no tiene \_ ámbito.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**\_red IP de cadena de \_ \_ red**</dt> </dl>                                    | NET \_ String \_ IPv4 \_ red \| \_ IPv6 red \_ IPv6 \_ .<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**NET \_ String \_ any \_ Address**</dt> </dl>                                 | la \_ cadena de red \_ denominada \_ dirección \| IP de \_ cadena \_ \_ de red.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**NET \_ String \_ cualquier \_ dirección \_ sin \_ ámbito**</dt> </dl>    | la \_ cadena de red \_ denominada \_ dirección \| IP de cadena de red \_ \_ \_ \_ no tiene \_ ámbito.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ String \_ any \_ Service**</dt> </dl>                                 | la \_ cadena de red denominada servicio IP de cadena de \_ \_ \| red \_ \_ \_ .<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ String \_ any \_ Service \_ sin \_ ámbito**</dt> </dl>    | la \_ cadena de red \_ denominada \_ dirección \| IP de cadena de red \_ \_ \_ \_ no tiene \_ ámbito.<br/>                                                                                                 |



## <a name="remarks"></a>Observaciones

Estos valores se definen en iphlpapi. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Iphlpapi. h</dt> </dl> |



 

 




