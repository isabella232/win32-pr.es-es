---
title: Acerca de la versión 1 del administrador de tablas de enrutamiento
description: El administrador de tabla de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 1
- RRAS del servicio de enrutamiento y acceso remoto, versión 1 del administrador de tablas de enrutamiento, descrito
- RRAS de administrador de tablas de enrutamiento versión 1
- Administrador de tablas de enrutamiento versión 1 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075845"
---
# <a name="about-routing-table-manager-version-1"></a>Acerca de la versión 1 del administrador de tablas de enrutamiento

**Windows Server 2003:** Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las nuevas aplicaciones deben usar la API del administrador de tablas de enrutamiento versión 2.

El administrador de tabla de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS). El administrador de tablas de enrutamiento proporciona información de enrutamiento a todos los componentes interesados, como los protocolos de enrutamiento, los agentes de administración y los agentes de supervisión. El administrador de tablas de enrutamiento también determina la mejor ruta para cada red de destino conocida para los protocolos de enrutamiento. Determina esta ruta en función de las prioridades del Protocolo de enrutamiento y de las métricas asociadas a las rutas. Tenga en cuenta que el administrador puede configurar las prioridades del Protocolo de enrutamiento. A continuación, el administrador de tablas de enrutamiento pasa la información de la mejor ruta a los reenviadores y de nuevo a los protocolos de enrutamiento.

Cada protocolo de enrutamiento llama a [**RtmRegisterClient**](rtmregisterclient.md) para registrar con el administrador de tablas de enrutamiento. **RtmRegisterClient** devuelve un identificador que usa el protocolo de enrutamiento para agregar o eliminar entradas de ruta. **RtmRegisterClient** también permite que el protocolo de enrutamiento registre un objeto de evento con el administrador de tablas de enrutamiento. El administrador de tablas de enrutamiento señala este objeto de evento para notificar al Protocolo de enrutamiento los cambios en la información de la mejor ruta. Todos los demás componentes pueden obtener información almacenada en el administrador de tablas de enrutamiento a través de la enumeración de rutas.

 

 




