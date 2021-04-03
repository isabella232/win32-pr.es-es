---
title: Ordenación causal de llamadas asincrónicas
description: En una aplicación RPC asincrónica, es posible que un subproceso de cliente realice una segunda llamada asincrónica en un identificador de enlace antes de que se haya completado una llamada anterior realizada en ese controlador.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075643"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Ordenación causal de llamadas asincrónicas

En una aplicación RPC asincrónica, es posible que un subproceso de cliente realice una segunda llamada asincrónica en un identificador de enlace antes de que se haya completado una llamada anterior realizada en ese controlador. La biblioteca en tiempo de ejecución de RPC controla esta situación de la siguiente manera:

-   El mecanismo RPC asincrónico garantiza que las llamadas asincrónicas realizadas en el mismo identificador de enlace, en el mismo subproceso, en el mismo nivel de seguridad, se envíen en el orden en el que se realizaron. La ejecución real de las llamadas puede producirse sin orden.
-   Al igual que con las llamadas sincrónicas, las llamadas a procedimientos remotos asincrónicas de diferentes subprocesos de cliente se ejecutan simultáneamente.
-   Si una llamada asincrónica desde una aplicación cliente va seguida de una o más llamadas sincrónicas, la llamada asincrónica se puede ejecutar mientras se ejecutan las llamadas sincrónicas. Independientemente del estado de la llamada asincrónica, las llamadas sincrónicas se ejecutan en el orden en que se reciben en el servidor.
-   Si una aplicación cliente selecciona una ordenación no causal para un identificador de enlace determinado, deshabilita la serialización de ese identificador. Las aplicaciones habilitan la ordenación no causal mediante una llamada a [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con el parámetro *Option* establecido en el enlace no causal de RPC \_ C \_ \_ \_ y el parámetro *OptionValue* establecido en **true**. Para obtener más información, consulte [constantes de opciones de enlace](binding-option-constants.md).

 

 




