---
title: Estructuras de WFP
description: Las Windows API de plataforma de filtrado de filtros (WFP) son las siguientes.
ms.assetid: e957132f-417b-40c1-afe3-5aec0e2192f7
keywords:
- Windows Filtrar tipos enumerados de API de plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b1bd45efbe1a93ddeb0c95161aa52764bf1812ecc5f8e914e01317b657f251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069175"
---
# <a name="wfp-structures"></a>Estructuras de WFP

Las Windows API de plataforma de filtrado de filtros (WFP) son las siguientes.

Estructuras de administración

-   [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
-   [**FWPM \_ CALLOUT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout0)
-   [**FWPM \_ CALLOUT \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_change0)
-   [**FWPM \_ CALLOUT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_enum_template0)
-   [**FWPM \_ CALLOUT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
-   [**FWPM \_ CLASSIFY \_ OPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
-   [**OPCIONES DE \_ CLASIFICACIÓN DE FWPM0 \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ CONNECTION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM \_ CONNECTION \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)
-   [**FWPM \_ FIELD0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_field0)
-   [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)
-   [**FWPM \_ FILTER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)
-   [**FWPM \_ FILTER \_ CONDITION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)
-   [**FWPM \_ FILTER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_enum_template0)
-   [**FWPM \_ FILTER \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)
-   [**FWPM \_ LAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer0)
-   [**FWPM \_ LAYER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)
-   [**FWPM \_ LAYER \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)
-   EVENTO DE NET \_ \_ FWPM:
    -   [**FWPM \_ NET \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event1) (Windows 7)
    -   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2) (Windows 8)
-   [**FWPM \_ NET \_ EVENT \_ CAPABILITY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ EVENT \_ CAPABILITY \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP:
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1) (Windows 7 y versiones posteriores)
    -   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2) (Windows 8)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ EVENT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)
-   ENCABEZADO DE EVENTO \_ DE FWPM \_ \_ NET:
    -   [**FWPM \_ NET \_ EVENT \_ HEADER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ HEADER1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1) (Windows 7)
    -   [**FWPM \_ NET \_ EVENT \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2) (Windows 8)
-   ERROR DE EM DEL EVENTO DE NET \_ \_ \_ FWPM \_ \_ NET:
    -   [**FWPM \_ NET \_ EVENT \_ IXT EM \_ \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ IXT EM \_ \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) (Windows 7 y versiones posteriores)
-   ERROR DE \_ \_ \_ IXTXT MM DEL EVENTO NET FWPM \_ \_ NET:
    -   [**FWPM \_ NET \_ EVENT \_ IXT MM \_ \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ IXTXT \_ MM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1) (Windows 7 y versiones posteriores)
-   [**FWPM \_ NET \_ EVENT \_ IXT \_ QM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ DOSP \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0)
-   [**FWPM \_ NET \_ EVENT \_ IPSEC \_ KERNEL \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0)
-   [**FWPM \_ NET \_ EVENT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)
-   [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)
-   [**FWPM \_ PROVIDER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)
-   CONTEXTO DEL \_ PROVEEDOR \_ FWPM:
    -   [**FWPM \_ PROVIDER \_ CONTEXT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context0) (Windows Vista)
    -   [**FWPM \_ PROVIDER \_ CONTEXT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context1) (Windows 7)
    -   FWPM \_ PROVIDER \_ CONTEXT2 (Windows 8)
-   [**FWPM \_ PROVIDER \_ CONTEXT \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)
-   [**FWPM \_ PROVIDER \_ CONTEXT \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0)
-   [**FWPM \_ PROVIDER \_ CONTEXT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)
-   [**FWPM \_ PROVIDER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)
-   [**FWPM \_ PROVIDER \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)
-   [**FWPM \_ SESSION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0)
-   [**FWPM \_ SESSION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session_enum_template0)
-   [**FWPM \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_statistics0)
-   [**FWPM \_ SUBLAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)
-   [**FWPM \_ SUBLAYER \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_change0)
-   [**FWPM \_ SUBLAYER \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_enum_template0)
-   [**FWPM \_ SUBLAYER \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)
-   [**FWPM \_ SYSTEM \_ PORTS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)
-   [**PUERTOS \_ DEL SISTEMA \_ FWPM POR \_ \_ TIPO0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ VSWITCH \_ EVENT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

Estructuras compartidas

-   [**FWP \_ BYTE \_ ARRAY6**](/windows/win32/api/fwptypes/ns-fwptypes-fwp_byte_array6)
-   [**FWP \_ BYTE \_ ARRAY16**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_array16)
-   [**FWP \_ BYTE \_ BLOB**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_blob)
-   [**FWP \_ CONDITION \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)
-   [**FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)
-   [**TIPO DE \_ COINCIDENCIA \_ FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)
-   [**FWP \_ V4 \_ ADDR \_ AND \_ MASK**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)
-   [**FWP \_ V6 \_ ADDR \_ AND \_ MASK**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)
-   [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)

Estructuras IKE/AuthIP

-   MÉTODO DE \_ AUTENTICACIÓN \_ IXT:
    -   [**IXTXT \_ AUTHENTICATION \_ METHOD0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0) (Windows Vista)
    -   [**IXTXT \_ AUTHENTICATION \_ METHOD1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1) (Windows 7)
    -   [**IXTXT \_ AUTHENTICATION \_ METHOD2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2) (Windows 8)
-   [**IXTXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IXTXT \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IXTXT \_ CERT \_ ROOT \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   AUTENTICACIÓN DE \_ CERTIFICADOS \_ IXT:
    -   [**IXTXT \_ CERTIFICATE \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0) (Windows Vista)
    -   [**IXTXT \_ AUTENTICACIÓN \_ DE CERTIFICADO1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1) (Windows 7)
    -   [**IXTXT \_ AUTENTICACIÓN \_ DE CERTIFICADO2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) (Windows 8)
-   CREDENCIAL \_ DE CERTIFICADO \_ IXT:
    -   [**IXTXT \_ CERTIFICATE \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0) (Windows Vista)
    -   [**IXTXT \_ CERTIFICATE \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1) (Windows 7 y versiones posteriores)
-   [**CRITERIOS DE CERTIFICADO \_ \_ IXT0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**ALGORITMO DE CIFRADO \_ \_ IXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   ESTADÍSTICAS COMUNES \_ DE IXT: \_
    -   [**IXTXT \_ COMMON \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0) (Windows Vista)
    -   [**IXTXT \_ COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1) (Windows 7 y versiones posteriores)
-   [**\_IXTXT COOKIE \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   CREDENCIAL \_ IXT:
    -   [**IXTXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0) (Windows Vista)
    -   [**IXTXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1) (Windows 7 y versiones posteriores)
-   PAR DE CREDENCIALES \_ \_ IXT:
    -   [**IXTXT \_ CREDENTIAL \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0) (Windows Vista)
    -   [**IXTXT \_ CREDENTIAL \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1) (Windows 7 y versiones posteriores)
-   CREDENCIALES DE \_ IXT:
    -   [**IXTXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0) (Windows Vista)
    -   [**IXTXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1) (Windows 7 y versiones posteriores)
-   [**AUTENTICACIÓN \_ DE EAP DE IXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   DIRECTIVA \_ EM DE IXT: \_
    -   [**IXTXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0) (Windows Vista)
    -   [**IXTXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1) (Windows 7)
    -   [**IXTXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2) (Windows 8)
-   [**ALGORITMO DE \_ INTEGRIDAD DE IXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   ESTADÍSTICAS COMUNES \_ ESPECÍFICAS DE LA VERSIÓN DE IP DE \_ \_ \_ \_ IXT:
    -   [**IXTXT \_ ESTADÍSTICAS COMUNES ESPECÍFICAS DE LA VERSIÓN DE \_ \_ \_ \_ IP0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) (Windows Vista)
    -   [**IXTXT \_ ESTADÍSTICAS COMUNES ESPECÍFICAS DE LA VERSIÓN DE \_ \_ \_ \_ IP1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1) (Windows 7 y versiones posteriores)
-   ESTADÍSTICAS \_ KEYMODULE ESPECÍFICAS DE LA VERSIÓN DE IP \_ DE \_ \_ \_ IXT:
    -   [**IXTXT \_ \_KEYMODULE \_ \_ \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0) ESPECÍFICO DE LA VERSIÓN DE IP (Windows Vista)
    -   [**IXTXT \_ \_KEYMODULE \_ \_ \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) ESPECÍFICO DE LA VERSIÓN DE IP (Windows 7 y versiones posteriores)
-   [**IXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   ESTADÍSTICAS \_ DE KEYMODULE \_ DE IXT:
    -   [**IXTXT \_ AUTENTICACIÓN \_ KERBEROS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0) (Windows Vista y Windows 7)
    -   [**IXTXT \_ AUTENTICACIÓN \_ KERBEROS1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1) (Windows 8)
-   -   ESTADÍSTICAS \_ DE KEYMODULE \_ DE IXT:
    -   [**IXTXT \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0) (Windows Vista)
    -   [**IXTXT \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1) (Windows 7 y versiones posteriores)
-   [**IXTXT \_ NAME \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**AUTENTICACIÓN IXT \_ NTLM \_ \_ V20**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   DIRECTIVA DE \_ IXT:
    -   [**IXTXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0) (Windows Vista)
    -   [**IXTXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1) (Windows 7)
    -   [**IXTXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2) (Windows 8)
-   AUTENTICACIÓN \_ DE CLAVE PREVIAMENTE COMPARTIDA \_ DE IXT: \_
    -   [**IXTXT \_ PRESHARED \_ KEY \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0) (Windows Vista)
    -   [**IXTXT \_ PRESHARED \_ KEY \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1) (Windows 7 y versiones posteriores)
-   [**IXT \_ PROPOSAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**AUTENTICACIÓN RESERVADA \_ DE IXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   DETALLES DE \_ SA DE IXT: \_
    -   [**IXTXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0) (Windows Vista)
    -   [**IXTXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1) (Windows 7 y versiones posteriores)
-   [**IXTXT \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   ESTADÍSTICAS \_ DE IXT:
    -   [**IXTXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0) (Windows Vista)
    -   [**IXTXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1) (Windows 7 y versiones posteriores)
-   [**IXT \_ TRAFFIC0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

Estructuras IPsec

-   [**IPSEC \_ ADDRESS \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   ESTADÍSTICAS DE \_ PAQUETES \_ DROP \_ AGREGADOS DE IPSEC: \_
    -   [**IPSEC \_ AGGREGATE \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0) (Windows Vista)
    -   [**IPSEC \_ AGGREGATE \_ DROP \_ PACKET \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1) (Windows 7 y versiones posteriores)
-   [**IPSEC \_ AGGREGATE \_ SA \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**IPSEC \_ AH \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**AUTENTICACIÓN DE IPSEC \_ \_ Y TRANSFORMACIÓN DE \_ \_ CIFRADO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**IPSEC \_ AUTH \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**IPSEC \_ AUTH \_ TRANSFORM \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**IPSEC \_ CIPHER \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**ID0 DE TRANSFORMACIÓN \_ DE \_ CIFRADO \_ IPSEC**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**OPCIONES \_ DE DOSP de \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**IPSEC \_ DOSP \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**IPSEC \_ DOSP \_ STATE \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**IPSEC \_ DOSP \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**IPSEC \_ ESP \_ DROP \_ PACKET \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   IPSEC \_ GETSPI:
    -   [**IPSEC \_ GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0) (Windows Vista)
    -   [**IPSEC \_ GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1) (Windows 7 y versiones posteriores)
-   [**IPSEC \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**IPSEC \_ KEY \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**DEVOLUCIONES DE \_ LLAMADA DEL ADMINISTRADOR DE CLAVES \_ \_ IPSEC0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   DIRECTIVA DE \_ CLAVES \_ IPSEC:
    -   [**IPSEC \_ KEYING \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0) (Windows Vista y Windows 7)
    -   [**IPSEC \_ KEYING \_ POLICY1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1) (Windows 8)
-   [**IPSEC \_ KEYMODULE \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**IPSEC \_ PROPOSAL0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**IPSEC \_ SA0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**INFORMACIÓN DE CIFRADO Y AUTENTICACIÓN DE SA DE \_ \_ \_ \_ \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**INFORMACIÓN DE \_ AUTENTICACIÓN DE SA de \_ IPSEC0 \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   PAQUETE \_ SA de \_ IPSEC:
    -   [**IPSEC \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0) (Windows Vista)
    -   [**IPSEC \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) (Windows 7 y versiones posteriores)
-   [**INFORMACIÓN DE \_ CIFRADO SA DE IPSEC0 \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   CONTEXTO DE \_ SA de IPSEC: \_
    -   [**IPSEC \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0) (Windows Vista)
    -   [**IPSEC \_ SA \_ CONTEXT1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1) (Windows 7 y versiones posteriores)
-   [**CAMBIO DE \_ CONTEXTO DE SA DE IPSEC0 \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSEC \_ SA \_ CONTEXT ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**IPSEC \_ SA \_ CONTEXT \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   DETALLES DE \_ SA de IPSEC: \_
    -   [**IPSEC \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0) (Windows Vista)
    -   [**IPSEC \_ SA \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1) (Windows 7 y versiones posteriores)
-   [**IPSEC \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**TIEMPO DE ESPERA \_ DE INACTIVIDAD DE SA de \_ IPSEC0 \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSEC \_ SA \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**IPSEC \_ SA \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   ESTADÍSTICAS \_ DE IPSEC:
    -   [**IPSEC \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0) (Windows Vista)
    -   [**IPSEC \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1) (Windows 7 y versiones posteriores)
-   [**TOKEN0 de IPSEC \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   TRÁFICO \_ IPSEC:
    -   [**IPSEC \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) (Windows Vista)
    -   [**IPSEC \_ TRAFFIC1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1) (Windows 7 y versiones posteriores)
-   ESTADÍSTICAS DE \_ TRÁFICO \_ IPSEC:
    -   [**IPSEC \_ TRAFFIC \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) (Windows Vista)
    -   [**IPSEC \_ TRAFFIC \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) (Windows 7 y versiones posteriores)
-   DIRECTIVA DE \_ TRANSPORTE \_ IPSEC:
    -   [**IPSEC \_ DIRECTIVA \_ DE TRANSPORTE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) (Windows Vista)
    -   [**IPSEC \_ DIRECTIVA \_ DE TRANSPORTE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1) (Windows 7)
    -   [**IPSEC \_ DIRECTIVA \_ DE TRANSPORTE2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2) (Windows 8)
-   [**PUNTO DE CONEXIÓN DE \_ TÚNEL IPSEC0 \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   PUNTOS DE CONEXIÓN \_ \_ DE TÚNEL IPSEC:
    -   [**IPSEC \_ TUNNEL \_ ENDPOINTS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) (Windows Vista)
    -   [**IPSEC \_ TUNNEL \_ ENDPOINTS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) (Windows 7)
    -   [**IPSEC \_ TUNNEL \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) (Windows 8)
-   DIRECTIVA DE \_ TÚNEL \_ IPSEC:
    -   [**IPSEC \_ TUNNEL \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0) (Windows Vista)
    -   [**IPSEC \_ TUNNEL \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1) (Windows 7)
    -   [**IPSEC \_ TUNNEL \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) (Windows 8)
-   [**ENCAPSULACIÓN UDP DE IPSEC \_ \_ \_ V40**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSEC \_ VIRTUAL \_ IF \_ TUNNEL \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




