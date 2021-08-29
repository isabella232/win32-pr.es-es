---
title: Control de llamadas asincrónicas
description: La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada al procedimiento remoto asincrónico.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc05efd8c94a8b67ad68f2d19cacd6c46ed16e80ad6bbdf6df5b475b4dc68eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020845"
---
# <a name="handling-asynchronous-calls"></a>Control de llamadas asincrónicas

La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada al procedimiento remoto asincrónico.

Si el servidor necesita anular una RPC asincrónica, llama a [**RpcAsyncAbortCall.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) Esta función realiza la misma limpieza del lado servidor que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) y propaga un código de excepción (proporcionado por la aplicación de servidor) de nuevo al cliente, salvo que no realiza la cálculo de la salida de los argumentos.

Para obtener un ejemplo de un procedimiento asincrónico, vea [Enviar la respuesta asincrónica](sending-the-asynchronous-reply.md).

 

 




