---
title: Funciones de autorización (RPC)
description: Cada vez que un programa de servidor recibe una solicitud de cliente para acceder a uno de los procedimientos remotos de administración, la biblioteca rpc en tiempo de ejecución invoca una función de autorización predeterminada.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47234f83ae76ab6ee29ed434099ba3e4a7dbb3f9c7a01a2448d0cb0dad0267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023424"
---
# <a name="authorization-functions"></a>Funciones de autorización

Cada vez que un programa de servidor recibe una solicitud de cliente para acceder a uno de los procedimientos remotos de administración, la biblioteca rpc en tiempo de ejecución invoca una función de autorización predeterminada. Esta función usa el SSP para comprobar las credenciales del cliente y autorizar o rechazar la solicitud.

El programa de servidor puede invalidar la función de autorización que proporciona el SSP. Invoque la [**función RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) y pásala a la dirección de la función de autorización. Una vez que el programa de servidor establece la función de autorización, la biblioteca rpc en tiempo de ejecución la llama cada vez que el programa de servidor recibe una solicitud de cliente a una de las funciones de administración. Para obtener más información, vea [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)y [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 




