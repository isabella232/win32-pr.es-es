---
title: Controles de número
description: Con un control de número, los usuarios pueden hacer clic en los botones de flecha para cambiar incrementalmente el valor dentro de su cuadro de texto numérico asociado.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361819"
---
# <a name="spin-controls"></a><span data-ttu-id="aee62-103">Controles de número</span><span class="sxs-lookup"><span data-stu-id="aee62-103">Spin Controls</span></span>

> [!NOTE]
> <span data-ttu-id="aee62-104">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="aee62-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="aee62-105">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="aee62-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="aee62-106">Con un control de número, los usuarios pueden hacer clic en los botones de flecha para cambiar incrementalmente el valor dentro de su [cuadro de texto numérico](ctrl-text-boxes.md)asociado.</span><span class="sxs-lookup"><span data-stu-id="aee62-106">With a spin control, users can click arrow buttons to change incrementally the value within its associated [numeric text box](ctrl-text-boxes.md).</span></span> <span data-ttu-id="aee62-107">El término cuadro de número hace referencia a la combinación de un cuadro de texto y su control de número asociado.</span><span class="sxs-lookup"><span data-stu-id="aee62-107">The term spin box refers to the combination of a text box and its associated spin control.</span></span>

![<span data-ttu-id="aee62-108">captura de pantalla del control de número y el cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="aee62-108">screen shot of spin control and text box</span></span> ](images/ctrl-spin-controls-image1.png)

<span data-ttu-id="aee62-109">Cuadro de número típico.</span><span class="sxs-lookup"><span data-stu-id="aee62-109">A typical spin box.</span></span>

<span data-ttu-id="aee62-110">A menudo, los usuarios prefieren controles de número, ya que pueden realizar cambios sin mover las manos del mouse.</span><span class="sxs-lookup"><span data-stu-id="aee62-110">Users often prefer spin controls because they can make changes without moving their hands from the mouse.</span></span> <span data-ttu-id="aee62-111">Cuando el control de número se empareja con un cuadro de texto, los usuarios pueden escribir o pegar la entrada directamente en el cuadro de texto, por lo que el uso del control de número es opcional.</span><span class="sxs-lookup"><span data-stu-id="aee62-111">When the spin control is paired with a text box, users can type or paste input directly in the text box, so use of the spin control is optional.</span></span>

<span data-ttu-id="aee62-112">Aunque los controles de número se usan para la entrada numérica, la entrada no tiene que ser un número entero puro.</span><span class="sxs-lookup"><span data-stu-id="aee62-112">While spin controls are used for numeric input, the input doesn't have to be a pure whole number.</span></span> <span data-ttu-id="aee62-113">La entrada puede ser números decimales y puede tener signos negativos, delimitadores (como dos puntos o guiones) y modificadores de unidad.</span><span class="sxs-lookup"><span data-stu-id="aee62-113">The input can be decimal numbers and it can have negative signs, delimiters (such as colons or hyphens), and unit modifiers.</span></span>

> [!Note]  
> <span data-ttu-id="aee62-114">Las instrucciones relacionadas con los [cuadros de texto](ctrl-text-boxes.md) y el [diseño](vis-layout.md) se presentan en artículos independientes.</span><span class="sxs-lookup"><span data-stu-id="aee62-114">Guidelines related to [text boxes](ctrl-text-boxes.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="aee62-115">¿Es este el control adecuado?</span><span class="sxs-lookup"><span data-stu-id="aee62-115">Is this the right control?</span></span>

<span data-ttu-id="aee62-116">Para decidirte, intenta responder a estas preguntas:</span><span class="sxs-lookup"><span data-stu-id="aee62-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="aee62-117">**¿Se usa el control para la entrada numérica?**</span><span class="sxs-lookup"><span data-stu-id="aee62-117">**Is the control used for numeric input?**</span></span> <span data-ttu-id="aee62-118">Si no es así, use otro control, como una [lista desplegable](/windows/desktop/uxguide/ctrl-drop) o un [control deslizante](ctrl-sliders.md), para seleccionar un conjunto de valores fijo.</span><span class="sxs-lookup"><span data-stu-id="aee62-118">If not, use another control, such as a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [slider](ctrl-sliders.md), to select from a fixed set of values.</span></span> <span data-ttu-id="aee62-119">Usar barras de desplazamiento para el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="aee62-119">Use scroll bars for scrolling.</span></span>
-   <span data-ttu-id="aee62-120">**¿Los usuarios piensan en el valor como una cantidad relativa, no un valor numérico?**</span><span class="sxs-lookup"><span data-stu-id="aee62-120">**Do users think of the value as a relative quantity, not a numeric value?**</span></span> <span data-ttu-id="aee62-121">Si es así, use un control deslizante en su lugar.</span><span class="sxs-lookup"><span data-stu-id="aee62-121">If so, use a slider instead.</span></span> <span data-ttu-id="aee62-122">Use cuadros de número solo para valores numéricos exactos conocidos.</span><span class="sxs-lookup"><span data-stu-id="aee62-122">Use spin boxes only for exact, known numeric values.</span></span> <span data-ttu-id="aee62-123">Por ejemplo, al ajustar el volumen, los usuarios piensan en términos de bajo o medio, y no piensan que deben ajustar el valor de volumen en 2 o 5.</span><span class="sxs-lookup"><span data-stu-id="aee62-123">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>
-   <span data-ttu-id="aee62-124">**¿El control está emparejado con un cuadro de texto?**</span><span class="sxs-lookup"><span data-stu-id="aee62-124">**Is the control paired with a text box?**</span></span> <span data-ttu-id="aee62-125">En caso contrario, no utilice.</span><span class="sxs-lookup"><span data-stu-id="aee62-125">If not, don't use.</span></span> <span data-ttu-id="aee62-126">Los controles de número no se deben usar solo o con otros tipos de controles además de un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="aee62-126">Spin controls shouldn't be used alone or with other types of controls besides a text box.</span></span>

    <span data-ttu-id="aee62-127">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="aee62-127">**Incorrect:**</span></span>

    ![<span data-ttu-id="aee62-128">captura de pantalla del control de número, gráfico, sin cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="aee62-128">screen shot of spin control, graphic, no text box</span></span> ](images/ctrl-spin-controls-image2.png)

    <span data-ttu-id="aee62-129">En este ejemplo, se utiliza un control de número para controlar un gráfico dinámico.</span><span class="sxs-lookup"><span data-stu-id="aee62-129">In this example, a spin control is used to control a dynamic graphic.</span></span>

-   <span data-ttu-id="aee62-130">**¿Son válidos los intervalos de valores contiguos?**</span><span class="sxs-lookup"><span data-stu-id="aee62-130">**Are contiguous value ranges valid?**</span></span> <span data-ttu-id="aee62-131">En caso contrario, utilice en su lugar una lista desplegable de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="aee62-131">If not, use a drop-down list of valid values instead.</span></span>

    ![<span data-ttu-id="aee62-132">captura de pantalla de la lista desplegable</span><span class="sxs-lookup"><span data-stu-id="aee62-132">screen shot of drop-down list</span></span> ](images/ctrl-spin-controls-image3.png)

    <span data-ttu-id="aee62-133">En este ejemplo, no todos los números de unidad de disco son válidos, por lo que una lista desplegable es una opción mejor.</span><span class="sxs-lookup"><span data-stu-id="aee62-133">In this example, not all disk drive numbers are valid, so a drop-down list is a better choice.</span></span>

-   <span data-ttu-id="aee62-134">**¿Está utilizando el control de número práctico?**</span><span class="sxs-lookup"><span data-stu-id="aee62-134">**Is using the spin control practical?**</span></span> <span data-ttu-id="aee62-135">El uso de un control de número es práctico para:</span><span class="sxs-lookup"><span data-stu-id="aee62-135">Using a spin control is practical for:</span></span>

    -   <span data-ttu-id="aee62-136">Escribir un número pequeño, normalmente en 100.</span><span class="sxs-lookup"><span data-stu-id="aee62-136">Entering a small number, typically under 100.</span></span>
    -   <span data-ttu-id="aee62-137">Realizar pequeños cambios en un valor predeterminado o existente.</span><span class="sxs-lookup"><span data-stu-id="aee62-137">Making small changes to an existing or default value.</span></span>

    <span data-ttu-id="aee62-138">Aunque los controles de número se pueden usar para cualquier entrada numérica, son ineficaces en situaciones distintas a estas.</span><span class="sxs-lookup"><span data-stu-id="aee62-138">While spin controls can be used for any numeric input, they are inefficient in situations other than these.</span></span>

-   <span data-ttu-id="aee62-139">**¿Es útil el control de número?**</span><span class="sxs-lookup"><span data-stu-id="aee62-139">**Is the spin control helpful?**</span></span> <span data-ttu-id="aee62-140">¿Se usa el control en un contexto en el que es probable que los usuarios usen el mouse?</span><span class="sxs-lookup"><span data-stu-id="aee62-140">Is the control used in a context where users are likely to be using their mouse?</span></span> <span data-ttu-id="aee62-141">Si no es así, considere la posibilidad de usar un control de número opcional.</span><span class="sxs-lookup"><span data-stu-id="aee62-141">If not, consider a spin control optional.</span></span>
-   <span data-ttu-id="aee62-142">**¿Son las listas desplegables de controles relacionados?**</span><span class="sxs-lookup"><span data-stu-id="aee62-142">**Are the sibling controls drop-down lists?**</span></span> <span data-ttu-id="aee62-143">Si hay otras listas desplegables, considere la posibilidad de usar una lista desplegable para mantener la coherencia.</span><span class="sxs-lookup"><span data-stu-id="aee62-143">If there are other drop-down lists, consider using a drop-down list for consistency.</span></span>

    ![<span data-ttu-id="aee62-144">captura de pantalla del cuadro de diálogo con listas desplegables</span><span class="sxs-lookup"><span data-stu-id="aee62-144">screen shot of dialog box with drop-down lists</span></span> ](images/ctrl-spin-controls-image4.png)

    <span data-ttu-id="aee62-145">En este ejemplo, se podría usar un cuadro de número, pero se utilizará una lista desplegable por coherencia.</span><span class="sxs-lookup"><span data-stu-id="aee62-145">In this example, a spin box could be used, but a drop-down list is used for consistency.</span></span>

-   <span data-ttu-id="aee62-146">**¿Son los usuarios táctiles o de lápiz un destino principal?**</span><span class="sxs-lookup"><span data-stu-id="aee62-146">**Are touch or pen users a primary target?**</span></span> <span data-ttu-id="aee62-147">En caso afirmativo, considere la posibilidad de usar una lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="aee62-147">If so, consider using a drop-down list instead.</span></span> <span data-ttu-id="aee62-148">Los botones de flecha de un control de número son demasiado pequeños para usarlos de forma eficaz con la entrada táctil o un lápiz.</span><span class="sxs-lookup"><span data-stu-id="aee62-148">The arrow buttons in a spin control are too small to be used efficiently with touch or a pen.</span></span>

<span data-ttu-id="aee62-149">Si un control deslizante o un cuadro de número es posible, use un cuadro de número si:</span><span class="sxs-lookup"><span data-stu-id="aee62-149">If a slider or a spin box is possible, use a spin box if:</span></span>

-   <span data-ttu-id="aee62-150">El espacio en pantalla es limitado.</span><span class="sxs-lookup"><span data-stu-id="aee62-150">Screen space is tight.</span></span>
-   <span data-ttu-id="aee62-151">Es probable que un usuario prefiera usar el teclado.</span><span class="sxs-lookup"><span data-stu-id="aee62-151">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="aee62-152">Usa el control deslizante si:</span><span class="sxs-lookup"><span data-stu-id="aee62-152">Use a slider if:</span></span>

-   <span data-ttu-id="aee62-153">Los usuarios van a sacar provecho de una respuesta instantánea.</span><span class="sxs-lookup"><span data-stu-id="aee62-153">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="aee62-154">Directrices</span><span class="sxs-lookup"><span data-stu-id="aee62-154">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="aee62-155">General</span><span class="sxs-lookup"><span data-stu-id="aee62-155">General</span></span>

-   <span data-ttu-id="aee62-156">**Use controles de número siempre que sean prácticos y útiles.**</span><span class="sxs-lookup"><span data-stu-id="aee62-156">**Use spin controls whenever they are practical and helpful.**</span></span> <span data-ttu-id="aee62-157">Vea [¿este es el control correcto?](#is-this-the-right-control)</span><span class="sxs-lookup"><span data-stu-id="aee62-157">See [Is this the right control?](#is-this-the-right-control)</span></span>

    -   <span data-ttu-id="aee62-158">**Excepción:** Para ser coherente con otros cuadros de texto en la misma interfaz de usuario (IU), use los controles de número aunque no siempre sean prácticos.</span><span class="sxs-lookup"><span data-stu-id="aee62-158">**Exception:** To be consistent with other text boxes on the same user interface (UI), use spin controls even if they aren't always practical.</span></span>

    <span data-ttu-id="aee62-159">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="aee62-159">**Correct:**</span></span>

    ![<span data-ttu-id="aee62-160">captura de pantalla de los controles de número de mes, día y año</span><span class="sxs-lookup"><span data-stu-id="aee62-160">screen shot of month, day, year spin controls</span></span> ](images/ctrl-spin-controls-image5.png)

    <span data-ttu-id="aee62-161">En este ejemplo, se usa un control de número con el control de año para mantener la coherencia, aunque no siempre es práctico.</span><span class="sxs-lookup"><span data-stu-id="aee62-161">In this example, a spin control is used with the year control for consistency, even though it isn't always practical.</span></span>

    <span data-ttu-id="aee62-162">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="aee62-162">**Incorrect:**</span></span>

    ![<span data-ttu-id="aee62-163">captura de pantalla del control de giro de dirección IP</span><span class="sxs-lookup"><span data-stu-id="aee62-163">screen shot of ip address spin control</span></span> ](images/ctrl-spin-controls-image6.png)

    <span data-ttu-id="aee62-164">En este ejemplo, el control de número no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="aee62-164">In this example, the spin control is unusable.</span></span>

-   <span data-ttu-id="aee62-165">**Convierta siempre un control de número en el "Buddy" del cuadro de texto.**</span><span class="sxs-lookup"><span data-stu-id="aee62-165">**Always make a spin control the "buddy" of the text box.**</span></span> <span data-ttu-id="aee62-166">Al hacerlo, se coloca el control de número dentro del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="aee62-166">Doing so places the spin control inside the text box.</span></span>

    <span data-ttu-id="aee62-167">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="aee62-167">**Correct:**</span></span>

    ![<span data-ttu-id="aee62-168">captura de pantalla del cuadro de texto control de número colocado dentro</span><span class="sxs-lookup"><span data-stu-id="aee62-168">screen shot of spin control placed inside text box</span></span> ](images/ctrl-spin-controls-image7.png)

    <span data-ttu-id="aee62-169">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="aee62-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="aee62-170">captura de pantalla del control de número colocado fuera del cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="aee62-170">screen shot of spin control placed outside text box</span></span> ](images/ctrl-spin-controls-image8.png)

    <span data-ttu-id="aee62-171">En el ejemplo correcto, el control de número se coloca dentro de su cuadro de texto asociado.</span><span class="sxs-lookup"><span data-stu-id="aee62-171">In the correct example, the spin control is placed inside its associated text box.</span></span>

-   <span data-ttu-id="aee62-172">**Deshabilitar un control de número cuando se deshabilita el cuadro de texto asociado.**</span><span class="sxs-lookup"><span data-stu-id="aee62-172">**Disable a spin control when its associated text box is disabled.**</span></span> <span data-ttu-id="aee62-173">El control de número es un método de entrada complementario; nunca es el único método de entrada.</span><span class="sxs-lookup"><span data-stu-id="aee62-173">The spin control is a supplemental input method—never the only input method.</span></span>

### <a name="values"></a><span data-ttu-id="aee62-174">Valores</span><span class="sxs-lookup"><span data-stu-id="aee62-174">Values</span></span>

-   <span data-ttu-id="aee62-175">**Defina el botón superior para aumentar el valor en una unidad y el botón inferior para reducir en una unidad.**</span><span class="sxs-lookup"><span data-stu-id="aee62-175">**Define the top button to increase the value by one unit and the bottom button to decrease by one unit.**</span></span> <span data-ttu-id="aee62-176">Normalmente, la unidad es una, pero debe ser el cambio común más pequeño en el valor.</span><span class="sxs-lookup"><span data-stu-id="aee62-176">Typically, the unit is one, but it should be the smallest common change in value.</span></span> <span data-ttu-id="aee62-177">Idealmente, el control de número debe cubrir todos los valores válidos y debe ser más conveniente que escribir en el texto.</span><span class="sxs-lookup"><span data-stu-id="aee62-177">Ideally, the spin control should cover all valid values, and it should be more convenient than typing in the text.</span></span>

    ![<span data-ttu-id="aee62-178">captura de pantalla del control de número ' Margins '</span><span class="sxs-lookup"><span data-stu-id="aee62-178">screen shot of 'margins' spin control</span></span> ](images/ctrl-spin-controls-image9.png)

    <span data-ttu-id="aee62-179">En este ejemplo, al hacer clic en un control de número, se cambian los valores por 0,1, que es el cambio común más pequeño en el valor.</span><span class="sxs-lookup"><span data-stu-id="aee62-179">In this example, clicking a spin control changes the values by .1, which is the smallest common change in value.</span></span> <span data-ttu-id="aee62-180">El uso de una unidad más pequeña abarcaría el intervalo de valores válidos, pero hace que los controles de número no se puedan usar.</span><span class="sxs-lookup"><span data-stu-id="aee62-180">Using a smaller unit would cover the range of valid values but make the spin controls unusable.</span></span>

-   <span data-ttu-id="aee62-181">**Utilice el control de número para limitar la entrada a valores válidos.**</span><span class="sxs-lookup"><span data-stu-id="aee62-181">**Use the spin control to limit input to valid values.**</span></span> <span data-ttu-id="aee62-182">El uso de un control de número nunca debe dar como resultado un valor incorrecto.</span><span class="sxs-lookup"><span data-stu-id="aee62-182">Using a spin control should never result in an incorrect value.</span></span>
-   <span data-ttu-id="aee62-183">**Al final de un intervalo de valores válidos, reinicie el intervalo.**</span><span class="sxs-lookup"><span data-stu-id="aee62-183">**At the end of a range of valid values, restart the range.**</span></span> <span data-ttu-id="aee62-184">La metáfora del control de número es que el usuario está girando una rueda de valores, por lo que este comportamiento de tipo rueda.</span><span class="sxs-lookup"><span data-stu-id="aee62-184">The spin control metaphor is that the user is spinning a wheel of values, hence this wheel-like behavior.</span></span>
    -   <span data-ttu-id="aee62-185">**Excepción:** No reinicie el intervalo si el valor resultante es seguro que es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="aee62-185">**Exception:** Don't restart the range if the resulting value is certain to be incorrect.</span></span>

        ![<span data-ttu-id="aee62-186">captura de pantalla del control de número ' número de copias '</span><span class="sxs-lookup"><span data-stu-id="aee62-186">screen shot of 'number of copies' spin control</span></span> ](images/ctrl-spin-controls-image10.png)

        <span data-ttu-id="aee62-187">En este ejemplo, al hacer clic en el botón de flecha abajo no se reinicia el intervalo (yendo al valor máximo) porque ese valor está seguro de que es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="aee62-187">In this example, clicking the down arrow button doesn't restart the range (by going to the maximum value) because that value is certain to be incorrect.</span></span>

-   <span data-ttu-id="aee62-188">**Use texto en lugar de valores numéricos especiales.**</span><span class="sxs-lookup"><span data-stu-id="aee62-188">**Use text instead of special numeric values.**</span></span> <span data-ttu-id="aee62-189">Permita que los usuarios giren a estos valores especiales en lugar de tener que conocerlos y escribirlos en.</span><span class="sxs-lookup"><span data-stu-id="aee62-189">Allow users to spin to these special values instead of having to know them and type them in.</span></span>

    ![<span data-ttu-id="aee62-190">captura de pantalla del control de número "suspender después (nunca)"</span><span class="sxs-lookup"><span data-stu-id="aee62-190">screen shot of 'sleep after (never)' spin control</span></span> ](images/ctrl-spin-controls-image11.png)

    <span data-ttu-id="aee62-191">En este ejemplo, nunca es un valor especial, pero los usuarios pueden hacerlo.</span><span class="sxs-lookup"><span data-stu-id="aee62-191">In this example, Never is a special value but users can spin to it.</span></span>

-   <span data-ttu-id="aee62-192">**Si el valor tiene delimitadores, el cuadro de texto asociado debe tener varios puntos de foco de entrada.**</span><span class="sxs-lookup"><span data-stu-id="aee62-192">**If the value has delimiters, the associated text box should have multiple input focus points.**</span></span> <span data-ttu-id="aee62-193">Esto permite manipular los segmentos numéricos de forma individual.</span><span class="sxs-lookup"><span data-stu-id="aee62-193">Doing so allows the numeric segments to be manipulated individually.</span></span>

    ![<span data-ttu-id="aee62-194">captura de pantalla de control de tiempo, minutos seleccionados</span><span class="sxs-lookup"><span data-stu-id="aee62-194">screen shot of time spin control, minutes selected</span></span> ](images/ctrl-spin-controls-image12.png)

    <span data-ttu-id="aee62-195">En este ejemplo, el control de número afecta a los valores de horas, minutos, segundos y A.M./P.M., lo que tenga el foco.</span><span class="sxs-lookup"><span data-stu-id="aee62-195">In this example, the spin control affects the values for hours, minutes, seconds, and A.M./P.M.—whichever has the focus.</span></span>

-   <span data-ttu-id="aee62-196">**Si el valor tiene unidades, use el control de número para cambiar también dichas unidades.**</span><span class="sxs-lookup"><span data-stu-id="aee62-196">**If the value has units, use the spin control to change those units as well.**</span></span>

    ![<span data-ttu-id="aee62-197">captura de pantalla de control de tiempo de tiempo, "AM"</span><span class="sxs-lookup"><span data-stu-id="aee62-197">screen shot of time spin control, 'a.m.'</span></span> <span data-ttu-id="aee62-198">Seleccionado</span><span class="sxs-lookup"><span data-stu-id="aee62-198">selected</span></span> ](images/ctrl-spin-controls-image13.png)

    <span data-ttu-id="aee62-199">En este ejemplo, el control de número se puede usar para cambiar las unidades.</span><span class="sxs-lookup"><span data-stu-id="aee62-199">In this example, the spin control can be used to change units.</span></span>

## <a name="labels"></a><span data-ttu-id="aee62-200">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="aee62-200">Labels</span></span>

-   <span data-ttu-id="aee62-201">Aplique las instrucciones de [etiqueta del cuadro de texto](ctrl-text-boxes.md) para etiquetar el cuadro de texto asociado.</span><span class="sxs-lookup"><span data-stu-id="aee62-201">Apply the [text box labeling](ctrl-text-boxes.md) guidelines to label the associated text box.</span></span> <span data-ttu-id="aee62-202">Los controles de número nunca se etiquetan directamente.</span><span class="sxs-lookup"><span data-stu-id="aee62-202">Spin controls are never labeled directly.</span></span>

## <a name="documentation"></a><span data-ttu-id="aee62-203">Documentación</span><span class="sxs-lookup"><span data-stu-id="aee62-203">Documentation</span></span>

<span data-ttu-id="aee62-204">Al hacer referencia a los controles de número:</span><span class="sxs-lookup"><span data-stu-id="aee62-204">When referring to spin controls:</span></span>

-   <span data-ttu-id="aee62-205">No haga referencia a los controles de número en la documentación de usuario.</span><span class="sxs-lookup"><span data-stu-id="aee62-205">Don't refer to spin controls in user documentation.</span></span> <span data-ttu-id="aee62-206">En su lugar, haga referencia a la etiqueta del cuadro de texto asociado.</span><span class="sxs-lookup"><span data-stu-id="aee62-206">Instead, refer to the label of the associated text box.</span></span>
-   <span data-ttu-id="aee62-207">Consulte controles de número y cuadros de número solo en programación y otra documentación técnica.</span><span class="sxs-lookup"><span data-stu-id="aee62-207">Refer to spin controls and spin boxes only in programming and other technical documentation.</span></span>

<span data-ttu-id="aee62-208">Ejemplo: en el cuadro **fecha** , escriba o seleccione la parte de la fecha que desee cambiar.</span><span class="sxs-lookup"><span data-stu-id="aee62-208">Example: In the **Date** box, type or select the part of the date you want to change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aee62-209">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aee62-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aee62-210">Glosario</span><span class="sxs-lookup"><span data-stu-id="aee62-210">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 