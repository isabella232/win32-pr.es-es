---
title: Referencia de joystick
description: Referencia de joystick
ms.assetid: c2ad092f-a0c5-4e28-ada7-227dc52c3c83
keywords:
- Windows multimedia, referencia de joystick
- multimedia, referencia de joystick
- entrada multimedia, referencia de joystick
- joysticks, referencia
- referencia de joysticks, acerca de
- referencia de joystick, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242f3fb21f9da9b1853ae8e9e7f694b9ad3bf711
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904529"
---
# <a name="joystick-reference"></a><span data-ttu-id="3c37e-109">Referencia de joystick</span><span class="sxs-lookup"><span data-stu-id="3c37e-109">Joystick Reference</span></span>

<span data-ttu-id="3c37e-110">En esta sección se describen las funciones, las estructuras y los mensajes asociados a los joysticks.</span><span class="sxs-lookup"><span data-stu-id="3c37e-110">This section describes the functions, structures, and messages associated with joysticks.</span></span> <span data-ttu-id="3c37e-111">Los elementos se agrupan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3c37e-111">The elements are grouped as follows:</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="3c37e-112">Capacidades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c37e-112">Device Capabilities</span></span>

-   [<span data-ttu-id="3c37e-113">**joyGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="3c37e-113">**joyGetDevCaps**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)
-   [<span data-ttu-id="3c37e-114">**joyGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="3c37e-114">**joyGetNumDevs**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs)
-   [<span data-ttu-id="3c37e-115">**JOYCAPS**</span><span class="sxs-lookup"><span data-stu-id="3c37e-115">**JOYCAPS**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)

## <a name="querying-a-joystick"></a><span data-ttu-id="3c37e-116">Consulta de un joystick</span><span class="sxs-lookup"><span data-stu-id="3c37e-116">Querying a Joystick</span></span>

-   [<span data-ttu-id="3c37e-117">**joyConfigChanged**</span><span class="sxs-lookup"><span data-stu-id="3c37e-117">**joyConfigChanged**</span></span>](/windows/desktop/api/joystickapi/nf-joystickapi-joyconfigchanged)
-   [<span data-ttu-id="3c37e-118">**joyGetPos**</span><span class="sxs-lookup"><span data-stu-id="3c37e-118">**joyGetPos**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos)
-   [<span data-ttu-id="3c37e-119">**joyGetPosEx**</span><span class="sxs-lookup"><span data-stu-id="3c37e-119">**joyGetPosEx**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)
-   [<span data-ttu-id="3c37e-120">**JOYINFO**</span><span class="sxs-lookup"><span data-stu-id="3c37e-120">**JOYINFO**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfo)
-   [<span data-ttu-id="3c37e-121">**JOYINFOEX**</span><span class="sxs-lookup"><span data-stu-id="3c37e-121">**JOYINFOEX**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfoex)

## <a name="capturing-a-joystick"></a><span data-ttu-id="3c37e-122">Captura de un joystick</span><span class="sxs-lookup"><span data-stu-id="3c37e-122">Capturing a Joystick</span></span>

-   [<span data-ttu-id="3c37e-123">**joyGetThreshold**</span><span class="sxs-lookup"><span data-stu-id="3c37e-123">**joyGetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetthreshold)
-   [<span data-ttu-id="3c37e-124">**joyReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="3c37e-124">**joyReleaseCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture)
-   [<span data-ttu-id="3c37e-125">**joySetCapture**</span><span class="sxs-lookup"><span data-stu-id="3c37e-125">**joySetCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)
-   [<span data-ttu-id="3c37e-126">**joySetThreshold**</span><span class="sxs-lookup"><span data-stu-id="3c37e-126">**joySetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold)
-   [<span data-ttu-id="3c37e-127">**MM \_ JOY1BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="3c37e-127">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md)
-   [<span data-ttu-id="3c37e-128">**MM \_ JOY1BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="3c37e-128">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)
-   [<span data-ttu-id="3c37e-129">**MM \_ JOY1MOVE**</span><span class="sxs-lookup"><span data-stu-id="3c37e-129">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)
-   [<span data-ttu-id="3c37e-130">**MM \_ JOY1ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="3c37e-130">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)
-   [<span data-ttu-id="3c37e-131">**MM \_ JOY2BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="3c37e-131">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md)
-   [<span data-ttu-id="3c37e-132">**MM \_ JOY2BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="3c37e-132">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)
-   [<span data-ttu-id="3c37e-133">**MM \_ JOY2MOVE**</span><span class="sxs-lookup"><span data-stu-id="3c37e-133">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)
-   [<span data-ttu-id="3c37e-134">**MM \_ JOY2ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="3c37e-134">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)

## <a name="related-topics"></a><span data-ttu-id="3c37e-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c37e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c37e-136">Joysticks</span><span class="sxs-lookup"><span data-stu-id="3c37e-136">Joysticks</span></span>](joysticks.md)
</dt> </dl>

 

 