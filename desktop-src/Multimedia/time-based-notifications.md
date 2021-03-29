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
# <a name="time-based-notifications"></a><span data-ttu-id="4c90a-107">Notificaciones de Time-Based</span><span class="sxs-lookup"><span data-stu-id="4c90a-107">Time-Based Notifications</span></span>

<span data-ttu-id="4c90a-108">Puede notificar al sistema operativo que envíe mensajes de joystick a una aplicación a intervalos de tiempo regulares estableciendo el parámetro *fChanged* de [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) en **false** y especificando la longitud del intervalo entre los mensajes sucesivos.</span><span class="sxs-lookup"><span data-stu-id="4c90a-108">You can notify the operating system to send joystick messages to an application at regular time intervals by setting the *fChanged* parameter of [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to **FALSE** and by specifying the interval length between successive messages.</span></span> <span data-ttu-id="4c90a-109">Para ello, asigne al parámetro *uPeriod* un valor entre las frecuencias de sondeo mínima y máxima del joystick.</span><span class="sxs-lookup"><span data-stu-id="4c90a-109">To do this, assign the *uPeriod* parameter a value between the minimum and maximum polling frequencies for the joystick.</span></span> <span data-ttu-id="4c90a-110">Puede determinar este intervalo mediante la función [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , que rellena los miembros **wPeriodMin** y **wPeriodMax** de la estructura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) .</span><span class="sxs-lookup"><span data-stu-id="4c90a-110">You can determine this range by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function, which fills the **wPeriodMin** and **wPeriodMax** members in the [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure.</span></span> <span data-ttu-id="4c90a-111">Si el valor de *uPeriod* está fuera del intervalo de frecuencias de sondeo válidas para el joystick, el controlador de joystick utiliza la frecuencia de sondeo mínima o máxima, lo que esté más cerca del valor de *uPeriod* .</span><span class="sxs-lookup"><span data-stu-id="4c90a-111">If the *uPeriod* value is outside the range of valid polling frequencies for the joystick, the joystick driver uses the minimum or maximum polling frequency, whichever is closer to the *uPeriod* value.</span></span>

> [!Note]  
> <span data-ttu-id="4c90a-112">Windows configura un evento de temporizador con cada llamada a **joySetCapture**.</span><span class="sxs-lookup"><span data-stu-id="4c90a-112">Windows sets up a timer event with each call to **joySetCapture**.</span></span>

 

 

 