---
title: Conmutadores
description: Conmutadores
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, conmutadores
- mezcladores, controles
- mezcladores, conmutadores
- cambiar controles
- Estructura de MIXERCONTROLDETAILS_BOOLEAN
- Boolean (control)
- Button (control)
- control ON/OFF
- control mono
- control de sonoridad
- control mejorado de estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904543"
---
# <a name="switches"></a><span data-ttu-id="fdec5-115">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="fdec5-115">Switches</span></span>

<span data-ttu-id="fdec5-116">Los controles Switch son modificadores de dos Estados.</span><span class="sxs-lookup"><span data-stu-id="fdec5-116">The switch controls are two-state switches.</span></span> <span data-ttu-id="fdec5-117">Estos controles usan la [**estructura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar y establecer las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="fdec5-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="fdec5-118">En la tabla siguiente se describen los tipos de modificadores.</span><span class="sxs-lookup"><span data-stu-id="fdec5-118">The following table describes the types of switches.</span></span>



| <span data-ttu-id="fdec5-119">Control</span><span class="sxs-lookup"><span data-stu-id="fdec5-119">Control</span></span>         | <span data-ttu-id="fdec5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdec5-120">Description</span></span>                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdec5-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="fdec5-121">Boolean</span></span>         | <span data-ttu-id="fdec5-122">El modificador genérico.</span><span class="sxs-lookup"><span data-stu-id="fdec5-122">The generic switch.</span></span> <span data-ttu-id="fdec5-123">Se puede establecer en **true** o en **false**.</span><span class="sxs-lookup"><span data-stu-id="fdec5-123">It can be set to **TRUE** or **FALSE**.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="fdec5-124">Botón</span><span class="sxs-lookup"><span data-stu-id="fdec5-124">Button</span></span>          | <span data-ttu-id="fdec5-125">Establézcalo en **true** para todos los botones que el controlador debe controlar como si hubieran sido presionados.</span><span class="sxs-lookup"><span data-stu-id="fdec5-125">Set to **TRUE** for all buttons that the driver should handle as though they had been pressed.</span></span> <span data-ttu-id="fdec5-126">Si el valor es **false**, no se realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="fdec5-126">If the value is **FALSE**, no action is taken.</span></span>                                                                                         |
| <span data-ttu-id="fdec5-127">Activado/Desactivado</span><span class="sxs-lookup"><span data-stu-id="fdec5-127">On/Off</span></span>          | <span data-ttu-id="fdec5-128">Modificador alternativo que se representa mediante un gráfico distinto del que se usa para el modificador booleano.</span><span class="sxs-lookup"><span data-stu-id="fdec5-128">An alternative switch that is represented by a graphic other than the one used for the Boolean switch.</span></span> <span data-ttu-id="fdec5-129">Se puede establecer en ON u OFF.</span><span class="sxs-lookup"><span data-stu-id="fdec5-129">It can be set to ON or OFF.</span></span>                                                                                                    |
| <span data-ttu-id="fdec5-130">Silencio</span><span class="sxs-lookup"><span data-stu-id="fdec5-130">Mute</span></span>            | <span data-ttu-id="fdec5-131">Silencia una línea de audio (suprimiendo el flujo de datos de la línea) o permite reproducir los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="fdec5-131">Mutes an audio line (suppressing the data flow of the line) or allows the audio data to play.</span></span> <span data-ttu-id="fdec5-132">Este modificador se usa con frecuencia para ayudar a controlar las líneas que alimentan el mezclador.</span><span class="sxs-lookup"><span data-stu-id="fdec5-132">This switch is frequently used to help control the lines feeding into the mixer.</span></span>                                                        |
| <span data-ttu-id="fdec5-133">Mono</span><span class="sxs-lookup"><span data-stu-id="fdec5-133">Mono</span></span>            | <span data-ttu-id="fdec5-134">Cambia entre la salida mono y estéreo para una línea de audio estéreo.</span><span class="sxs-lookup"><span data-stu-id="fdec5-134">Switches between mono and stereo output for a stereo audio line.</span></span> <span data-ttu-id="fdec5-135">Establézcalo en OFF para reproducir los datos estéreo como canales independientes.</span><span class="sxs-lookup"><span data-stu-id="fdec5-135">Set to OFF to play stereo data as separate channels.</span></span> <span data-ttu-id="fdec5-136">Establezca en ON para combinar datos de ambos canales en una línea de audio mono.</span><span class="sxs-lookup"><span data-stu-id="fdec5-136">Set to ON to combine data from both channels into a mono audio line.</span></span>                                            |
| <span data-ttu-id="fdec5-137">Sonoridad</span><span class="sxs-lookup"><span data-stu-id="fdec5-137">Loudness</span></span>        | <span data-ttu-id="fdec5-138">Aumenta el bajo volumen bajo de una línea de audio.</span><span class="sxs-lookup"><span data-stu-id="fdec5-138">Boosts low-volume bass for an audio line.</span></span> <span data-ttu-id="fdec5-139">Establezca en ON para aumentar el número de bajos de volumen bajo.</span><span class="sxs-lookup"><span data-stu-id="fdec5-139">Set to ON to boost low-volume bass.</span></span> <span data-ttu-id="fdec5-140">Establezca esta opción en desactivado para establecer los niveles de volumen en normal.</span><span class="sxs-lookup"><span data-stu-id="fdec5-140">Set to OFF to set volume levels to normal.</span></span> <span data-ttu-id="fdec5-141">La cantidad de aumento es específica del hardware.</span><span class="sxs-lookup"><span data-stu-id="fdec5-141">The amount of boost is hardware specific.</span></span> <span data-ttu-id="fdec5-142">Para obtener más información, consulte la documentación del dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="fdec5-142">For more information, see the documentation for your mixer device.</span></span> |
| <span data-ttu-id="fdec5-143">Estéreo mejorado</span><span class="sxs-lookup"><span data-stu-id="fdec5-143">Stereo Enhanced</span></span> | <span data-ttu-id="fdec5-144">Aumenta la separación estéreo.</span><span class="sxs-lookup"><span data-stu-id="fdec5-144">Increases stereo separation.</span></span> <span data-ttu-id="fdec5-145">Establezca en ON para aumentar la separación estéreo.</span><span class="sxs-lookup"><span data-stu-id="fdec5-145">Set to ON to increase stereo separation.</span></span> <span data-ttu-id="fdec5-146">Se establece en OFF para no mejorar.</span><span class="sxs-lookup"><span data-stu-id="fdec5-146">Set to OFF for no enhancement.</span></span>                                                                                                                                  |



 

 

 