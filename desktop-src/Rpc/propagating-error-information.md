---
title: Propagar información de error
description: La propagación de información de error extendida permite a los servidores que reciben un error RPC S\, o cualquier otro código de error, permitir que el tiempo de ejecución de RPC propague la información que recibió a sus \_ \_ llamadores.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361922"
---
# <a name="propagating-error-information"></a>Propagar información de error

La propagación de información de error extendida permite a los servidores que reciben un error de RPC S, o cualquier otro código de error en ese caso, permitir que el tiempo de ejecución de RPC propague la información que recibió a sus \_ \_ \* llamadores. Todo lo que debe hacer el servidor es llamar a [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) al encontrar un error irresanable. El tiempo de ejecución de RPC se encarga de encadenar la información de error extendida, si existe, lo que hace que el error irresal informe del propio error grave, siempre y cuando el código de error dado a **RpcRaiseException** o **RpcAsyncAbortCall** sea el mismo que el código de error que causa el error grave.

 

 




