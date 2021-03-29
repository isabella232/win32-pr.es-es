---
title: Filtrado con estado ALE
description: Los filtros instalados en las capas de aplicación de nivel de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) realizan el filtrado de red con estado.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077749"
---
# <a name="ale-stateful-filtering"></a>Filtrado con estado ALE

Los filtros instalados en las capas de aplicación de nivel de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) realizan el filtrado de red con estado. Un *flujo de Ale* se utiliza como base para el filtrado con estado ALE.

Un flujo ALE es una manera de clasificar el tráfico de red mediante su agrupación en función de una dirección IP de origen, una dirección IP de destino, un puerto de origen, un puerto de destino y un protocolo. Un flujo ALE podría ser genérico, es decir, uno o varios de los descriptores podrían coincidir con todo (o con comodín \* ). Por ejemplo, un flujo de ALE de UDP genérico se describiría como la dirección IP de origen = \* , la dirección IP de destino = \* , el puerto de origen =, el puerto de \* destino = \* y el protocolo = UDP.

Una vez que se autoriza una conexión (las conexiones entrantes están autorizadas en el nivel de FWPM de recepción de autenticación Ale de la capa de la versión de [**\_ \_ \_ \_ \_ aceptación \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) y las conexiones salientes en la capa de FWPM de la **\_ \_ \_ autenticación \_ \_ \| Ale** de la capa de), se crea un flujo ALE de modo que, con el bloqueo de un cambio de Directiva, todos los paquetes, entrantes y salientes, que pertenezcan al mismo flujo de Ale se permitan automáticamente. Dado que un cambio de directiva podría requerir el bloqueo de conexiones permitidas previamente, los flujos de ALE deben [reautorizarse](ale-re-authorization.md) cuando se produce un cambio de directiva.

El filtrado con estado ALE reduce drásticamente el número de clasificaciones necesarias mediante la clasificación solo del primer paquete que pertenece a un flujo ALE. Por comparación, el filtrado sin estado requiere la clasificación de cada paquete que atraviesa la red.

Un flujo ALE tiene una dirección asociada, que es la dirección del primer paquete del flujo. Esto permite directivas más flexibles, ya que permite que las conexiones iniciadas entrantes tengan diferentes directivas de las conexiones iniciadas salientes.

## <a name="tcp-ale-flow"></a>Flujo ALE TCP

Un flujo ALE para el tráfico TCP se identifica mediante la tupla de cinco de TCP/IP (dirección IP de origen, dirección IP de destino, Puerto de origen, Puerto de destino y Protocolo).

Un flujo ALE TCP tiene la misma duración que un socket TCP conectado. Un socket TCP conectado podría ser un socket creado mediante [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) o un socket creado como resultado de una llamada a [**accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .

ALE mantiene una relación uno a uno entre un flujo ALE TCP y un bloque de control TCP (TCB).

## <a name="udp-ale-flow"></a>Flujo ALE UDP

> [!Note]  
> Los protocolos que no son TCP o ICMP se tratan como UDP.

 

Un flujo ALE para el tráfico UDP se identifica mediante la tupla de cinco de TCP/IP (dirección IP de origen, dirección IP de destino, Puerto de origen, Puerto de destino y Protocolo).

Un flujo ALE UDP se crea basándose en un socket UDP y representa el elemento remoto del mismo nivel con el que se comunica la aplicación. Un elemento remoto del mismo nivel se identifica mediante una tupla (dirección IP de destino y puerto de destino).

Existe una relación de uno a varios entre un socket UDP y los pares remotos a los que se comunica.

Cuando se cierra el socket UDP local, se eliminarán todos los flujos de ALE asociados a él.

En ausencia de cierres de socket, los flujos ALE de unidifusión de UDP tienen un tiempo de espera de inactividad [configurable](ale-flow-customization.md) que tiene como valor predeterminado 60 segundos. Si no se envía ni se recibe ningún paquete en esta ventana, se eliminará el flujo de ALE. Este tiempo de espera predeterminado se acorta progresivamente cuando el número de flujos ALE en todo el sistema alcanza un umbral determinado.

## <a name="icmp-ale-flow"></a>Flujo ALE de ICMP

Un flujo ALE para el tráfico ICMP se identifica mediante las seis tuplas (dirección IP de origen, dirección IP de destino, tipo de ICMP, Código ICMP, protocolo e ID. de ICMP). El identificador de ICMP forma parte del flujo de ALE solo para el tráfico ICMP de eco y respuesta.

En ausencia de cierres de socket, los flujos ALE de unidifusión ICMP tienen un tiempo de espera de inactividad [configurable](ale-flow-customization.md) cuyo valor predeterminado es de 60 segundos. Si no se envía ni se recibe ningún paquete en esta ventana, se eliminará el flujo de ALE. Este tiempo de espera predeterminado se acorta progresivamente cuando el número de flujos ALE en todo el sistema alcanza un umbral determinado.

Solo se indican los mensajes que no son de error de ICMP a las capas ALE. Los mensajes de error de ICMP se pueden inspeccionar en capas de error de ICMP \_ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación del nivel de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Niveles ALE](ale-layers.md)
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
</dt> </dl>

 

 