---
title: Notificaciones de Event-Based
description: Notificaciones de Event-Based
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- joysticks, notificaciones
- joysticks, mensajes
- joysticks, notificaciones basadas en eventos
- joysticks, umbral de movimiento
- notificaciones de joystick basadas en eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789999"
---
# <a name="event-based-notifications"></a><span data-ttu-id="0ff81-108">Notificaciones de Event-Based</span><span class="sxs-lookup"><span data-stu-id="0ff81-108">Event-Based Notifications</span></span>

<span data-ttu-id="0ff81-109">Puede pedir al sistema que envíe mensajes de joystick a una aplicación cada vez que la posición del eje del joystick cambie con un valor mayor que el *umbral de movimiento* del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff81-109">You can ask the system to send joystick messages to an application whenever the position of a joystick axis changes by a value greater than the *movement threshold* of the device.</span></span> <span data-ttu-id="0ff81-110">El umbral de movimiento es la distancia a la que se debe mover el joystick antes de que se envíe un mensaje de cambio de posición de joystick a una ventana que haya capturado el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff81-110">The movement threshold is the distance the joystick must be moved before a joystick position change message is sent to a window that has captured the device.</span></span> <span data-ttu-id="0ff81-111">Para obtener más información, [**consulte \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), mm [**\_ JOY2MOVE**](mm-joy2move.md)o [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).</span><span class="sxs-lookup"><span data-stu-id="0ff81-111">For more information, see [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1ZMOVE**](mm-joy1zmove.md), [**MM\_JOY2MOVE**](mm-joy2move.md), or [**MM\_JOY2ZMOVE**](mm-joy2zmove.md).</span></span>

<span data-ttu-id="0ff81-112">El umbral es inicialmente cero.</span><span class="sxs-lookup"><span data-stu-id="0ff81-112">The threshold is initially zero.</span></span> <span data-ttu-id="0ff81-113">Puede establecer el umbral de movimiento mediante la función [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) .</span><span class="sxs-lookup"><span data-stu-id="0ff81-113">You can set the movement threshold by using the [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) function.</span></span> <span data-ttu-id="0ff81-114">Puede recuperar la frecuencia de sondeo mínima del joystick mediante la función [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="0ff81-114">You can retrieve the minimum polling frequency of the joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span>

 

 