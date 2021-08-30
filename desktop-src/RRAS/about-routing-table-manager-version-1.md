---
title: Acerca de la versión 1 de Routing Table Manager
description: El administrador de tablas de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el Servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, Routing Table Manager versión 1
- RRAS del servicio de enrutamiento y acceso remoto, versión 1 de Routing Table Manager, descrito
- RRAS de Routing Table Manager versión 1
- RRAS de Routing Table Manager versión 1, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6552f07bb8307d662d6b0c6c602e91dbe092357e87d4224e84da8080984a4da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030765"
---
# <a name="about-routing-table-manager-version-1"></a>Acerca de la versión 1 de Routing Table Manager

**Windows Server 2003:** Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las nuevas aplicaciones deben usar la API de Routing Table Manager versión 2.

El administrador de tablas de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el Servicio de enrutamiento y acceso remoto (RRAS). El administrador de tablas de enrutamiento proporciona información de enrutamiento a todos los componentes interesados, como los protocolos de enrutamiento, los agentes de administración y los agentes de supervisión. El administrador de tablas de enrutamiento también determina la mejor ruta a cada red de destino conocida por los protocolos de enrutamiento. Determina esta ruta en función de las prioridades del protocolo de enrutamiento y de las métricas asociadas a las rutas. Tenga en cuenta que el administrador puede configurar las prioridades del protocolo de enrutamiento. A continuación, el administrador de tablas de enrutamiento pasa la información de mejor ruta a los reenviadores y de vuelta a los protocolos de enrutamiento.

Cada protocolo de enrutamiento llama [**a RtmRegisterClient para**](rtmregisterclient.md) registrarse con el administrador de tablas de enrutamiento. **RtmRegisterClient** devuelve un identificador que usa el protocolo de enrutamiento para agregar o eliminar entradas de ruta. **RtmRegisterClient también** permite que el protocolo de enrutamiento registre un objeto de evento con el administrador de tablas de enrutamiento. El administrador de tablas de enrutamiento indica a este objeto de evento que notifique al protocolo de enrutamiento los cambios en la información de mejor ruta. Todos los demás componentes pueden obtener información almacenada en el administrador de tablas de enrutamiento a través de la enumeración de rutas.

 

 




