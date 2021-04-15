---
title: Mensajes de notificación de joystick
description: Mensajes de notificación de joystick
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- joysticks, notificaciones
- joysticks, mensajes
- joysticks, posición
- joysticks, botones
- Mensajes de MM_JOY1
- Mensajes de MM_JOY2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676131"
---
# <a name="joystick-notification-messages"></a><span data-ttu-id="4eeb3-109">Mensajes de notificación de joystick</span><span class="sxs-lookup"><span data-stu-id="4eeb3-109">Joystick Notification Messages</span></span>

<span data-ttu-id="4eeb3-110">Los mensajes de joystick notifican a la aplicación que un joystick ha cambiado de posición o que uno de sus botones ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-110">Joystick messages notify your application that a joystick has changed position or that one of its buttons has changed states.</span></span> <span data-ttu-id="4eeb3-111">Los mensajes que comienzan con MM \_ JOY1 se envían a la función si la aplicación solicita entradas del joystick mediante el identificador JOYSTICKID1 y \_ se envían mensajes JOY2 de mm si la aplicación solicita entradas del joystick mediante el identificador JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-111">Messages beginning with MM\_JOY1 are sent to the function if your application requests input from the joystick using the identifier JOYSTICKID1, and MM\_JOY2 messages are sent if your application requests input from the joystick using the identifier JOYSTICKID2.</span></span>

<span data-ttu-id="4eeb3-112">Los mensajes de la tabla siguiente identifican el estado de los botones del joystick:</span><span class="sxs-lookup"><span data-stu-id="4eeb3-112">The messages in the following table identify the status of the joystick buttons:</span></span>



| <span data-ttu-id="4eeb3-113">Message</span><span class="sxs-lookup"><span data-stu-id="4eeb3-113">Message</span></span>                                         | <span data-ttu-id="4eeb3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4eeb3-114">Description</span></span>                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="4eeb3-115">**MM \_ JOY1BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-115">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md) | <span data-ttu-id="4eeb3-116">Se presionó un botón en el joystick JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-116">A button on joystick JOYSTICKID1 has been pressed.</span></span>              |
| [<span data-ttu-id="4eeb3-117">**MM \_ JOY1BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-117">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)     | <span data-ttu-id="4eeb3-118">Se ha lanzado un botón en el joystick JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-118">A button on joystick JOYSTICKID1 has been released.</span></span>             |
| [<span data-ttu-id="4eeb3-119">**MM \_ JOY1MOVE**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-119">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)             | <span data-ttu-id="4eeb3-120">El joystick JOYSTICKID1 ha cambiado la posición en la dirección x o y.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-120">Joystick JOYSTICKID1 changed position in the x- or y-direction.</span></span> |
| [<span data-ttu-id="4eeb3-121">**MM \_ JOY1ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-121">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)           | <span data-ttu-id="4eeb3-122">El joystick JOYSTICKID1 ha cambiado la posición en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-122">Joystick JOYSTICKID1 changed position in the z-direction.</span></span>       |
| [<span data-ttu-id="4eeb3-123">**MM \_ JOY2BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-123">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md) | <span data-ttu-id="4eeb3-124">Se presionó un botón en el joystick JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-124">A button on joystick JOYSTICKID2 has been pressed.</span></span>              |
| [<span data-ttu-id="4eeb3-125">**MM \_ JOY2BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-125">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)     | <span data-ttu-id="4eeb3-126">Se ha lanzado un botón en el joystick JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-126">A button on joystick JOYSTICKID2 has been released.</span></span>             |
| [<span data-ttu-id="4eeb3-127">**MM \_ JOY2MOVE**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-127">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)             | <span data-ttu-id="4eeb3-128">El joystick JOYSTICKID2 ha cambiado la posición en la dirección x o y</span><span class="sxs-lookup"><span data-stu-id="4eeb3-128">Joystick JOYSTICKID2 changed position in the x- or y-direction</span></span>  |
| [<span data-ttu-id="4eeb3-129">**MM \_ JOY2ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="4eeb3-129">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)           | <span data-ttu-id="4eeb3-130">El joystick JOYSTICKID2 ha cambiado la posición en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-130">Joystick JOYSTICKID2 changed position in the z-direction.</span></span>       |



 

<span data-ttu-id="4eeb3-131">Todos los mensajes informan de los botones inexistentes como liberados.</span><span class="sxs-lookup"><span data-stu-id="4eeb3-131">All messages report nonexistent buttons as released.</span></span>

 

 




