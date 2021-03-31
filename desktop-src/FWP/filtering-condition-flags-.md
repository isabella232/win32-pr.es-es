---
title: Marcas de condición de filtrado (Fwptypes. h)
description: Las marcas de condición de filtrado de la plataforma de filtrado de Windows (WFP) están representadas por un campo de bits.
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
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803512"
---
# <a name="filtering-condition-flags"></a>Marcas de condición de filtrado

Las marcas de condición de filtrado de la plataforma de filtrado de Windows (WFP) están representadas por un campo de bits.

Estas marcas y las capas de filtrado donde se pueden usar se definen como se indica a continuación.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**la \_ marca de condición de FWP \_ es de \_ \_ bucle invertido**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red es un tráfico de bucle invertido.

Filtrar capas:

-   FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}
-   FWPM de \_ salida de nivel de \_ \_ IPPACKET \_ V {4 \| 6}
-   \_Transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6}
-   \_Transporte de salida de capa FWPM \_ \_ \_ V {4 \| 6}
-   Flujo de capa de FWPM \_ \_ \_ {V4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   \_Error ICMP entrante de la capa FWPM \_ \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   \_Error de \_ ICMP saliente de nivel FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}
-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   \_Flujo ALE de capa de FWPM \_ establecido en \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**la \_ marca de condición de FWP \_ \_ está \_ protegida por IPsec \_**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red está protegido por IPsec.

Filtrar capas:

-   FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}
-   \_Transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}
-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**la \_ marca de condición de FWP \_ \_ se ha \_ reautorizado**
</dt> <dd> <dl> <dt>



Comprueba un cambio de directiva en lugar de una nueva conexión.

Filtrar capas:

-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}
-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**la \_ marca de condición de FWP \_ es un \_ \_ \_ enlace comodín**
</dt> <dd> <dl> <dt>



Comprueba si la aplicación especificó una dirección comodín al enlazar con una dirección de red local.

Nivel de filtrado:

-   \_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**la \_ marca de condición de FWP \_ es un punto de \_ \_ conexión sin formato \_**
</dt> <dd> <dl> <dt>



Comprueba si el punto de conexión local que está enviando y recibiendo tráfico es un punto de conexión sin formato.

Filtrar capas:

-   \_Transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   \_Transporte de salida de capa FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   \_Datos de datagrama de capa FWPM \_ \_ \_ {V4 \| 6}
    > [!Note]  
    > Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

     

-   \_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}
-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**la \_ marca de condición de FWP \_ \_ es \_ FRAGMENT**
</dt> <dd> <dl> <dt>



Comprueba si la estructura de la \_ lista de búferes de red que se \_ pasa a un controlador de llamada es un fragmento de paquetes IP.

Filtrar capas:

-   FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ \_ \_ IPPACKET \_ V {4 \| 6} \_ descartar


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**la \_ marca de condición de FWP \_ es un \_ \_ grupo de fragmentos \_**
</dt> <dd> <dl> <dt>



Comprueba si la \_ \_ estructura de la lista de búferes de red pasada a un controlador de llamada describe una lista vinculada de fragmentos de paquetes.

Nivel de filtrado:

-   \_Capa FWPM \_ IPFORWARD \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**la \_ marca de condición de FWP \_ \_ es \_ Natt de \_ \_ reclasificación de IPSec**
</dt> <dd> <dl> <dt>



Indica que el mismo paquete se está reclasificando en el nivel de transporte, cuando la corrección de compatibilidad de IPsec NAT traduce el valor del puerto remoto.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**la \_ marca de condición de FWP \_ \_ requiere \_ \_ clasificación Ale**
</dt> <dd> <dl> <dt>



Indica que el paquete se reclasificará en la capa de recepción y aceptación de ALE.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**la \_ marca de condición de FWP \_ es un \_ \_ \_ enlace implícito**
</dt> <dd> <dl> <dt>



Comprueba si Windows Sockets realiza un enlace implícito.

Solo está disponible en Windows Vista y Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**la \_ marca de condición de FWP \_ \_ se \_ reensambla**
</dt> <dd> <dl> <dt>



Comprueba si el paquete se ha reensamblado.

> [!Note]  
> Solo está disponible en Windows Server 2008, Windows Vista con SP1 y versiones posteriores.

 

Nivel de filtrado:

-   FWPM \_ de \_ entrada \_ IPPACKET \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**la \_ marca de condición de FWP \_ es la aplicación de \_ \_ nombre \_ \_ especificada**
</dt> <dd> <dl> <dt>



Comprueba si el nombre del equipo del mismo nivel al que espera la aplicación se ha recibido a través de una API como [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) y no se ha obtenido a través de la heurística de almacenamiento en caché.

> [!Note]  
> Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**la \_ marca de condición de FWP \_ \_ es \_ promiscuo**
</dt> <dd> <dl> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**la \_ marca de condición de FWP \_ \_ es \_ auth \_ FW**
</dt> <dd> <dl> <dt>



Comprueba si la conexión se ha autenticado de un extremo a otro, incluso si no se han comprobado los paquetes individuales.

> [!Note]  
> Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**la \_ marca de condición de FWP \_ \_ se está \_ reclasificando**
</dt> <dd> <dl> <dt>



Comprueba si el motor de filtrado está reclasificando una solicitud BIND o Listen anterior.

> [!Note]  
> Solo está disponible en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

Nivel de filtrado:

-   \_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}
-   \_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**la \_ marca de condición de FWP \_ es una \_ \_ conexión de proxy \_**
</dt> <dd> <dl> <dt>



Comprueba si la conexión usa un proxy.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**la \_ marca de condición de FWP \_ es un \_ \_ \_ bucle invertido de APPCONTAINER**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red es el tráfico de bucle invertido del contenedor de la aplicación.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**la \_ marca de condición de FWP \_ \_ no es un \_ \_ \_ bucle invertido de APPCONTAINER**
</dt> <dd> <dl> <dt>



Comprueba si el tráfico de red es un tráfico de bucle invertido que no es de aplicación.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**la \_ marca de condición de FWP \_ \_ está \_ reservada**
</dt> <dd> <dl> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**la \_ marca de condición de FWP \_ \_ está \_ respetando la \_ \_ autorización de la Directiva**
</dt> <dd> <dl> <dt>



Indica que se está realizando la clasificación actual para respetar la intención de que una aplicación de la tienda Windows redirigida se conecte a un host especificado. Esta clasificación contendrá los mismos valores de campo clasificables que si la aplicación nunca se redirigió. La marca también indica que se invocará una clasificación futura para que coincida con el destino Redirigido efectivo. Si la aplicación se redirige a un servicio de proxy para su inspección, también significa que se invocará una clasificación futura en la conexión del proxy. Los controladores de llamadas normalmente deben permitir esta clasificación.

> [!Note]  
> Solo está disponible en Windows 8 y Windows Server 2012.

 

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Las marcas siguientes especifican el motivo por el que se va a autorizar una conexión previamente autorizada. Estas marcas y las capas de filtrado donde se pueden usar se definen como se indica a continuación.

> [!Note]  
> Estas condiciones de filtrado solo están disponibles en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**cambio en la \_ \_ Directiva de motivo de reautorización de la condición de \_ \_ FWP \_**
</dt> <dd> <dl> <dt>



Indica que la conexión se ha reautorizado debido a que se han agregado o quitado filtros.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**causa de reautor de la condición de FWP \_ \_ \_ \_ nueva \_ interfaz de llegada \_**
</dt> <dd> <dl> <dt>



Indica que el paquete llegó desde una interfaz desconocida.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**condición de FWP reautor de la razón de la \_ \_ \_ \_ nueva \_ salto \_ de la interfaz**
</dt> <dd> <dl> <dt>



Indica que el paquete se va a deshacer de una interfaz desconocida.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**\_paso de \_ creación de \_ Perfil de \_ motivo \_ de la condición de FWP**
</dt> <dd> <dl> <dt>



Indica que el paquete ha pasado a través de interfaces de más de una categoría de red.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**\_conclusión de \_ reautorización de la condición de \_ \_ FWP \_**
</dt> <dd> <dl> <dt>



Indica que ahora se permite completar una conexión retenida previamente.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**\_motivo de REautorización de la condición de FWP propiedades de \_ \_ \_ IPSec \_ \_ modificadas**
</dt> <dd> <dl> <dt>



Indica que las propiedades de IPsec han cambiado o que la conexión ha cambiado de texto no cifrado a una conexión segura.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**Estado de la \_ \_ inspección de \_ \_ flujo medio \_ \_ de la condición de FWP REAUTORICE**
</dt> <dd> <dl> <dt>



Indica que ahora se está inspeccionando una conexión TCP establecida previamente.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**error de la \_ \_ propiedad de \_ socket de motivo de reautorización de la \_ \_ condición de FWP \_**
</dt> <dd> <dl> <dt>



Indica que se han establecido las propiedades de socket una vez que se ha autorizado y establecido una conexión.

Nivel de filtrado:

-   FWPM de \_ autenticación Ale de capa de la \_ \_ \_ conexión \_ V {4 \| 6}
-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**condición de FWP \_ \_ reautor de la causa del \_ \_ nuevo \_ paquete de entrada de \_ MCAST \_ BCAST \_**
</dt> <dd> <dl> <dt>



Indica que se están volviendo a autorizar nuevos paquetes entrantes de multidifusión o difusión en las llamadas de aceptación de recepción de ALE \_ \_ .

Nivel de filtrado:

-   Aceptación de recepción de Ale de FWPM de capa de la \_ \_ \_ \_ \_ aceptación \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Las marcas siguientes especifican las propiedades de socket que están relacionadas con si una aplicación desea recibir tráfico de cruce seguro del perímetro. Estas marcas y las capas de filtrado donde se pueden usar se definen como se indica a continuación.

> [!Note]  
> Estas condiciones de filtrado solo están disponibles en Windows Server 2008 R2, Windows 7 y versiones posteriores.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**la \_ marca de propiedad del socket de condición de FWP \_ \_ es el \_ \_ \_ \_ Puerto RPC del sistema \_**
</dt> <dd> <dl> <dt>



Indica que la aplicación se comunica con un puerto RPC dinámico.

Nivel de filtrado:

-   \_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}
-   \_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**identificador de propiedad de socket de condición de FWP \_ \_ \_ \_ \_ permitir \_ \_ tráfico perimetral**
</dt> <dd> <dl> <dt>



Indica que la aplicación desea recibir tráfico específico de cruce seguro del perímetro.

Nivel de filtrado:

-   \_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}
-   \_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**identificador de propiedad del socket de condición de FWP \_ \_ \_ \_ \_ denegar el \_ \_ tráfico perimetral**
</dt> <dd> <dl> <dt>



Indica que la aplicación no desea recibir o procesar el tráfico específico de cruce seguro del perímetro.

Nivel de filtrado:

-   \_Escucha de \_ autenticación Ale de capa FWPM \_ \_ \_ V {4 \| 6}
-   \_Asignación de recursos Ale de FWPM capa \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Las marcas siguientes especifican los detalles de conexión relacionados con el filtrado L2.

> [!Note]  
> Estas condiciones de filtrado solo están disponibles en Windows 8 y Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**La \_ condición de FWP \_ L2 \_ es una \_ \_ Ethernet nativa**
</dt> <dd> <dl> <dt>



Indica que la conexión es un Ethernet nativo.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**La \_ condición de FWP \_ L2 \_ es \_ Wi-Fi**
</dt> <dd> <dl> <dt>



Indica que la conexión es Wi-Fi.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**La \_ condición de FWP \_ L2 \_ es \_ \_ banda ancha móvil**
</dt> <dd> <dl> <dt>



Indica que la conexión es banda ancha móvil.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**La \_ condición de FWP \_ L2 \_ es \_ Wi-Fi \_ Direct \_ Data**
</dt> <dd> <dl> <dt>



Indica que la conexión es Wi-Fi directa.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**La \_ condición de FWP \_ L2 \_ es \_ VM2VM**
</dt> <dd> <dl> <dt>



Indica que la conexión se encuentra entre las máquinas virtuales.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**La \_ condición de FWP \_ L2 \_ tiene un paquete con \_ formato incorrecto \_**
</dt> <dd> <dl> <dt>



Indica que un paquete parece tener un formato incorrecto.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**La \_ condición de FWP \_ L2 \_ es \_ grupo de \_ fragmentos IP \_**
</dt> <dd> <dl> <dt>



Indica un grupo de fragmentos de paquetes IP.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**Condición de FWP \_ \_ L2 \_ si el \_ conector \_ está presente**
</dt> <dd> <dl> <dt>



Indica que hay un conector presente.

Nivel de filtrado:

-   \_Ethernet de \_ \_ \_ fotogramas Mac de entrada \_ de capa FWPM
-   marco de Mac de entrada de capa de FWPM \_ \_ \_ \_ \_ nativo
-   \_Ethernet de \_ \_ \_ fotogramas de \_ Mac de salida de capa de FWPM
-   \_marco Mac de salida de capa de FWPM \_ \_ \_ \_ nativo


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Fwptypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

