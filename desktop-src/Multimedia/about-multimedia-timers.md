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
- CreateWaitableTimer (función)
- WM_TIMER mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370951"
---
# <a name="about-multimedia-timers"></a>Acerca de los temporizadores multimedia

Los servicios de temporizador multimedia permiten a las aplicaciones programar eventos de temporizador con la mayor resolución (o precisión) posible para la plataforma de hardware. Estos servicios de temporizador multimedia permiten programar eventos de temporizador con una resolución mayor que otros servicios de temporizador.

Estos servicios de temporizador son útiles para las aplicaciones que exigen un tiempo de alta resolución. Por ejemplo, un secuenciador MIDI requiere un temporizador de alta resolución porque debe mantener el ritmo de los eventos DE MIDI en una resolución de 1 milisegundo.

Las aplicaciones que no usan el tiempo de alta resolución deben usar la [función SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) en lugar de los servicios de temporizador multimedia. Los servicios de temporizador proporcionados por **SetTimer** publican mensajes [WM \_ TIMER](../winmsg/wm-timer.md) en una cola de mensajes, mientras que los servicios de temporizador multimedia llaman a una función de devolución de llamada. Las aplicaciones que desean un temporizador que se puede esperar deben usar [la función CreateWaitableTimer.](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)

 

 