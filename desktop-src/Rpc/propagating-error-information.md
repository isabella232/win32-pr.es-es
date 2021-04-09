---
title: Propagar información de errores
description: La propagación de la información de error extendida permite a los servidores que reciben un \_ \_ error de RPC S \ o a cualquier otro código de error, para permitir que el tiempo de ejecución de RPC propague la información recibida a sus llamadores.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903736"
---
# <a name="propagating-error-information"></a>Propagar información de errores

La propagación de la información de error extendida permite a los servidores que reciben un \_ \_ \* error de RPC S, o cualquier otro código de error de este asunto, permitir que el tiempo de ejecución de RPC propague la información recibida a sus llamadores. Todo lo que debe hacer el servidor es llamar a [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) al encontrar un error irrecuperable. El tiempo de ejecución de RPC se encarga de encadenar la información de error extendida, si la hubiera, que provoca el error irrecuperable para notificar el error irrecuperable en sí, siempre que el código de error dado a **RpcRaiseException** o **RpcAsyncAbortCall** sea el mismo que el código de error que produce el error irrecuperable.

 

 




