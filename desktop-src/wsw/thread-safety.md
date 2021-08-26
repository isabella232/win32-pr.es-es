---
title: Seguridad para subprocesos
description: Todas las funciones de esta API son seguras para llamar simultáneamente desde subprocesos diferentes. Sin embargo, cada objeto pasado como parámetro a las funciones tiene un comportamiento de subprocesamiento específico, como se describe a continuación.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Servicios web de seguridad de subprocesos para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25528f3315fcfae95d07d973d4743548eb35ec84bf754fdaafe067bcaccc56f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054465"
---
# <a name="thread-safety"></a>Seguridad para subprocesos

Todas las funciones de esta API son seguras para llamar simultáneamente desde subprocesos diferentes. Sin embargo, cada objeto pasado como parámetro a las funciones tiene un comportamiento de subprocesamiento específico, como se describe a continuación.


Los siguientes identificadores son de subproceso único y no admiten operaciones simultáneas para una instancia determinada:

-   [WS \_ HEAP](ws-heap.md)
-   [WS \_ MESSAGE](ws-message.md)
-   [BÚFER XML DE WS \_ \_](ws-xml-buffer.md)
-   [WS \_ XML \_ READER](ws-xml-reader.md)
-   [WS \_ XML \_ WRITER](ws-xml-writer.md)
-   [ERROR \_ DE WS](ws-error.md)
-   [CONTEXTO DE OPERACIÓN DE WS \_ \_](ws-operation-context.md)
-   [WS \_ POLICY](ws-policy.md)
-   [METADATOS DE WS \_](ws-metadata.md)
-   [TOKEN DE SEGURIDAD DE WS \_ \_](ws-security-token.md)
-   [CONTEXTO DE SEGURIDAD DE WS \_ \_](ws-security-context.md)

Los siguientes identificadores son subprocesos libres y admiten operaciones simultáneas para una instancia determinada:

-   [WS \_ CHANNEL](ws-channel.md)
-   [AGENTE DE ESCUCHA DE WS \_](ws-listener.md)
-   [HOST DE \_ SERVICIO WS \_](ws-service-host.md)
-   [PROXY DE \_ SERVICIO WS \_](ws-service-proxy.md)

Para todos estos identificadores, el subprocesamiento se define en términos de operaciones (no llamadas a funciones). Una operación se define de forma diferente para las funciones invocadas sincrónicamente frente a las funciones invocadas de forma asincrónica:

-   Para las funciones invocadas sincrónicamente, la operación está pendiente durante la ejecución de la función.
-   Para las funciones invocadas de forma asincrónica, si la función devuelve un código de retorno distinto de **WS \_ S \_ ASYNC,** la operación está pendiente durante la ejecución de la función. Sin embargo, si la función devuelve **WS \_ S \_ ASYNC,** la operación está pendiente hasta que se invoca la devolución de llamada de [**WS \_ ASYNC. \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) Para obtener más información sobre cómo invocar funciones de forma asincrónica, vea el [tema Modelo](asynchronous-model.md) asincrónico. Para obtener códigos de error, [vea Windows valores devueltos de servicios web](windows-web-services-return-values.md).

Si no se sigue el contrato de subprocesos de un objeto, se produce un comportamiento indefinido.

 

 




