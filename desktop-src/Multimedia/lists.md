---
title: Listas
description: Listas
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, listas
- mezcladores, controles
- mezcladores, listas
- controles de lista
- Estructura de MIXERCONTROLDETAILS_BOOLEAN
- Estructura de MIXERCONTROLDETAILS_LISTTEXT
- control de selección única
- control de selección múltiple
- control Mixer
- Multiplexor (MUX)
- MUX (multiplexor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358855"
---
# <a name="lists"></a><span data-ttu-id="ccef5-115">Listas</span><span class="sxs-lookup"><span data-stu-id="ccef5-115">Lists</span></span>

<span data-ttu-id="ccef5-116">Los controles de lista proporcionan Estados de selección única o selección múltiple para las líneas de audio complejas.</span><span class="sxs-lookup"><span data-stu-id="ccef5-116">The list controls provide single-select or multiple-select states for complex audio lines.</span></span> <span data-ttu-id="ccef5-117">Estos controles usan la [**estructura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar y establecer las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="ccef5-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="ccef5-118">La estructura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) también se usa para recuperar todas las descripciones de texto de un control de varios elementos.</span><span class="sxs-lookup"><span data-stu-id="ccef5-118">The [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure is also used to retrieve all text descriptions of a multiple-item control.</span></span> <span data-ttu-id="ccef5-119">En la tabla siguiente se describen los tipos de controles de lista.</span><span class="sxs-lookup"><span data-stu-id="ccef5-119">The following table describes the types of list controls.</span></span>



| <span data-ttu-id="ccef5-120">Control</span><span class="sxs-lookup"><span data-stu-id="ccef5-120">Control</span></span>           | <span data-ttu-id="ccef5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccef5-121">Description</span></span>                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccef5-122">Selección única</span><span class="sxs-lookup"><span data-stu-id="ccef5-122">Single-select</span></span>     | <span data-ttu-id="ccef5-123">Restringe la selección del control a un elemento cada vez.</span><span class="sxs-lookup"><span data-stu-id="ccef5-123">Restricts the control selection to one item at a time.</span></span> <span data-ttu-id="ccef5-124">A diferencia del control multiplexor, este control se puede usar para controlar más de líneas de origen de audio.</span><span class="sxs-lookup"><span data-stu-id="ccef5-124">Unlike the multiplexer control, this control can be used to control more than audio source lines.</span></span> <span data-ttu-id="ccef5-125">Por ejemplo, podría utilizar este control para seleccionar un filtro de paso bajo de una lista de filtros admitidos por un dispositivo de mezclador.</span><span class="sxs-lookup"><span data-stu-id="ccef5-125">For example, you could use this control to select a low-pass filter from a list of filters supported by a mixer device.</span></span> |
| <span data-ttu-id="ccef5-126">Multiplexor (MUX)</span><span class="sxs-lookup"><span data-stu-id="ccef5-126">Multiplexer (MUX)</span></span> | <span data-ttu-id="ccef5-127">Restringe la selección de línea a una línea de código fuente a la vez.</span><span class="sxs-lookup"><span data-stu-id="ccef5-127">Restricts the line selection to one source line at a time.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="ccef5-128">Selección múltiple</span><span class="sxs-lookup"><span data-stu-id="ccef5-128">Multiple-select</span></span>   | <span data-ttu-id="ccef5-129">Permite al usuario seleccionar varios elementos de una lista simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="ccef5-129">Allows the user to select multiple items from a list simultaneously.</span></span> <span data-ttu-id="ccef5-130">A diferencia del control de mezclador, el control de selección múltiple se puede usar para controlar más de líneas de origen de audio.</span><span class="sxs-lookup"><span data-stu-id="ccef5-130">Unlike the mixer control, the multiple-select control can be used to control more than audio source lines.</span></span>                                                                                                  |
| <span data-ttu-id="ccef5-131">Mixer</span><span class="sxs-lookup"><span data-stu-id="ccef5-131">Mixer</span></span>             | <span data-ttu-id="ccef5-132">Permite al usuario seleccionar las líneas de origen de una lista simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="ccef5-132">Allows the user to select source lines from a list simultaneously.</span></span>                                                                                                                                                                                                               |



 

 

 