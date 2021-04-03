---
title: Equilibrio de carga de RPC
description: Equilibrio de carga de RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075165"
---
# <a name="rpc-load-balancing"></a>Equilibrio de carga de RPC

El equilibrio de carga de Microsoft RPC está diseñado para proporcionar una solución escalable para escenarios en los que se exige una carga elevada de tráfico de [RPC a través de http](remote-procedure-calls-using-rpc-over-http.md) . El objetivo principal del Load Balancer RPC es asegurarse de que una granja de servidores puede atender el tráfico RPC/HTTP para mejorar la escalabilidad. Para ello, RPC debe asegurarse de que el mismo punto de conexión de servidor en la granja de servidores presta servicio a todas las conexiones de un proceso de cliente. La Load Balancer RPC se implementa como un servicio que se ejecuta junto con el servicio de proxy RPC a través de HTTP.

Para habilitar el equilibrio de carga, el servicio de equilibrio de carga de RPC que se ejecuta en cada uno de los servidores se comunica entre sí para determinar el servidor preferido para la conexión de cliente inicial. Este proceso se denomina arbitraje y se produce en el momento de la conexión inicial del cliente. Para reducir el tráfico entre servidores, el servicio de equilibrio de carga de RPC elige el extremo local para atender la conexión si el cliente no está ya asociado a un servidor. Para una conexión de cliente determinada, el resultado del arbitraje es una de estas dos posibilidades:

-   Si el cliente ya ha realizado una conexión, el servidor que debe recibir la conexión por primera vez controlará las conexiones posteriores.
-   Si esta es la primera conexión desde el cliente, el arbitraje dará lugar al servidor local que controla la conexión y, por tanto, a todas las conexiones del cliente. Esta información, una vez determinada, se confirmará en los otros servicios de Load Balancer de RPC de la granja de servidores, lo que les informará del servidor que controla todas las solicitudes del cliente.

En esta sección se proporciona información general sobre el equilibrio de carga de RPC en los temas siguientes:

-   [Implementar el equilibrio de carga](deploying-load-balancing.md)
-   [Configurar el equilibrio de carga](configuring-load-balancing.md)
-   [Prácticas recomendadas de equilibrio de carga](load-balancing-best-practices.md)

## <a name="requirements"></a>Requisitos

El servicio de equilibrio de carga de RPC es compatible con los servidores que ejecutan Windows Server 2008 R2 o posterior y los clientes que ejecutan Windows 7 o versiones posteriores de Windows.

El servicio de proxy RPC, el servicio de equilibrio de carga de RPC y los puntos de conexión de servidor deben ejecutarse en el mismo equipo. Además, todos los servidores de la granja de servidores deben ser capaces de atender el punto de conexión solicitado. Para obtener información sobre la configuración del servicio de proxy RPC y el servicio de equilibrio de carga de RPC, vea [configurar equipos para RPC a través de http](configuring-computers-for-rpc-over-http.md) y [configurar el equilibrio de carga](configuring-load-balancing.md), respectivamente.

## <a name="limitations"></a>Limitaciones

En este momento, el equilibrio de carga RPC solo admite una granja de servidores por recurso. Todos los servidores de todas las granjas de servidores deben ser capaces de atender también todos los recursos.

 

 




