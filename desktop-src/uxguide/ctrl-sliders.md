---
title: Controles deslizantes (conceptos básicos del diseño)
description: Con un control deslizante, los usuarios pueden elegir entre un intervalo continuo de valores.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555888"
---
# <a name="sliders-design-basics"></a><span data-ttu-id="c9d25-103">Controles deslizantes (conceptos básicos del diseño)</span><span class="sxs-lookup"><span data-stu-id="c9d25-103">Sliders (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="c9d25-104">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="c9d25-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="c9d25-105">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="c9d25-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="c9d25-106">Con un control deslizante, los usuarios pueden elegir entre un intervalo continuo de valores.</span><span class="sxs-lookup"><span data-stu-id="c9d25-106">With a slider, users can choose from a continuous range of values.</span></span> <span data-ttu-id="c9d25-107">Un control deslizante tiene una barra que muestra el rango y un indicador que muestra el valor actual.</span><span class="sxs-lookup"><span data-stu-id="c9d25-107">A slider has a bar that shows the range and an indicator that shows the current value.</span></span> <span data-ttu-id="c9d25-108">Las marcas de graduación opcionales muestran valores.</span><span class="sxs-lookup"><span data-stu-id="c9d25-108">Optional tick marks show values.</span></span>

![<span data-ttu-id="c9d25-109">Ilustración que muestra la barra, el control deslizante y las marcas de graduación</span><span class="sxs-lookup"><span data-stu-id="c9d25-109">figure showing bar, slider, and tick marks</span></span> ](images/ctrl-sliders-image1.png)

<span data-ttu-id="c9d25-110">Control deslizante típico.</span><span class="sxs-lookup"><span data-stu-id="c9d25-110">A typical slider.</span></span>

> [!Note]  
> <span data-ttu-id="c9d25-111">Las instrucciones relacionadas con el [diseño](vis-layout.md) se presentan en un artículo independiente.</span><span class="sxs-lookup"><span data-stu-id="c9d25-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="c9d25-112">¿Es este el control adecuado?</span><span class="sxs-lookup"><span data-stu-id="c9d25-112">Is this the right control?</span></span>

<span data-ttu-id="c9d25-113">Use un control deslizante cuando desee que los usuarios puedan **establecer valores contiguos y definidos (como el volumen o el brillo) o un intervalo de valores discretos (como la configuración de la resolución de pantalla).**</span><span class="sxs-lookup"><span data-stu-id="c9d25-113">Use a slider when you want your users to be able to **set defined, contiguous values (such as volume or brightness) or a range of discrete values (such as screen resolution settings).**</span></span>

<span data-ttu-id="c9d25-114">Un control deslizante es una buena opción si sabes que los usuarios ven el valor como una cantidad relativa y no como un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="c9d25-114">A slider is a good choice when you know that users think of the value as a relative quantity, not a numeric value.</span></span> <span data-ttu-id="c9d25-115">Por ejemplo, al ajustar el volumen, los usuarios piensan en términos de bajo o medio, y no piensan que deben ajustar el valor de volumen en 2 o 5.</span><span class="sxs-lookup"><span data-stu-id="c9d25-115">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>

<span data-ttu-id="c9d25-116">Para decidirte, intenta responder a estas preguntas:</span><span class="sxs-lookup"><span data-stu-id="c9d25-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="c9d25-117">**¿El valor de configuración parece una cantidad relativa?**</span><span class="sxs-lookup"><span data-stu-id="c9d25-117">**Does the setting seem like a relative quantity?**</span></span> <span data-ttu-id="c9d25-118">Si no es así, use los [botones de radio](ctrl-radio-buttons.md) [o una lista desplegable o](/windows/desktop/uxguide/ctrl-drop) [de selección única](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="c9d25-118">If not, use [radio buttons](ctrl-radio-buttons.md), or a [drop-down](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="c9d25-119">**¿El valor de configuración es un valor numérico exacto y conocido?**</span><span class="sxs-lookup"><span data-stu-id="c9d25-119">**Is the setting an exact, known numeric value?**</span></span> <span data-ttu-id="c9d25-120">Si es así, use un [cuadro de texto numérico](ctrl-text-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="c9d25-120">If so, use a [numeric text boxes](ctrl-text-boxes.md).</span></span>
-   <span data-ttu-id="c9d25-121">**¿Sería bueno que el usuario obtuviera una respuesta inmediata sobre el efecto de los cambios realizados en la configuración?**</span><span class="sxs-lookup"><span data-stu-id="c9d25-121">**Would a user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="c9d25-122">Si es así, usa un control deslizante.</span><span class="sxs-lookup"><span data-stu-id="c9d25-122">If so, use a slider.</span></span> <span data-ttu-id="c9d25-123">Por ejemplo, los usuarios pueden elegir un color más fácilmente si ven de forma inmediata el efecto de los cambios en los valores de matiz, saturación o luminosidad.</span><span class="sxs-lookup"><span data-stu-id="c9d25-123">For example, users can choose a color more easily by immediately seeing the effect of changes to hue, saturation, or luminosity values.</span></span>
-   <span data-ttu-id="c9d25-124">**¿La configuración tiene un intervalo de cuatro o más valores?**</span><span class="sxs-lookup"><span data-stu-id="c9d25-124">**Does the setting have a range of four or more values?**</span></span> <span data-ttu-id="c9d25-125">Si no es así, usa botones de radio.</span><span class="sxs-lookup"><span data-stu-id="c9d25-125">If not, use radio buttons.</span></span>
-   <span data-ttu-id="c9d25-126">**¿El usuario puede cambiar el valor?**</span><span class="sxs-lookup"><span data-stu-id="c9d25-126">**Can the user change the value?**</span></span> <span data-ttu-id="c9d25-127">Los controles deslizantes están destinados a la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="c9d25-127">Sliders are for user interaction.</span></span> <span data-ttu-id="c9d25-128">Si un usuario no puede cambiar el valor, use en su lugar un [cuadro de texto](ctrl-text-boxes.md) de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c9d25-128">If a user can't ever change the value, use a read-only [text box](ctrl-text-boxes.md) instead.</span></span>

<span data-ttu-id="c9d25-129">Si un control deslizante o un cuadro de texto numérico es posible, use un cuadro de texto numérico si:</span><span class="sxs-lookup"><span data-stu-id="c9d25-129">If a slider or a numeric text box is possible, use a numeric text box if:</span></span>

-   <span data-ttu-id="c9d25-130">El espacio en pantalla es limitado.</span><span class="sxs-lookup"><span data-stu-id="c9d25-130">Screen space is tight.</span></span>
-   <span data-ttu-id="c9d25-131">Es probable que un usuario prefiera usar el teclado.</span><span class="sxs-lookup"><span data-stu-id="c9d25-131">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="c9d25-132">Usa el control deslizante si:</span><span class="sxs-lookup"><span data-stu-id="c9d25-132">Use a slider if:</span></span>

-   <span data-ttu-id="c9d25-133">Los usuarios van a sacar provecho de una respuesta instantánea.</span><span class="sxs-lookup"><span data-stu-id="c9d25-133">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="c9d25-134">Directrices</span><span class="sxs-lookup"><span data-stu-id="c9d25-134">Guidelines</span></span>

-   <span data-ttu-id="c9d25-135">**Usa una orientación natural.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-135">**Use a natural orientation.**</span></span> <span data-ttu-id="c9d25-136">Por ejemplo, si el control deslizante representa un valor del mundo real que normalmente se muestra en vertical (como la temperatura), usa una orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="c9d25-136">For example, if the slider represents a real-world value that is normally shown vertically (such as temperature), use a vertical orientation.</span></span>
-   <span data-ttu-id="c9d25-137">**Oriente el control deslizante para reflejar la referencia cultural de los usuarios.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-137">**Orient the slider to reflect the culture of your users.**</span></span> <span data-ttu-id="c9d25-138">Por ejemplo, las referencias culturales occidentales se leen de izquierda a derecha, por lo que para los controles deslizantes horizontalmente, coloque el extremo inferior del rango a la izquierda y el extremo superior de la derecha.</span><span class="sxs-lookup"><span data-stu-id="c9d25-138">For example, Western cultures read from left to right, so for horizontal sliders, put the low end of the range on the left and the high end on the right.</span></span> <span data-ttu-id="c9d25-139">En el caso de las referencias culturales que se leen de derecha a izquierda, haga lo contrario.</span><span class="sxs-lookup"><span data-stu-id="c9d25-139">For cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="c9d25-140">**Ajuste el tamaño del control para que un usuario pueda establecer fácilmente el valor deseado.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-140">**Size the control so that a user can easily set the desired value.**</span></span> <span data-ttu-id="c9d25-141">En el caso de opciones con valores discretos, asegúrate de que al usuario le resulte fácil seleccionar cualquier valor mediante el mouse.</span><span class="sxs-lookup"><span data-stu-id="c9d25-141">For settings with discrete values, make sure the user can easily select any value using the mouse.</span></span>
-   <span data-ttu-id="c9d25-142">**Considere la posibilidad de usar una escala no lineal si el intervalo de valores es grande y los usuarios probablemente seleccionarán valores en un extremo del intervalo.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-142">**Consider using a non-linear scale if the range of values is large and users will likely select values at one end of the range.**</span></span> <span data-ttu-id="c9d25-143">Por ejemplo, el valor de hora puede ser 1 minuto, 1 hora, 1 día o 1 mes.</span><span class="sxs-lookup"><span data-stu-id="c9d25-143">For example, time value might be 1 minute, 1 hour, 1 day, or 1 month.</span></span>
-   <span data-ttu-id="c9d25-144">**Siempre que sea práctico, proporcione comentarios inmediatos mientras o después de que un usuario realice una selección.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-144">**Whenever practical, give immediate feedback while or after a user makes a selection.**</span></span> <span data-ttu-id="c9d25-145">Por ejemplo, el control de volumen de Microsoft Windows emite un pitido para indicar el volumen de audio resultante.</span><span class="sxs-lookup"><span data-stu-id="c9d25-145">For example, the Microsoft Windows volume control beeps to indicate the resulting audio volume.</span></span>
-   <span data-ttu-id="c9d25-146">**Usa etiquetas para mostrar el intervalo de valores.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-146">**Use labels to show the range of values.**</span></span>

    <span data-ttu-id="c9d25-147">**Excepción:** Si el control deslizante está orientado verticalmente y la etiqueta superior es máxima, alta, más o equivalente, puede omitir las demás etiquetas, ya que el significado es claro.</span><span class="sxs-lookup"><span data-stu-id="c9d25-147">**Exception:** If the slider is vertically oriented and the top label is Maximum, High, More, or equivalent, you can omit the other labels since the meaning is clear.</span></span>

    ![<span data-ttu-id="c9d25-148">figura de un control deslizante vertical</span><span class="sxs-lookup"><span data-stu-id="c9d25-148">figure of a vertical slider</span></span> ](images/ctrl-sliders-image2.png)

    <span data-ttu-id="c9d25-149">En este ejemplo, la orientación vertical del control deslizante hace que las etiquetas de rango sean innecesarias.</span><span class="sxs-lookup"><span data-stu-id="c9d25-149">In this example, the slider's vertical orientation makes the range labels unnecessary.</span></span>

-   <span data-ttu-id="c9d25-150">**Use marcas de graduación cuando los usuarios necesiten conocer el valor aproximado de la configuración.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-150">**Use tick marks when users need to know the approximate value of the setting.**</span></span>
-   <span data-ttu-id="c9d25-151">**Use marcas de graduación y una etiqueta de valor cuando los usuarios necesiten conocer el valor exacto de la configuración que elijan.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-151">**Use tick marks and a value label when users need to know the exact value of the setting they choose.**</span></span> <span data-ttu-id="c9d25-152">Use siempre una etiqueta de valor si un usuario debe conocer las unidades para tener sentido en la configuración.</span><span class="sxs-lookup"><span data-stu-id="c9d25-152">Always use a value label if a user needs to know the units to make sense of the setting.</span></span>

    ![<span data-ttu-id="c9d25-153">figura del control deslizante mostrando el número de píxeles seleccionado</span><span class="sxs-lookup"><span data-stu-id="c9d25-153">figure of slider showing number of pixels selected</span></span> ](images/ctrl-sliders-image3.png)

    <span data-ttu-id="c9d25-154">En este ejemplo, se utiliza una etiqueta para indicar claramente el valor seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c9d25-154">In this example, a label is used to clearly indicate the selected value.</span></span>

-   <span data-ttu-id="c9d25-155">**En los controles deslizantes orientados horizontalmente, coloque marcas de graduación en el control deslizante.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-155">**For horizontally-oriented sliders, place tick marks under the slider.**</span></span> <span data-ttu-id="c9d25-156">En los controles deslizantes orientados verticalmente, coloque las marcas de graduación a la derecha para las referencias culturales occidentales; en el caso de las referencias culturales que se leen de derecha a izquierda, haga lo contrario.</span><span class="sxs-lookup"><span data-stu-id="c9d25-156">For vertically-oriented sliders, place tick marks to the right for Western cultures; for cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="c9d25-157">**Coloque la etiqueta de valor completamente debajo del control deslizante para que la relación sea clara.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-157">**Place the value label completely under the slider control so that the relationship is clear.**</span></span>

    <span data-ttu-id="c9d25-158">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="c9d25-158">**Incorrect:**</span></span>

    ![<span data-ttu-id="c9d25-159">figura de una etiqueta que es más larga que su control deslizante</span><span class="sxs-lookup"><span data-stu-id="c9d25-159">figure of a label that is longer than its slider</span></span> ](images/ctrl-sliders-image4.png)

    <span data-ttu-id="c9d25-160">En este ejemplo, la etiqueta de valor no está alineada en el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="c9d25-160">In this example, the value label isn't aligned under the slider.</span></span>

-   <span data-ttu-id="c9d25-161">**Al deshabilitar un control deslizante, deshabilite también las etiquetas asociadas.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-161">**When disabling a slider, also disable any associated labels.**</span></span>
-   <span data-ttu-id="c9d25-162">**No use un control deslizante y un cuadro de texto numérico para la misma configuración.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-162">**Don't use both a slider and a numeric text box for the same setting.**</span></span> <span data-ttu-id="c9d25-163">Use solo el control más adecuado.</span><span class="sxs-lookup"><span data-stu-id="c9d25-163">Use only the more appropriate control.</span></span>

    <span data-ttu-id="c9d25-164">**Excepción:** Use ambos controles cuando el usuario necesite comentarios inmediatos y la capacidad de establecer un valor numérico exacto.</span><span class="sxs-lookup"><span data-stu-id="c9d25-164">**Exception:** Use both controls when the user needs both immediate feedback and the ability to set an exact numeric value.</span></span>

-   <span data-ttu-id="c9d25-165">**No uses un control deslizante como indicador de progreso.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-165">**Don't use a slider as a progress indicator.**</span></span>
-   <span data-ttu-id="c9d25-166">**No cambie el tamaño del indicador deslizante del tamaño predeterminado.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-166">**Don't change the size of the slider indicator from the default size.**</span></span>

    <span data-ttu-id="c9d25-167">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="c9d25-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="c9d25-168">figura del control deslizante que es menor que el valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="c9d25-168">figure of slider that is smaller than the default</span></span> ](images/ctrl-sliders-image5.png)

    <span data-ttu-id="c9d25-169">En este ejemplo, se usa un tamaño menor que el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c9d25-169">In this example, a size smaller than the default is used.</span></span>

    <span data-ttu-id="c9d25-170">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="c9d25-170">**Correct:**</span></span>

    ![<span data-ttu-id="c9d25-171">Ilustración que muestra el control deslizante predeterminado</span><span class="sxs-lookup"><span data-stu-id="c9d25-171">figure showing the default slider</span></span> ](images/ctrl-sliders-image6.png)

    <span data-ttu-id="c9d25-172">En este ejemplo, se usa el tamaño predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c9d25-172">In this example, the default size is used.</span></span>

-   <span data-ttu-id="c9d25-173">**No etiquete todas las marcas de graduación.**</span><span class="sxs-lookup"><span data-stu-id="c9d25-173">**Don't label every tick mark.**</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="c9d25-174">Ajuste de tamaño y espaciado recomendados</span><span class="sxs-lookup"><span data-stu-id="c9d25-174">Recommended sizing and spacing</span></span>

![<span data-ttu-id="c9d25-175">figura de ajuste de tamaño y espaciado del control deslizante recomendado</span><span class="sxs-lookup"><span data-stu-id="c9d25-175">figure of recommended slider sizing and spacing</span></span> ](images/ctrl-sliders-image7.png)

<span data-ttu-id="c9d25-176">Ajuste de tamaño y espaciado recomendados para los controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="c9d25-176">Recommended sizing and spacing for sliders.</span></span>

## <a name="labels"></a><span data-ttu-id="c9d25-177">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="c9d25-177">Labels</span></span>

### <a name="slider-labels"></a><span data-ttu-id="c9d25-178">Etiquetas de control deslizante</span><span class="sxs-lookup"><span data-stu-id="c9d25-178">Slider labels</span></span>

-   <span data-ttu-id="c9d25-179">Use una etiqueta de texto estático que termine con un signo de dos puntos o una etiqueta de cuadro de grupo sin puntuación final.</span><span class="sxs-lookup"><span data-stu-id="c9d25-179">Use a static text label ending with a colon, or a group box label with no ending punctuation.</span></span>
-   <span data-ttu-id="c9d25-180">Asigne una clave de acceso única a cada etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c9d25-180">Assign a unique access key to each label.</span></span> <span data-ttu-id="c9d25-181">Para obtener instrucciones sobre las asignaciones, consulte [teclado](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="c9d25-181">For assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="c9d25-182">Use mayúsculas de estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="c9d25-182">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c9d25-183">Coloque la etiqueta del control deslizante a la izquierda del control deslizante, o encima y alineada con el borde izquierdo del control deslizante (o su identificador de intervalo izquierdo, si está presente).</span><span class="sxs-lookup"><span data-stu-id="c9d25-183">Position the slider label either to the left of the slider, or above and aligned with the left edge of the slider (or its left range identifier, if present).</span></span>

### <a name="range-labels"></a><span data-ttu-id="c9d25-184">Etiquetas de intervalo</span><span class="sxs-lookup"><span data-stu-id="c9d25-184">Range labels</span></span>

-   <span data-ttu-id="c9d25-185">Etiqueta los dos extremos del intervalo del control deslizante, a menos que la orientación vertical haga que resulte innecesario.</span><span class="sxs-lookup"><span data-stu-id="c9d25-185">Label the two ends of the slider range, unless a vertical orientation makes this unnecessary.</span></span>
-   <span data-ttu-id="c9d25-186">Use solo Word, si es posible, para cada etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c9d25-186">Use only word, if possible, for each label.</span></span>
-   <span data-ttu-id="c9d25-187">No uses puntuación final.</span><span class="sxs-lookup"><span data-stu-id="c9d25-187">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="c9d25-188">Asegúrate de que las etiquetas sean descriptivas y estén paralelas.</span><span class="sxs-lookup"><span data-stu-id="c9d25-188">Make sure these labels are descriptive and parallel.</span></span> <span data-ttu-id="c9d25-189">Ejemplos: Máximo/Mínimo, Más/Menos, Bajo/Alto, Suave/Fuerte.</span><span class="sxs-lookup"><span data-stu-id="c9d25-189">Examples: Maximum/Minimum, More/Less, Low/High, Soft/Loud.</span></span>
-   <span data-ttu-id="c9d25-190">Use mayúsculas de estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="c9d25-190">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c9d25-191">No asigne claves de acceso.</span><span class="sxs-lookup"><span data-stu-id="c9d25-191">Don't assign access keys.</span></span>

### <a name="value-labels"></a><span data-ttu-id="c9d25-192">Etiquetas de valor</span><span class="sxs-lookup"><span data-stu-id="c9d25-192">Value labels</span></span>

-   <span data-ttu-id="c9d25-193">Si necesitas una etiqueta de valor, muéstrala debajo del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="c9d25-193">If you need a value label, display it below the slider.</span></span>
-   <span data-ttu-id="c9d25-194">Centra el texto en relación con el control e incluye las unidades (como pueden ser píxeles).</span><span class="sxs-lookup"><span data-stu-id="c9d25-194">Center the text relative to the control and include the units (such as pixels).</span></span>

    ![<span data-ttu-id="c9d25-195">figura de la etiqueta centrada en el control deslizante</span><span class="sxs-lookup"><span data-stu-id="c9d25-195">figure of label centered under the slider</span></span> ](images/ctrl-sliders-image8.png)

    <span data-ttu-id="c9d25-196">En este ejemplo, la etiqueta de valor se centra en el control deslizante e incluye las unidades.</span><span class="sxs-lookup"><span data-stu-id="c9d25-196">In this example, the value label is centered under the slider and includes the units.</span></span>

## <a name="documentation"></a><span data-ttu-id="c9d25-197">Documentación</span><span class="sxs-lookup"><span data-stu-id="c9d25-197">Documentation</span></span>

<span data-ttu-id="c9d25-198">Al hacer referencia a los controles deslizantes:</span><span class="sxs-lookup"><span data-stu-id="c9d25-198">When referring to sliders:</span></span>

-   <span data-ttu-id="c9d25-199">Use el texto de etiqueta exacto, incluido el uso de mayúsculas, e incluya el control deslizante de palabra.</span><span class="sxs-lookup"><span data-stu-id="c9d25-199">Use the exact label text, including its capitalization, and include the word slider.</span></span> <span data-ttu-id="c9d25-200">No incluya el carácter de subrayado o el signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="c9d25-200">Don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="c9d25-201">Para describir la interacción del usuario, use Move.</span><span class="sxs-lookup"><span data-stu-id="c9d25-201">To describe user interaction, use move.</span></span>
-   <span data-ttu-id="c9d25-202">Siempre que sea posible, dé formato a la etiqueta usando texto en negrita.</span><span class="sxs-lookup"><span data-stu-id="c9d25-202">When possible, format the label using bold text.</span></span> <span data-ttu-id="c9d25-203">De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.</span><span class="sxs-lookup"><span data-stu-id="c9d25-203">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="c9d25-204">Ejemplo: para aumentar la resolución de pantalla, mueva el control deslizante de **resolución de pantalla** a la derecha.</span><span class="sxs-lookup"><span data-stu-id="c9d25-204">Example: To increase your screen resolution, move the **Screen resolution** slider to the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9d25-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9d25-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d25-206">Glosario</span><span class="sxs-lookup"><span data-stu-id="c9d25-206">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 