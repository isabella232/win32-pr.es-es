---
title: Operaciones de eventos de temporizador
description: Operaciones de eventos de temporizador
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- temporizadores multimedia, eventos
- temporizadores, eventos
- timeSetEvent función)
- timeKillEvent función)
- iniciar eventos de temporizador
- eventos de temporizador único
- eventos de temporizador periódicos
- Cancelando eventos de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789748"
---
# <a name="timer-event-operations"></a>Operaciones de eventos de temporizador

Una vez establecida la resolución del temporizador de la aplicación, puede iniciar los eventos del temporizador mediante la función [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) . Esta función devuelve un identificador de temporizador que se puede usar para detener o identificar eventos de temporizador. Uno de los parámetros de la función es la dirección de una función de devolución de llamada [**TimeProc**](/previous-versions//dd757631(v=vs.85)) a la que se llama cuando tiene lugar el evento del temporizador.

Hay dos tipos de eventos de temporizador: *único* y *periódico*. Un solo evento de temporizador se produce una vez, después de un número de milisegundos especificado. Un evento de temporizador periódico se produce cada vez que transcurre un número especificado de milisegundos. El intervalo entre eventos periódicos se denomina *retraso de evento*. Los eventos de temporizador periódicos con un retraso de evento de 10 milisegundos o menos consumen una parte significativa de los recursos de CPU.

La relación entre la resolución de un evento de temporizador y la duración del retraso de evento es importante en los eventos de temporizador. Por ejemplo, si especifica una resolución de 5 y un retraso de evento de 100, los servicios de temporizador notifican a la función de devolución de llamada después de un intervalo comprendido entre 95 y 105 milisegundos.

Puede cancelar un evento de temporizador activo en cualquier momento mediante la función [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) . Asegúrese de cancelar los temporizadores pendientes antes de liberar la memoria que contiene la función de devolución de llamada.

> [!Note]  
> El temporizador multimedia se ejecuta en su propio subproceso.

 

 

 