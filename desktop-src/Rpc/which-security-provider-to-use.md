---
title: Qué proveedor de seguridad se va a usar
description: Todas las demás cosas son iguales, use RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS o RPC C \_ \_ \_ AUTHN GSS \_ NEGOTIATE.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b89bdb10eb95952183b2a992fd12a668e79b0716f3c453f597d2241323c4ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010453"
---
# <a name="which-security-provider-to-use"></a>Qué proveedor de seguridad se va a usar

Todas las demás cosas son iguales, use RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS o RPC C \_ \_ \_ AUTHN GSS \_ NEGOTIATE. Cada una de ellas proporciona el servicio más escalable y seguro. Si usa RPC \_ C \_ AUTHN GSS NEGOTIATE en el servidor, esto permite que los clientes de nivel inferior, como los clientes \_ NTLM, se conecten \_ al servidor. Si no quiere, limite la opción a RPC C AUTHN GSS KERBEROS solo, o llame a \_ \_ \_ \_ [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para determinar qué proveedor de seguridad usa el cliente y deniegue el acceso a los clientes mediante NTLM. El método preferido para establecer qué proveedor de seguridad usa el cliente es [**la función RpcServerInqCallAttributes.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa)

 

 




