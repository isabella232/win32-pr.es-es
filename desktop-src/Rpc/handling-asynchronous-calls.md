---
title: Controlar llamadas asincrónicas
description: La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada asincrónica al procedimiento remoto.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418813"
---
# <a name="handling-asynchronous-calls"></a>Controlar llamadas asincrónicas

La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada asincrónica al procedimiento remoto.

Si el servidor necesita anular una RPC asincrónica, llama a [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall). Esta función realiza la misma limpieza de servidor que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) y propaga un código de excepción (proporcionado por la aplicación de servidor) al cliente, salvo que no realiza la serialización de los argumentos de salida.

Para obtener un ejemplo de un procedimiento asincrónico, consulte [enviar la respuesta asincrónica](sending-the-asynchronous-reply.md).

 

 




