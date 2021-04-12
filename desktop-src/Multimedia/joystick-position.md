---
title: Posición del joystick
description: Posición del joystick
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- joysticks, posición
- joysticks, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271136"
---
# <a name="joystick-position"></a><span data-ttu-id="dcc4c-105">Posición del joystick</span><span class="sxs-lookup"><span data-stu-id="dcc4c-105">Joystick Position</span></span>

<span data-ttu-id="dcc4c-106">Puede consultar un joystick para obtener información sobre la posición y el botón mediante la función [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="dcc4c-106">You can query a joystick for position and button information by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="dcc4c-107">Por ejemplo, una aplicación puede consultar el joystick para obtener valores de posición de línea de base.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-107">For example, an application can query the joystick for baseline position values.</span></span> <span data-ttu-id="dcc4c-108">La hoja de propiedades del panel de control joystick utiliza esta técnica al calibrar el joystick.</span><span class="sxs-lookup"><span data-stu-id="dcc4c-108">The Joystick Control Panel property sheet uses this technique when calibrating the joystick.</span></span>

<span data-ttu-id="dcc4c-109">También puede consultar un joystick u otro dispositivo que tenga capacidades extendidas mediante la función [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="dcc4c-109">You can also query a joystick or other device that has extended capabilities by using the [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

 

 