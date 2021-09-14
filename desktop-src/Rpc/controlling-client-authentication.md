---
title: Control de la autenticación de cliente
description: El mejor método para autenticar un cliente es instalar una función de devolución de llamada de seguridad mediante las funciones RpcServerRegisterIf2 o RpcServerRegisterIfEx; acepta una función de devolución de llamada de seguridad como argumento.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259868"
---
# <a name="controlling-client-authentication"></a>Control de la autenticación de cliente

El mejor método para autenticar un cliente es instalar una función de devolución de llamada de seguridad mediante las [**funciones RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) [**o RpcServerRegisterIfEx;**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) acepta una función de devolución de llamada de seguridad como argumento. Cuando se llame a la función de devolución de llamada de seguridad, realice las comprobaciones necesarias. Se pueden comprobar los atributos de la conexión, la identidad del autor de la llamada o ambos. Para comprobar los atributos de una conexión, llame a [**la función RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) o [**RpcBindingInqAuthClient.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) Esto permite el filtrado de clientes que no están autenticados, clientes que usan un proveedor de seguridad específico o clientes que no usan una protección lo suficientemente segura (como la privacidad).

Para permitir el acceso a un subconjunto de los usuarios autenticados, use [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Esta función devuelve un contexto de cliente de Authz que se puede usar para realizar comprobaciones de acceso muy sofisticadas. Por ejemplo, este método podría usarse para permitir el acceso solo a los vicepresidentes de una organización durante el horario comercial normal y al director general durante cualquier hora mediante los servicios de Active Directory para asignar un nombre de usuario a su puesto. Se puede suplantar al usuario y obtener su nombre. Una vez conocida su identidad, se pueden realizar las comprobaciones deseadas.

 

 




