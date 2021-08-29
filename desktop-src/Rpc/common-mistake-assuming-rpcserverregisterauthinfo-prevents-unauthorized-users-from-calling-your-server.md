---
title: Error común Suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor
description: Cuando los proveedores de seguridad se registran en el servidor con la función RpcServerRegisterAuthInfo, se agrega una opción, no un requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdcaee5f017b27610834949f7debcd027e605eed41bf1f809ea0135ec716c0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022495"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>Error común: Suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor

Cuando los proveedores de seguridad se registran en el servidor con la [**función RpcServerRegisterAuthInfo,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) se agrega una opción, no un requisito. Esto significa que los registros anteriores **con RpcServerRegisterAuthInfo** no se reemplazan. Esto también significa que los clientes no autenticados todavía pueden conectarse. Al llamar a **la función RpcServerRegisterAuthInfo,** los clientes no autenticados no pueden conectarse; todavía pueden conectarse, pero se producirá un error en las llamadas a funciones como [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcGetAuthorizationContextForClient.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) Por lo tanto, cuando se llama a la función **RpcServerRegisterAuthInfo,** los atacantes potenciales no se han descartado, sino que los clientes que deben tener acceso tienen la oportunidad de demostrar su identidad. Las comprobaciones deben seguir en su lugar para determinar si los atacantes potenciales están intentando conectarse.

 

 




