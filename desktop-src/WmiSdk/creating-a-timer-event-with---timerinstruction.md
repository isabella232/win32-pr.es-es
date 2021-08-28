---
description: Para crear un evento de temporizador, cree una instancia de clases derivadas de la \_ \_ clase TimerInstruction en cualquier espacio de nombres WMI.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Crear un evento de temporizador con __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb943419a255846fbde4e17e357f8ce199824085d542d8ad300fb7e301fa3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030675"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Crear un evento de temporizador con \_ \_ TimerInstruction

Para crear un evento de temporizador, cree una instancia de clases derivadas de la [**\_ \_ clase TimerInstruction**](--timerinstruction.md) en cualquier espacio de nombres WMI. A continuación, WMI genera el evento de temporizador en el momento adecuado. Si se pierde un evento de temporizador debido al tiempo de inactividad del equipo, WMI le notifica el evento que falta. WMI admite eventos de temporizador por compatibilidad con versiones anteriores y para escenarios en los que debe saber cuántos eventos ha perdido desde el último evento entregado. Sin embargo, para la mayoría de los eventos de temporizador, debe crear un filtro de eventos para [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime.**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) Para obtener más información, vea [Crear un evento de temporizador con Win32 \_ LocalTime o Win32 \_ UTCTime.](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)

En el procedimiento siguiente se describe cómo crear y recibir un evento de temporizador con \_ \_ TimerInstruction.

**Para crear y recibir un evento de temporizador \_ \_ con TimerInstruction**

1.  Cree una instancia de las [**\_ \_ clases AbsoluteTimerInstruction**](--absolutetimerinstruction.md) [**\_ \_ o IntervalTimerInstruction.**](--intervaltimerinstruction.md)

    Las clases [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) se derivan de la [**\_ \_ clase TimerInstruction,**](--timerinstruction.md) que contiene una cadena única asignada por el desarrollador que identifica el tipo de evento de temporizador. La **\_ \_ clase TimerInstruction** también contiene un valor que especifica si WMI debe enviar una notificación desaprobada si el evento de temporizador se produce cuando WMI no está disponible.

    Use [**\_ \_ AbsoluteTimerInstruction para enviar**](--absolutetimerinstruction.md) eventos de temporizador absolutos, que se producen en una fecha específica a una hora específica. Use [**\_ \_ IntervalTimerInstruction para enviar**](--intervaltimerinstruction.md) eventos de temporizador de intervalo, que se producen de forma periódica.

2.  Establezca la aplicación para que reciba una [**\_ \_ instancia de TimerEvent.**](--timerevent.md)

    Para generar un evento, WMI crea una instancia de la [**\_ \_ clase TimerEvent**](--timerevent.md) y reenvía la instancia al consumidor. La **\_ \_ instancia de TimerEvent** contiene el identificador de instrucción del temporizador del consumidor. La instancia de también contiene un valor que especifica cuántas veces WMI debe enviar la notificación de eventos de temporizador durante cualquier intervalo en el que WMI no pueda llegar al consumidor.

 

 
