---
title: Implementar el equilibrio de carga
description: Implementar el equilibrio de carga
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268566"
---
# <a name="deploying-load-balancing"></a>Implementar el equilibrio de carga

A continuación se muestra el entorno de implementación típico y el caso de uso que se utiliza en el equilibrador de carga de RPC:![equilibrio de carga de RPC](images/rpc-load-balancing.png)

1.  El cliente RPC realiza una conexión RPC/HTTP con la granja de servidores.
2.  La conexión se reenvía a través de la red a un equilibrador de carga de front-end
3.  El equilibrador de carga de front-end elige un servidor para atender la solicitud. En este ejemplo, el equilibrador de carga de front-end reenvía la conexión al servidor 1.
4.  El servicio del equilibrador de carga de RPC arbitra la conexión. Determina que esta es la primera conexión desde el cliente y asocia la conexión con el servidor local, servidor 1.
5.  El cliente realiza una segunda solicitud RPC/HTTP.
6.  La solicitud se reenvía a través de la red al equilibrador de carga de front-end.
7.  El equilibrador de carga de front-end elige un servidor para atender la solicitud. En este caso, el equilibrador de carga front-end elige el servidor 2 para atender la solicitud.
8.  El servicio RPC Load Balancer arbitra la conexión. Reconoce que el servidor 1 está realizando el mantenimiento de las conexiones de este cliente.
9.  La conexión se reenvía al servidor 1.

 

 




