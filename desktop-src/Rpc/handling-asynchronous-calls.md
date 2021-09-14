---
title: Control de llamadas asincrónicas
description: La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada al procedimiento remoto asincrónico.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259791"
---
# <a name="handling-asynchronous-calls"></a>Control de llamadas asincrónicas

La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada al procedimiento remoto asincrónico.

Si el servidor necesita anular una RPC asincrónica, llama a [**RpcAsyncAbortCall.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) Esta función realiza la misma limpieza del lado servidor que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) y propaga un código de excepción (proporcionado por la aplicación de servidor) de nuevo al cliente, salvo que no realiza la cálculo de la salida de los argumentos.

Para obtener un ejemplo de un procedimiento asincrónico, vea [Enviar la respuesta asincrónica](sending-the-asynchronous-reply.md).

 

 




