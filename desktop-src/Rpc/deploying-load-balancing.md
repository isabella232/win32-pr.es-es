---
title: Implementación del equilibrio de carga
description: Implementación del equilibrio de carga
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36d1ba29aedd5e94c29095d18fb84790ec4b76956ea20bc2ffd584b5a6a179f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021855"
---
# <a name="deploying-load-balancing"></a>Implementación del equilibrio de carga

A continuación se muestra el entorno de implementación y el caso de uso típicos en los que se usa el equilibrador de carga RPC:![equilibrio de carga rpc](images/rpc-load-balancing.png)

1.  El cliente RPC realiza una conexión RPC/HTTP a la granja de servidores.
2.  La conexión se reenvía a través de la red a un equilibrador de carga front-end
3.  El equilibrador de carga front-end elige un servidor para dar servicio a la solicitud. En este ejemplo, el equilibrador de carga front-end reenvía la conexión al servidor 1.
4.  El servicio equilibrador de carga RPC reebaba la conexión. Determina que se trata de la primera conexión del cliente y asocia la conexión con el servidor local, Server 1.
5.  El cliente realiza una segunda solicitud RPC/HTTP.
6.  La solicitud se reenvía a través de la red al equilibrador de carga front-end.
7.  El equilibrador de carga front-end elige un servidor para dar servicio a la solicitud. En este caso, el equilibrador de carga front-end elige Server 2 para dar servicio a la solicitud.
8.  El servicio Load Balancer RPC de la conexión. Reconoce que el servidor 1 está atendidas las conexiones desde este cliente.
9.  La conexión se reenvía al servidor 1.

 

 




