---
title: Filtrar marcas de condición (Fwptypes.h)
description: Las Windows de condición de filtrado de la Plataforma de filtrado de Windows filtrado (WFP) se representan mediante un campo de bits.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a43ae080a9ef1c17baa262cc1154f9ae89a837f0ec6f6919d80c22376f3b995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150898"
---
# <a name="filtering-condition-flags"></a>Filtrar marcas de condición

Las Windows de condición de filtrado de la Plataforma de filtrado de Windows filtrado (WFP) se representan mediante un campo de bits.

Estas marcas y las capas de filtrado donde se pueden usar se definen de la manera siguiente.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**MARCA DE CONDICIÓN \_ FWP \_ IS \_ \_ LOOPBACK**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red es tráfico de bucles de retorno.

Capas de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER INBOUND TRANSPORT \_ \_ \_ V{4 \| 6}
-   FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ STREAM \_ {V4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   ERROR ICMP ENTRANTE \_ \_ DE CAPA \_ FWPM \_ \_ V{4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   ERROR ICMP DE \_ \_ SALIDA DE CAPA \_ FWPM \_ \_ V{4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**LA MARCA \_ DE CONDICIÓN \_ FWP ESTÁ PROTEGIDA CON \_ \_ \_ IPSEC**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red está protegido por IPsec.

Capas de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER INBOUND TRANSPORT \_ \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**LA MARCA \_ DE CONDICIÓN \_ FWP ES \_ \_ REAUTORIZACIÓN**
</dt> <dd> <dl> <dt>



Comprueba un cambio de directiva en lugar de una nueva conexión.

Capas de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**MARCA DE CONDICIÓN \_ FWP \_ ES ENLACE DE \_ CARACTERES \_ \_ COMODÍN**
</dt> <dd> <dl> <dt>



Comprueba si la aplicación especificó una dirección comodín al enlazar a una dirección de red local.

Capa de filtrado:

-   ASIGNACIÓN DE RECURSOS ALE DE CAPA FWPM \_ \_ \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**MARCA DE CONDICIÓN \_ FWP \_ ES PUNTO DE CONEXIÓN SIN \_ \_ \_ FORMATO**
</dt> <dd> <dl> <dt>



Comprueba si el punto de conexión local que envía y recibe tráfico es un punto de conexión sin procesar.

Capas de filtrado:

-   FWPM \_ LAYER INBOUND TRANSPORT \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   DATOS DEL \_ \_ DATAGRAMA DE CAPA \_ FWPM \_ {V4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   ASIGNACIÓN DE RECURSOS ALE DE CAPA FWPM \_ \_ \_ \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**LA MARCA DE \_ CONDICIÓN FWP \_ ES \_ \_ FRAGMENT**
</dt> <dd> <dl> <dt>



Comprueba si la estructura NET \_ BUFFER LIST pasada a un controlador de llamada es un fragmento de paquete \_ IP.

Capas de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6} \_ DISCARD


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**MARCA DE CONDICIÓN \_ FWP \_ ES GRUPO \_ DE \_ \_ FRAGMENTOS**
</dt> <dd> <dl> <dt>



Comprueba si la estructura NET \_ BUFFER LIST pasada a un controlador de llamada describe una lista vinculada de \_ fragmentos de paquetes.

Capa de filtrado:

-   FWPM \_ LAYER \_ IPFORWARD \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**LA MARCA \_ DE CONDICIÓN \_ FWP ES \_ \_ \_ RECLASIFICACIÓN DE NATT DE IPSEC \_**
</dt> <dd> <dl> <dt>



Indica que el mismo paquete se vuelve a clasificar en la capa de transporte, cuando la corrección de compatibilidad (shim) nat de IPsec traduce el valor del puerto remoto.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**LA MARCA \_ DE CONDICIÓN \_ FWP REQUIERE CLASIFICACIÓN DE \_ \_ ALE \_**
</dt> <dd> <dl> <dt>



Indica que el paquete se volverá a clasificar en la capa de recepción/aceptación de ALE.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**LA MARCA DE \_ CONDICIÓN FWP \_ ES ENLACE \_ \_ \_ IMPLÍCITO**
</dt> <dd> <dl> <dt>



Comprueba si Windows Sockets está realizando un enlace implícito.

Solo está disponible en Windows Vista y Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**LA MARCA \_ DE CONDICIÓN \_ FWP SE VUELVE A \_ \_ ENSAMBLAR**
</dt> <dd> <dl> <dt>



Comprueba si el paquete se ha reensamblado.

> [!Note]  
> Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

 

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**LA MARCA \_ DE CONDICIÓN \_ FWP ES LA APLICACIÓN \_ DE NOMBRE \_ \_ \_ ESPECIFICADA**
</dt> <dd> <dl> <dt>



Comprueba si el nombre del equipo del mismo nivel al que la aplicación espera conectarse se ha recibido a través de una API como [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) y no se ha obtenido a través de la heurística de almacenamiento en caché.

> [!Note]  
> Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**LA MARCA \_ DE \_ CONDICIÓN FWP ES \_ \_ PROMISCUA**
</dt> <dd> <dl> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**LA MARCA DE \_ CONDICIÓN \_ FWP \_ ES \_ AUTH \_ FW**
</dt> <dd> <dl> <dt>



Comprueba si la conexión está autenticada de un extremo a otro, incluso si no se han comprobado los paquetes individuales.

> [!Note]  
> Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**LA MARCA \_ DE CONDICIÓN \_ FWP SE VUELVE A \_ \_ CLASIFICAR**
</dt> <dd> <dl> <dt>



Comprueba si el motor de filtrado está reclasificando una solicitud de enlace o escucha anterior.

> [!Note]  
> Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   ASIGNACIÓN DE RECURSOS ALE DE CAPA FWPM \_ \_ \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**MARCA DE CONDICIÓN \_ FWP \_ ES CONEXIÓN DE \_ \_ \_ PROXY**
</dt> <dd> <dl> <dt>



Comprueba si la conexión usa un proxy.

> [!Note]  
> Disponible solo en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**MARCA DE CONDICIÓN \_ FWP \_ ES BUCLE DE BUCLE \_ \_ DE APPCONTAINER \_**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red es tráfico de bucles de bucles de contenedor de aplicaciones.

> [!Note]  
> Disponible solo en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**LA MARCA DE \_ CONDICIÓN \_ FWP \_ NO ES \_ UN \_ BUCLEBACK DE \_ APPCONTAINER**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red es tráfico de bucle de bucles de contenedor que no es de aplicación.

> [!Note]  
> Disponible solo en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**LA MARCA DE \_ CONDICIÓN FWP \_ ESTÁ \_ \_ RESERVADA**
</dt> <dd> <dl> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**LA MARCA DE \_ CONDICIÓN \_ FWP \_ RESPETA LA AUTORIZACIÓN DE LA \_ \_ \_ DIRECTIVA**
</dt> <dd> <dl> <dt>



Indica que la clasificación actual se realiza para respetar la intención de una aplicación redirigida Windows Store para conectarse a un host especificado. Esta clasificación contendrá los mismos valores de campo clasificables que si la aplicación nunca se redirija. La marca también indica que se invocará una clasificación futura para que coincida con el destino redirigido efectivo. Si la aplicación se redirige a un servicio de proxy para su inspección, también significa que se invocará una clasificación futura en la conexión de proxy. Por lo general, los controladores de llamada deben permitir esta clasificación.

> [!Note]  
> Disponible solo en Windows 8 y Windows Server 2012.

 

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Las marcas siguientes especifican el motivo para volver a autorizar una conexión autorizada previamente. Estas marcas y las capas de filtrado donde se pueden usar se definen de la manera siguiente.

> [!Note]  
> Estas condiciones de filtrado solo están disponibles en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**CONDICIÓN FWP \_ \_ REAUTORIZAR CAMBIO \_ DE DIRECTIVA DE \_ MOTIVO \_**
</dt> <dd> <dl> <dt>



Indica que la conexión se reautorizó debido a que se agregaron o quitaron filtros.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**CONDICIÓN FWP \_ \_ REAUTORIZAR LA NUEVA \_ INTERFAZ DE \_ \_ LLEGADA \_ DEL MOTIVO**
</dt> <dd> <dl> <dt>



Indica que el paquete ha llegado desde una interfaz desconocida.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**CONDICIÓN FWP \_ \_ REAUTHORIZE \_ REASON \_ NEW \_ NEXTHOP \_ INTERFACE**
</dt> <dd> <dl> <dt>



Indica que el paquete va a salir de una interfaz desconocida.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**CONDICIÓN FWP \_ \_ REAUTORIZAR CRUCE DE \_ PERFIL \_ DE \_ MOTIVO**
</dt> <dd> <dl> <dt>



Indica que el paquete ha pasado a través de interfaces de más de una categoría de red.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**CONDICIÓN FWP \_ \_ REAUTORIZAR FINALIZACIÓN \_ DE CLASIFICACIÓN DE \_ RAZONES \_**
</dt> <dd> <dl> <dt>



Indica que ahora se permite que se complete una conexión previamente retenido.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**CONDICIÓN FWP \_ \_ REAUTORIZACIÓN DE LA \_ RAZÓN POR \_ LA QUE SE CAMBIARON LAS PROPIEDADES DE IPSEC \_ \_**
</dt> <dd> <dl> <dt>



Indica que las propiedades de IPsec han cambiado o que la conexión ha cambiado de texto no cifrado a una conexión segura.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**CONDICIÓN FWP \_ \_ REAUTORIZAR MOTIVO DE \_ INSPECCIÓN DE FLUJO \_ \_ \_ MEDIO**
</dt> <dd> <dl> <dt>



Indica que ahora se está inspeccionando una conexión TCP establecida previamente.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**SE HA CAMBIADO LA PROPIEDAD DE SOCKET DE MOTIVO DE LA CONDICIÓN FWP \_ \_ PARA VOLVER A \_ \_ \_ \_ AUTORIZARLA**
</dt> <dd> <dl> <dt>



Indica que las propiedades de socket se han establecido después de que se autorizara y se estableciera una conexión.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**CONDICIÓN FWP \_ \_ REAUTHORIZE \_ REASON NEW INBOUND \_ \_ \_ MCAST \_ BCAST \_ PACKET**
</dt> <dd> <dl> <dt>



Indica que se están reautoriendo nuevos paquetes de difusión o multidifusión entrantes en las llamadas ACCEPT de \_ RECV de ALE. \_

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Las marcas siguientes especifican propiedades de socket que están relacionadas con si una aplicación desea recibir tráfico de Edge Traversal. Estas marcas y las capas de filtrado donde se pueden usar se definen de la manera siguiente.

> [!Note]  
> Estas condiciones de filtrado solo están disponibles en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**LA MARCA DE PROPIEDAD DE SOCKET DE CONDICIÓN FWP \_ ES RPC DE PUERTO DEL \_ \_ \_ \_ \_ \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>



Indica que la aplicación se está comunicando con un puerto RPC dinámico.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   ASIGNACIÓN DE \_ RECURSOS DE FWPM LAYER \_ ALE \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**MARCA DE PROPIEDAD DE SOCKET DE CONDICIÓN FWP \_ \_ ALLOW EDGE \_ \_ \_ \_ \_ TRAFFIC**
</dt> <dd> <dl> <dt>



Indica que la aplicación quiere recibir tráfico específico del recorrido perimetral.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   ASIGNACIÓN DE \_ RECURSOS DE FWPM LAYER \_ ALE \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**MARCA DE PROPIEDAD DE SOCKET DE CONDICIÓN FWP \_ \_ DENEGAR TRÁFICO \_ \_ \_ \_ PERIMETRAL \_**
</dt> <dd> <dl> <dt>



Indica que la aplicación no quiere recibir ni procesar tráfico específico del recorrido perimetral.

Capa de filtrado:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   ASIGNACIÓN DE \_ RECURSOS DE FWPM LAYER \_ ALE \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Las marcas siguientes especifican los detalles de conexión relacionados con el filtrado L2.

> [!Note]  
> Estas condiciones de filtrado solo están disponibles en Windows 8 y Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**LA CONDICIÓN \_ \_ FWP L2 \_ ES ETHERNET \_ \_ NATIVA**
</dt> <dd> <dl> <dt>



Indica que la conexión es Ethernet nativa.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ WIFI**
</dt> <dd> <dl> <dt>



Indica que la conexión es Wi-Fi.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**LA CONDICIÓN FWP \_ \_ L2 \_ ES BANDA ANCHA \_ \_ MÓVIL**
</dt> <dd> <dl> <dt>



Indica que la conexión es de banda ancha móvil.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ WIFI \_ DIRECT \_ DATA**
</dt> <dd> <dl> <dt>



Indica que la conexión es Wi-Fi Directo.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**LA CONDICIÓN \_ DE \_ FWP L2 \_ ES \_ VM2VM**
</dt> <dd> <dl> <dt>



Indica que la conexión está entre máquinas virtuales.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ MALFORMED \_ PACKET**
</dt> <dd> <dl> <dt>



Indica que un paquete parece estar malformado.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**LA CONDICIÓN FWP \_ \_ L2 \_ ES UN GRUPO \_ DE \_ FRAGMENTOS DE \_ IP**
</dt> <dd> <dl> <dt>



Indica un grupo de fragmentos de paquetes IP.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**CONDICIÓN FWP \_ \_ L2 \_ SI EL CONECTOR \_ ESTÁ \_ PRESENTE**
</dt> <dd> <dl> <dt>



Indica que hay un conector presente.

Capa de filtrado:

-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO DE MAC ENTRANTE DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   MARCO MAC DE SALIDA DE CAPA FWPM \_ \_ \_ \_ \_ NATIVO


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Fwptypes.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Filtrado de identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

