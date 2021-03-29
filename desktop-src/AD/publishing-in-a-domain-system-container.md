---
title: Publicación en un contenedor de sistema de dominio
description: El contenedor System de una partición de dominio contiene información operativa por dominio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publicación en un contenedor de sistema de dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903097"
---
# <a name="publishing-in-a-domain-system-container"></a>Publicación en un contenedor de sistema de dominio

El contenedor System de una partición de dominio contiene información operativa por dominio. Esto incluye la Directiva de seguridad local predeterminada, el seguimiento de vínculos de archivos, las reuniones de red y los contenedores para el registro y la resolución de Windows Sockets (RnR) y los puntos de conexión del servicio de nombres de RPC (RpcNs). De forma predeterminada, el contenedor System está oculto y proporciona un lugar cómodo para almacenar objetos que son de interés para los administradores, pero no para los usuarios finales.

Los servicios que no están vinculados a un solo host pueden querer crear sus SCP en el contenedor del sistema de una partición de dominio. Esta alternativa puede ser útil para los servicios con réplicas instaladas en varios hosts, cada réplica proporciona servicios idénticos a los clientes de todo el dominio. Permite agrupar todos los objetos del servicio replicado bajo un único contenedor.

Los servicios que crean objetos específicos del servicio en el contenedor del sistema deben hacer lo siguiente:

1.  Cree un subcontenedor de **contenedor** de clase de objeto como un elemento secundario inmediato del contenedor del sistema. Asigne a este subcontenedor un nombre que lo identifique claramente como perteneciente al servicio.
2.  Cree los objetos relacionados con el servicio en este subcontenedor. Por ejemplo, NetMeeting usa el contenedor reuniones para publicar objetos de reunión de red.

Un proveedor con varios productos puede usar una estrategia similar para agrupar objetos relacionados con el servicio para todos sus productos. En este caso, podría crear un objeto **contenedor** con un nombre que identifique claramente al proveedor; a continuación, cree objetos de **contenedor** para cada servicio como elementos secundarios del contenedor del proveedor. Cree el contenedor específico del proveedor como un elemento secundario del contenedor del sistema.

 

 




