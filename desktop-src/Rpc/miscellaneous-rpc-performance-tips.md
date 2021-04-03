---
title: Sugerencias de rendimiento de RPC varias
description: En esta sección se describen varias sugerencias de rendimiento para desarrollar servidores RPC de alto rendimiento. En esta sección se proporcionan muchas sugerencias que hacen referencia al cliente RPC. Desarrollar correctamente un cliente RPC permite que el servidor RPC realice menos trabajo.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075355"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Sugerencias de rendimiento de RPC varias

En esta sección se describen varias sugerencias de rendimiento para desarrollar servidores RPC de alto rendimiento. En esta sección se proporcionan muchas sugerencias que hacen referencia al cliente RPC. Desarrollar correctamente un cliente RPC permite que el servidor RPC realice menos trabajo.

## <a name="use-kerberos"></a>Usar Kerberos

Si se usa la seguridad, use Kerberos. En el lado del servidor, Kerberos no requiere acceso al KDC. Esto mueve la carga de trabajo del servidor al cliente, lo que proporciona servidores de mejor rendimiento.

## <a name="use-static-identity-tracking"></a>Usar seguimiento de identidad estático

Si se usa la seguridad, intente usar el seguimiento de identidad estático. El seguimiento de identidades estáticas es más barato en términos de uso de recursos que el seguimiento de identidad dinámica. Si la identidad del cliente cambia y el servidor no debe ser consciente del cambio, use el seguimiento dinámico en lugar de crear un identificador de enlace diferente para cada identidad. Pero si la identidad es la misma, asegúrese de que RPC tenga en cuenta este hecho para evitar que RPC realice comprobaciones de la identidad modificada cada vez.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Usar la función RpcGetAuthorizationContextForClient

Si necesita comprobar el acceso en Windows XP, utilice la función [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) . Los contextos de authz resultantes permiten comprobaciones de acceso muy rápidas, que se almacenan en caché eficazmente en el tiempo de ejecución de RPC.

## <a name="do-not-modify-the-token-unless-necessary"></a>No modifique el token a menos que sea necesario.

Si se utiliza el seguimiento de identidad dinámica, no modifique el token de subproceso o proceso a menos que sea absolutamente necesario. Aunque se modifique a la configuración que tenía anteriormente, el token a menudo es lo suficientemente diferente para el sistema de seguridad para desencadenar el establecimiento de un nuevo contexto de seguridad.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Considerar la serialización en modo mixto para los identificadores de contexto

El modo de serialización predeterminado para el identificador de contexto es en serie (exclusivo). Considere la posibilidad de realizar todas las llamadas que no modifiquen el estado del identificador de contexto en el modo de serialización compartida. Vea [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) para obtener más información.

 

 




