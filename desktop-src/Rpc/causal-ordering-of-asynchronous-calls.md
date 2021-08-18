---
title: Orden causal de las llamadas asincrónicas
description: En una aplicación RPC asincrónica, es posible que un subproceso de cliente realice una segunda llamada asincrónica en un identificador de enlace antes de que se haya completado una llamada anterior realizada en ese identificador.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbafc5f9166d28a80d514abd4ebea20ab01ea32f542561e2108feae4a5769458
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932299"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Orden causal de las llamadas asincrónicas

En una aplicación RPC asincrónica, es posible que un subproceso de cliente realice una segunda llamada asincrónica en un identificador de enlace antes de que se haya completado una llamada anterior realizada en ese identificador. La biblioteca en tiempo de ejecución de RPC controla esta situación de la siguiente manera:

-   El mecanismo RPC asincrónico garantiza que las llamadas asincrónicas realizadas en el mismo identificador de enlace, en el mismo subproceso, en el mismo nivel de seguridad, se envíen en el orden en que se realizaron. La ejecución real de las llamadas puede producirse fuera de orden.
-   Al igual que con las llamadas sincrónicas, las llamadas a procedimientos remotos asincrónicos de distintos subprocesos de cliente se ejecutan simultáneamente.
-   Si una llamada asincrónica desde una aplicación cliente va seguida de una o varias llamadas sincrónicas, la llamada asincrónica se puede ejecutar mientras se ejecutan las llamadas sincrónicas. Independientemente del estado de la llamada asincrónica, las llamadas sincrónicas se ejecutan en el orden en que el servidor las recibe.
-   Si una aplicación cliente selecciona un orden no obligatorio para un identificador de enlace determinado, deshabilita la serialización de ese identificador. Las aplicaciones habilitan la ordenación no segura mediante una llamada [**a RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con el parámetro *Option* establecido en RPC \_ C OPT BINDING \_ \_ NONCAUSAL y el \_ parámetro *OptionValue* establecido en **TRUE.** Para obtener más información, [vea Binding Option Constants](binding-option-constants.md).

 

 




