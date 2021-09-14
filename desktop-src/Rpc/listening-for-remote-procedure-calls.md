---
title: Escucha de llamadas a procedimientos remotos
description: Después de que un programa de servidor registre su información de enlace y anuncie su presencia en una base de datos de servicio de nombres, puede empezar a escuchar al punto de conexión para las llamadas a procedimiento remoto.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244532"
---
# <a name="listening-for-remote-procedure-calls"></a>Escucha de llamadas a procedimientos remotos

Después de que un programa de servidor registre su información de enlace y anuncie su presencia en una base de datos de servicio de nombres, puede empezar a escuchar al punto de conexión para las llamadas a procedimiento remoto. Los programas de servidor llaman a [**la función RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para supervisar los puntos de conexión en busca de invocaciones de cliente de procedimientos remotos.

La especificación DCE de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica que no debe devolverse hasta que una función del programa de servidor llame a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening). La implementación RPC de Microsoft **de RpcServerListen** usa dos parámetros que no aparecen en la especificación de DCE: *DontWait* y *MinimumCallThreads*. El programa de servidor puede pasar un valor distinto de cero para el *parámetro DontWait.* Si es así, la **función RpcServerListen** se devolverá inmediatamente. Use la [**rutina RpcMgmtWaitServerListen para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) realizar la operación de espera asociada normalmente a **RpcServerListen**.

 

 




