---
title: Acerca de los temporizadores multimedia
description: Acerca de los temporizadores multimedia
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows multimedia, temporizadores
- multimedia, temporizadores
- entrada multimedia, temporizadores
- temporizadores multimedia, acerca de
- timers,about
- temporizadores multimedia, programación de eventos
- timers,scheduling events
- programar eventos de temporizador
- tiempo de alta resolución
- Función SetTimer
- Función CreateWaitableTimer
- WM_TIMER mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b5d899c93f0f292d7ef45e8584ae9e2b5e0e001037c456dcc4900f1c0d3f26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498215"
---
# <a name="about-multimedia-timers"></a>Acerca de los temporizadores multimedia

Los servicios de temporizador multimedia permiten a las aplicaciones programar eventos de temporizador con la mayor resolución (o precisión) posible para la plataforma de hardware. Estos servicios de temporizador multimedia permiten programar eventos de temporizador con una resolución mayor que otros servicios de temporizador.

Estos servicios de temporizador son útiles para las aplicaciones que exigen un tiempo de alta resolución. Por ejemplo, un secuenciador MIDI requiere un temporizador de alta resolución porque debe mantener el ritmo de los eventos MIDI en una resolución de 1 milisegundo.

Las aplicaciones que no usan el control de tiempo de alta resolución deben usar la [función SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) en lugar de los servicios de temporizador multimedia. Los servicios de temporizador proporcionados por **SetTimer** publican mensajes [WM \_ TIMER](../winmsg/wm-timer.md) en una cola de mensajes, mientras que los servicios de temporizador multimedia llaman a una función de devolución de llamada. Las aplicaciones que desean un temporizador de espera deben usar [la función CreateWaitableTimer.](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)

 

 