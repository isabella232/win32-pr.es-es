---
title: Escuchando llamadas a procedimientos remotos
description: Una vez que un programa de servidor registra su información de enlace y anuncia su presencia en una base de datos de servicio de nombres, puede empezar a escuchar el punto de conexión para las llamadas a procedimientos remotos.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075008"
---
# <a name="listening-for-remote-procedure-calls"></a>Escuchando llamadas a procedimientos remotos

Una vez que un programa de servidor registra su información de enlace y anuncia su presencia en una base de datos de servicio de nombres, puede empezar a escuchar el punto de conexión para las llamadas a procedimientos remotos. Los programas de servidor llaman a la función [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para supervisar los extremos de las invocaciones de cliente de procedimientos remotos.

La especificación de DCE de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica que no debe devolver hasta que una función del programa del servidor llame a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening). La implementación de Microsoft RPC de **RpcServerListen** usa dos parámetros que no aparecen en la especificación de DCE: *DontWait* y *MinimumCallThreads*. El programa de servidor puede pasar un valor distinto de cero para el parámetro *DontWait* . Si es así, la función **RpcServerListen** se devolverá inmediatamente. Use la rutina [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para realizar la operación de espera normalmente asociada a **RpcServerListen**.

 

 




