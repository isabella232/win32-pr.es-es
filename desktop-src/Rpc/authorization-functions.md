---
title: Funciones de autorización (RPC)
description: Cada vez que un programa de servidor recibe una solicitud de cliente para acceder a uno de los procedimientos remotos de administración, la biblioteca en tiempo de ejecución de RPC invoca una función de autorización predeterminada.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476620"
---
# <a name="authorization-functions"></a>Funciones de autorización

Cada vez que un programa de servidor recibe una solicitud de cliente para acceder a uno de los procedimientos remotos de administración, la biblioteca en tiempo de ejecución de RPC invoca una función de autorización predeterminada. Esta función usa el SSP para comprobar las credenciales del cliente y autorizar o rechazar la solicitud.

El programa de servidor puede invalidar la función de autorización que proporciona el SSP. Invoque [**la función RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) y pásala a la dirección de la función de autorización. Una vez que el programa de servidor establece la función de autorización, la biblioteca en tiempo de ejecución de RPC la llama cada vez que el programa de servidor recibe una solicitud de cliente a una de las funciones de administración. Para obtener más información, vea [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids) [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)y [**RpcMgmtInqStats.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats)

 

 




