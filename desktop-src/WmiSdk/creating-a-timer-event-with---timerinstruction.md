---
description: Para crear un evento de temporizador, cree una instancia de las clases derivadas de la \_ \_ clase TimerInstruction en cualquier espacio de nombres WMI.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Crear un evento de temporizador con __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e502678525569dae272edb7b03c0916db25edfd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278770"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Crear un evento de temporizador con \_ \_ TimerInstruction

Para crear un evento de temporizador, cree una instancia de las clases derivadas de la clase [**\_ \_ TimerInstruction**](--timerinstruction.md) en cualquier espacio de nombres WMI. WMI genera entonces el evento de temporizador en el momento adecuado. Si se pierde un evento de temporizador debido al tiempo de inactividad del equipo, WMI le notificará sobre el evento que se ha perdido. WMI admite eventos de temporizador para la compatibilidad con versiones anteriores y para escenarios en los que se debe saber cuántos eventos se han perdido desde el último evento entregado. Sin embargo, para la mayoría de los eventos de temporizador, debe crear un filtro de eventos para [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime). Para obtener más información, vea [crear un evento de temporizador con Win32 \_ localtime o Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

En el procedimiento siguiente se describe cómo crear y recibir un evento de temporizador con \_ \_ TimerInstruction.

**Para crear y recibir un evento de temporizador con \_ \_ TimerInstruction**

1.  Cree una instancia de las clases [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) o [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

    Las clases [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) y [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) se derivan de la clase [**\_ \_ TimerInstruction**](--timerinstruction.md) , que contiene una cadena única asignada por el desarrollador que identifica el tipo de evento de temporizador. La clase **\_ \_ TimerInstruction** también contiene un valor que especifica si WMI debe enviar una notificación tardía si el evento de temporizador se produce cuando WMI no está disponible.

    Use [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) para enviar eventos de temporizador absolutos, que se producen en una fecha específica en un momento determinado. Use [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) para enviar eventos de temporizador de intervalo, que se producen de forma periódica.

2.  Establezca la aplicación para recibir una instancia de [**\_ \_ TimerEvent**](--timerevent.md) .

    Para generar un evento, WMI crea una instancia de la clase [**\_ \_ TimerEvent**](--timerevent.md) y reenvía la instancia al consumidor. La instancia de **\_ \_ TimerEvent** contiene el identificador de instrucción del temporizador del consumidor. La instancia también contiene un valor que especifica el número de veces que WMI debe enviar la notificación de eventos del temporizador durante cualquier intervalo cuando WMI no puede llegar al consumidor.

 

 
