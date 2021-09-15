---
title: Administrador de tablas de enrutamiento
description: El administrador de tablas de enrutamiento es el repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que operan en el Servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271964"
---
# <a name="routing-table-manager"></a>Administrador de tablas de enrutamiento

El administrador de tablas de enrutamiento es el repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que operan en el Servicio de enrutamiento y acceso remoto (RRAS). Notifica a los clientes cuándo se han producido cambios y permite a los clientes intercambiar información privada.

El administrador de tablas de enrutamiento proporciona información de enrutamiento a todos los clientes interesados, como protocolos de enrutamiento, programas de administración y programas de supervisión. El administrador de tablas de enrutamiento también determina la mejor ruta a cada red de destino conocida por los protocolos de enrutamiento. El administrador de tablas de enrutamiento determina esta ruta en función de las prioridades del protocolo de enrutamiento y de las métricas asociadas a las rutas. La persona que administra el enrutador puede configurar prioridades de protocolo de enrutamiento mediante la consola de administración de RRAS.

El administrador de tablas de enrutamiento pasa la información de mejor ruta a los reenviadores (uno por familia de direcciones o uno por interfaz) y a todos los clientes interesados.

Cada cliente se registra con el administrador de tablas de enrutamiento y, a cambio, recibe un identificador que el cliente usa para agregar o eliminar rutas. Los clientes pueden recuperar información almacenada en la tabla de enrutamiento. Además, los clientes pueden registrarse con el administrador de tablas de enrutamiento para recibir notificaciones de cambios en la mejor ruta a un destino.

 

 




