---
title: Equilibrio de carga de RPC
description: Equilibrio de carga de RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473600"
---
# <a name="rpc-load-balancing"></a>Equilibrio de carga de RPC

El equilibrio de carga rpc de Microsoft está pensado para proporcionar una solución escalable para escenarios que exigen una carga elevada de RPC a [través del tráfico HTTP.](remote-procedure-calls-using-rpc-over-http.md) El objetivo Load Balancer rpc es garantizar que una granja de servidores pueda atender el tráfico RPC/HTTP para mejorar la escalabilidad. Para ello, RPC debe asegurarse de que todas las conexiones de un proceso de cliente sean atendidas por el mismo punto de conexión de servidor en la granja de servidores. La rpc Load Balancer se implementa como un servicio que se ejecuta junto con el servicio RPC sobre proxy HTTP.

Para habilitar el equilibrio de carga, el servicio de equilibrio de carga rpc que se ejecuta en cada uno de los servidores se comunica entre sí para determinar el servidor preferido para la conexión de cliente inicial. Este proceso se denomina arbitraje y se produce en el momento de la conexión de cliente inicial. Para reducir el tráfico entre servidores, el servicio de equilibrio de carga de RPC elige el punto de conexión local para dar servicio a la conexión si el cliente aún no está asociado a un servidor. Para una conexión de cliente determinada, el resultado del arbitraje es una de estas dos posibilidades:

-   Si el cliente ya ha realizado una conexión, el servidor que recibirá primero la conexión controlará las conexiones posteriores.
-   Si se trata de la primera conexión del cliente, el arbitraje dará como resultado que el servidor local controle la conexión y, por tanto, todas las conexiones del cliente. Esta información, una vez determinada, se confirma en los demás servicios rpc Load Balancer de la granja de servidores, informándolos así del servidor que administra todas las solicitudes del cliente.

En esta sección se proporciona información general sobre el equilibrio de carga de RPC en los temas siguientes:

-   [Implementación del equilibrio de carga](deploying-load-balancing.md)
-   [Configuración del equilibrio de carga](configuring-load-balancing.md)
-   [Procedimientos recomendados de equilibrio de carga](load-balancing-best-practices.md)

## <a name="requirements"></a>Requisitos

El servicio de equilibrio de carga RPC se admite en servidores que ejecutan Windows Server 2008 R2 o posterior y clientes que ejecutan Windows 7 o versiones posteriores de Windows.

El servicio de proxy RPC, el servicio de equilibrio de carga de RPC y los puntos de conexión de servidor deben ejecutarse en la misma máquina. Además, todos los servidores de la granja de servidores deben ser capaces de atender el punto de conexión solicitado. Para obtener información sobre cómo configurar el servicio de proxy RPC y el servicio de equilibrio de carga de RPC, vea [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) (Configuración de equipos para RPC a través de HTTP) y [Configuring Load Balancing](configuring-load-balancing.md)(Configurar equilibrio de carga), respectivamente.

## <a name="limitations"></a>Limitaciones

En este momento, el equilibrio de carga de RPC solo admite una granja de servidores por recurso. Todos los servidores de todas las granjas de servidores también deben ser capaces de atender todos los recursos.

 

 




