---
title: Qué proveedor de seguridad usar
description: Todas las demás cosas son iguales, use \_ el \_ Protocolo RPC c authn \_ GSS \_ Kerberos o RPC \_ c \_ authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776105"
---
# <a name="which-security-provider-to-use"></a>Qué proveedor de seguridad usar

Todas las demás cosas son iguales, use \_ el \_ Protocolo RPC c authn \_ GSS \_ Kerberos o RPC \_ c \_ authn \_ GSS \_ Negotiate. Cada una de ellas proporciona el servicio más seguro y escalable. Si usa \_ \_ \_ la negociación de GSS de RPC C authn \_ en el servidor, permite que los clientes de nivel inferior, como los clientes NTLM, se conecten al servidor. Si eso no es deseable, limite la elección a la opción de \_ \_ Kerberos C authn \_ GSS \_ solo para Kerberos, o llame a [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para determinar qué proveedor de seguridad usa el cliente y deniegue el acceso a los clientes mediante NTLM. El método preferido para establecer el proveedor de seguridad que utiliza el cliente es la función [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




