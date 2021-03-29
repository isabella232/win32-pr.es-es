---
title: Error común suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor
description: Cuando los proveedores de seguridad se registran en el servidor con la función RpcServerRegisterAuthInfo, se agrega una opción, no un requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778876"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>Error común: suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor

Cuando los proveedores de seguridad se registran en el servidor con la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , se agrega una opción, no un requisito. Esto significa que los registros anteriores con **RpcServerRegisterAuthInfo** no se reemplazan. Esto también significa que los clientes no autenticados todavía pueden conectarse. Al llamar a la función **RpcServerRegisterAuthInfo** , no se impide que los clientes no autenticados se conecten; todavía se pueden conectar, pero se producirá un error en las llamadas de función como [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) . Por tanto, cuando se llama a la función **RpcServerRegisterAuthInfo** , los atacantes potenciales no se han extraído, sino que los clientes que deberían tener acceso tienen la oportunidad de demostrar su identidad. Las comprobaciones deben seguir vigentes para determinar si los posibles atacantes intentan conectarse.

 

 




