---
title: Casillas
description: Con una casilla, los usuarios tomarán una decisión entre dos opciones claramente opuestas.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 20cf5bc4fd13b974f87fbb33a5fea9a365f99735
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524309"
---
# <a name="check-boxes"></a><span data-ttu-id="e1698-103">Casillas</span><span class="sxs-lookup"><span data-stu-id="e1698-103">Check Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="e1698-104">Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1698-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="e1698-105">Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)</span><span class="sxs-lookup"><span data-stu-id="e1698-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="e1698-106">Con una casilla, los usuarios tomarán una decisión entre dos opciones claramente opuestas.</span><span class="sxs-lookup"><span data-stu-id="e1698-106">With a check box, users make a decision between two clearly opposite choices.</span></span> <span data-ttu-id="e1698-107">La etiqueta de casilla indica el estado seleccionado, mientras que el significado del estado borrado debe ser el opuesto inequívoco del estado seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e1698-107">The check box label indicates the selected state, whereas the meaning of the cleared state must be the unambiguous opposite of the selected state.</span></span> <span data-ttu-id="e1698-108">Por lo tanto, solo se deben usar casillas para activar o desactivar una opción o para seleccionar o **anular la selección de un elemento.**</span><span class="sxs-lookup"><span data-stu-id="e1698-108">Consequently, **check boxes should be used only to toggle an option on or off or to select or deselect an item.**</span></span>

![<span data-ttu-id="e1698-109">captura de pantalla de una de las cuatro casillas activadas</span><span class="sxs-lookup"><span data-stu-id="e1698-109">screen shot of one of four check boxes selected</span></span> ](images/ctrl-check-boxes-image1.png)

<span data-ttu-id="e1698-110">Un grupo típico de casillas.</span><span class="sxs-lookup"><span data-stu-id="e1698-110">A typical group of check boxes.</span></span>

> [!Note]  
> <span data-ttu-id="e1698-111">Las instrucciones relacionadas [con el diseño](vis-layout.md) se presentan en un artículo independiente.</span><span class="sxs-lookup"><span data-stu-id="e1698-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="e1698-112">¿Es este el control adecuado?</span><span class="sxs-lookup"><span data-stu-id="e1698-112">Is this the right control?</span></span>

<span data-ttu-id="e1698-113">Para decidirte, intenta responder a estas preguntas:</span><span class="sxs-lookup"><span data-stu-id="e1698-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="e1698-114">**¿Se usa la casilla para activar o desactivar una opción o para seleccionar o anular la selección de un elemento?**</span><span class="sxs-lookup"><span data-stu-id="e1698-114">**Is the check box used to toggle an option on or off or to select or deselect an item?**</span></span> <span data-ttu-id="e1698-115">Si no es así, usa otro control.</span><span class="sxs-lookup"><span data-stu-id="e1698-115">If not, use another control.</span></span>
-   <span data-ttu-id="e1698-116">**¿Los estados seleccionados y borrados son opuestos claros e inequívocos?**</span><span class="sxs-lookup"><span data-stu-id="e1698-116">**Are the selected and cleared states clear and unambiguous opposites?**</span></span> <span data-ttu-id="e1698-117">Si no es así, use [botones](ctrl-radio-buttons.md) de radio o [una lista](/windows/desktop/uxguide/ctrl-drop) desplegable para poder etiquetar los estados de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="e1698-117">If not, use [radio buttons](ctrl-radio-buttons.md) or a [drop-down list](/windows/desktop/uxguide/ctrl-drop) so that you can label the states independently.</span></span>
-   <span data-ttu-id="e1698-118">**Cuando se usa en un grupo, ¿consta el grupo de opciones independientes, entre las que los usuarios pueden elegir cero o más?**</span><span class="sxs-lookup"><span data-stu-id="e1698-118">**When used in a group, does the group comprise independent choices, from which users may choose zero or more?**</span></span> <span data-ttu-id="e1698-119">Si no es así, tenga en cuenta los controles para las opciones dependientes, como los botones de radio y las [vistas de árbol de casillas](ctrl-tree-views.md).</span><span class="sxs-lookup"><span data-stu-id="e1698-119">If not, consider controls for dependent choices, such as radio buttons and [check box tree views](ctrl-tree-views.md).</span></span>
-   <span data-ttu-id="e1698-120">**Cuando se usa en un grupo, ¿consta el grupo de opciones dependientes, entre las que los usuarios deben elegir uno o varios?**</span><span class="sxs-lookup"><span data-stu-id="e1698-120">**When used in a group, does the group comprise dependent choices, from which users must choose one or more?**</span></span> <span data-ttu-id="e1698-121">Si es así, use un grupo de casillas y controle el error cuando no se seleccione ninguna de las opciones.</span><span class="sxs-lookup"><span data-stu-id="e1698-121">If so, use a group of check boxes and handle the error when none of the options are selected.</span></span>
-   <span data-ttu-id="e1698-122">**¿El número de opciones de un grupo es 10 o menos?**</span><span class="sxs-lookup"><span data-stu-id="e1698-122">**Is the number of options in a group 10 or fewer?**</span></span> <span data-ttu-id="e1698-123">Puesto que el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de casillas en 10 o menos.</span><span class="sxs-lookup"><span data-stu-id="e1698-123">Since the screen space used is proportional to the number of options, keep the number of check boxes to 10 or fewer.</span></span> <span data-ttu-id="e1698-124">Para más de 10 opciones, use una lista [de casillas](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="e1698-124">For more than 10 options, use a [check box list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="e1698-125">**¿Sería mejor un botón de radio?**</span><span class="sxs-lookup"><span data-stu-id="e1698-125">**Would a radio button be a better choice?**</span></span> <span data-ttu-id="e1698-126">Cuando las casillas solo son adecuadas para activar o desactivar una opción, se pueden usar botones de radio para opciones completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="e1698-126">Where check boxes are suitable only for turning an option on or off, radio buttons can be used for completely different options.</span></span> <span data-ttu-id="e1698-127">Si ambas soluciones son posibles:</span><span class="sxs-lookup"><span data-stu-id="e1698-127">If both solutions are possible:</span></span>
    -   <span data-ttu-id="e1698-128">Use botones de radio si el significado de la casilla desactivada no es completamente obvio.</span><span class="sxs-lookup"><span data-stu-id="e1698-128">Use radio buttons if the meaning of the cleared check box isn't completely obvious.</span></span>

        <span data-ttu-id="e1698-129">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-129">**Incorrect:**</span></span>

        ![<span data-ttu-id="e1698-130">captura de pantalla de una casilla con la etiqueta horizontal</span><span class="sxs-lookup"><span data-stu-id="e1698-130">screen shot of one check box labeled landscape</span></span> ](images/ctrl-check-boxes-image2.png)

        <span data-ttu-id="e1698-131">En este ejemplo, la opción opuesta de Horizontal no está clara, por lo que la casilla no es una buena opción.</span><span class="sxs-lookup"><span data-stu-id="e1698-131">In this example, the opposite choice from Landscape isn't clear, so the check box isn't a good choice.</span></span>

        <span data-ttu-id="e1698-132">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-132">**Correct:**</span></span>

        ![<span data-ttu-id="e1698-133">captura de pantalla de dos botones de radio</span><span class="sxs-lookup"><span data-stu-id="e1698-133">screen shot of two radio buttons</span></span> ](images/ctrl-check-boxes-image3.png)

        <span data-ttu-id="e1698-134">En este ejemplo, las opciones no son opuestas, por lo que los botones de radio son la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="e1698-134">In this example, the choices are not opposites so radio buttons are the better choice.</span></span>

    -   <span data-ttu-id="e1698-135">Use botones de radio en las páginas del asistente para borrar las alternativas, aunque una casilla sea aceptable de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="e1698-135">Use radio buttons on wizard pages to make the alternatives clear, even if a check box is otherwise acceptable.</span></span>
    -   <span data-ttu-id="e1698-136">Use botones de radio si tiene suficiente espacio en la pantalla y las opciones son lo suficientemente importantes como para ser un buen uso de ese espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e1698-136">Use radio buttons if you have enough screen space and the options are important enough to be a good use of that screen space.</span></span> <span data-ttu-id="e1698-137">De lo contrario, use una casilla o una lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="e1698-137">Otherwise, use a check box or a drop-down list.</span></span>

        <span data-ttu-id="e1698-138">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-138">**Incorrect:**</span></span>

        ![<span data-ttu-id="e1698-139">captura de pantalla de los botones mostrar y no mostrar relación</span><span class="sxs-lookup"><span data-stu-id="e1698-139">screen shot of show and don't show ratio buttons</span></span> ](images/ctrl-check-boxes-image4.png)

        <span data-ttu-id="e1698-140">En este ejemplo, las opciones no son lo suficientemente importantes como para usar botones de radio.</span><span class="sxs-lookup"><span data-stu-id="e1698-140">In this example, the options aren't important enough to use radio buttons.</span></span>

        <span data-ttu-id="e1698-141">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-141">**Correct:**</span></span>

        ![<span data-ttu-id="e1698-142">captura de pantalla de la casilla con no mostrar el mensaje</span><span class="sxs-lookup"><span data-stu-id="e1698-142">screen shot of check box with don't show message</span></span> ](images/ctrl-check-boxes-image5.png)

        <span data-ttu-id="e1698-143">En este ejemplo, una casilla es un uso eficaz del espacio de pantalla para esta opción de periférico.</span><span class="sxs-lookup"><span data-stu-id="e1698-143">In this example, a check box is an efficient use of screen space for this peripheral option.</span></span>

-   <span data-ttu-id="e1698-144">Use una casilla si hay otras casillas en la ventana.</span><span class="sxs-lookup"><span data-stu-id="e1698-144">Use a check box if there other check boxes on the window.</span></span>
-   <span data-ttu-id="e1698-145">**¿La opción presenta una opción de programa, en lugar de datos?**</span><span class="sxs-lookup"><span data-stu-id="e1698-145">**Does the option present a program option, rather than data?**</span></span> <span data-ttu-id="e1698-146">Los valores de la opción no deben basarse en el contexto ni en otros datos.</span><span class="sxs-lookup"><span data-stu-id="e1698-146">The option's values shouldn't be based on context or other data.</span></span> <span data-ttu-id="e1698-147">Para los datos, use una lista de casillas o [una lista de selección múltiple](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="e1698-147">For data, use a check box list or [multiple-selection list](ctrl-list-boxes.md).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="e1698-148">Patrones de uso</span><span class="sxs-lookup"><span data-stu-id="e1698-148">Usage patterns</span></span>

<span data-ttu-id="e1698-149">Las casillas tienen varios patrones de uso:</span><span class="sxs-lookup"><span data-stu-id="e1698-149">Check boxes have several usage patterns:</span></span>



|    <span data-ttu-id="e1698-150">Uso</span><span class="sxs-lookup"><span data-stu-id="e1698-150">Usage</span></span>                                                                          |         <span data-ttu-id="e1698-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1698-151">Example</span></span>                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1698-152">**Una opción individual** Se usa una sola casilla para seleccionar una opción individual.</span><span class="sxs-lookup"><span data-stu-id="e1698-152">**An individual choice** A single check box is used to select an individual choice.</span></span> <br/>                                                                                                             | ![<span data-ttu-id="e1698-153">captura de pantalla de una casilla con recordatorios etiqueta</span><span class="sxs-lookup"><span data-stu-id="e1698-153">screen shot of one check box with remind me label</span></span> ](images/ctrl-check-boxes-image6.png)<br/> <span data-ttu-id="e1698-154">Se usa una sola casilla para una opción individual.</span><span class="sxs-lookup"><span data-stu-id="e1698-154">A single check box is used for an individual choice.</span></span><br/>                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e1698-155">**Opciones independientes (cero o más)** Se usa un grupo de casillas para seleccionar entre un conjunto de cero o más opciones.</span><span class="sxs-lookup"><span data-stu-id="e1698-155">**Independent choices (zero or more)** A group of check boxes is used to select from a set of zero or more choices.</span></span><br/>                                                                              | <span data-ttu-id="e1698-156">A diferencia de los controles de selección única, como los [botones de radio,](ctrl-radio-buttons.md)los usuarios pueden seleccionar cualquier combinación de opciones en un grupo de casillas.</span><span class="sxs-lookup"><span data-stu-id="e1698-156">unlike single-selection controls such as [radio buttons](ctrl-radio-buttons.md), users can select any combination of options in a group of check boxes.</span></span><br/> <span data-ttu-id="e1698-157">![captura de pantalla de dos de tres casillas activadas ](images/ctrl-check-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="e1698-157">![screen shot of two of three check boxes selected ](images/ctrl-check-boxes-image7.png)</span></span><br/> <span data-ttu-id="e1698-158">Se usa un grupo de casillas para las opciones independientes.</span><span class="sxs-lookup"><span data-stu-id="e1698-158">A group of check boxes is used for independent choices.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="e1698-159">**Opciones dependientes (una o varias)** También se puede usar un grupo de casillas para seleccionar entre un conjunto de una o varias opciones.</span><span class="sxs-lookup"><span data-stu-id="e1698-159">**Dependent choices (one or more)** A group of check boxes can also be used to select from a set of one or more choices.</span></span><br/>                                                                         | <span data-ttu-id="e1698-160">**es posible que tenga que representar una selección de una o varias opciones dependientes.**</span><span class="sxs-lookup"><span data-stu-id="e1698-160">**you may need to represent a selection of one or more dependent choices**.</span></span> <span data-ttu-id="e1698-161">Dado que microsoft?windows no tiene un control que admita directamente este tipo de entrada, la mejor solución es usar un grupo de casillas y controlar el error cuando no se selecciona ninguna de las opciones.</span><span class="sxs-lookup"><span data-stu-id="e1698-161">because microsoft?windows doesn't have a control that directly supports this type of input, the best solution is to use a group of check boxes and handle the error when none of the options are selected.</span></span><br/> <span data-ttu-id="e1698-162">![captura de pantalla de una de las dos casillas activadas ](images/ctrl-check-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="e1698-162">![screen shot of one of two check boxes selected ](images/ctrl-check-boxes-image8.png)</span></span><br/> <span data-ttu-id="e1698-163">Se usa un grupo de casillas donde se debe seleccionar al menos un protocolo.</span><span class="sxs-lookup"><span data-stu-id="e1698-163">A group of check boxes is used where at least one protocol must be selected.</span></span><br/> |
| <span data-ttu-id="e1698-164">**Opción mixta** Además de sus estados seleccionados y desactivados, las casillas también tienen un estado mixto para varias selecciones para indicar que la opción está establecida para algunos objetos, pero no para todos.</span><span class="sxs-lookup"><span data-stu-id="e1698-164">**Mixed choice** In addition to their selected and cleared states, check boxes also have a mixed state for multiple selection to indicate that the option is set for some, but not all, objects.</span></span><br/> | ![<span data-ttu-id="e1698-165">captura de pantalla de una casilla azul sólido de solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1698-165">screen shot of a solid blue read-only check box</span></span> ](images/ctrl-check-boxes-image9.png)<br/> <span data-ttu-id="e1698-166">Casilla de verificación de estado mixto.</span><span class="sxs-lookup"><span data-stu-id="e1698-166">A mixed-state check box.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a><span data-ttu-id="e1698-167">Directrices</span><span class="sxs-lookup"><span data-stu-id="e1698-167">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="e1698-168">General</span><span class="sxs-lookup"><span data-stu-id="e1698-168">General</span></span>

-   <span data-ttu-id="e1698-169">**Casillas relacionadas con el grupo**.</span><span class="sxs-lookup"><span data-stu-id="e1698-169">**Group related check boxes**.</span></span> <span data-ttu-id="e1698-170">Combine opciones relacionadas y separe las opciones no relacionadas en grupos de 10 o menos, mediante varios grupos si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e1698-170">Combine related options and separate unrelated options into groups of 10 or fewer, using multiple groups if necessary.</span></span>

    ![<span data-ttu-id="e1698-171">captura de pantalla de casillas relacionadas y no relacionadas</span><span class="sxs-lookup"><span data-stu-id="e1698-171">screen shot of related and unrelated check boxes</span></span> ](images/ctrl-check-boxes-image10.png)

    <span data-ttu-id="e1698-172">Un ejemplo de grupos de opciones relacionadas e independientes.</span><span class="sxs-lookup"><span data-stu-id="e1698-172">An example of groups of related, independent options.</span></span>

-   <span data-ttu-id="e1698-173">**El uso de cuadros de grupo para organizar grupos de casillas** suele dar lugar a un desorden innecesario en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e1698-173">**Reconsider using group boxes to organize groups of check boxes** this often results in unnecessary screen clutter.</span></span>
-   <span data-ttu-id="e1698-174">**Active las casillas en un** orden lógico, como agrupar opciones muy relacionadas, colocar primero las opciones más comunes o seguir alguna otra progresión natural.</span><span class="sxs-lookup"><span data-stu-id="e1698-174">**List check boxes in a logical order**, such as grouping highly related options together or placing most common options first, or following some other natural progression.</span></span> <span data-ttu-id="e1698-175">No se recomienda el orden alfabético porque depende del idioma y, por lo tanto, no es localizable.</span><span class="sxs-lookup"><span data-stu-id="e1698-175">Alphabetical ordering isn't recommended because it is language dependent, and therefore not localizable.</span></span>
-   <span data-ttu-id="e1698-176">**Alinee las casillas verticalmente, no horizontalmente.**</span><span class="sxs-lookup"><span data-stu-id="e1698-176">**Align check boxes vertically, not horizontally**.</span></span> <span data-ttu-id="e1698-177">La alineación horizontal es más difícil de leer.</span><span class="sxs-lookup"><span data-stu-id="e1698-177">Horizontal alignment is harder to read.</span></span>

    <span data-ttu-id="e1698-178">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-178">**Correct:**</span></span>

    ![<span data-ttu-id="e1698-179">captura de pantalla de casillas alineadas verticalmente</span><span class="sxs-lookup"><span data-stu-id="e1698-179">screen shot of check boxes aligned vertically</span></span> ](images/ctrl-check-boxes-image11.png)

    <span data-ttu-id="e1698-180">En este ejemplo, las casillas están alineadas correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1698-180">In this example, the check boxes are correctly aligned.</span></span>

    <span data-ttu-id="e1698-181">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-181">**Incorrect:**</span></span>

    ![<span data-ttu-id="e1698-182">captura de pantalla de casillas alineadas horizontalmente</span><span class="sxs-lookup"><span data-stu-id="e1698-182">screen shot of check boxes aligned horizontally</span></span> ](images/ctrl-check-boxes-image12.png)

    <span data-ttu-id="e1698-183">En este ejemplo, la alineación horizontal es más difícil de leer.</span><span class="sxs-lookup"><span data-stu-id="e1698-183">In this example, the horizontal alignment is harder to read.</span></span>

-   <span data-ttu-id="e1698-184">**No use el estado mixto para representar un tercer estado.**</span><span class="sxs-lookup"><span data-stu-id="e1698-184">**Don't use the mixed state to represent a third state.**</span></span> <span data-ttu-id="e1698-185">El estado mixto se usa para indicar que se ha establecido una opción para algunos objetos secundarios, pero no para todos.</span><span class="sxs-lookup"><span data-stu-id="e1698-185">The mixed state is used to indicate that an option is set for some, but not all, child objects.</span></span> <span data-ttu-id="e1698-186">Los usuarios no deben poder establecer un estado mixto directamente, sino que el estado mixto es un reflejo de los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e1698-186">Users shouldn't be able to set a mixed state directly rather the mixed state is a reflection of the child objects.</span></span> <span data-ttu-id="e1698-187">El estado mixto no se usa como tercer estado para un elemento individual.</span><span class="sxs-lookup"><span data-stu-id="e1698-187">The mixed state isn't used as a third state for an individual item.</span></span> <span data-ttu-id="e1698-188">Para representar un tercer estado, use botones de radio o una lista desplegable en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e1698-188">To represent a third state, use radio buttons or a drop-down list instead.</span></span>

    <span data-ttu-id="e1698-189">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-189">**Incorrect:**</span></span>

    ![<span data-ttu-id="e1698-190">captura de pantalla del servicio de tema azul sólido</span><span class="sxs-lookup"><span data-stu-id="e1698-190">screen shot of solid blue theme service check box</span></span> ](images/ctrl-check-boxes-image13.png)

    <span data-ttu-id="e1698-191">En este ejemplo, se supone que el estado mixto indica que el servicio Theme no está instalado.</span><span class="sxs-lookup"><span data-stu-id="e1698-191">In this example, the mixed state is supposed to indicate that the Theme service isn't installed.</span></span>

    <span data-ttu-id="e1698-192">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-192">**Correct:**</span></span>

    ![<span data-ttu-id="e1698-193">captura de pantalla de la lista desplegable con tres opciones</span><span class="sxs-lookup"><span data-stu-id="e1698-193">screen shot of drop-down list with three options</span></span> ](images/ctrl-check-boxes-image14.png)

    <span data-ttu-id="e1698-194">En este ejemplo, los usuarios pueden elegir entre una lista de tres opciones claras.</span><span class="sxs-lookup"><span data-stu-id="e1698-194">In this example, users can choose from a list of three clear options.</span></span>

-   <span data-ttu-id="e1698-195">**Al hacer clic en una casilla de estado mixto, debe recorrer todos los estados seleccionados, todos desactivados y los estados mixtos originales.**</span><span class="sxs-lookup"><span data-stu-id="e1698-195">**Clicking a mixed state check box should cycle through all selected, all cleared, and the original mixed states.**</span></span> <span data-ttu-id="e1698-196">Por motivos de restauración, es importante poder restaurar el estado mixto original porque la configuración puede ser compleja o desconocida para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e1698-196">For forgiveness, it's important to be able to restore the original mixed state because the settings might be complex or unknown to the user.</span></span> <span data-ttu-id="e1698-197">De lo contrario, la única manera de restaurar el estado mixto con confianza sería cancelar la tarea e iniciar de nuevo.</span><span class="sxs-lookup"><span data-stu-id="e1698-197">Otherwise, the only way to restore the mixed state with confidence would be to cancel the task and start over.</span></span>
-   <span data-ttu-id="e1698-198">**No use casillas como indicador de progreso.**</span><span class="sxs-lookup"><span data-stu-id="e1698-198">**Don't use check boxes as a progress indicator**.</span></span> <span data-ttu-id="e1698-199">En su lugar, use un control [de indicador](progress-bars.md) de progreso.</span><span class="sxs-lookup"><span data-stu-id="e1698-199">Use a [progress indicator](progress-bars.md) control instead.</span></span>

    <span data-ttu-id="e1698-200">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-200">**Incorrect:**</span></span>

    ![<span data-ttu-id="e1698-201">captura de pantalla de cuatro casillas que muestran el progreso</span><span class="sxs-lookup"><span data-stu-id="e1698-201">screen shot of four check boxes showing progress</span></span> ](images/ctrl-check-boxes-image15.png)

    <span data-ttu-id="e1698-202">En este ejemplo, las casillas se usan incorrectamente como indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="e1698-202">In this example, check boxes are used incorrectly as a progress indicator.</span></span>

    <span data-ttu-id="e1698-203">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-203">**Correct:**</span></span>

    ![<span data-ttu-id="e1698-204">captura de pantalla de una barra de progreso parcialmente rellenada</span><span class="sxs-lookup"><span data-stu-id="e1698-204">screen shot of a partially filled progress bar</span></span> ](images/ctrl-check-boxes-image16.png)

    <span data-ttu-id="e1698-205">Ejemplo de una barra de progreso típica.</span><span class="sxs-lookup"><span data-stu-id="e1698-205">Example of a typical progress bar.</span></span>

-   <span data-ttu-id="e1698-206">**Mostrar las casillas deshabilitadas con el estado de selección correcto.**</span><span class="sxs-lookup"><span data-stu-id="e1698-206">**Show disabled check boxes using the correct selection state.**</span></span> <span data-ttu-id="e1698-207">Aunque los usuarios no puedan cambiarlos, las casillas deshabilitadas transmiten información para que sean coherentes con los resultados.</span><span class="sxs-lookup"><span data-stu-id="e1698-207">Even though users can't change them, disabled check boxes convey information so they should be consistent with results.</span></span>

    <span data-ttu-id="e1698-208">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-208">**Incorrect:**</span></span>

    ![<span data-ttu-id="e1698-209">captura de pantalla de una de las dos casillas atenuadas</span><span class="sxs-lookup"><span data-stu-id="e1698-209">screen shot of one of two check boxes dimmed</span></span> ](images/ctrl-check-boxes-image17.png)

    <span data-ttu-id="e1698-210">En este ejemplo, se debe borrar la opción "Leer siempre en voz alta esta sección" porque la sección no se lee cuando la opción está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e1698-210">In this example, the "Always read this section aloud" option should be cleared because the section isn't read when the option is disabled.</span></span>

-   <span data-ttu-id="e1698-211">**No use la selección de una casilla para**:</span><span class="sxs-lookup"><span data-stu-id="e1698-211">**Don't use the selection of a check box to**:</span></span>
    -   <span data-ttu-id="e1698-212">Realice comandos.</span><span class="sxs-lookup"><span data-stu-id="e1698-212">Perform commands.</span></span>
    -   <span data-ttu-id="e1698-213">Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.</span><span class="sxs-lookup"><span data-stu-id="e1698-213">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="e1698-214">Mostrar dinámicamente otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar tales eventos).</span><span class="sxs-lookup"><span data-stu-id="e1698-214">Dynamically display other controls related to the selected control (screen readers cannot detect such events).</span></span>

### <a name="dont-show-this-item-again"></a><span data-ttu-id="e1698-215">No mostrar esto</span><span class="sxs-lookup"><span data-stu-id="e1698-215">Don't show this</span></span> <item> <span data-ttu-id="e1698-216">Otra vez</span><span class="sxs-lookup"><span data-stu-id="e1698-216">again</span></span>

-   <span data-ttu-id="e1698-217">**Considere la posibilidad de usar una opción No volver a mostrar esta opción para permitir a los usuarios suprimir un cuadro de diálogo periódico solo si no <item> hay una alternativa mejor.**</span><span class="sxs-lookup"><span data-stu-id="e1698-217">**Consider using a Don't show this <item> again option to allow users to suppress a recurring dialog box only if there isn't a better alternative.**</span></span> <span data-ttu-id="e1698-218">Intente determinar de antemano si los usuarios realmente necesitan el cuadro de diálogo. Si lo hace, muestre siempre el diálogo y, si no lo hace, elimine el diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1698-218">Try to determine beforehand if users really need the dialog; if they do, always show the dialog, and if they don't, eliminate the dialog.</span></span>

<span data-ttu-id="e1698-219">Para obtener más instrucciones y ejemplos, vea [Cuadros de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="e1698-219">For more guidelines and examples, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="subordinate-controls"></a><span data-ttu-id="e1698-220">Controles subordinados</span><span class="sxs-lookup"><span data-stu-id="e1698-220">Subordinate controls</span></span>

-   <span data-ttu-id="e1698-221">Coloque los controles subordinados a la derecha o debajo (con sangría, vaciar con la etiqueta de casilla) la casilla y su etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e1698-221">Place subordinate controls to the right of or below (indented, flush with the check box label) the check box and its label.</span></span> <span data-ttu-id="e1698-222">Finalice la etiqueta de casilla con dos puntos.</span><span class="sxs-lookup"><span data-stu-id="e1698-222">End the check box label with a colon.</span></span>

    ![<span data-ttu-id="e1698-223">captura de pantalla del cuadro de texto debajo de la etiqueta de la casilla</span><span class="sxs-lookup"><span data-stu-id="e1698-223">screen shot of text box below check box label</span></span> ](images/ctrl-check-boxes-image18.png)

    <span data-ttu-id="e1698-224">En este ejemplo, la casilla y su control subordinado comparten la etiqueta de casilla y su clave de acceso.</span><span class="sxs-lookup"><span data-stu-id="e1698-224">In this example, the check box and its subordinate control share the check box label and its access key.</span></span>

-   <span data-ttu-id="e1698-225">**Deje habilitados los cuadros de texto editables dependientes y las listas desplegables si comparten la etiqueta de la casilla.**</span><span class="sxs-lookup"><span data-stu-id="e1698-225">**Leave dependent editable text boxes and drop-down lists enabled if they share the check box's label.**</span></span> <span data-ttu-id="e1698-226">Cuando los usuarios escriban o peguen algo en el cuadro, seleccione automáticamente la opción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e1698-226">When users type or paste anything into the box, select the corresponding option automatically.</span></span> <span data-ttu-id="e1698-227">Esto simplifica la interacción.</span><span class="sxs-lookup"><span data-stu-id="e1698-227">Doing so simplifies the interaction.</span></span>

    ![<span data-ttu-id="e1698-228">captura de pantalla de cuadros de texto de encabezado y pie de página</span><span class="sxs-lookup"><span data-stu-id="e1698-228">screen shot of header and footer text boxes</span></span> ](images/ctrl-check-boxes-image19.png)

    <span data-ttu-id="e1698-229">En este ejemplo, si se escribe un encabezado o un pie de página, se selecciona automáticamente la opción .</span><span class="sxs-lookup"><span data-stu-id="e1698-229">In this example, entering a header or footer automatically selects the option.</span></span>

-   <span data-ttu-id="e1698-230">Si anida casillas con botones de radio u otras casillas, **deshabilite** estos controles subordinados hasta que se seleccione la opción de alto nivel .</span><span class="sxs-lookup"><span data-stu-id="e1698-230">If you nest check boxes with radio buttons or other check boxes, **disable these subordinate controls until the high-level option is selected**.</span></span> <span data-ttu-id="e1698-231">Al hacerlo, se evita la confusión sobre el significado de los controles subordinados.</span><span class="sxs-lookup"><span data-stu-id="e1698-231">Doing so avoids confusion about the meaning of the subordinate controls.</span></span>
-   <span data-ttu-id="e1698-232">Haga que los controles subordinados en una casilla contigua con la casilla en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="e1698-232">Make subordinate controls to a check box contiguous with the check box in the tab order.</span></span>
-   <span data-ttu-id="e1698-233">**Si la selección de una opción implica la selección de casillas subordinadas, active explícitamente esas casillas para que la relación sea clara.**</span><span class="sxs-lookup"><span data-stu-id="e1698-233">**If selecting an option implies selecting subordinate check boxes, explicitly select those check boxes to make the relationship clear.**</span></span>

    <span data-ttu-id="e1698-234">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-234">**Incorrect:**</span></span>

    ![<span data-ttu-id="e1698-235">captura de pantalla: botón seleccionado, casillas desactivadas</span><span class="sxs-lookup"><span data-stu-id="e1698-235">screen shot: selected button, cleared check boxes</span></span> ](images/ctrl-check-boxes-image20.png)

    <span data-ttu-id="e1698-236">En este ejemplo, no se seleccionan las casillas subordinadas.</span><span class="sxs-lookup"><span data-stu-id="e1698-236">In this example, the subordinate check boxes aren't selected.</span></span>

    <span data-ttu-id="e1698-237">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-237">**Correct:**</span></span>

    ![<span data-ttu-id="e1698-238">captura de pantalla: botón seleccionado, casillas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="e1698-238">screen shot: selected button, selected check boxes</span></span> ](images/ctrl-check-boxes-image21.png)

    <span data-ttu-id="e1698-239">En este ejemplo, se seleccionan las casillas subordinadas, lo que hace que su relación con la opción seleccionada esté clara.</span><span class="sxs-lookup"><span data-stu-id="e1698-239">In this example, the subordinate check boxes are selected, making their relationship to the selected option clear.</span></span>

-   <span data-ttu-id="e1698-240">**Use las casillas dependientes si las alternativas agregan complejidad innecesaria.**</span><span class="sxs-lookup"><span data-stu-id="e1698-240">**Use dependent check boxes if the alternatives add unnecessary complexity**.</span></span> <span data-ttu-id="e1698-241">Aunque las casillas deben ser opciones independientes, a veces alternativas como los botones de radio agregan complejidad innecesaria.</span><span class="sxs-lookup"><span data-stu-id="e1698-241">While check boxes should be independent options, sometimes alternatives such as radio buttons add unnecessary complexity.</span></span>

    <span data-ttu-id="e1698-242">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-242">**Correct:**</span></span>

    ![<span data-ttu-id="e1698-243">captura de pantalla de botones y casillas confusos</span><span class="sxs-lookup"><span data-stu-id="e1698-243">screen shot of confusing buttons and check boxes</span></span> ](images/ctrl-check-boxes-image22.png)

    <span data-ttu-id="e1698-244">En este ejemplo, el uso de botones de radio es preciso, pero crea complejidad innecesaria.</span><span class="sxs-lookup"><span data-stu-id="e1698-244">In this example, the use of radio buttons is accurate, but creates unnecessary complexity.</span></span>

    <span data-ttu-id="e1698-245">**Mejor:**</span><span class="sxs-lookup"><span data-stu-id="e1698-245">**Better:**</span></span>

    ![<span data-ttu-id="e1698-246">captura de pantalla de las casillas solo</span><span class="sxs-lookup"><span data-stu-id="e1698-246">screen shot of check boxes only</span></span> ](images/ctrl-check-boxes-image23.png)

    <span data-ttu-id="e1698-247">En este ejemplo, el uso de casillas es más sencillo y permite a los usuarios centrarse en seleccionar las opciones deseadas en lugar de en su relación compleja.</span><span class="sxs-lookup"><span data-stu-id="e1698-247">In this example, the use of check boxes is simpler and allows users to focus on selecting the desired options instead of on their complex relationship.</span></span>

    <span data-ttu-id="e1698-248">**Importante: Aplique esta directriz solo en circunstancias** extremadamente poco frecuentes, al mostrar las dependencias agrega una complejidad significativa sin agregar claridad.</span><span class="sxs-lookup"><span data-stu-id="e1698-248">**Important: Apply this guideline only in extremely rare circumstances**, when showing the dependencies adds significant complexity without adding clarity.</span></span> <span data-ttu-id="e1698-249">En el ejemplo anterior, es poco probable que los usuarios intenten elegir superíndice y subíndice, y si lo hacen, sería fácil entender que eran opciones exclusivas.</span><span class="sxs-lookup"><span data-stu-id="e1698-249">In the previous example, it is unlikely that users would attempt to choose both superscript and subscript, and if they did, it would be easy to understand that they were exclusive options.</span></span>

### <a name="default-values"></a><span data-ttu-id="e1698-250">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="e1698-250">Default values</span></span>

-   <span data-ttu-id="e1698-251">Si una casilla es para una opción de usuario, establezca el estado más seguro (para evitar la pérdida de datos o el acceso al sistema), el estado más seguro y privado **de forma predeterminada.**</span><span class="sxs-lookup"><span data-stu-id="e1698-251">If a check box is for a user option, **set the safest (to prevent loss of data or system access), most secure and private state by default.**</span></span> <span data-ttu-id="e1698-252">Si la seguridad y la seguridad no son factores, seleccione el valor más probable o práctico.</span><span class="sxs-lookup"><span data-stu-id="e1698-252">If safety and security aren't factors, select the most likely or convenient value.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="e1698-253">Tamaño y espaciado recomendados</span><span class="sxs-lookup"><span data-stu-id="e1698-253">Recommended sizing and spacing</span></span>

![<span data-ttu-id="e1698-254">figura de tamaño y espaciado sugeridos de la casilla</span><span class="sxs-lookup"><span data-stu-id="e1698-254">figure of suggested check box sizing and spacing</span></span> ](images/ctrl-check-boxes-image24.png)

<span data-ttu-id="e1698-255">Tamaño y espaciado recomendados para las casillas.</span><span class="sxs-lookup"><span data-stu-id="e1698-255">Recommended sizing and spacing for check boxes.</span></span>

## <a name="labels"></a><span data-ttu-id="e1698-256">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="e1698-256">Labels</span></span>

<span data-ttu-id="e1698-257">**Etiquetas de casilla**</span><span class="sxs-lookup"><span data-stu-id="e1698-257">**Check box labels**</span></span>

-   <span data-ttu-id="e1698-258">Etiquete cada casilla.</span><span class="sxs-lookup"><span data-stu-id="e1698-258">Label every check box.</span></span>
-   <span data-ttu-id="e1698-259">Asigne una clave [de acceso única](glossary.md) a cada etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e1698-259">Assign a unique [access key](glossary.md) to each label.</span></span> <span data-ttu-id="e1698-260">Para obtener instrucciones, vea [Teclado](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="e1698-260">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="e1698-261">Use [mayúsculas de estilo oración.](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="e1698-261">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="e1698-262">Escriba la etiqueta como frase o frase imperativa y no use ningún signo de puntuación final.</span><span class="sxs-lookup"><span data-stu-id="e1698-262">Write the label as a phrase or an imperative sentence, and use no ending punctuation.</span></span>
    -   <span data-ttu-id="e1698-263">**Excepción:** Si una etiqueta de casilla también etiqueta un control subordinado que le sigue, finalice la etiqueta con dos puntos.</span><span class="sxs-lookup"><span data-stu-id="e1698-263">**Exception:** If a check box label also labels a subordinate control that follows it, end the label with a colon.</span></span>
-   <span data-ttu-id="e1698-264">Escriba la etiqueta para que describa el estado seleccionado de la casilla.</span><span class="sxs-lookup"><span data-stu-id="e1698-264">Write the label so that it describes the selected state of the check box.</span></span>
-   <span data-ttu-id="e1698-265">Para un grupo de casillas, use expresiones paralelas e intente mantener la longitud aproximadamente igual para todas las etiquetas.</span><span class="sxs-lookup"><span data-stu-id="e1698-265">For a group of check boxes, use parallel phrasing and try to keep the length about the same for all labels.</span></span>
-   <span data-ttu-id="e1698-266">Para un grupo de casillas, centre el texto de la etiqueta en las diferencias entre las opciones.</span><span class="sxs-lookup"><span data-stu-id="e1698-266">For a group of check boxes, focus the label text on the differences among the options.</span></span> <span data-ttu-id="e1698-267">Si todas las opciones tienen el mismo texto introductorio, mueva ese texto a la etiqueta de grupo.</span><span class="sxs-lookup"><span data-stu-id="e1698-267">If all the options have the same introductory text, move that text to the group label.</span></span>
-   <span data-ttu-id="e1698-268">Use expresiones positivas.</span><span class="sxs-lookup"><span data-stu-id="e1698-268">Use positive phrasing.</span></span> <span data-ttu-id="e1698-269">No frasee una etiqueta para que al activar una casilla no se realice una acción.</span><span class="sxs-lookup"><span data-stu-id="e1698-269">Don't phrase a label so that selecting a check box means not to perform an action.</span></span>

    -   <span data-ttu-id="e1698-270">**Excepción: no vuelva a mostrar esta <item> casilla.**</span><span class="sxs-lookup"><span data-stu-id="e1698-270">**Exception:Don't show this <item> again** check boxes.</span></span>

    <span data-ttu-id="e1698-271">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-271">**Incorrect:**</span></span>

    ![captura de pantalla de la etiqueta negativa 'turn off'](images/ctrl-check-boxes-image25.png)

    <span data-ttu-id="e1698-273">En este ejemplo, la opción no usa expresiones positivas.</span><span class="sxs-lookup"><span data-stu-id="e1698-273">In this example, the option doesn't use positive phrasing.</span></span>

-   <span data-ttu-id="e1698-274">Describa solo la opción con la etiqueta .</span><span class="sxs-lookup"><span data-stu-id="e1698-274">Describe just the option with the label.</span></span> <span data-ttu-id="e1698-275">Mantenga las etiquetas breves para que sea fácil hacer referencia a ellas en mensajes y documentación.</span><span class="sxs-lookup"><span data-stu-id="e1698-275">Keep labels brief so it's easy to refer to them in messages and documentation.</span></span> <span data-ttu-id="e1698-276">Si la opción requiere una explicación adicional, proporcione la explicación en un [control](./glossary.md) de texto estático mediante oraciones completas y signos de puntuación finales.</span><span class="sxs-lookup"><span data-stu-id="e1698-276">If the option requires further explanation, provide the explanation in a [static text](./glossary.md) control using complete sentences and ending punctuation.</span></span>

    > [!Note]
    >
    > <span data-ttu-id="e1698-277">Agregar una explicación a una casilla de un grupo no significa que tenga que proporcionar explicaciones para todas las casillas del grupo.</span><span class="sxs-lookup"><span data-stu-id="e1698-277">Adding an explanation to one check box in a group doesn't mean that you have to provide explanations for all check boxes in the group.</span></span> <span data-ttu-id="e1698-278">Proporcione la información pertinente en la etiqueta si es posible y use explicaciones solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e1698-278">Provide the relevant information in the label if you can, and use explanations only when necessary.</span></span> <span data-ttu-id="e1698-279">No simplemente vuelva a establecer la etiqueta para mantener la coherencia.</span><span class="sxs-lookup"><span data-stu-id="e1698-279">Don't merely restate the label for consistency.</span></span>

     

    ![<span data-ttu-id="e1698-280">captura de pantalla de casilla, etiqueta y descripción</span><span class="sxs-lookup"><span data-stu-id="e1698-280">screen shot of checkbox, label, and description</span></span> ](images/ctrl-check-boxes-image26.png)

    <span data-ttu-id="e1698-281">En este ejemplo, una etiqueta de casilla tiene texto explicativo adicional debajo.</span><span class="sxs-lookup"><span data-stu-id="e1698-281">In this example, a check box label has additional explanatory text beneath it.</span></span>

-   <span data-ttu-id="e1698-282">Si se recomienda encarecidamente una opción, considere la posibilidad de agregar "(recommended)" a la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e1698-282">If an option is strongly recommended, consider adding "(recommended)" to the label.</span></span> <span data-ttu-id="e1698-283">Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.</span><span class="sxs-lookup"><span data-stu-id="e1698-283">Be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="e1698-284">Si debe usar etiquetas de varias líneas, alinee la parte superior de la etiqueta con la casilla.</span><span class="sxs-lookup"><span data-stu-id="e1698-284">If you must use multi-line labels, align the top of the label with the check box.</span></span>
-   <span data-ttu-id="e1698-285">No use un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase.</span><span class="sxs-lookup"><span data-stu-id="e1698-285">Don't use a subordinate control, the values it contains, or its units label to create a sentence or phrase.</span></span> <span data-ttu-id="e1698-286">Este diseño no es localizable porque la estructura de oraciones varía según el lenguaje.</span><span class="sxs-lookup"><span data-stu-id="e1698-286">Such a design isn't localizable because sentence structure varies with language.</span></span>

    <span data-ttu-id="e1698-287">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-287">**Incorrect:**</span></span>

    ![<span data-ttu-id="e1698-288">captura de pantalla de la etiqueta de casilla con un cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="e1698-288">screen shot of checkbox label with text box in it</span></span> ](images/ctrl-check-boxes-image27.png)

    <span data-ttu-id="e1698-289">En este ejemplo, el cuadro de texto se coloca incorrectamente dentro de la etiqueta de casilla.</span><span class="sxs-lookup"><span data-stu-id="e1698-289">In this example, the text box is incorrectly placed inside the check box label.</span></span>

<span data-ttu-id="e1698-290">**Etiquetas de grupo de casillas**</span><span class="sxs-lookup"><span data-stu-id="e1698-290">**Check box group labels**</span></span>

-   <span data-ttu-id="e1698-291">Use la etiqueta de grupo para explicar el propósito del grupo, no cómo realizar la selección.</span><span class="sxs-lookup"><span data-stu-id="e1698-291">Use the group label to explain the purpose of the group, not how to make the selection.</span></span> <span data-ttu-id="e1698-292">Supongamos que los usuarios saben cómo usar las casillas.</span><span class="sxs-lookup"><span data-stu-id="e1698-292">Assume that users know how to use check boxes.</span></span> <span data-ttu-id="e1698-293">Por ejemplo, no diga "Seleccionar cualquiera de las siguientes opciones".</span><span class="sxs-lookup"><span data-stu-id="e1698-293">For example, don't say "Select any of the following choices".</span></span>
-   <span data-ttu-id="e1698-294">Termine cada etiqueta con dos puntos.</span><span class="sxs-lookup"><span data-stu-id="e1698-294">End each label with a colon.</span></span>
-   <span data-ttu-id="e1698-295">No asigne una clave de acceso a la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e1698-295">Don't assign an access key to the label.</span></span> <span data-ttu-id="e1698-296">No es necesario hacerlo y dificulta la asignación de las otras claves de acceso.</span><span class="sxs-lookup"><span data-stu-id="e1698-296">Doing so isn't necessary and it makes the other access keys harder to assign.</span></span>
-   <span data-ttu-id="e1698-297">Para una selección de una o varias opciones dependientes, explique el requisito en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e1698-297">For a selection of one or more dependent choices, explain the requirement on the label.</span></span>

    <span data-ttu-id="e1698-298">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="e1698-298">**Correct:**</span></span>

    ![<span data-ttu-id="e1698-299">captura de pantalla de la etiqueta para dos controles: protocolos</span><span class="sxs-lookup"><span data-stu-id="e1698-299">screen shot of label for two controls: protocols</span></span> ](images/ctrl-check-boxes-image28.png)

    <span data-ttu-id="e1698-300">En este ejemplo, los usuarios podrían pensar que solo pueden realizar una selección.</span><span class="sxs-lookup"><span data-stu-id="e1698-300">In this example, users might think that they can only make one selection.</span></span>

    <span data-ttu-id="e1698-301">**Mejor:**</span><span class="sxs-lookup"><span data-stu-id="e1698-301">**Better:**</span></span>

    ![<span data-ttu-id="e1698-302">captura de pantalla de la etiqueta: los protocolos seleccionan uno o varios</span><span class="sxs-lookup"><span data-stu-id="e1698-302">screen shot of label: protocols select one or more</span></span> ](images/ctrl-check-boxes-image29.png)

    <span data-ttu-id="e1698-303">En este ejemplo, está claro que los usuarios pueden realizar más de una selección.</span><span class="sxs-lookup"><span data-stu-id="e1698-303">In this example, it's clear that users can make more than one selection.</span></span>

## <a name="documentation"></a><span data-ttu-id="e1698-304">Documentación</span><span class="sxs-lookup"><span data-stu-id="e1698-304">Documentation</span></span>

<span data-ttu-id="e1698-305">Al hacer referencia a las casillas:</span><span class="sxs-lookup"><span data-stu-id="e1698-305">When referring to check boxes:</span></span>

-   <span data-ttu-id="e1698-306">Use el texto exacto de la etiqueta, incluida su inclusión en mayúsculas, pero no incluya el carácter de subrayado ni los dos puntos de la clave de acceso.</span><span class="sxs-lookup"><span data-stu-id="e1698-306">Use the exact label text, including its capitalization, but don't include the access key underscore or colon.</span></span> <span data-ttu-id="e1698-307">Incluya la casilla de palabras.</span><span class="sxs-lookup"><span data-stu-id="e1698-307">Include the word check box.</span></span>
-   <span data-ttu-id="e1698-308">Haga referencia a una casilla como casilla, no como opción, casilla o simplemente casilla, ya que solo box es ambiguo para los localizadores.</span><span class="sxs-lookup"><span data-stu-id="e1698-308">Refer to a check box as a check box, not option, checkbox, or just box, because box alone is ambiguous for localizers.</span></span>
-   <span data-ttu-id="e1698-309">Para describir la interacción del usuario, use seleccionar y borrar.</span><span class="sxs-lookup"><span data-stu-id="e1698-309">To describe user interaction, use select and clear.</span></span>
-   <span data-ttu-id="e1698-310">Cuando sea posible, formatee la etiqueta con texto en negrita.</span><span class="sxs-lookup"><span data-stu-id="e1698-310">When possible, format the label using bold text.</span></span> <span data-ttu-id="e1698-311">De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.</span><span class="sxs-lookup"><span data-stu-id="e1698-311">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="e1698-312">Ejemplo: active la **casilla Subrayado.**</span><span class="sxs-lookup"><span data-stu-id="e1698-312">Example: Select the **Underline** check box.</span></span>

