---
title: Time-Based notificaciones
description: Time-Based notificaciones
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- y, por último, notificaciones
- sms, mensajes
- y notificaciones basadas en el tiempo
- notificaciones de notificación de notificación basadas en el tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260644"
---
# <a name="time-based-notifications"></a>Time-Based notificaciones

Puede notificar al sistema operativo que envíe mensajes de mensajes de mensaje a una aplicación a intervalos de tiempo regulares estableciendo el parámetro *fChanged* de [**fuefSetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) en **FALSE** y especificando la longitud del intervalo entre los mensajes sucesivos. Para ello, asigne al *parámetro uPeriod* un valor entre las frecuencias de sondeo mínimas y máximas del intervalo. Puede determinar este intervalo mediante la [**funcióngetGetDevCaps,**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) que rellena los **miembros wPeriodMin** y **wPeriodMax** en la [**estructura DECAPS.**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) Si el valor *uPeriod* está fuera del intervalo de frecuencias de sondeo válidas para el taxi, el controlador de driver usa la frecuencia de sondeo mínima o máxima, la que esté más cerca del valor *uPeriod.*

> [!Note]  
> Windows configura un evento de temporizador con cada llamada a **.**

 

 

 