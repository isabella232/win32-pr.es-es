---
title: Números (Windows multimedia)
description: Números
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, números
- mezcladores, controles
- mezcladores, números
- controles numéricos
- Estructura de MIXERCONTROLDETAILS_SIGNED
- Estructura de MIXERCONTROLDETAILS_UNSIGNED
- control de decibelios
- control de porcentaje
- control firmado
- control sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149789"
---
# <a name="numbers-windows-multimedia"></a><span data-ttu-id="d20e4-114">Números (Windows multimedia)</span><span class="sxs-lookup"><span data-stu-id="d20e4-114">Numbers (Windows Multimedia)</span></span>

<span data-ttu-id="d20e4-115">Los controles de número permiten al usuario escribir datos numéricos asociados a una línea.</span><span class="sxs-lookup"><span data-stu-id="d20e4-115">The number controls allow the user to enter numerical data associated with a line.</span></span> <span data-ttu-id="d20e4-116">Los datos numéricos se expresan como enteros con signo, enteros sin signo o valores de decibelios enteros.</span><span class="sxs-lookup"><span data-stu-id="d20e4-116">The numerical data is expressed as signed integers, unsigned integers, or integer decibel values.</span></span> <span data-ttu-id="d20e4-117">Estos controles usan las estructuras [**\_ sin firmar**](/previous-versions//dd757298(v=vs.85)) [**MIXERCONTROLDETAILS \_ con signo**](/previous-versions//dd757297(v=vs.85)) y MIXERCONTROLDETAILS para recuperar y establecer las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="d20e4-117">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="d20e4-118">En la tabla siguiente se describen los tipos de controles numéricos.</span><span class="sxs-lookup"><span data-stu-id="d20e4-118">The following table describes the types of number controls.</span></span>



| <span data-ttu-id="d20e4-119">Control</span><span class="sxs-lookup"><span data-stu-id="d20e4-119">Control</span></span>  | <span data-ttu-id="d20e4-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d20e4-120">Description</span></span>                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d20e4-121">Firmado</span><span class="sxs-lookup"><span data-stu-id="d20e4-121">Signed</span></span>   | <span data-ttu-id="d20e4-122">Permite valores enteros escritos en el intervalo de – 231 a (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="d20e4-122">Allows integer values entered in the range of – 231 through (231 –1).</span></span>                                                               |
| <span data-ttu-id="d20e4-123">Sin signo</span><span class="sxs-lookup"><span data-stu-id="d20e4-123">Unsigned</span></span> | <span data-ttu-id="d20e4-124">Permite valores enteros escritos en el intervalo de 0 a (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="d20e4-124">Allows integer values entered in the range of 0 through (232 –1).</span></span>                                                                   |
| <span data-ttu-id="d20e4-125">Decibelio</span><span class="sxs-lookup"><span data-stu-id="d20e4-125">Decibel</span></span>  | <span data-ttu-id="d20e4-126">Permite escribir valores enteros de decibelios, en décimas de decibelios.</span><span class="sxs-lookup"><span data-stu-id="d20e4-126">Allows integer decibel values to be entered, in tenths of decibels.</span></span> <span data-ttu-id="d20e4-127">El intervalo de valores para este control es de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="d20e4-127">The range of values for this control is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="d20e4-128">Percent</span><span class="sxs-lookup"><span data-stu-id="d20e4-128">Percent</span></span>  | <span data-ttu-id="d20e4-129">Permite especificar valores como porcentajes.</span><span class="sxs-lookup"><span data-stu-id="d20e4-129">Allows values to be entered as percentages.</span></span>                                                                                         |



 

 

 
