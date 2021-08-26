---
title: Recepción de la respuesta asincrónica
description: Una vez notificado que el servidor ha enviado una respuesta, el cliente llama a RpcAsyncCompleteCall con el identificador asincrónico para que pueda recibir la respuesta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24500e176a7c5a36342b4188e687c557d48646deef1de39845257d8e04ff7c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018825"
---
# <a name="receiving-the-asynchronous-reply"></a>Recepción de la respuesta asincrónica

Una vez notificado que el servidor ha enviado una respuesta, el cliente llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) con el identificador asincrónico para que pueda recibir la respuesta. Cuando **RpcAsyncCompleteCall se** ha completado correctamente, el parámetro *Reply* apunta a un búfer que contiene el valor devuelto de la función remota. Los búferes proporcionados por el programa cliente como out o en , los parámetros out de la función \[ [](/windows/desktop/Midl/out-idl) \] remota asincrónica \[ [](/windows/desktop/Midl/in)contienen  \] datos válidos. Si el cliente llama a **RpcAsyncCompleteCall** antes de que el servidor haya enviado la respuesta, esa llamada producirá un error y devolverá un valor de RPC \_ S \_ ASYNC \_ CALL \_ PENDING.

Si el programa cliente usa eventos o puertos de finalización de E/S para la notificación, debe llamar a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar el puerto o controlar cuando ya no los necesite.

 

 