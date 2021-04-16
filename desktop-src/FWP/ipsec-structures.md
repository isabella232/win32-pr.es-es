---
title: Estructuras IPsec
description: Estructuras IPsec
ms.assetid: FF1FE626-B9F9-4091-8B82-BEB9D229B93D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd268fda1ee98ec80d20d8c75625d4f68526c741
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "105685682"
---
# <a name="ipsec-structures"></a>Estructuras IPsec

## <a name="in-this-section"></a>En esta sección

-   [**\_Dirección IPSec \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   [**\_Paquete de eliminación de paquetes de \_ \_ \_ STATISTICS0 de IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0)
-   [**\_Paquete de eliminación de paquetes de \_ \_ \_ STATISTICS1 de IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1)
-   [**IPSEC \_ agregado \_ SA \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**IPSEC \_ ah \_ Drop \_ Packet \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**\_Autenticación IPSec \_ y \_ cifrado \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**\_Autenticación IPSec \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**\_ID0 de \_ transformación de autenticación IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**\_Cifrado IPSec \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**\_Transformación de cifrado de IPSec \_ \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**\_OPTIONS0 DOSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**\_STATE0 DOSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**DOSP de estado de la \_ \_ \_ enumeración \_ TEMPLATE0 de IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**\_STATISTICS0 DOSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**\_STATISTICS0 de \_ eliminación de \_ paquetes \_ IPsec ESP**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   [**\_GETSPI0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0)
-   [**\_GETSPI1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1)
-   [**\_ID0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_Clave IPSec \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_Administrador de claves IPSec \_ \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_POLICY0 de claves IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0)
-   [**\_Creación de claves IPSec \_ directiva1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**\_STATE0 KEYMODULE \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_PROPOSAL0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**\_Sa0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**\_ \_ Autenticación \_ y cifrado de SA de IPSec \_ \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**\_INFORMATION0 de \_ autenticación \_ SA de IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   [**IPSEC \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)
-   [**IPSEC \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)
-   [**\_Cifrado de SA de IPSec \_ \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   [**IPSEC \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0)
-   [**Context1 IPSEC \_ SA \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1)
-   [**Contexto de SA de IPSEC \_ \_ \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_Enumeración de contexto de SA de IPSec \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**Contexto de SA de IPSEC \_ \_ \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**IPSEC \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0)
-   [**IPSEC \_ SA \_ detalles**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1)
-   [**TEMPLATE0 de la \_ \_ enumeración SA de IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**IPSEC \_ SA \_ inactiva \_ TIMEOUT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSEC \_ SA \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**\_STATISTICS0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0)
-   [**\_STATISTICS1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1)
-   [**IPSEC \_ SA \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   [**\_TOKEN0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   [**\_TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0)
-   [**\_TRAFFIC1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1)
-   [**\_STATISTICS0 de tráfico IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)
-   [**\_STATISTICS1 de tráfico IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1)
-   [**\_POLICY0 de transporte IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)
-   [**Transporte de IPSEC \_ \_ directiva1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1)
-   [**\_POLICY2 de transporte IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_Túnel IPSec \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_Túnel IPSec \_ ENDPOINTS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0)
-   [**\_Túnel IPSec \_ ENDPOINTS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1)
-   [**\_Túnel IPSec \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_Túnel IPSec \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0)
-   [**\_Túnel IPSec \_ directiva1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)
-   [**\_Túnel IPSec \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**IPSEC \_ V4 \_ UDP \_ ENCAPSULATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSEC \_ virtual \_ si el \_ túnel \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




