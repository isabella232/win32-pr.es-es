---
title: Publicación en un contenedor de sistema de dominio
description: El contenedor System de una partición de dominio contiene información operativa por dominio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publicación en un contenedor de sistema de dominio de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb86a49bb14bc88d64a723ca9ab289723ff4ac2b9259f112323e19a04497362c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184959"
---
# <a name="publishing-in-a-domain-system-container"></a>Publicación en un contenedor de sistema de dominio

El contenedor System de una partición de dominio contiene información operativa por dominio. Esto incluye la directiva de seguridad local predeterminada, el seguimiento de vínculos de archivos, las reuniones de red y los contenedores para puntos de conexión de registro y resolución de sockets de Windows (RnR) y servicio de nombres RPC (RpcN). De forma predeterminada, el contenedor del sistema está oculto y proporciona un lugar adecuado para almacenar objetos que son de interés para los administradores, pero no para los usuarios finales.

Los servicios que no están vinculados a un único host pueden querer crear sus SCP en el contenedor System de una partición de dominio. Esta alternativa puede ser útil para los servicios con réplicas instaladas en varios hosts, cada réplica que proporciona servicios idénticos a los clientes en todo el dominio. Permite agrupar todos los objetos para el servicio replicado en un único contenedor.

Los servicios que crean objetos específicos del servicio en el contenedor System deben hacer lo siguiente:

1.  Cree un subcon contenedor de contenedor de clase **de objeto** como elemento secundario inmediato del contenedor System. Asigne a este contenedor un nombre que lo identifique claramente como perteneciente al servicio.
2.  Cree los objetos relacionados con el servicio en este subcon contenedor. Por ejemplo, NetMeeting usa el contenedor Meetings para publicar objetos de reunión de red.

Un proveedor con varios productos puede usar una estrategia similar para agrupar objetos relacionados con el servicio para todos sus productos. En este caso, podría crear un objeto **contenedor** con un nombre que identifique claramente al proveedor; a **continuación, cree** objetos de contenedor para cada servicio como secundarios del contenedor del proveedor. Cree el contenedor específico del proveedor como elemento secundario del contenedor Del sistema.

 

 




