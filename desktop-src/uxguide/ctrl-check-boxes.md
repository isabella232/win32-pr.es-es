---
title: Casillas
description: Con una casilla, los usuarios deciden elegir entre dos opciones claramente opuestas.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7a175893b2dfab2999ce37e3f00395d881f03973
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003284"
---
# <a name="check-boxes"></a><span data-ttu-id="66f36-103">Casillas</span><span class="sxs-lookup"><span data-stu-id="66f36-103">Check Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="66f36-104">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="66f36-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="66f36-105">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="66f36-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="66f36-106">Con una casilla, los usuarios deciden elegir entre dos opciones claramente opuestas.</span><span class="sxs-lookup"><span data-stu-id="66f36-106">With a check box, users make a decision between two clearly opposite choices.</span></span> <span data-ttu-id="66f36-107">La etiqueta de la casilla indica el estado seleccionado, mientras que el significado del estado desactivado debe ser el opuesto no ambiguo del estado seleccionado.</span><span class="sxs-lookup"><span data-stu-id="66f36-107">The check box label indicates the selected state, whereas the meaning of the cleared state must be the unambiguous opposite of the selected state.</span></span> <span data-ttu-id="66f36-108">Por lo tanto, las **casillas solo deben usarse para activar o desactivar una opción o para seleccionar o anular la selección de un elemento.**</span><span class="sxs-lookup"><span data-stu-id="66f36-108">Consequently, **check boxes should be used only to toggle an option on or off or to select or deselect an item.**</span></span>

![<span data-ttu-id="66f36-109">captura de pantalla de una de las cuatro casillas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="66f36-109">screen shot of one of four check boxes selected</span></span> ](images/ctrl-check-boxes-image1.png)

<span data-ttu-id="66f36-110">Un grupo de casillas típico.</span><span class="sxs-lookup"><span data-stu-id="66f36-110">A typical group of check boxes.</span></span>

> [!Note]  
> <span data-ttu-id="66f36-111">Las instrucciones relacionadas con el [diseño](vis-layout.md) se presentan en un artículo independiente.</span><span class="sxs-lookup"><span data-stu-id="66f36-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="66f36-112">¿Es este el control adecuado?</span><span class="sxs-lookup"><span data-stu-id="66f36-112">Is this the right control?</span></span>

<span data-ttu-id="66f36-113">Para decidirte, intenta responder a estas preguntas:</span><span class="sxs-lookup"><span data-stu-id="66f36-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="66f36-114">**¿Está activada o desactivada la casilla usada para activar o desactivar una opción o para seleccionar o anular la selección de un elemento?**</span><span class="sxs-lookup"><span data-stu-id="66f36-114">**Is the check box used to toggle an option on or off or to select or deselect an item?**</span></span> <span data-ttu-id="66f36-115">Si no es así, usa otro control.</span><span class="sxs-lookup"><span data-stu-id="66f36-115">If not, use another control.</span></span>
-   <span data-ttu-id="66f36-116">**¿Están los Estados seleccionados y desactivados claros y no ambiguos?**</span><span class="sxs-lookup"><span data-stu-id="66f36-116">**Are the selected and cleared states clear and unambiguous opposites?**</span></span> <span data-ttu-id="66f36-117">Si no es así, use los [botones de radio](ctrl-radio-buttons.md) o una [lista](/windows/desktop/uxguide/ctrl-drop) desplegable para que pueda etiquetar los Estados de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="66f36-117">If not, use [radio buttons](ctrl-radio-buttons.md) or a [drop-down list](/windows/desktop/uxguide/ctrl-drop) so that you can label the states independently.</span></span>
-   <span data-ttu-id="66f36-118">**Cuando se usa en un grupo, ¿el grupo comprende opciones independientes, desde las que los usuarios pueden elegir cero o más?**</span><span class="sxs-lookup"><span data-stu-id="66f36-118">**When used in a group, does the group comprise independent choices, from which users may choose zero or more?**</span></span> <span data-ttu-id="66f36-119">Si no es así, tenga en cuenta los controles para las opciones dependientes, como los botones de radio y las [vistas de árbol de casilla](ctrl-tree-views.md).</span><span class="sxs-lookup"><span data-stu-id="66f36-119">If not, consider controls for dependent choices, such as radio buttons and [check box tree views](ctrl-tree-views.md).</span></span>
-   <span data-ttu-id="66f36-120">**Cuando se usa en un grupo, ¿comprende el grupo las elecciones dependientes, desde las que los usuarios deben elegir una o más?**</span><span class="sxs-lookup"><span data-stu-id="66f36-120">**When used in a group, does the group comprise dependent choices, from which users must choose one or more?**</span></span> <span data-ttu-id="66f36-121">Si es así, use un grupo de casillas y controle el error cuando no se seleccione ninguna de las opciones.</span><span class="sxs-lookup"><span data-stu-id="66f36-121">If so, use a group of check boxes and handle the error when none of the options are selected.</span></span>
-   <span data-ttu-id="66f36-122">**¿El número de opciones de un grupo es 10 o menos?**</span><span class="sxs-lookup"><span data-stu-id="66f36-122">**Is the number of options in a group 10 or fewer?**</span></span> <span data-ttu-id="66f36-123">Dado que el espacio de pantalla utilizado es proporcional al número de opciones, mantenga el número de casillas en 10 o menos.</span><span class="sxs-lookup"><span data-stu-id="66f36-123">Since the screen space used is proportional to the number of options, keep the number of check boxes to 10 or fewer.</span></span> <span data-ttu-id="66f36-124">Para más de 10 opciones, use una [lista de casillas](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="66f36-124">For more than 10 options, use a [check box list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="66f36-125">**¿Sería un botón de radio una opción mejor?**</span><span class="sxs-lookup"><span data-stu-id="66f36-125">**Would a radio button be a better choice?**</span></span> <span data-ttu-id="66f36-126">En los casos en los que las casillas son adecuadas solo para activar o desactivar una opción, los botones de radio se pueden usar para opciones totalmente diferentes.</span><span class="sxs-lookup"><span data-stu-id="66f36-126">Where check boxes are suitable only for turning an option on or off, radio buttons can be used for completely different options.</span></span> <span data-ttu-id="66f36-127">Si ambas soluciones son posibles:</span><span class="sxs-lookup"><span data-stu-id="66f36-127">If both solutions are possible:</span></span>
    -   <span data-ttu-id="66f36-128">Use los botones de radio si el significado de la casilla desactivada no es completamente obvio.</span><span class="sxs-lookup"><span data-stu-id="66f36-128">Use radio buttons if the meaning of the cleared check box isn't completely obvious.</span></span>

        <span data-ttu-id="66f36-129">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-129">**Incorrect:**</span></span>

        ![<span data-ttu-id="66f36-130">captura de pantalla de una casilla con la etiqueta horizontal</span><span class="sxs-lookup"><span data-stu-id="66f36-130">screen shot of one check box labeled landscape</span></span> ](images/ctrl-check-boxes-image2.png)

        <span data-ttu-id="66f36-131">En este ejemplo, la opción opuesta de horizontal no está clara, por lo que la casilla no es una buena opción.</span><span class="sxs-lookup"><span data-stu-id="66f36-131">In this example, the opposite choice from Landscape isn't clear, so the check box isn't a good choice.</span></span>

        <span data-ttu-id="66f36-132">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-132">**Correct:**</span></span>

        ![<span data-ttu-id="66f36-133">captura de pantalla de dos botones de radio</span><span class="sxs-lookup"><span data-stu-id="66f36-133">screen shot of two radio buttons</span></span> ](images/ctrl-check-boxes-image3.png)

        <span data-ttu-id="66f36-134">En este ejemplo, las opciones no son opuestas, por lo que los botones de radio son la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="66f36-134">In this example, the choices are not opposites so radio buttons are the better choice.</span></span>

    -   <span data-ttu-id="66f36-135">Use los botones de radio de las páginas del Asistente para desactivar las alternativas, incluso si la casilla de verificación es aceptable.</span><span class="sxs-lookup"><span data-stu-id="66f36-135">Use radio buttons on wizard pages to make the alternatives clear, even if a check box is otherwise acceptable.</span></span>
    -   <span data-ttu-id="66f36-136">Use los botones de radio si tiene suficiente espacio de pantalla y las opciones son lo suficientemente importantes como para ser un buen uso de ese espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="66f36-136">Use radio buttons if you have enough screen space and the options are important enough to be a good use of that screen space.</span></span> <span data-ttu-id="66f36-137">De lo contrario, use una casilla o una lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="66f36-137">Otherwise, use a check box or a drop-down list.</span></span>

        <span data-ttu-id="66f36-138">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-138">**Incorrect:**</span></span>

        ![<span data-ttu-id="66f36-139">captura de pantalla de los botones Mostrar y no mostrar relación</span><span class="sxs-lookup"><span data-stu-id="66f36-139">screen shot of show and don't show ratio buttons</span></span> ](images/ctrl-check-boxes-image4.png)

        <span data-ttu-id="66f36-140">En este ejemplo, las opciones no son lo suficientemente importantes para usar botones de radio.</span><span class="sxs-lookup"><span data-stu-id="66f36-140">In this example, the options aren't important enough to use radio buttons.</span></span>

        <span data-ttu-id="66f36-141">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-141">**Correct:**</span></span>

        ![<span data-ttu-id="66f36-142">captura de pantalla de la casilla con no mostrar mensaje</span><span class="sxs-lookup"><span data-stu-id="66f36-142">screen shot of check box with don't show message</span></span> ](images/ctrl-check-boxes-image5.png)

        <span data-ttu-id="66f36-143">En este ejemplo, una casilla es un uso eficaz del espacio de pantalla para esta opción de periféricos.</span><span class="sxs-lookup"><span data-stu-id="66f36-143">In this example, a check box is an efficient use of screen space for this peripheral option.</span></span>

-   <span data-ttu-id="66f36-144">Utilice una casilla de verificación si hay otras casillas en la ventana.</span><span class="sxs-lookup"><span data-stu-id="66f36-144">Use a check box if there other check boxes on the window.</span></span>
-   <span data-ttu-id="66f36-145">**¿La opción presenta una opción de programa, en lugar de datos?**</span><span class="sxs-lookup"><span data-stu-id="66f36-145">**Does the option present a program option, rather than data?**</span></span> <span data-ttu-id="66f36-146">Los valores de la opción no deben basarse en el contexto u otros datos.</span><span class="sxs-lookup"><span data-stu-id="66f36-146">The option's values shouldn't be based on context or other data.</span></span> <span data-ttu-id="66f36-147">Para los datos, use una lista de casillas o una [lista de selección múltiple](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="66f36-147">For data, use a check box list or [multiple-selection list](ctrl-list-boxes.md).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="66f36-148">Patrones de uso</span><span class="sxs-lookup"><span data-stu-id="66f36-148">Usage patterns</span></span>

<span data-ttu-id="66f36-149">Las casillas tienen varios patrones de uso:</span><span class="sxs-lookup"><span data-stu-id="66f36-149">Check boxes have several usage patterns:</span></span>



|                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f36-150">**Una opción individual** Se utiliza una sola casilla para seleccionar una opción individual.</span><span class="sxs-lookup"><span data-stu-id="66f36-150">**An individual choice** A single check box is used to select an individual choice.</span></span> <br/>                                                                                                             | ![<span data-ttu-id="66f36-151">captura de pantalla de una casilla con la etiqueta Recordármelo</span><span class="sxs-lookup"><span data-stu-id="66f36-151">screen shot of one check box with remind me label</span></span> ](images/ctrl-check-boxes-image6.png)<br/> <span data-ttu-id="66f36-152">Se utiliza una sola casilla para una opción individual.</span><span class="sxs-lookup"><span data-stu-id="66f36-152">A single check box is used for an individual choice.</span></span><br/>                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="66f36-153">**Opciones independientes (cero o más)** Se usa un grupo de casillas para seleccionar entre un conjunto de cero o más opciones.</span><span class="sxs-lookup"><span data-stu-id="66f36-153">**Independent choices (zero or more)** A group of check boxes is used to select from a set of zero or more choices.</span></span><br/>                                                                              | <span data-ttu-id="66f36-154">a diferencia de los controles de selección única, como los [botones de radio](ctrl-radio-buttons.md), los usuarios pueden seleccionar cualquier combinación de opciones de un grupo de casillas.</span><span class="sxs-lookup"><span data-stu-id="66f36-154">unlike single-selection controls such as [radio buttons](ctrl-radio-buttons.md), users can select any combination of options in a group of check boxes.</span></span><br/> <span data-ttu-id="66f36-155">![captura de pantalla de dos de las tres casillas seleccionadas ](images/ctrl-check-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="66f36-155">![screen shot of two of three check boxes selected ](images/ctrl-check-boxes-image7.png)</span></span><br/> <span data-ttu-id="66f36-156">Se utiliza un grupo de casillas de verificación para opciones independientes.</span><span class="sxs-lookup"><span data-stu-id="66f36-156">A group of check boxes is used for independent choices.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="66f36-157">**Elecciones dependientes (una o más)** También se puede usar un grupo de casillas para seleccionar entre un conjunto de una o más opciones.</span><span class="sxs-lookup"><span data-stu-id="66f36-157">**Dependent choices (one or more)** A group of check boxes can also be used to select from a set of one or more choices.</span></span><br/>                                                                         | <span data-ttu-id="66f36-158">es **posible que necesite representar una selección de una o varias opciones dependientes**.</span><span class="sxs-lookup"><span data-stu-id="66f36-158">**you may need to represent a selection of one or more dependent choices**.</span></span> <span data-ttu-id="66f36-159">Dado que Microsoft? Windows no tiene un control que admita directamente este tipo de entrada, la mejor solución consiste en usar un grupo de casillas y controlar el error cuando no se selecciona ninguna de las opciones.</span><span class="sxs-lookup"><span data-stu-id="66f36-159">because microsoft?windows doesn't have a control that directly supports this type of input, the best solution is to use a group of check boxes and handle the error when none of the options are selected.</span></span><br/> <span data-ttu-id="66f36-160">![captura de pantalla de una de las dos casillas seleccionadas ](images/ctrl-check-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="66f36-160">![screen shot of one of two check boxes selected ](images/ctrl-check-boxes-image8.png)</span></span><br/> <span data-ttu-id="66f36-161">Se usa un grupo de casillas donde se debe seleccionar al menos un protocolo.</span><span class="sxs-lookup"><span data-stu-id="66f36-161">A group of check boxes is used where at least one protocol must be selected.</span></span><br/> |
| <span data-ttu-id="66f36-162">**Elección mixta** Además de los Estados seleccionados y desactivados, las casillas también tienen un estado mixto para la selección múltiple para indicar que la opción está establecida para algunos objetos, pero no para todos.</span><span class="sxs-lookup"><span data-stu-id="66f36-162">**Mixed choice** In addition to their selected and cleared states, check boxes also have a mixed state for multiple selection to indicate that the option is set for some, but not all, objects.</span></span><br/> | ![<span data-ttu-id="66f36-163">captura de pantalla de una casilla de solo lectura azul sólido</span><span class="sxs-lookup"><span data-stu-id="66f36-163">screen shot of a solid blue read-only check box</span></span> ](images/ctrl-check-boxes-image9.png)<br/> <span data-ttu-id="66f36-164">Una casilla de estado mixto.</span><span class="sxs-lookup"><span data-stu-id="66f36-164">A mixed-state check box.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a><span data-ttu-id="66f36-165">Directrices</span><span class="sxs-lookup"><span data-stu-id="66f36-165">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="66f36-166">General</span><span class="sxs-lookup"><span data-stu-id="66f36-166">General</span></span>

-   <span data-ttu-id="66f36-167">**Casillas relacionadas con grupos**.</span><span class="sxs-lookup"><span data-stu-id="66f36-167">**Group related check boxes**.</span></span> <span data-ttu-id="66f36-168">Combine opciones relacionadas y separe las opciones no relacionadas en grupos de 10 o menos, utilizando varios grupos si es necesario.</span><span class="sxs-lookup"><span data-stu-id="66f36-168">Combine related options and separate unrelated options into groups of 10 or fewer, using multiple groups if necessary.</span></span>

    ![<span data-ttu-id="66f36-169">captura de pantalla de las casillas relacionadas y no relacionadas</span><span class="sxs-lookup"><span data-stu-id="66f36-169">screen shot of related and unrelated check boxes</span></span> ](images/ctrl-check-boxes-image10.png)

    <span data-ttu-id="66f36-170">Un ejemplo de grupos de opciones relacionadas e independientes.</span><span class="sxs-lookup"><span data-stu-id="66f36-170">An example of groups of related, independent options.</span></span>

-   <span data-ttu-id="66f36-171">Volver **a considerar el uso de cuadros de grupo para organizar grupos de casillas** esto a menudo produce un desorden de pantalla innecesario.</span><span class="sxs-lookup"><span data-stu-id="66f36-171">**Reconsider using group boxes to organize groups of check boxes** this often results in unnecessary screen clutter.</span></span>
-   <span data-ttu-id="66f36-172">**Mostrar las casillas en un orden lógico**, como agrupar las opciones de alta relación o colocar las opciones más comunes en primer lugar o seguir algún otro progresión natural.</span><span class="sxs-lookup"><span data-stu-id="66f36-172">**List check boxes in a logical order**, such as grouping highly related options together or placing most common options first, or following some other natural progression.</span></span> <span data-ttu-id="66f36-173">No se recomienda el orden alfabético porque depende del lenguaje y, por lo tanto, no es localizable.</span><span class="sxs-lookup"><span data-stu-id="66f36-173">Alphabetical ordering isn't recommended because it is language dependent, and therefore not localizable.</span></span>
-   <span data-ttu-id="66f36-174">**Alinee las casillas verticalmente, no horizontalmente**.</span><span class="sxs-lookup"><span data-stu-id="66f36-174">**Align check boxes vertically, not horizontally**.</span></span> <span data-ttu-id="66f36-175">La alineación horizontal es más difícil de leer.</span><span class="sxs-lookup"><span data-stu-id="66f36-175">Horizontal alignment is harder to read.</span></span>

    <span data-ttu-id="66f36-176">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-176">**Correct:**</span></span>

    ![<span data-ttu-id="66f36-177">captura de pantalla de las casillas alineadas verticalmente</span><span class="sxs-lookup"><span data-stu-id="66f36-177">screen shot of check boxes aligned vertically</span></span> ](images/ctrl-check-boxes-image11.png)

    <span data-ttu-id="66f36-178">En este ejemplo, las casillas están correctamente alineadas.</span><span class="sxs-lookup"><span data-stu-id="66f36-178">In this example, the check boxes are correctly aligned.</span></span>

    <span data-ttu-id="66f36-179">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-179">**Incorrect:**</span></span>

    ![<span data-ttu-id="66f36-180">captura de pantalla de las casillas alineadas horizontalmente</span><span class="sxs-lookup"><span data-stu-id="66f36-180">screen shot of check boxes aligned horizontally</span></span> ](images/ctrl-check-boxes-image12.png)

    <span data-ttu-id="66f36-181">En este ejemplo, la alineación horizontal es más difícil de leer.</span><span class="sxs-lookup"><span data-stu-id="66f36-181">In this example, the horizontal alignment is harder to read.</span></span>

-   <span data-ttu-id="66f36-182">**No use el estado mixto para representar un tercer Estado.**</span><span class="sxs-lookup"><span data-stu-id="66f36-182">**Don't use the mixed state to represent a third state.**</span></span> <span data-ttu-id="66f36-183">El estado mixto se usa para indicar que se ha establecido una opción para algunos objetos secundarios, pero no para todos.</span><span class="sxs-lookup"><span data-stu-id="66f36-183">The mixed state is used to indicate that an option is set for some, but not all, child objects.</span></span> <span data-ttu-id="66f36-184">Los usuarios no deben poder establecer un estado mixto directamente en lugar de que el estado mixto sea un reflejo de los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="66f36-184">Users shouldn't be able to set a mixed state directly rather the mixed state is a reflection of the child objects.</span></span> <span data-ttu-id="66f36-185">El estado mixto no se utiliza como tercer Estado para un elemento individual.</span><span class="sxs-lookup"><span data-stu-id="66f36-185">The mixed state isn't used as a third state for an individual item.</span></span> <span data-ttu-id="66f36-186">Para representar un tercer Estado, use los botones de radio o una lista desplegable en su lugar.</span><span class="sxs-lookup"><span data-stu-id="66f36-186">To represent a third state, use radio buttons or a drop-down list instead.</span></span>

    <span data-ttu-id="66f36-187">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-187">**Incorrect:**</span></span>

    ![<span data-ttu-id="66f36-188">captura de pantalla de la casilla servicio de tema azul sólido</span><span class="sxs-lookup"><span data-stu-id="66f36-188">screen shot of solid blue theme service check box</span></span> ](images/ctrl-check-boxes-image13.png)

    <span data-ttu-id="66f36-189">En este ejemplo, se supone que el estado mixto indica que el servicio de tema no está instalado.</span><span class="sxs-lookup"><span data-stu-id="66f36-189">In this example, the mixed state is supposed to indicate that the Theme service isn't installed.</span></span>

    <span data-ttu-id="66f36-190">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-190">**Correct:**</span></span>

    ![<span data-ttu-id="66f36-191">captura de pantalla de la lista desplegable con tres opciones</span><span class="sxs-lookup"><span data-stu-id="66f36-191">screen shot of drop-down list with three options</span></span> ](images/ctrl-check-boxes-image14.png)

    <span data-ttu-id="66f36-192">En este ejemplo, los usuarios pueden elegir entre una lista de tres opciones claras.</span><span class="sxs-lookup"><span data-stu-id="66f36-192">In this example, users can choose from a list of three clear options.</span></span>

-   <span data-ttu-id="66f36-193">**Al hacer clic en una casilla de estado mixto, se recorren todos los Estados seleccionados, todos borrados y los originales.**</span><span class="sxs-lookup"><span data-stu-id="66f36-193">**Clicking a mixed state check box should cycle through all selected, all cleared, and the original mixed states.**</span></span> <span data-ttu-id="66f36-194">En el caso de forgiveness, es importante poder restaurar el estado mixto original, ya que la configuración podría ser compleja o desconocida para el usuario.</span><span class="sxs-lookup"><span data-stu-id="66f36-194">For forgiveness, it's important to be able to restore the original mixed state because the settings might be complex or unknown to the user.</span></span> <span data-ttu-id="66f36-195">De lo contrario, la única manera de restaurar el estado mixto con confianza sería cancelar la tarea y volver a empezar.</span><span class="sxs-lookup"><span data-stu-id="66f36-195">Otherwise, the only way to restore the mixed state with confidence would be to cancel the task and start over.</span></span>
-   <span data-ttu-id="66f36-196">**No use casillas como indicador de progreso**.</span><span class="sxs-lookup"><span data-stu-id="66f36-196">**Don't use check boxes as a progress indicator**.</span></span> <span data-ttu-id="66f36-197">En su lugar, use un control de [indicador de progreso](progress-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="66f36-197">Use a [progress indicator](progress-bars.md) control instead.</span></span>

    <span data-ttu-id="66f36-198">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-198">**Incorrect:**</span></span>

    ![<span data-ttu-id="66f36-199">captura de pantalla de cuatro casillas que muestran el progreso</span><span class="sxs-lookup"><span data-stu-id="66f36-199">screen shot of four check boxes showing progress</span></span> ](images/ctrl-check-boxes-image15.png)

    <span data-ttu-id="66f36-200">En este ejemplo, las casillas se usan incorrectamente como un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="66f36-200">In this example, check boxes are used incorrectly as a progress indicator.</span></span>

    <span data-ttu-id="66f36-201">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-201">**Correct:**</span></span>

    ![<span data-ttu-id="66f36-202">captura de pantalla de una barra de progreso parcialmente rellena</span><span class="sxs-lookup"><span data-stu-id="66f36-202">screen shot of a partially filled progress bar</span></span> ](images/ctrl-check-boxes-image16.png)

    <span data-ttu-id="66f36-203">Ejemplo de una barra de progreso típica.</span><span class="sxs-lookup"><span data-stu-id="66f36-203">Example of a typical progress bar.</span></span>

-   <span data-ttu-id="66f36-204">**Mostrar las casillas deshabilitadas con el estado de selección correcto.**</span><span class="sxs-lookup"><span data-stu-id="66f36-204">**Show disabled check boxes using the correct selection state.**</span></span> <span data-ttu-id="66f36-205">Aunque los usuarios no pueden cambiarlos, las casillas deshabilitadas transmiten información para que sean coherentes con los resultados.</span><span class="sxs-lookup"><span data-stu-id="66f36-205">Even though users can't change them, disabled check boxes convey information so they should be consistent with results.</span></span>

    <span data-ttu-id="66f36-206">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-206">**Incorrect:**</span></span>

    ![<span data-ttu-id="66f36-207">captura de pantalla de una de dos casillas atenuadas</span><span class="sxs-lookup"><span data-stu-id="66f36-207">screen shot of one of two check boxes dimmed</span></span> ](images/ctrl-check-boxes-image17.png)

    <span data-ttu-id="66f36-208">En este ejemplo, la opción "leer siempre esta sección en voz alta" debe borrarse porque la sección no se lee cuando la opción está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="66f36-208">In this example, the "Always read this section aloud" option should be cleared because the section isn't read when the option is disabled.</span></span>

-   <span data-ttu-id="66f36-209">**No use la selección de una casilla para**:</span><span class="sxs-lookup"><span data-stu-id="66f36-209">**Don't use the selection of a check box to**:</span></span>
    -   <span data-ttu-id="66f36-210">Ejecutar comandos.</span><span class="sxs-lookup"><span data-stu-id="66f36-210">Perform commands.</span></span>
    -   <span data-ttu-id="66f36-211">Mostrar otras ventanas, como un cuadro de diálogo para recopilar más entradas.</span><span class="sxs-lookup"><span data-stu-id="66f36-211">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="66f36-212">Mostrar de forma dinámica otros controles relacionados con el control seleccionado (los lectores de pantalla no pueden detectar dichos eventos).</span><span class="sxs-lookup"><span data-stu-id="66f36-212">Dynamically display other controls related to the selected control (screen readers cannot detect such events).</span></span>

### <a name="dont-show-this-item-again"></a><span data-ttu-id="66f36-213">No mostrar esta</span><span class="sxs-lookup"><span data-stu-id="66f36-213">Don't show this</span></span> <item> <span data-ttu-id="66f36-214">nuevo</span><span class="sxs-lookup"><span data-stu-id="66f36-214">again</span></span>

-   <span data-ttu-id="66f36-215">**Considere la posibilidad de usar una <item> opción no volver a mostrar esto para permitir que los usuarios supriman un cuadro de diálogo periódico solo si no hay una alternativa mejor.**</span><span class="sxs-lookup"><span data-stu-id="66f36-215">**Consider using a Don't show this <item> again option to allow users to suppress a recurring dialog box only if there isn't a better alternative.**</span></span> <span data-ttu-id="66f36-216">Intente determinar de antemano si los usuarios necesitan realmente el cuadro de diálogo; Si lo hacen, muestre siempre el cuadro de diálogo y, si no es así, elimine el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="66f36-216">Try to determine beforehand if users really need the dialog; if they do, always show the dialog, and if they don't, eliminate the dialog.</span></span>

<span data-ttu-id="66f36-217">Para obtener más instrucciones y ejemplos, vea [cuadros de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="66f36-217">For more guidelines and examples, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="subordinate-controls"></a><span data-ttu-id="66f36-218">Controles subordinados</span><span class="sxs-lookup"><span data-stu-id="66f36-218">Subordinate controls</span></span>

-   <span data-ttu-id="66f36-219">Coloque los controles subordinados a la derecha o debajo de (con sangría, vacíe con la etiqueta de la casilla) la casilla de verificación y su etiqueta.</span><span class="sxs-lookup"><span data-stu-id="66f36-219">Place subordinate controls to the right of or below (indented, flush with the check box label) the check box and its label.</span></span> <span data-ttu-id="66f36-220">Finalice la etiqueta de la casilla con un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="66f36-220">End the check box label with a colon.</span></span>

    ![<span data-ttu-id="66f36-221">captura de pantalla del cuadro de texto debajo de la etiqueta de la casilla</span><span class="sxs-lookup"><span data-stu-id="66f36-221">screen shot of text box below check box label</span></span> ](images/ctrl-check-boxes-image18.png)

    <span data-ttu-id="66f36-222">En este ejemplo, la casilla y su control subordinado comparten la etiqueta de la casilla y su clave de acceso.</span><span class="sxs-lookup"><span data-stu-id="66f36-222">In this example, the check box and its subordinate control share the check box label and its access key.</span></span>

-   <span data-ttu-id="66f36-223">**Deje las listas desplegables y los cuadros de texto modificables dependientes habilitados si comparten la etiqueta de la casilla.**</span><span class="sxs-lookup"><span data-stu-id="66f36-223">**Leave dependent editable text boxes and drop-down lists enabled if they share the check box's label.**</span></span> <span data-ttu-id="66f36-224">Cuando los usuarios escriban o peguen cualquier elemento en el cuadro, seleccione automáticamente la opción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="66f36-224">When users type or paste anything into the box, select the corresponding option automatically.</span></span> <span data-ttu-id="66f36-225">De este modo, se simplifica la interacción.</span><span class="sxs-lookup"><span data-stu-id="66f36-225">Doing so simplifies the interaction.</span></span>

    ![<span data-ttu-id="66f36-226">captura de pantalla de cuadros de texto de encabezado y pie de página</span><span class="sxs-lookup"><span data-stu-id="66f36-226">screen shot of header and footer text boxes</span></span> ](images/ctrl-check-boxes-image19.png)

    <span data-ttu-id="66f36-227">En este ejemplo, al escribir un encabezado o un pie de página, se selecciona automáticamente la opción.</span><span class="sxs-lookup"><span data-stu-id="66f36-227">In this example, entering a header or footer automatically selects the option.</span></span>

-   <span data-ttu-id="66f36-228">Si anida casillas con botones de radio u otras casillas, **deshabilite estos controles subordinados hasta que se seleccione la opción de alto nivel**.</span><span class="sxs-lookup"><span data-stu-id="66f36-228">If you nest check boxes with radio buttons or other check boxes, **disable these subordinate controls until the high-level option is selected**.</span></span> <span data-ttu-id="66f36-229">Al hacerlo, se evita la confusión sobre el significado de los controles subordinados.</span><span class="sxs-lookup"><span data-stu-id="66f36-229">Doing so avoids confusion about the meaning of the subordinate controls.</span></span>
-   <span data-ttu-id="66f36-230">Active la casilla de verificación de los controles subordinados junto con la casilla en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="66f36-230">Make subordinate controls to a check box contiguous with the check box in the tab order.</span></span>
-   <span data-ttu-id="66f36-231">**Si la selección de una opción implica seleccionar las casillas subordinadas, active las casillas de verificación de forma explícita para que la relación sea clara.**</span><span class="sxs-lookup"><span data-stu-id="66f36-231">**If selecting an option implies selecting subordinate check boxes, explicitly select those check boxes to make the relationship clear.**</span></span>

    <span data-ttu-id="66f36-232">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-232">**Incorrect:**</span></span>

    ![<span data-ttu-id="66f36-233">captura de pantalla: botón seleccionado, casillas desactivadas</span><span class="sxs-lookup"><span data-stu-id="66f36-233">screen shot: selected button, cleared check boxes</span></span> ](images/ctrl-check-boxes-image20.png)

    <span data-ttu-id="66f36-234">En este ejemplo, las casillas subordinadas no están seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="66f36-234">In this example, the subordinate check boxes aren't selected.</span></span>

    <span data-ttu-id="66f36-235">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-235">**Correct:**</span></span>

    ![<span data-ttu-id="66f36-236">captura de pantalla: botón seleccionado, casillas seleccionadas</span><span class="sxs-lookup"><span data-stu-id="66f36-236">screen shot: selected button, selected check boxes</span></span> ](images/ctrl-check-boxes-image21.png)

    <span data-ttu-id="66f36-237">En este ejemplo, se seleccionan las casillas subordinadas, haciendo que su relación con la opción seleccionada esté desactivada.</span><span class="sxs-lookup"><span data-stu-id="66f36-237">In this example, the subordinate check boxes are selected, making their relationship to the selected option clear.</span></span>

-   <span data-ttu-id="66f36-238">**Use casillas dependientes si las alternativas agregan complejidad innecesaria**.</span><span class="sxs-lookup"><span data-stu-id="66f36-238">**Use dependent check boxes if the alternatives add unnecessary complexity**.</span></span> <span data-ttu-id="66f36-239">Las casillas de verificación deben ser opciones independientes, a veces alternativas como los botones de radio agregan complejidad innecesaria.</span><span class="sxs-lookup"><span data-stu-id="66f36-239">While check boxes should be independent options, sometimes alternatives such as radio buttons add unnecessary complexity.</span></span>

    <span data-ttu-id="66f36-240">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-240">**Correct:**</span></span>

    ![<span data-ttu-id="66f36-241">captura de pantalla de botones y casillas confusos</span><span class="sxs-lookup"><span data-stu-id="66f36-241">screen shot of confusing buttons and check boxes</span></span> ](images/ctrl-check-boxes-image22.png)

    <span data-ttu-id="66f36-242">En este ejemplo, el uso de botones de radio es preciso, pero crea una complejidad innecesaria.</span><span class="sxs-lookup"><span data-stu-id="66f36-242">In this example, the use of radio buttons is accurate, but creates unnecessary complexity.</span></span>

    <span data-ttu-id="66f36-243">**Manera**</span><span class="sxs-lookup"><span data-stu-id="66f36-243">**Better:**</span></span>

    ![<span data-ttu-id="66f36-244">captura de pantalla de solo casillas</span><span class="sxs-lookup"><span data-stu-id="66f36-244">screen shot of check boxes only</span></span> ](images/ctrl-check-boxes-image23.png)

    <span data-ttu-id="66f36-245">En este ejemplo, el uso de casillas es más sencillo y permite a los usuarios centrarse en seleccionar las opciones deseadas en lugar de en su relación compleja.</span><span class="sxs-lookup"><span data-stu-id="66f36-245">In this example, the use of check boxes is simpler and allows users to focus on selecting the desired options instead of on their complex relationship.</span></span>

    <span data-ttu-id="66f36-246">**Importante: aplique esta directriz solo en circunstancias muy poco habituales**. al mostrar las dependencias, se agrega una complejidad significativa sin agregar claridad.</span><span class="sxs-lookup"><span data-stu-id="66f36-246">**Important: Apply this guideline only in extremely rare circumstances**, when showing the dependencies adds significant complexity without adding clarity.</span></span> <span data-ttu-id="66f36-247">En el ejemplo anterior, es improbable que los usuarios intentaran elegir superíndices y subíndices, y si lo hicieron, sería fácil entender que eran opciones exclusivas.</span><span class="sxs-lookup"><span data-stu-id="66f36-247">In the previous example, it is unlikely that users would attempt to choose both superscript and subscript, and if they did, it would be easy to understand that they were exclusive options.</span></span>

### <a name="default-values"></a><span data-ttu-id="66f36-248">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="66f36-248">Default values</span></span>

-   <span data-ttu-id="66f36-249">Si una casilla está desactivada para una opción de usuario, **establezca la más segura (para evitar la pérdida de datos o el acceso al sistema), el estado más seguro y privado de forma predeterminada.**</span><span class="sxs-lookup"><span data-stu-id="66f36-249">If a check box is for a user option, **set the safest (to prevent loss of data or system access), most secure and private state by default.**</span></span> <span data-ttu-id="66f36-250">Si seguridad y seguridad no son factores, seleccione el valor más probable o adecuado.</span><span class="sxs-lookup"><span data-stu-id="66f36-250">If safety and security aren't factors, select the most likely or convenient value.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="66f36-251">Ajuste de tamaño y espaciado recomendados</span><span class="sxs-lookup"><span data-stu-id="66f36-251">Recommended sizing and spacing</span></span>

![<span data-ttu-id="66f36-252">figura del tamaño y espaciado de las casillas sugeridas</span><span class="sxs-lookup"><span data-stu-id="66f36-252">figure of suggested check box sizing and spacing</span></span> ](images/ctrl-check-boxes-image24.png)

<span data-ttu-id="66f36-253">Ajuste de tamaño y espaciado recomendados para las casillas.</span><span class="sxs-lookup"><span data-stu-id="66f36-253">Recommended sizing and spacing for check boxes.</span></span>

## <a name="labels"></a><span data-ttu-id="66f36-254">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="66f36-254">Labels</span></span>

<span data-ttu-id="66f36-255">**Etiquetas de casilla**</span><span class="sxs-lookup"><span data-stu-id="66f36-255">**Check box labels**</span></span>

-   <span data-ttu-id="66f36-256">Etiquetar cada casilla.</span><span class="sxs-lookup"><span data-stu-id="66f36-256">Label every check box.</span></span>
-   <span data-ttu-id="66f36-257">Asigne una [clave de acceso](glossary.md) única a cada etiqueta.</span><span class="sxs-lookup"><span data-stu-id="66f36-257">Assign a unique [access key](glossary.md) to each label.</span></span> <span data-ttu-id="66f36-258">Para obtener instrucciones, consulte [teclado](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="66f36-258">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="66f36-259">Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="66f36-259">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="66f36-260">Escriba la etiqueta como una frase o frase imperativa y no use ningún signo de puntuación final.</span><span class="sxs-lookup"><span data-stu-id="66f36-260">Write the label as a phrase or an imperative sentence, and use no ending punctuation.</span></span>
    -   <span data-ttu-id="66f36-261">**Excepción:** Si una etiqueta de casilla también etiqueta un control subordinado que lo sigue, finalice la etiqueta con un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="66f36-261">**Exception:** If a check box label also labels a subordinate control that follows it, end the label with a colon.</span></span>
-   <span data-ttu-id="66f36-262">Escriba la etiqueta para que describa el estado seleccionado de la casilla.</span><span class="sxs-lookup"><span data-stu-id="66f36-262">Write the label so that it describes the selected state of the check box.</span></span>
-   <span data-ttu-id="66f36-263">En el caso de un grupo de casillas, use la formulación paralela e intente mantener la misma longitud para todas las etiquetas.</span><span class="sxs-lookup"><span data-stu-id="66f36-263">For a group of check boxes, use parallel phrasing and try to keep the length about the same for all labels.</span></span>
-   <span data-ttu-id="66f36-264">En un grupo de casillas, Centre el texto de la etiqueta en las diferencias entre las opciones.</span><span class="sxs-lookup"><span data-stu-id="66f36-264">For a group of check boxes, focus the label text on the differences among the options.</span></span> <span data-ttu-id="66f36-265">Si todas las opciones tienen el mismo texto de introducción, mueva el texto a la etiqueta de grupo.</span><span class="sxs-lookup"><span data-stu-id="66f36-265">If all the options have the same introductory text, move that text to the group label.</span></span>
-   <span data-ttu-id="66f36-266">Usar frases positivas.</span><span class="sxs-lookup"><span data-stu-id="66f36-266">Use positive phrasing.</span></span> <span data-ttu-id="66f36-267">No formule frases como una etiqueta, de modo que la selección de una casilla significa no realizar una acción.</span><span class="sxs-lookup"><span data-stu-id="66f36-267">Don't phrase a label so that selecting a check box means not to perform an action.</span></span>

    -   <span data-ttu-id="66f36-268">**Excepción: no <item> volver a mostrar** las casillas.</span><span class="sxs-lookup"><span data-stu-id="66f36-268">**Exception:Don't show this <item> again** check boxes.</span></span>

    <span data-ttu-id="66f36-269">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-269">**Incorrect:**</span></span>

    ![captura de pantalla de la etiqueta negativa ' desactivar '](images/ctrl-check-boxes-image25.png)

    <span data-ttu-id="66f36-271">En este ejemplo, la opción no usa frases positivas.</span><span class="sxs-lookup"><span data-stu-id="66f36-271">In this example, the option doesn't use positive phrasing.</span></span>

-   <span data-ttu-id="66f36-272">Describa solo la opción con la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="66f36-272">Describe just the option with the label.</span></span> <span data-ttu-id="66f36-273">Conserve las etiquetas breves, por lo que es fácil hacer referencia a ellas en los mensajes y la documentación.</span><span class="sxs-lookup"><span data-stu-id="66f36-273">Keep labels brief so it's easy to refer to them in messages and documentation.</span></span> <span data-ttu-id="66f36-274">Si la opción requiere una explicación más detallada, proporcione la explicación en un control de [texto estático](./glossary.md) mediante frases completas y puntuación final.</span><span class="sxs-lookup"><span data-stu-id="66f36-274">If the option requires further explanation, provide the explanation in a [static text](./glossary.md) control using complete sentences and ending punctuation.</span></span>

    > [!Note]
    >
    > <span data-ttu-id="66f36-275">Agregar una explicación a una casilla de un grupo no significa que tenga que proporcionar explicaciones para todas las casillas del grupo.</span><span class="sxs-lookup"><span data-stu-id="66f36-275">Adding an explanation to one check box in a group doesn't mean that you have to provide explanations for all check boxes in the group.</span></span> <span data-ttu-id="66f36-276">Proporcione la información relevante en la etiqueta, si es posible, y use explicaciones solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="66f36-276">Provide the relevant information in the label if you can, and use explanations only when necessary.</span></span> <span data-ttu-id="66f36-277">No solo tiene que volver a cambiar el estado de la etiqueta para que sea coherente.</span><span class="sxs-lookup"><span data-stu-id="66f36-277">Don't merely restate the label for consistency.</span></span>

     

    ![<span data-ttu-id="66f36-278">captura de pantalla de casilla, etiqueta y descripción</span><span class="sxs-lookup"><span data-stu-id="66f36-278">screen shot of checkbox, label, and description</span></span> ](images/ctrl-check-boxes-image26.png)

    <span data-ttu-id="66f36-279">En este ejemplo, una etiqueta de casilla tiene texto explicativo adicional debajo de ella.</span><span class="sxs-lookup"><span data-stu-id="66f36-279">In this example, a check box label has additional explanatory text beneath it.</span></span>

-   <span data-ttu-id="66f36-280">Si se recomienda encarecidamente, considere la posibilidad de agregar "(recomendado)" a la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="66f36-280">If an option is strongly recommended, consider adding "(recommended)" to the label.</span></span> <span data-ttu-id="66f36-281">Asegúrese de agregar a la etiqueta de control, no a las notas complementarias.</span><span class="sxs-lookup"><span data-stu-id="66f36-281">Be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="66f36-282">Si debe usar etiquetas de varias líneas, alinee la parte superior de la etiqueta con la casilla.</span><span class="sxs-lookup"><span data-stu-id="66f36-282">If you must use multi-line labels, align the top of the label with the check box.</span></span>
-   <span data-ttu-id="66f36-283">No utilice un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase.</span><span class="sxs-lookup"><span data-stu-id="66f36-283">Don't use a subordinate control, the values it contains, or its units label to create a sentence or phrase.</span></span> <span data-ttu-id="66f36-284">Este tipo de diseño no es localizable porque la estructura de oraciones varía según el idioma.</span><span class="sxs-lookup"><span data-stu-id="66f36-284">Such a design isn't localizable because sentence structure varies with language.</span></span>

    <span data-ttu-id="66f36-285">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-285">**Incorrect:**</span></span>

    ![<span data-ttu-id="66f36-286">captura de pantalla de la etiqueta de la casilla con el cuadro de texto en ella</span><span class="sxs-lookup"><span data-stu-id="66f36-286">screen shot of checkbox label with text box in it</span></span> ](images/ctrl-check-boxes-image27.png)

    <span data-ttu-id="66f36-287">En este ejemplo, el cuadro de texto se coloca incorrectamente dentro de la etiqueta de la casilla.</span><span class="sxs-lookup"><span data-stu-id="66f36-287">In this example, the text box is incorrectly placed inside the check box label.</span></span>

<span data-ttu-id="66f36-288">**Etiquetas de grupo de casillas**</span><span class="sxs-lookup"><span data-stu-id="66f36-288">**Check box group labels**</span></span>

-   <span data-ttu-id="66f36-289">Use la etiqueta de grupo para explicar el propósito del grupo, no cómo hacer la selección.</span><span class="sxs-lookup"><span data-stu-id="66f36-289">Use the group label to explain the purpose of the group, not how to make the selection.</span></span> <span data-ttu-id="66f36-290">Supongamos que los usuarios saben cómo usar las casillas.</span><span class="sxs-lookup"><span data-stu-id="66f36-290">Assume that users know how to use check boxes.</span></span> <span data-ttu-id="66f36-291">Por ejemplo, no indique "Seleccione cualquiera de las siguientes opciones".</span><span class="sxs-lookup"><span data-stu-id="66f36-291">For example, don't say "Select any of the following choices".</span></span>
-   <span data-ttu-id="66f36-292">Finalice cada etiqueta con un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="66f36-292">End each label with a colon.</span></span>
-   <span data-ttu-id="66f36-293">No asigne una clave de acceso a la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="66f36-293">Don't assign an access key to the label.</span></span> <span data-ttu-id="66f36-294">Esto no es necesario y hace que las demás claves de acceso sean más difíciles de asignar.</span><span class="sxs-lookup"><span data-stu-id="66f36-294">Doing so isn't necessary and it makes the other access keys harder to assign.</span></span>
-   <span data-ttu-id="66f36-295">Para obtener una selección de una o varias opciones dependientes, explique el requisito de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="66f36-295">For a selection of one or more dependent choices, explain the requirement on the label.</span></span>

    <span data-ttu-id="66f36-296">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="66f36-296">**Correct:**</span></span>

    ![<span data-ttu-id="66f36-297">captura de pantalla de la etiqueta de dos controles: protocolos</span><span class="sxs-lookup"><span data-stu-id="66f36-297">screen shot of label for two controls: protocols</span></span> ](images/ctrl-check-boxes-image28.png)

    <span data-ttu-id="66f36-298">En este ejemplo, los usuarios pueden creer que solo pueden hacer una selección.</span><span class="sxs-lookup"><span data-stu-id="66f36-298">In this example, users might think that they can only make one selection.</span></span>

    <span data-ttu-id="66f36-299">**Manera**</span><span class="sxs-lookup"><span data-stu-id="66f36-299">**Better:**</span></span>

    ![<span data-ttu-id="66f36-300">captura de pantalla de la etiqueta: los protocolos seleccionan uno o varios</span><span class="sxs-lookup"><span data-stu-id="66f36-300">screen shot of label: protocols select one or more</span></span> ](images/ctrl-check-boxes-image29.png)

    <span data-ttu-id="66f36-301">En este ejemplo, está claro que los usuarios pueden hacer más de una selección.</span><span class="sxs-lookup"><span data-stu-id="66f36-301">In this example, it's clear that users can make more than one selection.</span></span>

## <a name="documentation"></a><span data-ttu-id="66f36-302">Documentación</span><span class="sxs-lookup"><span data-stu-id="66f36-302">Documentation</span></span>

<span data-ttu-id="66f36-303">Al hacer referencia a las casillas:</span><span class="sxs-lookup"><span data-stu-id="66f36-303">When referring to check boxes:</span></span>

-   <span data-ttu-id="66f36-304">Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya el carácter de subrayado de la tecla de acceso o el signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="66f36-304">Use the exact label text, including its capitalization, but don't include the access key underscore or colon.</span></span> <span data-ttu-id="66f36-305">Incluya la palabra casilla.</span><span class="sxs-lookup"><span data-stu-id="66f36-305">Include the word check box.</span></span>
-   <span data-ttu-id="66f36-306">Haga referencia a una casilla de verificación como casilla, no como opción, casilla o simplemente cuadro, ya que Box solo es ambiguo para los localizadores.</span><span class="sxs-lookup"><span data-stu-id="66f36-306">Refer to a check box as a check box, not option, checkbox, or just box, because box alone is ambiguous for localizers.</span></span>
-   <span data-ttu-id="66f36-307">Para describir la interacción del usuario, use SELECT y Clear.</span><span class="sxs-lookup"><span data-stu-id="66f36-307">To describe user interaction, use select and clear.</span></span>
-   <span data-ttu-id="66f36-308">Siempre que sea posible, dé formato a la etiqueta usando texto en negrita.</span><span class="sxs-lookup"><span data-stu-id="66f36-308">When possible, format the label using bold text.</span></span> <span data-ttu-id="66f36-309">De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.</span><span class="sxs-lookup"><span data-stu-id="66f36-309">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="66f36-310">Ejemplo: Active la casilla **subrayado** .</span><span class="sxs-lookup"><span data-stu-id="66f36-310">Example: Select the **Underline** check box.</span></span>

