---
title: Error común Suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor
description: Cuando los proveedores de seguridad se registran en el servidor con la función RpcServerRegisterAuthInfo, se agrega una opción, no un requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071423"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>Error común: Suponiendo que RpcServerRegisterAuthInfo impide que usuarios no autorizados llamen al servidor

Cuando los proveedores de seguridad se registran en el servidor con la [**función RpcServerRegisterAuthInfo,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) se agrega una opción, no un requisito. Esto significa que los registros anteriores **con RpcServerRegisterAuthInfo** no se reemplazan. Esto también significa que los clientes no autenticados todavía pueden conectarse. Al llamar a **la función RpcServerRegisterAuthInfo,** los clientes no autenticados no pueden conectarse; todavía pueden conectarse, pero se producirá un error en las llamadas de función como [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcGetAuthorizationContextForClient.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) Por lo tanto, cuando se llama a la función **RpcServerRegisterAuthInfo,** los atacantes potenciales no se han descartado, sino que los clientes que deben tener acceso tienen la oportunidad de demostrar su identidad. Las comprobaciones deben seguir en su lugar para determinar si los atacantes potenciales están intentando conectarse.

 

 




