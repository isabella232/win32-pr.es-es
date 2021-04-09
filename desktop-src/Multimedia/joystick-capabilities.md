---
title: Funcionalidades del joystick
description: Funcionalidades del joystick
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrada multimedia, joysticks
- joysticks, movimiento de dos ejes
- joysticks, movimiento de tres ejes
- joysticks, botones
- joysticks, intervalos de movimiento
- joysticks, frecuencias de sondeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791188"
---
# <a name="joystick-capabilities"></a><span data-ttu-id="c22a3-109">Funcionalidades del joystick</span><span class="sxs-lookup"><span data-stu-id="c22a3-109">Joystick Capabilities</span></span>

<span data-ttu-id="c22a3-110">Los joysticks pueden admitir el movimiento de dos o tres ejes y hasta cuatro botones.</span><span class="sxs-lookup"><span data-stu-id="c22a3-110">Joysticks can support two- or three-axis movement and up to four buttons.</span></span> <span data-ttu-id="c22a3-111">Los joysticks también admiten diferentes *intervalos de frecuencias de movimiento* y *sondeo*.</span><span class="sxs-lookup"><span data-stu-id="c22a3-111">Joysticks also support different *ranges of motion* and *polling frequencies*.</span></span> <span data-ttu-id="c22a3-112">El intervalo de movimiento es la distancia que un controlador de joystick puede pasar de su posición de colocación a la posición más alejada de su posición de descanso.</span><span class="sxs-lookup"><span data-stu-id="c22a3-112">The range of motion is the distance a joystick handle can move from its resting position to the position farthest from its resting position.</span></span> <span data-ttu-id="c22a3-113">La frecuencia de sondeo es el intervalo de tiempo entre las consultas de joystick.</span><span class="sxs-lookup"><span data-stu-id="c22a3-113">The polling frequency is the time interval between joystick queries.</span></span>

<span data-ttu-id="c22a3-114">Los controladores de joystick pueden admitir uno o dos joysticks.</span><span class="sxs-lookup"><span data-stu-id="c22a3-114">Joystick drivers can support either one or two joysticks.</span></span> <span data-ttu-id="c22a3-115">Puede determinar el número de joysticks admitidos por un controlador de joystick mediante la función [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="c22a3-115">You can determine the number of joysticks supported by a joystick driver by using the [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) function.</span></span> <span data-ttu-id="c22a3-116">Esta función devuelve un entero sin signo que contiene el número de joysticks admitidos o cero si no hay compatibilidad con el joystick.</span><span class="sxs-lookup"><span data-stu-id="c22a3-116">This function returns an unsigned integer that contains the number of supported joysticks or zero if there is no joystick support.</span></span> <span data-ttu-id="c22a3-117">El valor devuelto no indica el número de joysticks conectados al sistema.</span><span class="sxs-lookup"><span data-stu-id="c22a3-117">The return value does not indicate the number of joysticks attached to the system.</span></span>

<span data-ttu-id="c22a3-118">Puede determinar si un joystick está conectado al sistema mediante la función [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="c22a3-118">You can determine if a joystick is attached to the system by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="c22a3-119">Esta función devuelve JOYERR \_ NoError si se adjunta el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c22a3-119">This function returns JOYERR\_NOERROR if the specified device is attached.</span></span> <span data-ttu-id="c22a3-120">De lo contrario, devuelve JOYERR \_ UNenchufado.</span><span class="sxs-lookup"><span data-stu-id="c22a3-120">Otherwise , it returns JOYERR\_UNPLUGGED.</span></span>

<span data-ttu-id="c22a3-121">Cada joystick tiene varias funciones que están disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c22a3-121">Each joystick has several capabilities that are available to your application.</span></span> <span data-ttu-id="c22a3-122">Puede recuperar las capacidades de un joystick mediante la función [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="c22a3-122">You can retrieve the capabilities of a joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span> <span data-ttu-id="c22a3-123">Esta función rellena una estructura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) con funciones de joystick como los valores mínimo y máximo de su sistema de coordenadas, el número de botones del joystick y las frecuencias de sondeo mínima y máxima.</span><span class="sxs-lookup"><span data-stu-id="c22a3-123">This function fills a [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure with joystick capabilities such as the minimum and maximum values for its coordinate system, the number of buttons on the joystick, and the minimum and maximum polling frequencies.</span></span>

 

 