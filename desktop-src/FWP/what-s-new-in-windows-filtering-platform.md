---
title: Novedades de la plataforma Windows filtrado de datos
description: Windows 8 y Windows Server 2012 nuevos elementos de programación Windows plataforma de filtrado.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e12c1e7add7568b931aabe43f3ab91763df2d5ab12ad448d3683afe13baa3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766665"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Novedades de la plataforma Windows filtrado de datos

Windows 8 y Windows Server 2012 nuevos elementos de programación Windows plataforma de filtrado. La nueva funcionalidad incluye lo siguiente:

-   *Filtrado de nivel 2:* proporciona acceso a la capa L2 (MAC), lo que permite filtrar el tráfico en esa capa.
-   *Filtrado de vSwitch:* permite inspeccionar o modificar los paquetes que atraviesan un vSwitch. Los filtros o las llamadas de WFP se pueden usar en la entrada y salida de vSwitch.
-   *Administración de contenedores de* aplicaciones: permite el acceso a información sobre los contenedores de aplicaciones y los problemas de conectividad de aislamiento de red.
-   *Actualizaciones de IPsec:* funcionalidad extendida de IPsec, incluida la supervisión del estado de conexión, la selección de certificados y la administración de claves.

El Windows Driver Kit también incluye información sobre los cambios [de WFP para Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Windows 8 Actualizaciones de API

Se han agregado muchas API nuevas para Windows 8 y Windows Server 2012.

## <a name="new-functions"></a>Nuevas funciones

-   [**FWPM \_ NET \_ EVENT \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [**FwpmConnectionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [**FwpmConnectionDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [**FwpmConnectionEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [**FwpmConnectionGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [**FwpmConnectionGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [**FwpmConnectionSetSecurityInfo0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [**FwpmConnectionSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [**FwpmConnectionSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [**FwpmConnectionUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [**FwpmvSwitchEventsGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [**FwpmvSwitchEventsSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [**FwpmvSwitchEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [**FwpmvSwitchEventUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [**IxtSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IxtSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**COMPROBACIÓN DE \_ DICTADO DE CLAVES DEL ADMINISTRADOR DE CLAVES \_ \_ \_ \_ IPSEC0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**IPSEC \_ KEY \_ MANAGER \_ DICTATE \_ KEY0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**NOTIFICACIÓN DE \_ IPSEC KEY \_ MANAGER A \_ \_ KEY0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**IPSEC \_ SA \_ CONTEXT \_ CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**NetworkIsolationDiagnoseConnectFailureAndGetInfo**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**NetworkIsolationEnumAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**NetworkIsolationEnumerateAppContainerRules**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**NetworkIsolationFreeAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**NetworkIsolationGetAppContainerConfig**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**NetworkIsolationRegisterForAppContainerChanges**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**NetworkIsolationSetAppContainerConfig**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**NetworkIsolationSetupAppContainerBinaries**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**PAC \_ CHANGES \_ CALLBACK \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Nuevas estructuras

-   [**MÉTODO DE \_ AUTENTICACIÓN \_ IXTXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IXTXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IXTXT \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**AUTENTICACIÓN DE \_ CERTIFICADOS \_ IXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**IXTXT \_ CERTIFICATE \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IXTXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**AUTENTICACIÓN \_ KERBEROS DE \_ IXT1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_IXTXT POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**IPSEC \_ KEY \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**DEVOLUCIONES DE \_ LLAMADA DEL ADMINISTRADOR DE CLAVES \_ \_ IPSEC0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**DIRECTIVA DE \_ CLAVES \_ IPSEC1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**CAMBIO DE \_ CONTEXTO DE SA DE IPSEC0 \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**IPSEC \_ SA \_ CONTEXT \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**DIRECTIVA DE \_ TRANSPORTE \_ IPSEC2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**PUNTO DE CONEXIÓN DE \_ TÚNEL IPSEC0 \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**PUNTOS DE CONEXIÓN \_ DE \_ TÚNEL IPSEC2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**DIRECTIVA DE \_ TÚNEL \_ IPSEC2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ CONNECTION \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM \_ CONNECTION \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**FWPM \_ NET \_ EVENT \_ CAPABILITY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ EVENT \_ CAPABILITY \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**FWPM \_ NET \_ EVENT \_ CLASSIFY \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ EVENT \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**FWPM \_ PROVIDER \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**FWPM \_ VSWITCH \_ EVENT \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Nuevos tipos enumerados

-   [**TIPO DE \_ RED DE VSWITCH \_ \_ FWP**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**TIPO DE \_ FUNCIONALIDAD DE RED FWPM APPC \_ \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**TIPO DE EVENTO \_ DE CONEXIÓN \_ \_ FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**TIPO DE EVENTO \_ FWPM VSWITCH \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**TIPO DE NOMBRE \_ DE CRITERIOS DE CERTIFICADO \_ \_ IXT \_**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**IPSEC \_ SA \_ CONTEXT \_ EVENT \_ TYPE0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Nuevos identificadores de capa de filtrado

[**Filtrar identificadores de capa:**](management-filtering-layer-identifiers-.md)

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC DE ENTRADA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   MARCO DE SALIDA DE CAPA FWPM \_ \_ NATIVO \_ DE MAC \_ \_
-   FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ ETHERNET
-   FWPM \_ LAYER \_ EGRESS \_ VSWITCH \_ ETHERNET
-   FWPM \_ LAYER \_ INGRESS \_ VSWITCH TRANSPORT \_ \_ V4 /FWPM \_ LAYER \_ INGRESS \_ VSWITCH TRANSPORT \_ \_ V6
-   FWPM \_ LAYER \_ EGRESS \_ VSWITCH TRANSPORT \_ \_ V4 /FWPM \_ LAYER \_ EGRESS \_ VSWITCH TRANSPORT \_ \_ V6

## <a name="new-filtering-condition-identifiers"></a>Nuevos identificadores de condición de filtrado

[**Filtrar identificadores de condición:**](filtering-condition-identifiers-.md)

-   DIRECCIÓN MAC DE \_ LA INTERFAZ DE CONDICIÓN \_ \_ \_ FWPM
-   DIRECCIÓN \_ LOCAL DE MAC DE LA \_ CONDICIÓN \_ \_ FWPM
-   DIRECCIÓN REMOTA \_ MAC DE LA CONDICIÓN \_ FWPM \_ \_
-   FWPM \_ CONDITION \_ ETHER \_ TYPE
-   ID. de \_ VLAN DE \_ CONDICIÓN \_ FWPM
-   PUERTO \_ NDIS DE CONDICIÓN \_ \_ FWPM
-   TIPO DE MEDIO \_ \_ NDIS DE \_ CONDICIÓN \_ FWPM
-   FWPM \_ CONDITION \_ NDIS \_ PHYSICAL \_ MEDIA \_ TYPE
-   MARCAS DE CONDICIÓN DE FWPM \_ \_ L2 \_
-   FWPM \_ CONDITION MAC LOCAL ADDRESS TYPE (TIPO DE DIRECCIÓN LOCAL DE MAC DE CONDICIÓN \_ \_ \_ \_ FWPM)
-   FWPM \_ CONDITION \_ MAC \_ REMOTE \_ ADDRESS \_ TYPE
-   ID. DE \_ PAQUETE \_ DE ALE DE CONDICIÓN \_ \_ FWPM
-   DIRECCIÓN DE ORIGEN \_ DE MAC DE LA CONDICIÓN \_ \_ \_ FWPM
-   DIRECCIÓN DE DESTINO \_ DE MAC DE CONDICIÓN \_ FWPM \_ \_
-   FWPM CONDITION MAC SOURCE ADDRESS TYPE (TIPO DE DIRECCIÓN DE ORIGEN DE MAC DE CONDICIÓN \_ \_ \_ \_ \_ FWPM)
-   TIPO DE DIRECCIÓN DE \_ DESTINO \_ DE MAC \_ DE \_ \_ CONDICIÓN FWPM
-   PUERTO DE ORIGEN DE IP DE CONDICIÓN FWPM \_ \_ \_ \_
-   PUERTO DE DESTINO \_ IP DE CONDICIÓN \_ FWPM \_ \_
-   ID. DE \_ VSWITCH DE \_ CONDICIÓN \_ FWPM
-   TIPO DE RED \_ VSWITCH DE CONDICIÓN FWPM \_ \_ \_
-   ID. DE INTERFAZ \_ DE \_ ORIGEN DE VSWITCH \_ DE \_ \_ CONDICIÓN FWPM
-   ID. DE INTERFAZ \_ DE \_ DESTINO DE VSWITCH \_ DE \_ \_ CONDICIÓN FWPM
-   ID. DE MÁQUINA \_ VIRTUAL DE ORIGEN DE \_ VSWITCH \_ DE \_ \_ CONDICIÓN FWPM
-   ID. DE MÁQUINA VIRTUAL DE \_ \_ DESTINO DE VSWITCH \_ DE \_ \_ CONDICIÓN FWPM
-   TIPO DE INTERFAZ DE \_ ORIGEN \_ DE VSWITCH \_ DE \_ \_ CONDICIÓN FWPM
-   ID. DE RED \_ \_ DE INQUILINO DE VSWITCH \_ DE \_ \_ CONDICIÓN FWPM

## <a name="new-filtering-condition-flags"></a>Nuevas marcas de condición de filtrado

[**Filtrar marcas de condición:**](filtering-condition-flags-.md)

-   MARCA DE CONDICIÓN \_ FWP \_ ES CONEXIÓN DE \_ \_ \_ PROXY
-   MARCA DE CONDICIÓN \_ FWP \_ ES BUCLE DE BUCLE \_ \_ DE APPCONTAINER \_
-   LA MARCA DE \_ CONDICIÓN \_ FWP \_ NO ES \_ UN \_ BUCLEBACK DE \_ APPCONTAINER
-   LA MARCA DE \_ CONDICIÓN \_ FWP \_ RESPETA LA AUTORIZACIÓN DE LA \_ \_ \_ DIRECTIVA
-   LA CONDICIÓN \_ FWP \_ L2 \_ ES ETHERNET \_ \_ NATIVA
-   FWP \_ CONDITION \_ L2 \_ IS \_ WIFI
-   LA CONDICIÓN DE FWP \_ \_ L2 \_ ES BANDA ANCHA \_ \_ MÓVIL
-   FWP \_ CONDITION \_ L2 \_ IS \_ WIFI \_ DIRECT \_ DATA
-   LA CONDICIÓN \_ DE \_ FWP L2 \_ ES \_ VM2VM
-   FWP \_ CONDITION \_ L2 \_ IS \_ MALFORMED \_ PACKET
-   CONDICIÓN FWP \_ \_ L2 \_ ES GRUPO DE \_ \_ FRAGMENTOS DE \_ IP
-   CONDICIÓN FWP \_ \_ L2 \_ SI EL CONECTOR \_ ESTÁ \_ PRESENTE

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Windows 7 actualizaciones de la plataforma Windows filtrado de datos

El documento [What's New in Windows Filtering Platform]() detalla muchas de las actualizaciones realizadas para Windows 7. También hay información disponible en el kit Windows Driver Kit sobre los cambios [de WFP para Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 