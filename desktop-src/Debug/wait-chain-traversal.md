---
description: El cruce seguro de cadenas de espera (WCT) permite que los depuradores diagnostiquen los bloqueos y bloqueos de la aplicación.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Recorrido de cadena de espera
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/04/2021
ms.locfileid: "103906289"
---
# <a name="wait-chain-traversal"></a>Recorrido de cadena de espera

El cruce seguro de cadenas de espera (WCT) permite que los depuradores diagnostiquen los bloqueos y bloqueos de la aplicación.

Una *cadena de espera* es una secuencia alterna de subprocesos y objetos de sincronización en los que cada subproceso espera el objeto que sigue. Cada objeto que sigue es, a su vez, propiedad del subproceso subsiguiente de la cadena.

Un subproceso espera un objeto de sincronización desde el momento en que el subproceso solicita el objeto hasta que el subproceso lo ha adquirido. Este "bloqueo" es propiedad de un subproceso desde el momento en que el subproceso lo adquiere hasta que el subproceso lo libera. En otras palabras, cuando el subproceso 1 está esperando un bloqueo propiedad del subproceso 2, el subproceso 1 está "esperando" para el subproceso 2.

WCT admite las siguientes primitivas de sincronización:

- [Llamada a procedimiento local avanzado (ALPC)](../etw/alpc.md)
- [Modelo de objetos componentes (COM)](../com/the-component-object-model.md)
- [Secciones críticas](../sync/critical-section-objects.md)
- [Mutexes](../sync/mutex-objects.md) (Clases Mutex)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- Operaciones de [espera](../sync/wait-functions.md) en [procesos y subprocesos](../procthread/processes-and-threads.md)

Para recuperar la cadena de espera de uno o más subprocesos, cree una sesión de WCT con las funciones [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) y [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) . Las sesiones de WCT se representan mediante un identificador de tipo **HWCT**.

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>Las sesiones pueden ser sincrónicas o asincrónicas

Las sesiones sincrónicas no se pueden cancelar y bloquean el subproceso que realiza la llamada hasta que se haya recuperado una cadena de espera.

Las sesiones asincrónicas no bloquean el subproceso que realiza la llamada y pueden ser canceladas por la aplicación mediante la función [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) . Los resultados de las operaciones asincrónicas se ponen a disposición a través de una función de devolución de llamada [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) proporcionada por la aplicación.

En el caso de las sesiones asincrónicas, el llamador puede especificar un puntero a una estructura de datos de contexto a través de [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (este mismo puntero se pasa a la función de devolución de llamada [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) ).

La estructura de datos de contexto es definida por el usuario y opaca a WCT. La aplicación puede utilizarla para comunicar el contexto entre una consulta de WCT y una función de devolución de llamada. Normalmente, se pasa un identificador de eventos a través de esta estructura y, cuando se ejecuta la devolución de llamada, se señala este evento y se informa a un subproceso de supervisión de que se ha completado la consulta.

Vea [usar WCT](using-wct.md) para obtener un ejemplo de cruce de cadenas de espera.

## <a name="related-topics"></a>Temas relacionados

[Uso de WCT](using-wct.md), [referencia de WCT](wct-reference.md), [MSDN Magazine 2007 julio-Bugslayer: permisión de cadena de espera](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)