---
title: Limpieza de conexión inactiva
description: De forma predeterminada, las conexiones del grupo de subprocesos no se cierran hasta que se cierra toda la asociación.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc7a7d4cefcead53e9b92678867cd76ceb6fab7f1ab5f1a573cf75378cf2a5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020805"
---
# <a name="idle-connection-cleanup"></a>Limpieza de conexión inactiva

De forma predeterminada, las conexiones del grupo de subprocesos no se cierran hasta que se cierra toda la asociación. Esta directiva permite a los clientes con un gran número de subprocesos o identidades de seguridad realizar llamadas RPC al servidor de una manera eficaz. El inconveniente es que una cantidad excesiva de recursos se puede comprometer a mantener esas conexiones. Para administrar el proceso, RPC proporciona la [**función RpcMgmtEnableIdleCleanup.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) Esta función habilita la limpieza de la conexión inactiva; el cliente examina periódicamente el grupo de conexiones y cierra las conexiones que no se han usado recientemente. Si la asociación ha mantenido identificadores de contexto, la limpieza de la conexión inactiva cierra todas las conexiones inactivas, pero se asegura de que al menos una conexión se deja abierta, incluso si la conexión está inactiva (de lo contrario, el servidor obtiene las pérdidas de control de contexto). Si la asociación no ha mantenido identificadores de contexto, la limpieza de la conexión inactiva cierra todas las conexiones inactivas, aunque no deje ninguna conexión en el grupo.

En Windows XP, el tiempo de ejecución de RPC realiza un seguimiento del número de conexiones abiertas en una asociación y activa automáticamente la limpieza de la conexión inactiva si el número de conexiones de cualquier asociación supera un umbral determinado.

 

 




