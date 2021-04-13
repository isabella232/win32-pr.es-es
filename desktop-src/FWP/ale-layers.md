---
title: Niveles ALE
description: El cumplimiento del nivel de aplicación (ALE) consta de varios niveles de filtrado y muchas capas de descarte coincidentes.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358836"
---
# <a name="ale-layers"></a>Niveles ALE

El cumplimiento del nivel de aplicación (ALE) consta de varias capas de filtrado y muchas capas de descarte coincidentes. Todas las capas del motor de filtrado de la plataforma de filtrado de Windows (WFP), incluida la EPA, se describen en [**filtrar los identificadores de capas**](management-filtering-layer-identifiers-.md). Este tema contiene una descripción más detallada de las capas de filtrado que forman parte de ALE.

## <a name="resource_assignment"></a>asignación de recursos \_

Un filtro en la capa de [**FWPM de \_ asignación de \_ \_ recursos Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las operaciones de enlace de red, explícita o implícita.

Si se compara un filtro en este nivel para autorizar la creación de un socket sin procesar, se establecerá la [**marca de condición de FWP \_ \_ \_ \_ sin formato \_**](filtering-condition-flags-.md) .

Si se compara un filtro en este nivel para autorizar la recepción del modo promiscuo, el campo del [**\_ \_ \_ \_ modo promiscuo**](filtering-condition-identifiers-.md) de la condición de FWP se establecerá en SiO \_ RCVALL. Para obtener una descripción de SIO \_ RCVALL, consulte [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Esta es la única capa en la que se puede filtrar el modo promiscuo.

 

Si no se especifica ningún puerto durante el **enlace ()**, es decir, el puerto se establece en 0 (cero), la pila TCP/IP seleccionará un puerto del intervalo de puertos dinámicos (19152 – 65535). El puerto seleccionado se clasificará en este nivel junto con la marca de condición de FWP como marca de [**\_ \_ \_ \_ \_ enlace de comodín**](filtering-condition-flags-.md) .

Si la dirección local no se especifica en la llamada [**BIND ()**](/windows/desktop/api/winsock/nf-winsock-bind) , el campo dirección local se establece en el valor de [**FWP \_ vacío**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

## <a name="auth_listen"></a>Escucha de autenticación \_

Un filtro en la capa de [**FWPM de \_ escucha de \_ \_ autenticación Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las llamadas de escucha de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-listen) .

## <a name="auth_recv_accept"></a>\_aceptación de recepción de autenticación \_

Un filtro en la capa de FWPM de mensajes de recepción de la autenticación Ale de la versión [**\_ \_ \_ \_ \_ Accept \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide con las llamadas de aceptación de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , para los primeros paquetes UDP (unidifusión) de una tupla de puerto/dirección remota única, y para los primeros mensajes entrantes de ICMP de error (unidifusión) con un tipo, código e identificador ICMP únicos.

> [!Note]  
> Los protocolos que no son TCP o ICMP se tratan como UDP.

 

Los paquetes TCP recibidos por Sockets sin formato se controlan de forma similar al tráfico UDP. Es decir, solo se filtrarán el primer envío de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-send) y el primer TCP [**RECV ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre Sockets sin formato.

## <a name="auth_connect"></a>conexión de autenticación \_

Se hace coincidir un filtro en la capa FWPM de la [**\_ \_ \_ conexión Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) de la capa de la conexión TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , para los primeros paquetes UDP enviados a una única dirección remota y a una tupla de puerto, y para los primeros mensajes salientes de ICMP que no son de error con un tipo, código e identificador de ICMP único.

> [!Note]  
> Los protocolos que no son TCP o ICMP se tratan como UDP.

 

Los paquetes TCP enviados por Sockets sin formato se controlan de forma similar al tráfico UDP. Es decir, solo se filtrarán el primer envío de TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-send) y el primer TCP [**RECV ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre Sockets sin formato.

## <a name="flow_established"></a>FLUJO \_ establecido

Un filtro en el [**flujo ALE de nivel FWPM establecido en la capa \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide después de que un protocolo de enlace de tres vías TCP se haya completado correctamente. En el caso del tráfico que no es TCP, se hace coincidir el filtro inmediatamente después de que se cumplan los filtros de la **\_ \_ aceptación de auth** o las capas de **\_ conexión de autenticación** .

Un filtro en esta capa no debe devolver Block ni permit.

Este nivel lo usan los controladores de llamada para realizar un seguimiento del estado de la conexión, que se describe en detalle en la documentación del [Kit de controladores de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="resource_release"></a>liberación de recursos \_

Una vez que se han liberado los recursos asignados a través de la **\_ asignación de recursos** , se ha liberado un filtro en la capa de la [**\_ \_ \_ \_ versión \_ V {4 \| 6} del recurso Ale de la capa FWPM**](management-filtering-layer-identifiers-.md) .

## <a name="endpoint_closure"></a>cierre de extremo \_

Un filtro en la capa de [**FWPM de \_ cierre del punto de \_ \_ conexión Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) coincide cuando se cierra un flujo TCP o un extremo de sockets UDP conectados.

## <a name="connect_redirect"></a>CONECTAR \_ REdirección

Un filtro en el nivel de [**FWPM de \_ \_ \_ redireccionamiento de la conexión Ale \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) de la capa se permite modificar los puertos y las direcciones remotas. La conexión saliente se redirigirá mientras dure la conexión.

## <a name="bind_redirect"></a>redirección de enlace \_

Un filtro en el nivel de [**\_ \_ \_ redirección de enlace Ale \_ \_ V {4 \| 6} de nivel FWPM**](management-filtering-layer-identifiers-.md) permite modificar la dirección local y los puertos del socket subyacente. El socket local se redirigirá a la duración del socket

## <a name="ale-discard-layers"></a>Capas de DESCARTe de ALE

Para cada uno de los niveles de ALE que se han descrito anteriormente, el motor de filtrado contiene una capa de descarte coincidente. Las capas de descarte de ALE se usan en las llamadas para fines de registro. Los paquetes y las indicaciones que se han descartado en uno de los niveles de filtrado ALE se indican a la capa de descarte de ALE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación del nivel de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Filtrado con estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalización del flujo ALE](ale-flow-customization.md)
</dt> <dt>

[Flujos de paquetes TCP](tcp-packet-flows.md)
</dt> <dt>

[Flujos de paquetes UDP](udp-packet-flows.md)
</dt> <dt>

[Funciones de Winsock](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Marcas de condición de filtrado**](filtering-condition-flags-.md)
</dt> <dt>

[**Condiciones de filtrado disponibles en cada nivel de filtrado**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 