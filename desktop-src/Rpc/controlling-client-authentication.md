---
title: Controlar la autenticación del cliente
description: El mejor método para autenticar un cliente es la instalación de una función de devolución de llamada de seguridad mediante la función RpcServerRegisterIf2 o RpcServerRegisterIfEx. acepta una función de devolución de llamada de seguridad como argumento.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903404"
---
# <a name="controlling-client-authentication"></a>Controlar la autenticación del cliente

El mejor método para autenticar un cliente es la instalación de una función de devolución de llamada de seguridad mediante la función [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) . acepta una función de devolución de llamada de seguridad como argumento. Cuando se llame a la función de devolución de llamada de seguridad, realice las comprobaciones necesarias. Se pueden comprobar los atributos de la conexión, la identidad del autor de la llamada o ambos. Para comprobar los atributos de una conexión, llame a la función [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) o [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) . Esto permite el filtrado de los clientes que no se autentican, los clientes que usan un proveedor de seguridad específico o los clientes que no usan una protección suficientemente segura (como la privacidad).

Para permitir el acceso a un subconjunto de los usuarios autenticados, use [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Esta función devuelve un contexto de cliente de authz que se puede usar para realizar comprobaciones de acceso muy sofisticadas. Por ejemplo, este método se puede usar para permitir el acceso solo a los Vicepresidentes de una organización durante el horario comercial normal y al CEO durante cualquier hora mediante Active Directory Services para asignar un nombre de usuario a su título. Se puede suplantar al usuario y se obtiene su nombre. Una vez que se conoce su identidad, se pueden realizar las comprobaciones deseadas.

 

 




