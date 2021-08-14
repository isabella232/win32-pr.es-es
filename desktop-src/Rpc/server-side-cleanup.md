---
title: Limpieza del lado servidor
description: Limpieza del lado servidor y llamada a procedimiento remoto (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 223cd15eb659a62c4a758098e9b0f70e977ebb069a2a305d2909b97b5fb12010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925297"
---
# <a name="server-side-cleanup"></a>Limpieza del lado servidor

Imagine el siguiente escenario:

Un cliente abre un identificador de contexto y, a continuación, detiene o pierde la conectividad con el servidor. ¿Cómo detecta el servidor que el cliente ha dado error y el identificador de contexto se debe ejecutar? Hay dos subscenarios: uno es que el cliente se cierra de forma ordenada. En tal caso, notifica al servidor que se está cerrando y el servidor puede limpiarlo, incluida la realización de operaciones de ejecución de contexto. Si el cliente no se cierra de forma ordenada o no puede notificar al servidor, el servidor usa keep alives para determinar si el cliente sigue estando disponible. En el lado servidor, la [**función RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) no tiene ningún efecto. En su lugar, el servidor usa la configuración global por equipo y mantener activo, que tiene como valor predeterminado aproximadamente dos horas. Si el cliente no responde a las conexiones continuas del servidor, la conexión se cierra. Cuando se cierran todas las conexiones a un proceso de cliente determinado, el servidor limpia y ejecuta los identificadores de contexto pendientes.

 

 




