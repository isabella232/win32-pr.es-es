---
title: Notificaciones de joystick
description: Notificaciones de joystick
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- joysticks, notificaciones
- joysticks, mensajes
- joysticks capturados
- joysticks desconectados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077712"
---
# <a name="joystick-notifications"></a><span data-ttu-id="9623c-107">Notificaciones de joystick</span><span class="sxs-lookup"><span data-stu-id="9623c-107">Joystick Notifications</span></span>

<span data-ttu-id="9623c-108">Puede capturar mensajes de joystick directos para enviarlos a una función mediante la función [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) .</span><span class="sxs-lookup"><span data-stu-id="9623c-108">You can capture direct joystick messages to be sent to a function by using the [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) function.</span></span> <span data-ttu-id="9623c-109">Solo una aplicación a la vez puede capturar mensajes de un joystick, pero puede consultar el joystick desde otra aplicación mediante la función [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) o [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="9623c-109">Only one application at a time can capture messages from a joystick, but you can query the joystick from another application by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) or [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

> [!Note]  
> <span data-ttu-id="9623c-110">Un mensaje de joystick puede no llegar a la aplicación que capturó el joystick si una segunda aplicación utiliza **joyGetPos** o **joyGetPosEx** para consultar el joystick aproximadamente al mismo tiempo que se envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9623c-110">A joystick message can fail to reach the application that captured the joystick if a second application uses **joyGetPos** or **joyGetPosEx** to query the joystick at approximately the same time that the message is sent.</span></span> <span data-ttu-id="9623c-111">En este caso, la segunda aplicación podría interceptar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9623c-111">In this case, the second application could intercept the message.</span></span>

 

<span data-ttu-id="9623c-112">Si desea capturar mensajes de dos joysticks conectados al sistema, utilice [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) dos veces, una para cada joystick.</span><span class="sxs-lookup"><span data-stu-id="9623c-112">If you want to capture messages from two joysticks attached to the system, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) twice, once for each joystick.</span></span> <span data-ttu-id="9623c-113">La ventana recibe mensajes independientes y distintos para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9623c-113">Your window receives separate and distinct messages for each device.</span></span>

<span data-ttu-id="9623c-114">Puede liberar un joystick capturado mediante la función [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) .</span><span class="sxs-lookup"><span data-stu-id="9623c-114">You can release a captured joystick by using the [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) function.</span></span> <span data-ttu-id="9623c-115">Si una aplicación no libera el joystick antes de finalizar, el joystick se liberará automáticamente poco después de que se destruya la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="9623c-115">If an application does not release the joystick before ending, the joystick is automatically released shortly after the capture window is destroyed.</span></span>

<span data-ttu-id="9623c-116">No se puede capturar un joystick desconectado.</span><span class="sxs-lookup"><span data-stu-id="9623c-116">You cannot capture an unplugged joystick.</span></span> <span data-ttu-id="9623c-117">La función **joySetCapture** devuelve JOYERR \_ unenchufado si el dispositivo especificado está desconectado.</span><span class="sxs-lookup"><span data-stu-id="9623c-117">The **joySetCapture** function returns JOYERR\_UNPLUGGED if the specified device is unplugged.</span></span>

 

 