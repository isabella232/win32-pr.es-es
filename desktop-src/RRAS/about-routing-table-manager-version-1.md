---
title: Acerca de la versión 1 del Administrador de tablas de enrutamiento
description: El administrador de tablas de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el Servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, Routing Table Manager versión 1
- RRAS del servicio de enrutamiento y acceso remoto, Routing Table Manager versión 1, descrito
- RRAS de Routing Table Manager versión 1
- RRAS de Routing Table Manager versión 1, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069170"
---
# <a name="about-routing-table-manager-version-1"></a>Acerca de la versión 1 del Administrador de tablas de enrutamiento

**Windows Server 2003:** Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las nuevas aplicaciones deben usar la API de Routing Table Manager versión 2.

El administrador de tablas de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el Servicio de enrutamiento y acceso remoto (RRAS). El administrador de tablas de enrutamiento proporciona información de enrutamiento a todos los componentes interesados, como protocolos de enrutamiento, agentes de administración y agentes de supervisión. El administrador de tablas de enrutamiento también determina la mejor ruta a cada red de destino conocida por los protocolos de enrutamiento. Determina esta ruta en función de las prioridades del protocolo de enrutamiento y de las métricas asociadas a las rutas. Tenga en cuenta que el administrador puede configurar las prioridades del protocolo de enrutamiento. A continuación, el administrador de tablas de enrutamiento pasa la información de mejor ruta a los reenviadores y de vuelta a los protocolos de enrutamiento.

Cada protocolo de enrutamiento llama [**a RtmRegisterClient para**](rtmregisterclient.md) registrarse con el administrador de tablas de enrutamiento. **RtmRegisterClient devuelve** un identificador que usa el protocolo de enrutamiento para agregar o eliminar entradas de ruta. **RtmRegisterClient también** permite que el protocolo de enrutamiento registre un objeto de evento con el administrador de tablas de enrutamiento. El administrador de tabla de enrutamiento señala este objeto de evento para notificar al protocolo de enrutamiento los cambios en la información de mejor ruta. Todos los demás componentes pueden obtener información almacenada en el administrador de tablas de enrutamiento a través de la enumeración de rutas.

 

 




