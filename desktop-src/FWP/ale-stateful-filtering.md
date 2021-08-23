---
title: Filtrado con estado de ALE
description: Los filtros instalados en las capas de aplicación de cumplimiento de la capa de aplicación (ALE) de Windows Filtering Platform (WFP) realizan el filtrado de red con estado.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbcb0517bb1e48c337f0ffd9589a1f39a3e4239aa0b3971dc81a71b402891f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388915"
---
# <a name="ale-stateful-filtering"></a>Filtrado con estado de ALE

Los filtros instalados en las capas de aplicación de cumplimiento de la capa de aplicación (ALE) de Windows Filtering Platform (WFP) realizan el filtrado de red con estado. Un *flujo de ALE* se usa como base para el filtrado con estado de ALE.

Un flujo de ALE es una manera de clasificar el tráfico de red agrupandolo en función de una dirección IP de origen, una dirección IP de destino, un puerto de origen, un puerto de destino y un protocolo. Un flujo de ALE podría ser genérico, es decir, uno o varios de los descriptores podrían coincidir con todo (o \* comodín). Por ejemplo, un flujo ALE de UDP genérico se describiría como Dirección IP de origen = , Dirección IP de destino = , Puerto de origen = , Puerto de destino \* = y Protocolo = \* \* \* UDP.

Una vez autorizada una conexión (las conexiones entrantes están autorizadas en la capa [**FWPM \_ LAYER \_ ALE \_ \_ AUTH RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) y las conexiones salientes en la capa **FWPM LAYER \_ \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}),** se crea un flujo de ALE de forma que, al bloquear un cambio de directiva, se permiten automáticamente todos los paquetes, entrantes y salientes, que pertenecen al mismo flujo de ALE. Dado que un cambio de directiva puede requerir el bloqueo de las conexiones permitidas previamente, los flujos de ALE deben volver a estar autorizados [cuando](ale-re-authorization.md) se produce un cambio de directiva.

El filtrado con estado de ALE reduce drásticamente el número de clasificaciones necesarias al clasificar solo el primer paquete que pertenece a un flujo de ALE. En comparación, el filtrado sin estado requiere la clasificación de todos los paquetes que atraviesan la red.

Un flujo de ALE tiene una dirección asociada, que es la dirección del primer paquete del flujo. Esto permite directivas más flexibles, ya que permite que las conexiones iniciadas de entrada tengan directivas diferentes de las conexiones iniciadas de salida.

## <a name="tcp-ale-flow"></a>Tcp ALE Flow

Un flujo de ALE para el tráfico TCP se identifica mediante la tupla de cinco de TCP/IP (dirección IP de origen, dirección IP de destino, puerto de origen, puerto de destino y protocolo).

Un flujo TCP ALE tiene la misma duración que un socket TCP conectado. Un socket TCP conectado podría ser un socket creado mediante [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) o un socket creado como resultado de una [**llamada accept().**](/windows/desktop/api/winsock2/nf-winsock2-accept)

ALE mantiene una relación uno a uno entre un flujo TCP ALE y un bloque de control TCP (TCB).

## <a name="udp-ale-flow"></a>Udp ALE Flow

> [!Note]  
> Los protocolos que no son TCP o ICMP se tratan como UDP.

 

Un flujo de ALE para el tráfico UDP se identifica mediante la tupla de cinco de TCP/IP (dirección IP de origen, dirección IP de destino, puerto de origen, puerto de destino y protocolo).

Se crea un flujo ALE udp basado en un socket UDP y representa el elemento remoto del mismo nivel con el que se comunica la aplicación. Un equipo remoto del mismo nivel se identifica mediante una tupla (Dirección IP de destino y puerto de destino).

Hay una relación uno a varios entre un socket UDP y los pares remotos con los que se habla.

Cuando se cierra el socket UDP local, se eliminarán todos los flujos de ALE asociados a él.

En ausencia de cierres de sockets, los flujos de ALE de unidifusión UDP tienen un tiempo de espera de inactividad [configurable](ale-flow-customization.md) que tiene como valor predeterminado 60 segundos. Si no se envían o reciben paquetes dentro de esta ventana, se eliminará el flujo de ALE. Este tiempo de espera predeterminado se reduce progresivamente cuando el número de flujos de ALE en todo el sistema alcanza un umbral determinado.

## <a name="icmp-ale-flow"></a>Icmp ALE Flow

Un flujo de ALE para el tráfico ICMP se identifica mediante la tupla de seis (dirección IP de origen, dirección IP de destino, tipo ICMP, código ICMP, protocolo e identificador ICMP). El identificador ICMP forma parte del flujo de ALE solo para el tráfico de eco/respuesta ICMP.

En ausencia de cierres de sockets, los flujos de ALE de unidifusión ICMP tienen un tiempo de espera de inactividad [configurable](ale-flow-customization.md) que tiene como valor predeterminado 60 segundos. Si no se envían o reciben paquetes dentro de esta ventana, se eliminará el flujo de ALE. Este tiempo de espera predeterminado se reduce progresivamente cuando el número de flujos de ALE en todo el sistema alcanza un umbral determinado.

Solo los mensajes ICMP que no son de error se indican a las capas de ALE. Los mensajes de error ICMP se pueden inspeccionar en capas DE \_ ERROR ICMP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de la capa de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Capas de ALE](ale-layers.md)
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
</dt> </dl>

 

 