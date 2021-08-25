---
description: Wait Chain Traversal (WCT) permite a los depuradores diagnosticar bloqueos e interbloqueos de la aplicación.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Recorrido de cadena de espera
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 695e5298d0f56d0c53afcd146b19b1fc3c6ccf25e4ec12aec7f2b6b74fb64243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912315"
---
# <a name="wait-chain-traversal"></a>Recorrido de cadena de espera

Wait Chain Traversal (WCT) permite a los depuradores diagnosticar bloqueos e interbloqueos de la aplicación.

Una *cadena de espera* es una secuencia alterna de subprocesos y objetos de sincronización donde cada subproceso espera el objeto siguiente. Cada objeto que sigue es, a su vez, propiedad del subproceso posterior de la cadena.

Un subproceso espera un objeto de sincronización desde el momento en que el subproceso solicita el objeto hasta que el subproceso lo ha adquirido. Este "bloqueo" es propiedad de un subproceso desde el momento en que el subproceso lo adquiere, hasta que el subproceso lo libera. En otras palabras, cuando el subproceso 1 está esperando un bloqueo que es propiedad del subproceso 2, el subproceso 1 está "esperando" para el subproceso 2.

WCT admite las siguientes primitivas de sincronización:

- [Llamada a procedimiento local avanzado (ALPC)](../etw/alpc.md)
- [Modelo de objetos componentes (COM)](../com/the-component-object-model.md)
- [Secciones críticas](../sync/critical-section-objects.md)
- [Mutexes](../sync/mutex-objects.md) (Clases Mutex)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- [Operaciones de](../sync/wait-functions.md) espera en [procesos y subprocesos](../procthread/processes-and-threads.md)

Para recuperar la cadena de espera de uno o varios subprocesos, cree una sesión de WCT mediante las funciones [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) y [GetThreadWaitChain.](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) Las sesiones WCT se representan mediante un identificador de **tipo HWCT**.

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>Las sesiones pueden ser sincrónicas o asincrónicas

Las sesiones sincrónicas no se pueden cancelar y bloquear el subproceso de llamada hasta que se recupere una cadena de espera.

Las sesiones asincrónicas no bloquean el subproceso que realiza la llamada y la aplicación puede cancelarla mediante la [función CloseThreadWaitChainSession.](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) Los resultados de las operaciones asincrónicas están disponibles a través de una función de devolución de llamada [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) proporcionada por la aplicación.

Para las sesiones asincrónicas, el autor de la llamada puede especificar un puntero a una estructura de datos de contexto a través de [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (este mismo puntero se pasa a la función de devolución de llamada [WaitChainCallback).](/windows/win32/api/wct/nc-wct-pwaitchaincallback)

La estructura de datos de contexto es definida por el usuario y opaca para WCT. La aplicación puede usarla para comunicar el contexto entre una consulta WCT y una función de devolución de llamada. Normalmente, se pasa un identificador de evento a través de esta estructura y, cuando se ejecuta la devolución de llamada, se señala este evento y se informa a un subproceso de supervisión de que se ha completado la consulta.

Consulte [Uso de WCT para](using-wct.md) obtener un ejemplo de recorrido de cadena de espera.

## <a name="related-topics"></a>Temas relacionados

[Uso de WCT,](using-wct.md) [Referencia de WCT,](wct-reference.md) [MSDN Magazine 2007 Julio - Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)