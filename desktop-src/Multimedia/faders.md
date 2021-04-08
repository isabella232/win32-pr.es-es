---
title: Atenua
description: Atenua
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, faders
- mezcladores, controles
- mezcladores, faders
- atenua
- Estructura de MIXERCONTROLDETAILS_UNSIGNED
- control de atenuación de volumen
- control de atenuación del volumen de graves
- control de atenuación de volumen de agudos
- control de ecualizador gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995151"
---
# <a name="faders"></a><span data-ttu-id="24782-113">Atenua</span><span class="sxs-lookup"><span data-stu-id="24782-113">Faders</span></span>

<span data-ttu-id="24782-114">Los controles atenuador suelen ser controles verticales que se pueden ajustar hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="24782-114">The fader controls are typically vertical controls that can be adjusted up or down.</span></span> <span data-ttu-id="24782-115">Estos controles tienen una escala lineal y usan la [**estructura \_ sin firmar MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) para recuperar y establecer los detalles del control.</span><span class="sxs-lookup"><span data-stu-id="24782-115">These controls have a linear scale and use the [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structure to retrieve and set control details.</span></span> <span data-ttu-id="24782-116">En la tabla siguiente se describen los tipos de faders.</span><span class="sxs-lookup"><span data-stu-id="24782-116">The following table describes the types of faders.</span></span>



| <span data-ttu-id="24782-117">Control</span><span class="sxs-lookup"><span data-stu-id="24782-117">Control</span></span>   | <span data-ttu-id="24782-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="24782-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24782-119">Fader</span><span class="sxs-lookup"><span data-stu-id="24782-119">Fader</span></span>     | <span data-ttu-id="24782-120">Control de atenuación general.</span><span class="sxs-lookup"><span data-stu-id="24782-120">General fade control.</span></span> <span data-ttu-id="24782-121">El intervalo de valores aceptables es de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="24782-121">The range of acceptable values is 0 through 65,535.</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="24782-122">Volumen</span><span class="sxs-lookup"><span data-stu-id="24782-122">Volume</span></span>    | <span data-ttu-id="24782-123">Control general de atenuación de volumen.</span><span class="sxs-lookup"><span data-stu-id="24782-123">General volume fade control.</span></span> <span data-ttu-id="24782-124">El intervalo de valores aceptables es de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="24782-124">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="24782-125">Para obtener información acerca de cómo cambiar este intervalo, consulte la documentación del dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="24782-125">For information about changing this range, see the documentation for your mixer device.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="24782-126">Improvisa</span><span class="sxs-lookup"><span data-stu-id="24782-126">Bass</span></span>      | <span data-ttu-id="24782-127">Control de atenuación del volumen de graves.</span><span class="sxs-lookup"><span data-stu-id="24782-127">Bass volume fade control.</span></span> <span data-ttu-id="24782-128">El intervalo de valores aceptables es de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="24782-128">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="24782-129">Los límites de la banda de la frecuencia de graves son específicos del hardware.</span><span class="sxs-lookup"><span data-stu-id="24782-129">The limits of the bass frequency band are hardware specific.</span></span> <span data-ttu-id="24782-130">Para obtener información sobre los límites de banda, consulte la documentación del dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="24782-130">For information about band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="24782-131">Agudos</span><span class="sxs-lookup"><span data-stu-id="24782-131">Treble</span></span>    | <span data-ttu-id="24782-132">Control de atenuación del volumen de agudos.</span><span class="sxs-lookup"><span data-stu-id="24782-132">Treble volume fade control.</span></span> <span data-ttu-id="24782-133">El intervalo de valores aceptables es de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="24782-133">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="24782-134">Los límites de la banda de frecuencia de agudos son específicos del hardware.</span><span class="sxs-lookup"><span data-stu-id="24782-134">The limits of the treble frequency band are hardware specific.</span></span> <span data-ttu-id="24782-135">Para obtener información sobre los límites de banda, consulte la documentación del dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="24782-135">For information about the band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="24782-136">Ecualizador</span><span class="sxs-lookup"><span data-stu-id="24782-136">Equalizer</span></span> | <span data-ttu-id="24782-137">Control de ecualizador gráfico.</span><span class="sxs-lookup"><span data-stu-id="24782-137">Graphic equalizer control.</span></span> <span data-ttu-id="24782-138">El intervalo de valores aceptables para una banda del ecualizador es de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="24782-138">The range of acceptable values for one band of the equalizer is 0 through 65,535.</span></span> <span data-ttu-id="24782-139">El número de bandas de ecualizador y sus límites es específico del hardware.</span><span class="sxs-lookup"><span data-stu-id="24782-139">The number of equalizer bands and their limits are hardware specific.</span></span> <span data-ttu-id="24782-140">Para obtener información sobre el ecualizador, consulte la documentación del dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="24782-140">For information about the equalizer, see the documentation for your mixer device.</span></span> <span data-ttu-id="24782-141">Puede usar la estructura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) para recuperar etiquetas de texto para el ecualizador.</span><span class="sxs-lookup"><span data-stu-id="24782-141">You can use the [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure to retrieve text labels for the equalizer.</span></span> |



 

 

 