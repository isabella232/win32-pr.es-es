---
title: Novedades de la plataforma de filtrado de Windows
description: Windows 8 y Windows Server 2012 presentan nuevos elementos de programación de la plataforma de filtrado de Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104359573"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Novedades de la plataforma de filtrado de Windows

Windows 8 y Windows Server 2012 presentan nuevos elementos de programación de la plataforma de filtrado de Windows. La nueva funcionalidad incluye lo siguiente:

-   *Filtrado de capa 2*: proporciona acceso a la capa L2 (Mac), lo que permite filtrar el tráfico en esa capa.
-   *filtrado de vSwitch*: permite que los paquetes que atraviesan un vSwitch se inspeccionen o modifiquen. Los filtros o las llamadas de WFP se pueden usar en la entrada y salida de vSwitch.
-   *Administración* de contenedores de aplicaciones: permite el acceso a información sobre los contenedores de aplicaciones y los problemas de conectividad de aislamiento de red.
-   *Actualizaciones de IPSec*: funcionalidad de IPSec extendida, incluida la supervisión del estado de conexión, la selección de certificados y la administración de claves.

Windows Driver Kit también incluye información sobre [los cambios de WFP para Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Actualizaciones de la API de Windows 8

Se han agregado muchas API nuevas para Windows 8 y Windows Server 2012.

## <a name="new-functions"></a>Nuevas funciones

-   [**\_Evento FWPM \_ net \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
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
-   [**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**\_Dictado de clave del administrador de claves IPSec \_ \_ \_ \_ CHECK0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**El \_ Administrador de claves IPSec \_ \_ dicta \_ KEY0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**\_Administrador de claves IPSec \_ \_ notificar a \_ KEY0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**Contexto de SA de IPSEC \_ \_ \_ CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
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
-   [**la \_ devolución de llamada de cambios de PAC \_ \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Nuevas estructuras

-   [**\_METHOD2 de autenticación de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_Cuadro de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CRITERIA0 de certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_POLICY2 de EM de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_AUTHENTICATION1 de Kerberos IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**POLICY2 de IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_Clave IPSec \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_Administrador de claves IPSec \_ \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_Creación de claves IPSec \_ directiva1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**Contexto de SA de IPSEC \_ \_ \_ CHANGE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**Contexto de SA de IPSEC \_ \_ \_ SUBSCRIPTION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_POLICY2 de transporte IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_Túnel IPSec \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_Túnel IPSec \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_Túnel IPSec \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**\_Enumeración de conexión de FWPM \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**\_SUBSCRIPTION0 de conexión FWPM \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ net \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**FWPM \_ de \_ capacidad de evento de net \_ \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ de \_ capacidad de evento de net \_ \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ clasificación de eventos netos \_ \_ \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**FWPM \_ clasificación de eventos netos \_ \_ \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**FWPM \_ \_ \_ \_ Drop \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**\_Evento FWPM \_ net \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**Proveedor de FWPM \_ \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**\_Evento FWPM \_ VSWITCH \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Nuevos tipos enumerados

-   [**tipo de red de FWP \_ VSWITCH \_ \_**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**FWPM \_ \_ tipo de \_ capacidad de red APPC \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**\_tipo de \_ evento de conexión FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**\_tipo de \_ evento \_ VSWITCH de FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**\_tipo de \_ nombre de criterios de certificado de IKEEXT \_ \_**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**Evento de contexto de SA de IPSEC \_ \_ \_ \_ TYPE0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Nuevos identificadores de capa de filtrado

[**Filtrar los identificadores de capa:**](management-filtering-layer-identifiers-.md)

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo
-   \_ \_ Ethernet VSWITCH de entrada de nivel FWPM \_ \_
-   \_ \_ Ethernet vSwitch de salida de capa \_ de FWPM \_
-   FWPM de entrada de capa de entrada de capa de \_ \_ \_ \_ transporte vSwitch \_ V4/FWPM de \_ entrada de nivel \_ \_ \_ \_ V6
-   Transporte de capa de salida de FWPM de salida de capa \_ \_ \_ \_ \_ V4/FWPM de \_ salida de capa \_ \_ \_ \_ de salida V6

## <a name="new-filtering-condition-identifiers"></a>Nuevos identificadores de condición de filtrado

[**Identificadores de condición de filtrado:**](filtering-condition-identifiers-.md)

-   \_ \_ \_ dirección Mac de la interfaz de condición FWPM \_
-   FWPM \_ condición \_ de \_ dirección Mac local \_
-   \_ \_ dirección remota de Mac de condición de \_ FWPM \_
-   \_tipo de condición \_ ether \_ de FWPM
-   \_identificador de \_ VLAN de condición de FWPM \_
-   \_ \_ Puerto NDIS de condición FWPM \_
-   \_condición FWPM \_ \_ tipo de medio NDIS \_
-   \_condición FWPM \_ \_ tipo de \_ medio físico NDIS \_
-   Marcas de FWPM de \_ condición \_ L2 \_
-   \_tipo de \_ \_ dirección Mac \_ de condición de FWPM \_
-   \_tipo de \_ \_ dirección remota \_ de Mac de condición de \_ FWPM
-   \_identificador de \_ \_ paquete Ale de condición \_ FWPM
-   \_dirección de \_ origen de Mac de condición de FWPM \_ \_
-   FWPM \_ condición \_ de \_ dirección Mac de destino \_
-   condición de FWPM \_ \_ tipo de \_ dirección de origen Mac \_ \_
-   \_tipo de \_ dirección Mac de \_ destino de \_ condición de FWPM \_
-   \_Puerto de \_ \_ origen IP de condición \_ FWPM
-   \_Puerto de \_ \_ destino IP de condición \_ FWPM
-   \_identificador de \_ VSWITCH de condición de FWPM \_
-   \_tipo de \_ \_ red VSWITCH de condición \_ de FWPM
-   identificador de la \_ \_ \_ interfaz de origen VSWITCH \_ de la condición FWPM \_
-   \_identificador de \_ interfaz de destino de VSWITCH de condición FWPM \_ \_ \_
-   \_identificador de \_ \_ \_ máquina virtual de origen VSWITCH \_ de condición FWPM
-   \_condición de \_ FWPM \_ \_ ID. de máquina virtual de destino VSWITCH \_
-   \_tipo de \_ \_ interfaz de origen VSWITCH de condición \_ FWPM \_
-   \_identificador de \_ red de inquilino de VSWITCH de condición FWPM \_ \_ \_

## <a name="new-filtering-condition-flags"></a>Nuevas marcas de condición de filtrado

[**Marcas de condición de filtrado:**](filtering-condition-flags-.md)

-   la \_ marca de condición de FWP \_ es una \_ \_ conexión de proxy \_
-   la \_ marca de condición de FWP \_ es un \_ \_ \_ bucle invertido de APPCONTAINER
-   la \_ marca de condición de FWP \_ \_ no es un \_ \_ \_ bucle invertido de APPCONTAINER
-   la \_ marca de condición de FWP \_ \_ está \_ respetando la \_ \_ autorización de la Directiva
-   La \_ condición de FWP \_ L2 \_ es una \_ \_ Ethernet nativa
-   La \_ condición de FWP \_ L2 \_ es \_ Wi-Fi
-   La \_ condición de FWP \_ L2 \_ es \_ \_ banda ancha móvil
-   La \_ condición de FWP \_ L2 \_ es \_ Wi-Fi \_ Direct \_ Data
-   La \_ condición de FWP \_ L2 \_ es \_ VM2VM
-   La \_ condición de FWP \_ L2 \_ tiene un paquete con \_ formato incorrecto \_
-   La \_ condición de FWP \_ L2 \_ es \_ grupo de \_ fragmentos IP \_
-   Condición de FWP \_ \_ L2 \_ si el \_ conector \_ está presente

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Actualizaciones de Windows 7 en la plataforma de filtrado de Windows

En el documento [What's New in Windows Filtering Platform]() se detallan muchas de las actualizaciones realizadas para Windows 7. La información también está disponible en el kit de controladores de Windows en [cambios de WFP para Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 