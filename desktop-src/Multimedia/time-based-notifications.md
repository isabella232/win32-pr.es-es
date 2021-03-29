---
title: Notificaciones de Time-Based
description: Notificaciones de Time-Based
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- joysticks, notificaciones
- joysticks, mensajes
- joysticks, notificaciones basadas en el tiempo
- notificaciones de joystick basadas en tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995112"
---
# <a name="time-based-notifications"></a>Notificaciones de Time-Based

Puede notificar al sistema operativo que envíe mensajes de joystick a una aplicación a intervalos de tiempo regulares estableciendo el parámetro *fChanged* de [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) en **false** y especificando la longitud del intervalo entre los mensajes sucesivos. Para ello, asigne al parámetro *uPeriod* un valor entre las frecuencias de sondeo mínima y máxima del joystick. Puede determinar este intervalo mediante la función [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , que rellena los miembros **wPeriodMin** y **wPeriodMax** de la estructura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) . Si el valor de *uPeriod* está fuera del intervalo de frecuencias de sondeo válidas para el joystick, el controlador de joystick utiliza la frecuencia de sondeo mínima o máxima, lo que esté más cerca del valor de *uPeriod* .

> [!Note]  
> Windows configura un evento de temporizador con cada llamada a **joySetCapture**.

 

 

 