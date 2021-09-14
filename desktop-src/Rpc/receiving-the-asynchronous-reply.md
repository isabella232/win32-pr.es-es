---
title: Recepción de la respuesta asincrónica
description: Una vez notificado que el servidor ha enviado una respuesta, el cliente llama a RpcAsyncCompleteCall con el identificador asincrónico para que pueda recibir la respuesta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361909"
---
# <a name="receiving-the-asynchronous-reply"></a>Recepción de la respuesta asincrónica

Una vez notificado que el servidor ha enviado una respuesta, el cliente llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) con el identificador asincrónico para que pueda recibir la respuesta. Cuando **RpcAsyncCompleteCall se** ha completado correctamente, el parámetro *Reply* apunta a un búfer que contiene el valor devuelto de la función remota. Los búferes proporcionados por el programa cliente como out o en , los parámetros out de la función \[ [](/windows/desktop/Midl/out-idl) \] remota asincrónica \[ [](/windows/desktop/Midl/in)contienen  \] datos válidos. Si el cliente llama a **RpcAsyncCompleteCall** antes de que el servidor haya enviado la respuesta, esa llamada producirá un error y devolverá un valor de RPC \_ S \_ ASYNC \_ CALL \_ PENDING.

Si el programa cliente usa eventos o puertos de finalización de E/S para la notificación, debe llamar a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar el puerto o controlar cuando ya no los necesite.

 

 