---
title: Recibir la respuesta asincrónica
description: Una vez que se le notifica que el servidor ha enviado una respuesta, el cliente llama a RpcAsyncCompleteCall con el identificador asincrónico para que pueda recibir la respuesta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421290"
---
# <a name="receiving-the-asynchronous-reply"></a>Recibir la respuesta asincrónica

Una vez que se le notifica que el servidor ha enviado una respuesta, el cliente llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) con el identificador asincrónico para que pueda recibir la respuesta. Cuando **RpcAsyncCompleteCall** se ha completado correctamente, el parámetro de *respuesta* apunta a un búfer que contiene el valor devuelto de la función remota. Cualquier búfer proporcionado por el programa cliente como \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ [**in**](/windows/desktop/Midl/in),  \] los parámetros out para la función remota asincrónica contienen datos válidos. Si el cliente llama a **RpcAsyncCompleteCall** antes de que el servidor haya enviado la respuesta, se producirá un error en esa llamada y se devolverá un valor de RPC \_ S \_ Async \_ Call \_ Pending.

Si el programa cliente utiliza puertos o eventos de finalización de e/s para la notificación, debe llamar a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar el puerto o el identificador cuando ya no los necesite.

 

 