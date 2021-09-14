---
title: Servicios de seguridad de MSMQ
description: Los mensajes RPC sincrónicos pueden usar cualquiera de las características de seguridad disponibles en el tiempo de ejecución de RPC. Consulte Seguridad para obtener más detalles.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071412"
---
# <a name="msmq-security-services"></a>Servicios de seguridad de MSMQ

Los mensajes RPC sincrónicos pueden usar cualquiera de las características de seguridad disponibles en el tiempo de ejecución de RPC. Consulte [Seguridad](security.md) para obtener más detalles.

Las llamadas a mensajes asincrónicos no pueden usar la seguridad RPC porque no hay ningún protocolo de enlace \[ [](/windows/desktop/Midl/message) \] entre el cliente y el servidor. De hecho, es posible que el servidor ni siquiera se esté ejecutando en el momento de la llamada. Para acceder a los servicios de seguridad proporcionados por Message Queuing Services (MSMQ), la aplicación cliente debe llamar a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para controlar el nivel de autenticación y privacidad de sus llamadas al servidor.

La aplicación de servidor puede llamar a [**RpcBindingInqAuthClient desde**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) una llamada a procedimiento remoto para determinar el nivel de seguridad de esa llamada. La asignación entre las constantes de seguridad RPC y la seguridad de MSMQ se muestra en la tabla siguiente.



| Nivel de seguridad rpc                | Descripción                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| RPC \_ AUTHN \_ LEVEL \_ NONE           | La llamada no está autenticada ni cifrada.                                                |
| RPC \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY | La llamada se autentica mediante la seguridad de MSMQ.                                             |
| PRIVACIDAD DE PKT DE NIVEL \_ DE \_ \_ AUTENTICACIÓN \_ RPC   | La llamada se autentica y cifra a medida que viaja entre la cola del cliente y el servidor. |



 

El servidor también puede forzar la autenticación y el cifrado de llamadas llamando a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) y estableciendo las marcas RPC \_ C MQ \_ \_ AUTHN \_ LEVEL \_ NONE, RPC C MQ \_ \_ \_ AUTHN LEVEL PKT INTEGRITY y \_ RPC C MQ \_ \_ \_ \_ \_ AUTHN \_ LEVEL PKT \_ \_ PRIVACY [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) en la estructura RPC POLICY.

 

 