---
title: Administrador de tablas de enrutamiento
description: El administrador de tabla de enrutamiento es el repositorio central de información de enrutamiento de todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676115"
---
# <a name="routing-table-manager"></a>Administrador de tablas de enrutamiento

El administrador de tabla de enrutamiento es el repositorio central de información de enrutamiento de todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS). Notifica a los clientes cuando se han producido cambios y permite a los clientes intercambiar información privada.

El administrador de tablas de enrutamiento proporciona información de enrutamiento a todos los clientes interesados, como los protocolos de enrutamiento, los programas de administración y los programas de supervisión. El administrador de tablas de enrutamiento también determina la mejor ruta para cada red de destino que se conoce en los protocolos de enrutamiento. El administrador de tablas de enrutamiento determina esta ruta en función de las prioridades del Protocolo de enrutamiento y de las métricas asociadas a las rutas. La persona que administra el enrutador puede configurar las prioridades del Protocolo de enrutamiento mediante la consola de administración de RRAS.

El administrador de tablas de enrutamiento pasa la información de la mejor ruta a los reenviadores (uno por familia de direcciones o uno por cada interfaz) y a todos los clientes interesados.

Cada cliente se registra con el administrador de tablas de enrutamiento y, a su vez, recibe un identificador que el cliente utiliza para agregar o eliminar rutas. Los clientes pueden recuperar la información almacenada en la tabla de enrutamiento. Además, los clientes pueden registrarse con el administrador de tablas de enrutamiento para recibir una notificación de los cambios en la mejor ruta a un destino.

 

 




