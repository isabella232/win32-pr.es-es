---
title: Seguridad para subprocesos
description: Todas las funciones de esta API son seguras para llamar a la vez desde subprocesos diferentes. Sin embargo, cada objeto que se pasa como parámetro a las funciones tiene un comportamiento de subprocesamiento específico, tal y como se describe a continuación.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Servicios Web de seguridad para subprocesos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797289"
---
# <a name="thread-safety"></a>Seguridad para subprocesos

Todas las funciones de esta API son seguras para llamar a la vez desde subprocesos diferentes. Sin embargo, cada objeto que se pasa como parámetro a las funciones tiene un comportamiento de subprocesamiento específico, tal y como se describe a continuación.


Los siguientes identificadores son de un solo subproceso y no admiten operaciones simultáneas para una instancia determinada:

-   [\_montón WS](ws-heap.md)
-   [\_mensaje WS](ws-message.md)
-   [búfer de WS \_ XML \_](ws-xml-buffer.md)
-   [\_lector de XML de WS \_](ws-xml-reader.md)
-   [\_escritor de XML de WS \_](ws-xml-writer.md)
-   [ERROR de WS \_](ws-error.md)
-   [\_contexto de operación WS \_](ws-operation-context.md)
-   [Directiva de WS \_](ws-policy.md)
-   [metadatos de WS \_](ws-metadata.md)
-   [\_token de seguridad de WS \_](ws-security-token.md)
-   [\_contexto de seguridad de WS \_](ws-security-context.md)

Los siguientes identificadores son de subprocesamiento libre y admiten operaciones simultáneas para una instancia determinada:

-   [canal de WS \_](ws-channel.md)
-   [agente de escucha de WS \_](ws-listener.md)
-   [\_host de servicio WS \_](ws-service-host.md)
-   [\_proxy de servicio WS \_](ws-service-proxy.md)

Para todos estos identificadores, los subprocesos se definen en términos de operaciones (no llamadas a función). Una operación se define de forma diferente para las funciones invocadas sincrónicamente frente a las funciones invocadas de forma asincrónica:

-   En el caso de las funciones invocadas sincrónicamente, la operación está pendiente durante la ejecución de la función.
-   En el caso de las funciones invocadas de forma asincrónica, si la función devuelve un código de retorno distinto de **WS \_ S \_ Async** , la operación está pendiente durante la ejecución de la función. Sin embargo, si la función devuelve **WS \_ S \_ Async** , la operación está pendiente hasta que se invoca la [**devolución de \_ \_ llamada de WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) . Para obtener más información sobre cómo invocar funciones de forma asincrónica, vea el tema sobre el [modelo asincrónico](asynchronous-model.md) . Para ver los códigos de error, vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md).

Si no se sigue el contrato de subprocesos de un objeto, se producirá un comportamiento indefinido.

 

 




