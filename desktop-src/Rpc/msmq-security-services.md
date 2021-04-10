---
title: Servicios de seguridad de MSMQ
description: Los mensajes RPC sincrónicos pueden utilizar cualquiera de las características de seguridad disponibles en el tiempo de ejecución de RPC. Consulte seguridad para obtener más detalles.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149446"
---
# <a name="msmq-security-services"></a>Servicios de seguridad de MSMQ

Los mensajes RPC sincrónicos pueden utilizar cualquiera de las características de seguridad disponibles en el tiempo de ejecución de RPC. Consulte [seguridad](security.md) para obtener más detalles.

Las llamadas asincrónicas \[ [](/windows/desktop/Midl/message) \] a mensajes no pueden utilizar la seguridad RPC porque no hay ningún protocolo de enlace entre el cliente y el servidor. De hecho, es posible que el servidor no se esté ejecutando en el momento de la llamada. Para tener acceso a los servicios de seguridad proporcionados por servicios de Message Queuing (MSMQ), la aplicación cliente debe llamar a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para controlar el nivel de autenticación y privacidad de sus llamadas al servidor.

La aplicación de servidor puede llamar a [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) desde dentro de una llamada a procedimiento remoto para determinar el nivel de seguridad de esa llamada. En la tabla siguiente se muestra la asignación entre las constantes de seguridad de RPC y la seguridad de MSMQ.



| Nivel de seguridad de RPC                | Descripción                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| \_ \_ nivel ninguno de autenticación \_ RPC           | La llamada no se ha autenticado ni cifrado.                                                |
| integridad de la PKT de nivel de autenticación de RPC \_ \_ \_ \_ | La llamada se autentica mediante la seguridad de MSMQ.                                             |
| privacidad de nivel de autenticación de RPC \_ \_ \_ \_   | La llamada se autentica y se cifra mientras viaja entre la cola del cliente y del servidor. |



 

El servidor también puede forzar la autenticación y el cifrado de llamadas mediante una llamada a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) y el establecimiento de las marcas de privacidad de nivel de autenticación de RPC c MQ authn nivel \_ \_ \_ \_ \_ ninguno, RPC \_ c \_ MQ \_ authn \_ \_ \_ y RPC \_ c \_ MQ \_ authn \_ \_ \_ en la estructura de [**\_ directivas RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) .

 

 