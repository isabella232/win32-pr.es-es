---
title: Rendimiento de RPC Sugerencias
description: En esta sección se de abordan varias sugerencias de rendimiento para desarrollar servidores RPC de alto rendimiento. En esta sección se proporcionan muchas sugerencias que hacen referencia al cliente RPC. El desarrollo de un cliente RPC correctamente permite que el servidor RPC realice menos trabajo.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0946b83aae296f7b908babca9135c35a0afe8dbe7588a8292ad66bc19dc6488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928074"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Rendimiento de RPC Sugerencias

En esta sección se de abordan varias sugerencias de rendimiento para desarrollar servidores RPC de alto rendimiento. En esta sección se proporcionan muchas sugerencias que hacen referencia al cliente RPC. El desarrollo de un cliente RPC correctamente permite que el servidor RPC realice menos trabajo.

## <a name="use-kerberos"></a>Uso de Kerberos

Si se usa la seguridad, use Kerberos. En el lado servidor, Kerberos no requiere acceso al KDC. Esto mueve la carga de trabajo del servidor al cliente, lo que proporciona servidores de mejor rendimiento.

## <a name="use-static-identity-tracking"></a>Uso del seguimiento de identidades estáticas

Si se usa la seguridad, intente usar el seguimiento de identidades estáticas. El seguimiento de identidades estáticas es más barato en términos de uso de recursos que el seguimiento dinámico de identidades. Si cambia la identidad del cliente y el servidor no debe tener en cuenta el cambio, use el seguimiento dinámico en lugar de crear un identificador de enlace diferente para cada identidad. Pero si la identidad es la misma, asegúrese de que RPC es consciente de ese hecho para evitar que RPC realice comprobaciones de identidad modificada cada vez.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Uso de la función RpcGetAuthorizationContextForClient

Si necesita comprobar el acceso en Windows XP, use la [**función RpcGetAuthorizationContextForClient.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) Los contextos Authz resultantes permiten comprobaciones de acceso muy rápidas, que se almacenan en caché de forma eficaz en el tiempo de ejecución de RPC.

## <a name="do-not-modify-the-token-unless-necessary"></a>No modificar el token a menos que sea necesario

Si se usa el seguimiento dinámico de identidades, no modifique el token de subproceso o proceso a menos que sea absolutamente necesario. Incluso si se modifica para la configuración que tenía anteriormente, el token suele ser lo suficientemente diferente al sistema de seguridad para desencadenar el establecimiento de un nuevo contexto de seguridad.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Considere la posibilidad de serializar el modo mixto para los identificadores de contexto.

El modo de serialización predeterminado para el identificador de contexto se serializa (exclusivo). Considere la posibilidad de realizar todas las llamadas que no modifiquen el estado del identificador de contexto en modo de serialización compartida. Consulte [**RpcSsContextLockExclusive para**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) obtener más información.

 

 




