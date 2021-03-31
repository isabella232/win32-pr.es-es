---
title: Abrir y cerrar dispositivos de mezclador
description: Abrir y cerrar dispositivos de mezclador
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- audio multimedia, dispositivos de mezclador de apertura
- audio, abrir dispositivos de mezclador
- Mezcladores de audio, abrir
- mezcladores, abrir
- audio multimedia, dispositivos de mezclador de cierre
- audio, cerrar dispositivos de mezclador
- Mezcladores de audio, cerrar
- mezcladores, cerrar
- abrir dispositivos de mezclador
- cerrar dispositivos de mezclador
- identificadores de dispositivo frente a identificadores de dispositivo
- Mezcladores de audio, identificadores de dispositivo y controladores de dispositivo
- mezcladores, identificadores de dispositivo frente a manipuladores de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077600"
---
# <a name="opening-and-closing-mixer-devices"></a><span data-ttu-id="4bd36-116">Abrir y cerrar dispositivos de mezclador</span><span class="sxs-lookup"><span data-stu-id="4bd36-116">Opening and Closing Mixer Devices</span></span>

<span data-ttu-id="4bd36-117">Si desea usar un dispositivo de mezclador, puede empezar a usarlo o bien puede abrirlo explícitamente antes de usarlo.</span><span class="sxs-lookup"><span data-stu-id="4bd36-117">When you want to use a mixer device, you can either simply begin using it or you can explicitly open the device before using it.</span></span> <span data-ttu-id="4bd36-118">Abrir explícitamente un dispositivo de mezclador ofrece dos ventajas principales:</span><span class="sxs-lookup"><span data-stu-id="4bd36-118">Explicitly opening a mixer device offers two main benefits:</span></span>

-   <span data-ttu-id="4bd36-119">Garantiza la existencia continua de ese dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="4bd36-119">It guarantees the continued existence of that mixer device.</span></span>
-   <span data-ttu-id="4bd36-120">Le permite recibir una notificación de los cambios de línea y control de audio.</span><span class="sxs-lookup"><span data-stu-id="4bd36-120">It lets you receive notification of audio line and control changes.</span></span>

<span data-ttu-id="4bd36-121">Puede usar la función [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) para abrir explícitamente un dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="4bd36-121">You can use the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function to explicitly open a mixer device.</span></span> <span data-ttu-id="4bd36-122">Esta función toma como parámetros un identificador de dispositivo, un puntero a una ubicación de memoria y otros valores exclusivos de cada tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bd36-122">This function takes as parameters a device identifier, a pointer to a memory location, and other values unique to each type of device.</span></span> <span data-ttu-id="4bd36-123">La ubicación de memoria se rellena con un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bd36-123">The memory location is filled with a device handle.</span></span> <span data-ttu-id="4bd36-124">Use este identificador de dispositivo para identificar el dispositivo de mezclador abierto al llamar a otras funciones del mezclador de audio.</span><span class="sxs-lookup"><span data-stu-id="4bd36-124">Use this device handle to identify the open mixer device when calling other audio mixer functions.</span></span> <span data-ttu-id="4bd36-125">Siempre que exista un identificador de dispositivo de mezclador, el dispositivo seguirá existiendo en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd36-125">As long as a handle of a mixer device exists, the device continues to exist in the system.</span></span> <span data-ttu-id="4bd36-126">Si se produce un cambio de configuración en el dispositivo de mezclador y no se ha abierto explícitamente, es posible que la aplicación no pueda acceder a él de repente.</span><span class="sxs-lookup"><span data-stu-id="4bd36-126">If a configuration change occurs to the mixer device and it hasn't been explicitly opened, your application might suddenly be unable to access it.</span></span>

> [!Note]  
> <span data-ttu-id="4bd36-127">La diferencia entre los identificadores de dispositivo y los controladores de dispositivo es importante.</span><span class="sxs-lookup"><span data-stu-id="4bd36-127">The difference between device identifiers and device handles is important.</span></span> <span data-ttu-id="4bd36-128">Los identificadores de dispositivo se devuelven cuando se abre un controlador de dispositivo mediante **mixerOpen**.</span><span class="sxs-lookup"><span data-stu-id="4bd36-128">Device handles are returned when you open a device driver by using **mixerOpen**.</span></span> <span data-ttu-id="4bd36-129">Los identificadores de dispositivo se determinan implícitamente a partir del número de dispositivos presentes en un sistema; Este número se obtiene mediante la función [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="4bd36-129">Device identifiers are determined implicitly from the number of devices present in a system; this number is obtained by using the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function.</span></span>

 

<span data-ttu-id="4bd36-130">Puede usar la función [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) para cerrar un dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="4bd36-130">You can use the [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) function to close a mixer device.</span></span> <span data-ttu-id="4bd36-131">Debe cerrar el dispositivo cuando termine de usarlo.</span><span class="sxs-lookup"><span data-stu-id="4bd36-131">You should close the device after you finish using it.</span></span>

 

 