---
title: Acerca de los temporizadores multimedia
description: Acerca de los temporizadores multimedia
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows multimedia, temporizadores
- multimedia, temporizadores
- entrada multimedia, temporizadores
- temporizadores multimedia, acerca de
- temporizadores, acerca de
- temporizadores multimedia, programar eventos
- temporizadores, programar eventos
- programar eventos de temporizador
- tiempo de alta resolución
- SetTimer función)
- CreateWaitableTimer función)
- Mensajes de WM_TIMER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077689"
---
# <a name="about-multimedia-timers"></a>Acerca de los temporizadores multimedia

Los servicios de temporizador multimedia permiten a las aplicaciones programar eventos de temporizador con la mayor resolución (o precisión) posible para la plataforma de hardware. Estos servicios de temporizador multimedia permiten programar eventos de temporizador con una resolución mayor que otros servicios de temporizador.

Estos servicios de temporizador son útiles para las aplicaciones que requieren tiempo de alta resolución. Por ejemplo, un secuenciador MIDI requiere un temporizador de alta resolución porque debe mantener el ritmo de los eventos MIDI en una resolución de 1 milisegundo.

Las aplicaciones que no utilizan el control de tiempo de alta resolución deben usar la función [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) en lugar de los servicios de temporizador de multimedia. Los servicios de temporizador que proporcionan los mensajes de [ \_ temporizador](../winmsg/wm-timer.md) de **SetTimer** post de WM a una cola de mensajes, mientras que los servicios de temporizador multimedia llaman a una función de devolución de llamada. Las aplicaciones que deseen un temporizador que se puede esperar deben usar la función [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .

 

 