---
title: Metros
description: Metros
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, medidores
- mezcladores, controles
- mezcladores, medidores
- controles de medidor
- Estructura de MIXERCONTROLDETAILS_BOOLEAN
- Estructura de MIXERCONTROLDETAILS_SIGNED
- Estructura de MIXERCONTROLDETAILS_UNSIGNED
- Boolean (control)
- control de pico
- control firmado
- control sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487719"
---
# <a name="meters"></a><span data-ttu-id="decae-115">Metros</span><span class="sxs-lookup"><span data-stu-id="decae-115">Meters</span></span>

<span data-ttu-id="decae-116">Los controles de medidor miden los datos que pasan a través de una línea de audio.</span><span class="sxs-lookup"><span data-stu-id="decae-116">The meter controls measure data passing through an audio line.</span></span> <span data-ttu-id="decae-117">Estos controles usan las estructuras [**MIXERCONTROLDETAILS \_ Boolean**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS \_ signed**](/previous-versions//dd757297(v=vs.85))y [**MIXERCONTROLDETAILS \_ sin firmar**](/previous-versions//dd757298(v=vs.85)) para recuperar y establecer las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="decae-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)), and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="decae-118">En la tabla siguiente se describen los tipos de medidores.</span><span class="sxs-lookup"><span data-stu-id="decae-118">The following table describes the types of meters.</span></span>



| <span data-ttu-id="decae-119">Control</span><span class="sxs-lookup"><span data-stu-id="decae-119">Control</span></span>  | <span data-ttu-id="decae-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="decae-120">Description</span></span>                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="decae-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="decae-121">Boolean</span></span>  | <span data-ttu-id="decae-122">Mide si un valor entero es FALSE/OFF (cero) o TRUE/ON (distinto de cero).</span><span class="sxs-lookup"><span data-stu-id="decae-122">Measures whether an integer value is FALSE/OFF (zero) or TRUE/ON (nonzero).</span></span>                                                                            |
| <span data-ttu-id="decae-123">Peak</span><span class="sxs-lookup"><span data-stu-id="decae-123">Peak</span></span>     | <span data-ttu-id="decae-124">Mide la desviación de 0 en las direcciones positivas y negativas.</span><span class="sxs-lookup"><span data-stu-id="decae-124">Measures the deflection from 0 in both the positive and negative directions.</span></span> <span data-ttu-id="decae-125">El intervalo de valores enteros para el medidor de picos es de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="decae-125">The range of integer values for the peak meter is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="decae-126">Firmado</span><span class="sxs-lookup"><span data-stu-id="decae-126">Signed</span></span>   | <span data-ttu-id="decae-127">Mide valores enteros en el intervalo de – 231 a (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="decae-127">Measures integer values in the range of –231 through (231 – 1).</span></span> <span data-ttu-id="decae-128">El controlador del mezclador define los límites de este medidor.</span><span class="sxs-lookup"><span data-stu-id="decae-128">The mixer driver defines the limits of this meter.</span></span>                                     |
| <span data-ttu-id="decae-129">Sin signo</span><span class="sxs-lookup"><span data-stu-id="decae-129">Unsigned</span></span> | <span data-ttu-id="decae-130">Mide valores enteros en el intervalo de 0 a (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="decae-130">Measures integer values in the range of 0 through (232 – 1).</span></span> <span data-ttu-id="decae-131">El controlador del mezclador define los límites de este medidor.</span><span class="sxs-lookup"><span data-stu-id="decae-131">The mixer driver defines the limits of this meter.</span></span>                                        |



 

 

 