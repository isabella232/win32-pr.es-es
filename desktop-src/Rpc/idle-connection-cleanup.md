---
title: Limpieza de conexión inactiva
description: De forma predeterminada, las conexiones del grupo de subprocesos no se cierran hasta que se cierra toda la asociación.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903213"
---
# <a name="idle-connection-cleanup"></a>Limpieza de conexión inactiva

De forma predeterminada, las conexiones del grupo de subprocesos no se cierran hasta que se cierra toda la asociación. Esta directiva permite a los clientes con un gran número de subprocesos o identidades de seguridad realizar llamadas RPC al servidor de una manera eficaz. El inconveniente es que se puede confirmar una cantidad imordenada de recursos para mantener esas conexiones. Para administrar el proceso, RPC proporciona la función [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) . Esta función habilita la limpieza de la conexión inactiva; el cliente examina periódicamente el grupo de conexiones y cierra las conexiones que no se han usado recientemente. Si la Asociación ha mantenido identificadores de contexto, la limpieza de la conexión inactiva cierra todas las conexiones inactivas, pero garantiza que al menos una conexión se deja abierta, incluso si la conexión está inactiva (de lo contrario, el servidor obtiene las ejecuciones de identificador de contexto). Si la asociación no ha mantenido los identificadores de contexto, la limpieza de la conexión inactiva cierra todas las conexiones inactivas, aunque no deje ninguna conexión en el grupo.

En Windows XP, el tiempo de ejecución de RPC realiza un seguimiento del número de conexiones abiertas en una asociación y activa automáticamente la limpieza de la conexión inactiva si el número de conexiones en cualquier asociación supera un determinado umbral.

 

 




