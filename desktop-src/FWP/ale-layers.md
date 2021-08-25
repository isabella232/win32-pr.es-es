---
title: Capas de ALE
description: El cumplimiento de la capa de aplicación (ALE) consta de varias capas de filtrado y muchas capas de descarte que coinciden.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9d13c7b5493171caa7216e8f2991e0350b79dd46dca612f241c9446cafa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901015"
---
# <a name="ale-layers"></a>Capas de ALE

El cumplimiento de la capa de aplicación (ALE) consta de varias capas de filtrado y muchas capas de descarte que coinciden. Todas las capas Windows motor de filtrado de la Plataforma de filtrado de filtros (WFP), incluido ALE, se describen en [**Identificadores**](management-filtering-layer-identifiers-.md)de capa de filtrado . Este tema contiene una descripción más detallada de las capas de filtrado que forman parte de ALE.

## <a name="resource_assignment"></a>ASIGNACIÓN \_ DE RECURSOS

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las operaciones de enlace de red, explícitas o implícitas.

Si un filtro de esta capa coincide para autorizar la creación de sockets sin formato, se establecerá la marca [**FWP \_ CONDITION FLAG IS RAW \_ \_ \_ \_ ENDPOINT.**](filtering-condition-flags-.md)

Si se encuentra un filtro en esta capa para autorizar la recepción del modo promiscuo, el campo [**FWP \_ CONDITION \_ ALE \_ PROMISCUOUS \_ MODE (MODO PROMISCUOUS de FWP CONDITION ALE)**](filtering-condition-identifiers-.md) se establecerá en SIO \_ RCVALL. Para obtener una descripción de SIO \_ RCVALL, vea [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Esta es la única capa en la que se puede filtrar el modo promiscuo.

 

Si no se especifica ningún puerto durante **bind(),** es decir, el puerto se establece en 0 (cero), la pila TCP/IP seleccionará un puerto del intervalo de puertos dinámicos (19152-65535). El puerto seleccionado se clasificará en esta capa junto con la marca [**FWP \_ CONDITION FLAG IS WILDCARD \_ \_ \_ \_ BIND.**](filtering-condition-flags-.md)

Si no se especifica la dirección local en la llamada [**bind(),**](/windows/desktop/api/winsock/nf-winsock-bind) el campo de dirección local se establece en [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)

## <a name="auth_listen"></a>ESCUCHA DE \_ AUTENTICACIÓN

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las llamadas de escucha [**TCP().**](/windows/desktop/api/winsock2/nf-winsock2-listen)

## <a name="auth_recv_accept"></a>AUTH \_ RECV \_ ACCEPT

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las llamadas TCP [**accept(),**](/windows/desktop/api/winsock2/nf-winsock2-accept) para los primeros paquetes UDP (unidifusión) desde una tupla de puerto o dirección remota única y para los primeros mensajes ICMP entrantes sin errores (unidifusión) con un tipo ICMP único, código e identificador.

> [!Note]  
> Los protocolos que no son TCP o ICMP se tratan como UDP.

 

Los paquetes TCP recibidos por sockets sin procesar se controlan de forma similar al tráfico UDP. Es decir, solo se filtrarán el primer envío [**TCP()**](/windows/desktop/api/winsock2/nf-winsock2-send) y el primer [**TCP recv()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre sockets sin formato.

## <a name="auth_connect"></a>AUTH \_ CONNECT

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las llamadas TCP [**connect(),**](/windows/desktop/api/winsock2/nf-winsock2-connect) para los primeros paquetes UDP enviados a una tupla de puerto y dirección remota únicas, y para los primeros mensajes ICMP salientes sin errores con un tipo, código e identificador ICMP únicos.

> [!Note]  
> Los protocolos que no son TCP o ICMP se tratan como UDP.

 

Los paquetes TCP enviados por sockets sin procesar se controlan de forma similar al tráfico UDP. Es decir, solo se filtrarán el primer envío [**TCP()**](/windows/desktop/api/winsock2/nf-winsock2-send) y el primer [**TCP recv()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre sockets sin formato.

## <a name="flow_established"></a>FLOW \_ ESTABLISHED

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ FLOW ESTABLISHED \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) coincide después de que se haya completado correctamente un protocolo de enlace triple TCP. Para el tráfico que no es TCP, el filtro coincide inmediatamente después de que se coincidan los filtros de las capas **AUTH \_ RECV \_ ACCEPT** o **AUTH \_ CONNECT.**

Un filtro de esta capa no debe devolver Block ni Permit.

Esta capa la usan los controladores de llamada para realizar un seguimiento del estado de conexión, que se describe en detalle en la [documentación de Windows Driver Kit.](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)

## <a name="resource_release"></a>VERSIÓN DE \_ RECURSOS

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ RESOURCE RELEASE \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) coincide después de liberar los recursos asignados a través de **RESOURCE \_ ASSIGNMENT.**

## <a name="endpoint_closure"></a>CIERRE DEL \_ PUNTO DE CONEXIÓN

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ ENDPOINT CLOSURE \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) coincide cuando se cierra un flujo TCP conectado o un punto de conexión de sockets UDP.

## <a name="connect_redirect"></a>REDIRECCIÓN DE \_ CONNECT

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) permite modificar direcciones remotas y puertos. La conexión saliente se redirigirá mientras dure esa conexión.

## <a name="bind_redirect"></a>REDIRECCIÓN DE \_ ENLACE

Un filtro en la capa [**FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) permite modificar la dirección local y los puertos del socket subyacente. El socket local se redirigirá durante la vigencia del socket.

## <a name="ale-discard-layers"></a>Capas ALE DISCARD

Para cada una de las capas de ALE descritas anteriormente, el motor de filtrado contiene una capa de descarte correspondiente. Las llamadas usan las capas de descarte de ALE con fines de registro. Los paquetes y las indicaciones que se han descartado en una de las capas de filtrado de ALE se indican en la capa de descarte de ALE correspondiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de la capa de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Filtrado con estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión de ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalización de Flow ALE](ale-flow-customization.md)
</dt> <dt>

[Flujos de paquetes TCP](tcp-packet-flows.md)
</dt> <dt>

[Flujos de paquetes UDP](udp-packet-flows.md)
</dt> <dt>

[Winsock Functions](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Filtrar marcas de condición**](filtering-condition-flags-.md)
</dt> <dt>

[**Condiciones de filtrado disponibles en cada capa de filtrado**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 