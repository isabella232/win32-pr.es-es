---
title: Cuadros de texto
description: Con un cuadro de texto, los usuarios pueden mostrar, escribir o modificar un texto o un valor numérico.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547270"
---
# <a name="text-boxes"></a><span data-ttu-id="2b878-103">Cuadros de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-103">Text Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="2b878-104">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="2b878-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="2b878-105">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="2b878-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="2b878-106">Con un cuadro de texto, los usuarios pueden mostrar, escribir o modificar un texto o un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="2b878-106">With a text box, users can display, enter, or edit a text or numeric value.</span></span>

![<span data-ttu-id="2b878-107">captura de pantalla de un cuadro de texto y una etiqueta típicos</span><span class="sxs-lookup"><span data-stu-id="2b878-107">screen shot of a typical text box and label</span></span> ](images/ctrl-text-boxes-image1.png)

<span data-ttu-id="2b878-108">Cuadro de texto típico.</span><span class="sxs-lookup"><span data-stu-id="2b878-108">A typical text box.</span></span>

> [!Note]  
> <span data-ttu-id="2b878-109">Las instrucciones relacionadas con el [diseño](vis-layout.md), las [fuentes](vis-fonts.md)y los [globos](ctrl-balloons.md) se presentan en artículos independientes.</span><span class="sxs-lookup"><span data-stu-id="2b878-109">Guidelines related to [layout](vis-layout.md), [fonts](vis-fonts.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="2b878-110">¿Es este el control adecuado?</span><span class="sxs-lookup"><span data-stu-id="2b878-110">Is this the right control?</span></span>

<span data-ttu-id="2b878-111">Para decidirte, intenta responder a estas preguntas:</span><span class="sxs-lookup"><span data-stu-id="2b878-111">To decide, consider these questions:</span></span>

-   <span data-ttu-id="2b878-112">**¿Es práctico enumerar todos los valores válidos de forma eficaz?**</span><span class="sxs-lookup"><span data-stu-id="2b878-112">**Is it practical to enumerate all the valid values efficiently?**</span></span> <span data-ttu-id="2b878-113">En caso afirmativo, considere la posibilidad de usar una lista de [selección única](ctrl-list-boxes.md), una [vista de lista](ctrl-list-views.md), una [lista](/windows/desktop/uxguide/ctrl-drop)desplegable, una lista desplegable editable o un [control deslizante](ctrl-sliders.md) .</span><span class="sxs-lookup"><span data-stu-id="2b878-113">If so, consider a [single-selection list](ctrl-list-boxes.md), [list view](ctrl-list-views.md), [drop-down list](/windows/desktop/uxguide/ctrl-drop), editable drop-down list, or [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="2b878-114">**¿Los datos válidos no están restringidos completamente? O son los datos válidos restringidos solo por formato (tipos de caracteres o longitud restringida)?**</span><span class="sxs-lookup"><span data-stu-id="2b878-114">**Is the valid data completely unconstrained? Or is the valid data constrained only by format (constrained length or character types)?**</span></span> <span data-ttu-id="2b878-115">Si es así, use un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-115">If so, use a text box.</span></span>
-   <span data-ttu-id="2b878-116">**¿Representa el valor un tipo de datos que tiene un control común especializado?**</span><span class="sxs-lookup"><span data-stu-id="2b878-116">**Does the value represent a data type that has a specialized common control?**</span></span> <span data-ttu-id="2b878-117">Entre los ejemplos se incluyen la fecha, la hora o la dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="2b878-117">Examples include date, time, or IPv4 or IPv6 address.</span></span> <span data-ttu-id="2b878-118">Si es así, utilice el control adecuado, como un control de fecha en lugar de un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-118">If so, use the appropriate control, such as a date control rather than a text box.</span></span>
-   <span data-ttu-id="2b878-119">Si los datos son numéricos:</span><span class="sxs-lookup"><span data-stu-id="2b878-119">If the data is numeric:</span></span>
    -   <span data-ttu-id="2b878-120">**¿Los usuarios perciben la configuración como una cantidad relativa?**</span><span class="sxs-lookup"><span data-stu-id="2b878-120">**Do users perceive the setting as a relative quantity?**</span></span> <span data-ttu-id="2b878-121">Si es así, usa un control deslizante.</span><span class="sxs-lookup"><span data-stu-id="2b878-121">If so, use a slider.</span></span>
    -   <span data-ttu-id="2b878-122">**¿Sería bueno que el usuario recibiera una respuesta instantánea del efecto de los cambios en la configuración?**</span><span class="sxs-lookup"><span data-stu-id="2b878-122">**Would the user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="2b878-123">Si es así, use un control deslizante, posiblemente junto con un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-123">If so, use a slider, possibly along with a text box.</span></span> <span data-ttu-id="2b878-124">Por ejemplo, los usuarios pueden elegir fácilmente un color con un control deslizante, ya que pueden ver de inmediato el efecto de los cambios en los valores de matiz, saturación o luminosidad.</span><span class="sxs-lookup"><span data-stu-id="2b878-124">For example, users can easily choose a color using a slider because they can immediately see the effect of changes to hue, saturation, or luminosity values.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="2b878-125">Conceptos de diseño</span><span class="sxs-lookup"><span data-stu-id="2b878-125">Design concepts</span></span>

<span data-ttu-id="2b878-126">Aunque los cuadros de texto tienen la ventaja de ser muy flexibles, tienen el inconveniente de tener restricciones mínimas.</span><span class="sxs-lookup"><span data-stu-id="2b878-126">While text boxes have the benefit of being very flexible, they have the drawback of having minimal constraints.</span></span> <span data-ttu-id="2b878-127">Las únicas restricciones en un cuadro de texto editable son:</span><span class="sxs-lookup"><span data-stu-id="2b878-127">The only constraints on an editable text box are:</span></span>

-   <span data-ttu-id="2b878-128">Opcionalmente, puede establecer el número máximo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2b878-128">You can optionally set the maximum number of characters.</span></span>
-   <span data-ttu-id="2b878-129">Opcionalmente, puede restringir la entrada solo a caracteres numéricos (0 9).</span><span class="sxs-lookup"><span data-stu-id="2b878-129">You can optionally restrict input to numeric characters (0   9) only.</span></span>
-   <span data-ttu-id="2b878-130">Si usa un [control de número](ctrl-spin-controls.md), puede limitar las opciones de control de número a valores válidos.</span><span class="sxs-lookup"><span data-stu-id="2b878-130">If you use a [spin control](ctrl-spin-controls.md), you can limit spin control choices to valid values.</span></span>

<span data-ttu-id="2b878-131">Aparte de su longitud y la presencia opcional de un control de número, los cuadros de texto no tienen ninguna pista visual que sugiera los valores válidos o su formato.</span><span class="sxs-lookup"><span data-stu-id="2b878-131">Aside from their length and the optional presence of a spin control, text boxes don't have any visual clues that suggest the valid values or their format.</span></span> <span data-ttu-id="2b878-132">Esto significa depender de etiquetas para transmitir esta información a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="2b878-132">This means relying on labels to convey this information to users.</span></span> <span data-ttu-id="2b878-133">Si los usuarios escriben texto que no es válido, debe controlar el error con un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="2b878-133">If users enter text that's not valid, you must handle the error with an error message.</span></span>

<span data-ttu-id="2b878-134">Como norma general, **debe usar el control más restringido que pueda**.</span><span class="sxs-lookup"><span data-stu-id="2b878-134">As a general rule, **you should use the most constrained control that you can**.</span></span> <span data-ttu-id="2b878-135">Usar controles sin restricciones como cuadros de texto como último recurso.</span><span class="sxs-lookup"><span data-stu-id="2b878-135">Use unconstrained controls like text boxes as a last resort.</span></span> <span data-ttu-id="2b878-136">Dicho esto, al considerar las restricciones, tenga en cuenta las necesidades de los usuarios globales.</span><span class="sxs-lookup"><span data-stu-id="2b878-136">That said, when you are considering constraints, bear in mind the needs of global users.</span></span> <span data-ttu-id="2b878-137">Por ejemplo, un control que está restringido a Estados Unidos códigos postales no se globaliza, pero un cuadro de texto sin restricciones que acepta cualquier formato de código postal es.</span><span class="sxs-lookup"><span data-stu-id="2b878-137">For example, a control that is constrained to United States ZIP Codes isn't globalized, but an unconstrained text box that accepts any postal code format is.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="2b878-138">Patrones de uso</span><span class="sxs-lookup"><span data-stu-id="2b878-138">Usage patterns</span></span>

<span data-ttu-id="2b878-139">Un cuadro de texto es un control flexible con varios usos posibles.</span><span class="sxs-lookup"><span data-stu-id="2b878-139">A text box is a flexible control with several possible uses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b878-140"><strong>Entrada de datos</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-140"><strong>Data input</strong></span></span><br/> <span data-ttu-id="2b878-141">Cuadro de texto sin restricciones de una sola línea que se usa para escribir o editar cadenas cortas.</span><span class="sxs-lookup"><span data-stu-id="2b878-141">A single-line, unconstrained text box used to enter or edit short strings.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> <span data-ttu-id="2b878-142">Cuadro de texto sin restricciones de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="2b878-142">A single-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b878-143"><strong>Entrada de datos con formato</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-143"><strong>Formatted data input</strong></span></span><br/> <span data-ttu-id="2b878-144">Un conjunto de cuadros de texto cortos de una sola línea y de tamaño fijo que se usan para escribir datos con un formato específico.</span><span class="sxs-lookup"><span data-stu-id="2b878-144">A set of short, fixed-sized, single-line text boxes used to enter data with a specific format.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> <span data-ttu-id="2b878-145">Cuadro de texto que se usa para la entrada de datos con formato.</span><span class="sxs-lookup"><span data-stu-id="2b878-145">A text box used for formatted data input.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2b878-146">La característica <a href="glossary.md">de salida automática</a> desplaza automáticamente el foco de entrada de un cuadro de texto al siguiente.</span><span class="sxs-lookup"><span data-stu-id="2b878-146">The <a href="glossary.md">auto-exit</a> feature automatically advances the input focus from one text box to the next.</span></span> <span data-ttu-id="2b878-147">Una desventaja de este enfoque es que los datos no se pueden copiar ni pegar como una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="2b878-147">One disadvantage to this approach is that the data can't be copied or pasted as a single unit.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b878-148"><strong>Entrada de datos asistida</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-148"><strong>Assisted data input</strong></span></span><br/> <span data-ttu-id="2b878-149">Cuadro de texto sin restricciones de una sola línea que se usa para escribir o editar cadenas, junto con un botón de comando que ayuda a los usuarios a seleccionar valores válidos.</span><span class="sxs-lookup"><span data-stu-id="2b878-149">A single-line, unconstrained text box used to enter or edit strings, combined with a command button that helps users select valid values.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> <span data-ttu-id="2b878-150">En este ejemplo, el comando Browse ayuda a los usuarios a seleccionar valores válidos.</span><span class="sxs-lookup"><span data-stu-id="2b878-150">In this example, the Browse command helps users select valid values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b878-151"><strong>Entrada de texto</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-151"><strong>Textual input</strong></span></span><br/> <span data-ttu-id="2b878-152">Cuadro de texto sin restricciones y de varias líneas que se usa para escribir o editar cadenas largas.</span><span class="sxs-lookup"><span data-stu-id="2b878-152">A multi-line, unconstrained text box used to enter or edit long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> <span data-ttu-id="2b878-153">Cuadro de texto sin restricciones de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="2b878-153">A multi-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b878-154"><strong>Entradas numéricas</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-154"><strong>Numeric input</strong></span></span><br/> <span data-ttu-id="2b878-155">Cuadro de texto de una sola línea y solo numérico que se usa para escribir o editar números, con un <a href="ctrl-spin-controls.md">control de número</a> opcional para facilitar la entrada basada en el mouse.</span><span class="sxs-lookup"><span data-stu-id="2b878-155">A single-line, numeric-only text box used to enter or edit numbers, with an optional <a href="ctrl-spin-controls.md">spin control</a> to facilitate mouse-based input.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> <span data-ttu-id="2b878-156">Cuadro de texto que se usa para la entrada numérica.</span><span class="sxs-lookup"><span data-stu-id="2b878-156">A text box used for numeric input.</span></span><br/> <span data-ttu-id="2b878-157">La combinación de un cuadro de texto y su control de número asociado se denomina <a href="ctrl-spin-controls.md">cuadro de número</a>.</span><span class="sxs-lookup"><span data-stu-id="2b878-157">The combination of a text box and its associated spin control is called a <a href="ctrl-spin-controls.md">spin box</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b878-158"><strong>Entrada de contraseña y PIN</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-158"><strong>Password and PIN input</strong></span></span><br/> <span data-ttu-id="2b878-159">Cuadro de texto sin restricciones de una sola línea que se usa para escribir contraseñas y PIN de forma segura.</span><span class="sxs-lookup"><span data-stu-id="2b878-159">A single-line, unconstrained text box used to enter passwords and PINs securely.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> <span data-ttu-id="2b878-160">Cuadro de texto que se usa para escribir contraseñas.</span><span class="sxs-lookup"><span data-stu-id="2b878-160">A text box used to enter passwords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b878-161"><strong>Salida de datos</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-161"><strong>Data output</strong></span></span><br/> <span data-ttu-id="2b878-162">Cuadro de texto de solo una línea de solo lectura, que siempre se muestra sin borde, que se usa para mostrar cadenas cortas.</span><span class="sxs-lookup"><span data-stu-id="2b878-162">A single-line, read-only text box, always displayed without a border, used to display short strings.</span></span> <br/></td>
<td><span data-ttu-id="2b878-163">A diferencia del texto estático, los datos que se muestran mediante un cuadro de texto se pueden desplazar (útil si los datos son más anchos que el control), se seleccionan y se copian.</span><span class="sxs-lookup"><span data-stu-id="2b878-163">Unlike static text, data displayed using a text box can be scrolled (useful if the data is wider than the control), selected, and copied.</span></span><br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> <span data-ttu-id="2b878-164">Cuadro de texto de solo una línea de solo lectura que se usa para mostrar los datos.</span><span class="sxs-lookup"><span data-stu-id="2b878-164">A single-line, read-only text box used to display data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b878-165"><strong>Salida de texto</strong></span><span class="sxs-lookup"><span data-stu-id="2b878-165"><strong>Textual output</strong></span></span><br/> <span data-ttu-id="2b878-166">Cuadro de texto de solo lectura y de varias líneas que se usa para mostrar cadenas largas.</span><span class="sxs-lookup"><span data-stu-id="2b878-166">A multi-line, read-only text box used to display long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> <span data-ttu-id="2b878-167">Cuadro de texto de solo lectura que se usa para mostrar los datos.</span><span class="sxs-lookup"><span data-stu-id="2b878-167">A read-only text box used to display data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="2b878-168">Directrices</span><span class="sxs-lookup"><span data-stu-id="2b878-168">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="2b878-169">General</span><span class="sxs-lookup"><span data-stu-id="2b878-169">General</span></span>

-   <span data-ttu-id="2b878-170">**Al deshabilitar un cuadro de texto, deshabilite también las etiquetas asociadas, las etiquetas de instrucciones, los controles de número y los botones de comando.**</span><span class="sxs-lookup"><span data-stu-id="2b878-170">**When disabling a text box, also disable any associated labels, instruction labels, spin controls, and command buttons.**</span></span>
-   <span data-ttu-id="2b878-171">**Usar Autocompletar para ayudar a los usuarios a escribir datos que es probable que se usen repetidamente**.</span><span class="sxs-lookup"><span data-stu-id="2b878-171">**Use auto-complete to help users enter data that is likely to be used repeatedly**.</span></span> <span data-ttu-id="2b878-172">Algunos ejemplos son los nombres de usuario, las direcciones y los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="2b878-172">Examples include user names, addresses, and file names.</span></span> <span data-ttu-id="2b878-173">Sin embargo, no use la función autocompletar para cuadros de texto que pueden contener información confidencial, como contraseñas, PIN, números de tarjetas de crédito o información médica.</span><span class="sxs-lookup"><span data-stu-id="2b878-173">However, don't use auto-complete for text boxes that may contain sensitive information, such as passwords, PINs, credit card numbers, or medical information.</span></span>
-   <span data-ttu-id="2b878-174">**No haga que los usuarios se desplacen innecesariamente.**</span><span class="sxs-lookup"><span data-stu-id="2b878-174">**Don't make users scroll unnecessarily.**</span></span> <span data-ttu-id="2b878-175">Si espera que los datos sean más grandes que el cuadro de texto y puede hacer que el cuadro de texto sea más grande sin dañar el diseño, ajuste el tamaño del cuadro para eliminar la necesidad de desplazarse.</span><span class="sxs-lookup"><span data-stu-id="2b878-175">If you expect data to be larger than the text box and you can readily make the text box larger without harming the layout, size the box to eliminate the need for scrolling.</span></span>

    <span data-ttu-id="2b878-176">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-176">**Incorrect:**</span></span>

    ![<span data-ttu-id="2b878-177">captura de pantalla de un cuadro de texto de nombre de equipo</span><span class="sxs-lookup"><span data-stu-id="2b878-177">screen shot of a computer name text box</span></span> ](images/ctrl-text-boxes-image10.png)

    <span data-ttu-id="2b878-178">En este ejemplo, el cuadro de texto debe realizarse mucho más para controlar sus datos.</span><span class="sxs-lookup"><span data-stu-id="2b878-178">In this example, the text box should be made much longer to handle its data.</span></span>

-   <span data-ttu-id="2b878-179">Barras de desplazamiento:</span><span class="sxs-lookup"><span data-stu-id="2b878-179">Scroll bars:</span></span>
    -   <span data-ttu-id="2b878-180">**No coloque barras de desplazamiento horizontal en cuadros de texto de varias líneas.**</span><span class="sxs-lookup"><span data-stu-id="2b878-180">**Don't put horizontal scroll bars on multi-line text boxes.**</span></span> <span data-ttu-id="2b878-181">En su lugar, use el desplazamiento vertical y el ajuste de línea.</span><span class="sxs-lookup"><span data-stu-id="2b878-181">Use vertical scrolling and line wrapping instead.</span></span>
    -   <span data-ttu-id="2b878-182">**No coloque ninguna barra de desplazamiento en los cuadros de texto de una sola línea.**</span><span class="sxs-lookup"><span data-stu-id="2b878-182">**Don't put any scroll bars on single-line text boxes.**</span></span>
-   <span data-ttu-id="2b878-183">**En el caso de entradas numéricas, puede utilizar un control de número.**</span><span class="sxs-lookup"><span data-stu-id="2b878-183">**For numeric input, you may use a spin control.**</span></span> <span data-ttu-id="2b878-184">En entrada de texto, use una lista desplegable o una lista desplegable editable.</span><span class="sxs-lookup"><span data-stu-id="2b878-184">For textual input, use a drop-down list or editable drop-down list instead.</span></span>
-   <span data-ttu-id="2b878-185">**No use la característica de salida automática excepto para la entrada de datos con formato.**</span><span class="sxs-lookup"><span data-stu-id="2b878-185">**Don't use the auto-exit feature except for formatted data input.**</span></span> <span data-ttu-id="2b878-186">El cambio de foco automático puede sorprender a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="2b878-186">The automatic shift of focus can surprise users.</span></span>

### <a name="editable-text-boxes"></a><span data-ttu-id="2b878-187">Cuadros de texto modificables</span><span class="sxs-lookup"><span data-stu-id="2b878-187">Editable text boxes</span></span>

-   <span data-ttu-id="2b878-188">**Limite la longitud del texto de entrada cuando sea posible.**</span><span class="sxs-lookup"><span data-stu-id="2b878-188">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="2b878-189">Por ejemplo, si la entrada válida es un número comprendido entre 0 y 999, use un cuadro de texto numérico que tenga un límite de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="2b878-189">For example, if the valid input is a number between 0 and 999, use a numeric text box that is limited to three characters.</span></span> <span data-ttu-id="2b878-190">Todas las partes de los cuadros de texto que usan la entrada de datos con formato deben tener una longitud fija corta.</span><span class="sxs-lookup"><span data-stu-id="2b878-190">All parts of text boxes that use formatted data input must have a short, fixed length.</span></span>
-   <span data-ttu-id="2b878-191">**Ser flexible con formatos de datos.**</span><span class="sxs-lookup"><span data-stu-id="2b878-191">**Be flexible with data formats.**</span></span> <span data-ttu-id="2b878-192">Si es probable que los usuarios escriban texto con una amplia variedad de formatos, intente administrar todos los más comunes.</span><span class="sxs-lookup"><span data-stu-id="2b878-192">If users are likely to enter text using a wide variety of formats, try to handle all the most common ones.</span></span> <span data-ttu-id="2b878-193">Por ejemplo, se pueden especificar muchos nombres, números e identificadores con espacios opcionales y signos de puntuación, y las mayúsculas y minúsculas no importan a menudo.</span><span class="sxs-lookup"><span data-stu-id="2b878-193">For example, many names, numbers, and identifiers can be entered with optional spaces and punctuation, and the capitalization often doesn't matter.</span></span>
-   <span data-ttu-id="2b878-194">Si no puede controlar los formatos más probables, solicite un formato específico mediante la entrada de datos con formato o indique los formatos válidos en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2b878-194">If you can't handle the likely formats, require a specific format by using formatted data input or indicate the valid formats in the label.</span></span>

    <span data-ttu-id="2b878-195">**Aceptable:**</span><span class="sxs-lookup"><span data-stu-id="2b878-195">**Acceptable:**</span></span>

    ![<span data-ttu-id="2b878-196">captura de pantalla de un cuadro de texto para entrada numérica</span><span class="sxs-lookup"><span data-stu-id="2b878-196">screen shot of a text box for numeric input</span></span> ](images/ctrl-text-boxes-image11.png)

    <span data-ttu-id="2b878-197">En este ejemplo, un cuadro de texto requiere una entrada en un formato específico.</span><span class="sxs-lookup"><span data-stu-id="2b878-197">In this example, a text box requires input in a specific format.</span></span>

    <span data-ttu-id="2b878-198">**Manera**</span><span class="sxs-lookup"><span data-stu-id="2b878-198">**Better:**</span></span>

    ![<span data-ttu-id="2b878-199">captura de pantalla del cuadro de texto de entrada de datos con formato</span><span class="sxs-lookup"><span data-stu-id="2b878-199">screen shot of formatted data input text box</span></span> ](images/ctrl-text-boxes-image12.png)

    <span data-ttu-id="2b878-200">En este ejemplo, el modelo de entrada de datos con formato se usa para requerir un formato específico.</span><span class="sxs-lookup"><span data-stu-id="2b878-200">In this example, the formatted data input pattern is used to require a specific format.</span></span>

    <span data-ttu-id="2b878-201">**Rendimiento**</span><span class="sxs-lookup"><span data-stu-id="2b878-201">**Best:**</span></span>

    ![<span data-ttu-id="2b878-202">captura de pantalla de un cuadro de texto sin restricciones</span><span class="sxs-lookup"><span data-stu-id="2b878-202">screen shot of an unconstrained text box</span></span> ](images/ctrl-text-boxes-image13.png)

    <span data-ttu-id="2b878-203">En este ejemplo, un cuadro de texto controla todos los formatos más probables.</span><span class="sxs-lookup"><span data-stu-id="2b878-203">In this example, a text box handles all likely formats.</span></span>

-   <span data-ttu-id="2b878-204">Considere la flexibilidad de formato al elegir la longitud máxima de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b878-204">Consider format flexibility when choosing the maximum input length.</span></span> <span data-ttu-id="2b878-205">Por ejemplo, un número de tarjeta de crédito válido puede usar hasta 19 caracteres, por lo que limitar la longitud a cualquier valor más corto dificultaría la entrada de números con formatos más largos.</span><span class="sxs-lookup"><span data-stu-id="2b878-205">For example, a valid credit card number can use up to 19 characters so limiting the length to anything shorter would make it difficult to enter numbers using the longer formats.</span></span>
-   <span data-ttu-id="2b878-206">**No use el patrón de entrada de datos con formato si es más probable que los usuarios peguen datos largos y complejos.**</span><span class="sxs-lookup"><span data-stu-id="2b878-206">**Don't use the formatted data input pattern if users are more likely to paste in long, complex data.**</span></span> <span data-ttu-id="2b878-207">En su lugar, Reserve el modelo de entrada de datos con formato para situaciones en las que es más probable que los usuarios escriban los datos.</span><span class="sxs-lookup"><span data-stu-id="2b878-207">Rather, reserve the formatted data input pattern for situations where users are more likely to type the data.</span></span>

    ![<span data-ttu-id="2b878-208">captura de pantalla de un cuadro de texto con la etiqueta: dirección IPv6</span><span class="sxs-lookup"><span data-stu-id="2b878-208">screen shot of a text box with label: ipv6 address</span></span> ](images/ctrl-text-boxes-image14.png)

    <span data-ttu-id="2b878-209">En este ejemplo, no se usa el modelo de entrada de datos con formato, por lo que los usuarios pueden pegar direcciones IPv6.</span><span class="sxs-lookup"><span data-stu-id="2b878-209">In this example, the formatted data input pattern isn't used, so that users can to paste IPv6 addresses.</span></span>

-   <span data-ttu-id="2b878-210">**Si es más probable que los usuarios vuelvan a escribir todo el valor, seleccione todo el texto en el foco de entrada.**</span><span class="sxs-lookup"><span data-stu-id="2b878-210">**If users are more likely going to reenter the entire value, select all the text on input focus.**</span></span> <span data-ttu-id="2b878-211">Si es más probable que los usuarios editen, coloque el símbolo de intercalación al final del texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-211">If users are more likely to edit, place the caret at the end of the text.</span></span>

    ![<span data-ttu-id="2b878-212">captura de pantalla de un cuadro de texto de contraseña</span><span class="sxs-lookup"><span data-stu-id="2b878-212">screen shot of a password text box</span></span> ](images/ctrl-text-boxes-image15.png)

    <span data-ttu-id="2b878-213">En este ejemplo, es más probable que los usuarios reemplacen a Edit, por lo que el valor completo se selecciona en el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b878-213">In this example, users are more likely to replace than edit, so the entire value is selected on input focus.</span></span>

    ![<span data-ttu-id="2b878-214">captura de pantalla de un cuadro de texto para escribir palabras clave</span><span class="sxs-lookup"><span data-stu-id="2b878-214">screen shot of a text box for entering keywords</span></span> ](images/ctrl-text-boxes-image16.png)

    <span data-ttu-id="2b878-215">En este ejemplo, es más probable que los usuarios agreguen palabras clave que reemplacen el texto, por lo que el símbolo de intercalación se coloca al final del texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-215">In this example, users are more likely to add keywords than replace the text, so the caret is placed at the end of the text.</span></span>

-   <span data-ttu-id="2b878-216">**Use siempre un cuadro de texto de varias líneas si los caracteres de nueva línea son entradas válidas.**</span><span class="sxs-lookup"><span data-stu-id="2b878-216">**Always use a multi-line text box if new-line characters are valid input.**</span></span>
-   <span data-ttu-id="2b878-217">**Cuando el cuadro de texto es para un archivo o una ruta de acceso, proporcione siempre un botón examinar.**</span><span class="sxs-lookup"><span data-stu-id="2b878-217">**When the text box is for a file or path, always provide a Browse button.**</span></span>

### <a name="numeric-text-boxes"></a><span data-ttu-id="2b878-218">Cuadros de texto numéricos</span><span class="sxs-lookup"><span data-stu-id="2b878-218">Numeric text boxes</span></span>

-   <span data-ttu-id="2b878-219">**Elija la unidad más cómoda y etiquete las unidades.**</span><span class="sxs-lookup"><span data-stu-id="2b878-219">**Choose the most convenient unit and label the units.**</span></span> <span data-ttu-id="2b878-220">Por ejemplo, considere la posibilidad de usar milliliters en lugar de los litros (o viceversa), los porcentajes en lugar de los valores directos (o viceversa), etc.</span><span class="sxs-lookup"><span data-stu-id="2b878-220">For example, consider using milliliters instead of liters (or vice versa), percentages instead of direct values (or vice versa), and so on.</span></span>

    <span data-ttu-id="2b878-221">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-221">**Correct:**</span></span>

    ![<span data-ttu-id="2b878-222">captura de pantalla de un cuadro de texto con un litro como unidad</span><span class="sxs-lookup"><span data-stu-id="2b878-222">screen shot of text box with liters as unit</span></span> ](images/ctrl-text-boxes-image17.png)

    <span data-ttu-id="2b878-223">En este ejemplo, la unidad tiene la etiqueta, pero requiere que los usuarios escriban números decimales.</span><span class="sxs-lookup"><span data-stu-id="2b878-223">In this example, the unit is labeled, but it requires users to enter decimal numbers.</span></span>

    <span data-ttu-id="2b878-224">**Manera**</span><span class="sxs-lookup"><span data-stu-id="2b878-224">**Better:**</span></span>

    ![<span data-ttu-id="2b878-225">captura de pantalla de un cuadro de texto con milliliters como unidad</span><span class="sxs-lookup"><span data-stu-id="2b878-225">screen shot of text box with milliliters as unit</span></span> ](images/ctrl-text-boxes-image18.png)

    <span data-ttu-id="2b878-226">En este ejemplo, el cuadro de texto utiliza una unidad más cómoda.</span><span class="sxs-lookup"><span data-stu-id="2b878-226">In this example, the text box uses a more convenient unit.</span></span>

-   <span data-ttu-id="2b878-227">**Use un control de número siempre que resulte útil.**</span><span class="sxs-lookup"><span data-stu-id="2b878-227">**Use a spin control whenever it is helpful.**</span></span> <span data-ttu-id="2b878-228">Sin embargo, a veces los controles de giro no son prácticos, como cuando los usuarios necesitan escribir muchos números grandes.</span><span class="sxs-lookup"><span data-stu-id="2b878-228">However, sometimes spin controls aren't practical, such as when users need to enter many large numbers.</span></span> <span data-ttu-id="2b878-229">Use los controles de número cuando:</span><span class="sxs-lookup"><span data-stu-id="2b878-229">Use spin controls when:</span></span>
    -   <span data-ttu-id="2b878-230">Es probable que la entrada sea un número pequeño, normalmente inferior a 100.</span><span class="sxs-lookup"><span data-stu-id="2b878-230">The input is likely to be a small number, typically under 100.</span></span>
    -   <span data-ttu-id="2b878-231">Es probable que los usuarios realicen un pequeño cambio en un número existente.</span><span class="sxs-lookup"><span data-stu-id="2b878-231">Users are likely to make a small change to an existing number.</span></span>
    -   <span data-ttu-id="2b878-232">Es más probable que los usuarios utilicen el mouse que el teclado.</span><span class="sxs-lookup"><span data-stu-id="2b878-232">Users are more likely to be using the mouse than the keyboard.</span></span>
-   <span data-ttu-id="2b878-233">**Alinear a la derecha el texto numérico siempre que:**</span><span class="sxs-lookup"><span data-stu-id="2b878-233">**Right-align numeric text whenever:**</span></span>

    -   <span data-ttu-id="2b878-234">Hay más de un cuadro de texto numérico.</span><span class="sxs-lookup"><span data-stu-id="2b878-234">There is more than one numeric text box.</span></span>
    -   <span data-ttu-id="2b878-235">Los cuadros de texto están alineados verticalmente.</span><span class="sxs-lookup"><span data-stu-id="2b878-235">The text boxes are vertically aligned.</span></span>
    -   <span data-ttu-id="2b878-236">Es probable que los usuarios agreguen o comparen los valores.</span><span class="sxs-lookup"><span data-stu-id="2b878-236">Users are likely to add or compare the values.</span></span>

    <span data-ttu-id="2b878-237">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-237">**Correct:**</span></span>

    ![<span data-ttu-id="2b878-238">captura de pantalla de los cuadros de texto de gastos (Hotel, etc.)</span><span class="sxs-lookup"><span data-stu-id="2b878-238">screen shot of expenses text boxes (hotel, etc.)</span></span> ](images/ctrl-text-boxes-image19.png)

    <span data-ttu-id="2b878-239">En este ejemplo, el texto numérico está alineado a la derecha para facilitar la comparación de los valores.</span><span class="sxs-lookup"><span data-stu-id="2b878-239">In this example, the numeric text is right-aligned to make it easy to compare values.</span></span>

    <span data-ttu-id="2b878-240">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-240">**Incorrect:**</span></span>

    ![<span data-ttu-id="2b878-241">captura de pantalla de cuadros de texto para valores RGB</span><span class="sxs-lookup"><span data-stu-id="2b878-241">screen shot of text boxes for rgb values</span></span> ](images/ctrl-text-boxes-image20.png)

    <span data-ttu-id="2b878-242">En este ejemplo, el texto numérico se alinea incorrectamente a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="2b878-242">In this example, the numeric text is incorrectly left-aligned.</span></span>

-   <span data-ttu-id="2b878-243">**Alinea siempre a la derecha los valores monetarios.**</span><span class="sxs-lookup"><span data-stu-id="2b878-243">**Always right-align monetary values.**</span></span>
-   <span data-ttu-id="2b878-244">**No asigne ningún significado especial a valores numéricos específicos**, incluso si la aplicación usa internamente esos significados especiales.</span><span class="sxs-lookup"><span data-stu-id="2b878-244">**Don't assign special meanings to specific numeric values**, even if those special meanings are used internally by your application.</span></span> <span data-ttu-id="2b878-245">En su lugar, use las casillas o los botones de radio para una selección de usuario explícita.</span><span class="sxs-lookup"><span data-stu-id="2b878-245">Instead, use check boxes or radio buttons for an explicit user selection.</span></span>

    <span data-ttu-id="2b878-246">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-246">**Incorrect:**</span></span>

    ![<span data-ttu-id="2b878-247">captura de pantalla de la etiqueta: Use-1 para deshabilitar el almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="2b878-247">screen shot of label: use -1 to disable caching</span></span> ](images/ctrl-text-boxes-image21.png)

    <span data-ttu-id="2b878-248">En este ejemplo, el valor-1 tiene un significado especial.</span><span class="sxs-lookup"><span data-stu-id="2b878-248">In this example, the value -1 has a special meaning.</span></span>

    <span data-ttu-id="2b878-249">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-249">**Correct:**</span></span>

    ![<span data-ttu-id="2b878-250">captura de pantalla de la etiqueta de la casilla: Caching</span><span class="sxs-lookup"><span data-stu-id="2b878-250">screen shot of check box label: caching</span></span> ](images/ctrl-text-boxes-image22.png)

    <span data-ttu-id="2b878-251">En este ejemplo, una casilla hace que la opción sea explícita.</span><span class="sxs-lookup"><span data-stu-id="2b878-251">In this example, a check box makes the option explicit.</span></span>

### <a name="password-and-pin-input"></a><span data-ttu-id="2b878-252">Entrada de contraseña y PIN</span><span class="sxs-lookup"><span data-stu-id="2b878-252">Password and PIN input</span></span>

-   <span data-ttu-id="2b878-253">**Use siempre el control común de contraseña en lugar de crear el suyo propio.**</span><span class="sxs-lookup"><span data-stu-id="2b878-253">**Always use the password common control instead of creating your own.**</span></span> <span data-ttu-id="2b878-254">Las contraseñas y los pin requieren un tratamiento especial para que se controle de forma segura.</span><span class="sxs-lookup"><span data-stu-id="2b878-254">Passwords and PINs require special treatment to be handled securely.</span></span>

<span data-ttu-id="2b878-255">Para obtener más instrucciones y ejemplos, vea [globos](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="2b878-255">For more guidelines and examples, see [Balloons](ctrl-balloons.md).</span></span>

### <a name="textual-output"></a><span data-ttu-id="2b878-256">Salida de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-256">Textual output</span></span>

-   <span data-ttu-id="2b878-257">**Considere la posibilidad de usar el color de fondo blanco del sistema para texto de solo lectura de varias líneas.**</span><span class="sxs-lookup"><span data-stu-id="2b878-257">**Consider using the white background system color for large, multi-line read-only text.**</span></span> <span data-ttu-id="2b878-258">Un fondo blanco facilita la lectura del texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-258">A white background makes the text easier to read.</span></span> <span data-ttu-id="2b878-259">Una gran cantidad de texto sobre un fondo gris desaconseja la lectura.</span><span class="sxs-lookup"><span data-stu-id="2b878-259">Lots of text on a gray background discourages reading.</span></span>

<span data-ttu-id="2b878-260">Para obtener más información sobre los colores de fondo, vea [fuentes](vis-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="2b878-260">For more information on background colors, see [Fonts](vis-fonts.md).</span></span>

### <a name="data-output"></a><span data-ttu-id="2b878-261">Salida de datos</span><span class="sxs-lookup"><span data-stu-id="2b878-261">Data output</span></span>

-   <span data-ttu-id="2b878-262">**No use un borde para cuadros de texto de solo una línea de solo lectura.**</span><span class="sxs-lookup"><span data-stu-id="2b878-262">**Don't use a border for single-line, read-only text boxes.**</span></span> <span data-ttu-id="2b878-263">El borde es una pista visual de que el texto es editable.</span><span class="sxs-lookup"><span data-stu-id="2b878-263">The border is a visual clue that the text is editable.</span></span>
-   <span data-ttu-id="2b878-264">**No deshabilite cuadros de texto de una sola línea y de solo lectura.**</span><span class="sxs-lookup"><span data-stu-id="2b878-264">**Don't disable single-line, read-only text boxes.**</span></span> <span data-ttu-id="2b878-265">Esto impide que los usuarios seleccionen y copien el texto en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="2b878-265">This prevents users from selecting and copying the text to the clipboard.</span></span> <span data-ttu-id="2b878-266">También impide que los usuarios desplacen los datos si superan el tamaño de sus límites.</span><span class="sxs-lookup"><span data-stu-id="2b878-266">It also prevents users from scrolling the data if it exceeds the size of its boundaries.</span></span>
-   <span data-ttu-id="2b878-267">**No establezca una detención de tabulación en el cuadro de texto de solo una línea de solo lectura a menos que el usuario tenga que desplazarse o copiar el texto.**</span><span class="sxs-lookup"><span data-stu-id="2b878-267">**Don't set a tab stop on single-line, read-only text box unless the user is likely to need to scroll or copy the text.**</span></span>

## <a name="input-validation-and-error-handling"></a><span data-ttu-id="2b878-268">Validación de entrada y control de errores</span><span class="sxs-lookup"><span data-stu-id="2b878-268">Input validation and error handling</span></span>

<span data-ttu-id="2b878-269">Dado que los cuadros de texto normalmente no están restringidos para aceptar solo entradas válidas, es posible que tenga que validar la entrada y controlar los problemas.</span><span class="sxs-lookup"><span data-stu-id="2b878-269">Because text boxes are usually not constrained to accept only valid input, you may need to validate the input and handle any problems.</span></span> <span data-ttu-id="2b878-270">Valide los distintos tipos de problemas de entrada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2b878-270">Validate the various types of input problems as follows:</span></span>

-   <span data-ttu-id="2b878-271">Si el usuario escribe un carácter que no es válido, ignore el carácter y muestre un [globo de problema de entrada](ctrl-balloons.md) que explique los caracteres válidos.</span><span class="sxs-lookup"><span data-stu-id="2b878-271">If the user enters a character that isn't valid, ignore the character and display an [input problem balloon](ctrl-balloons.md) that explains the valid characters.</span></span>

    ![captura de pantalla del cuadro de texto clave de producto](images/ctrl-text-boxes-image23.png)

    <span data-ttu-id="2b878-273">En este ejemplo, un globo informa de un carácter de entrada incorrecto.</span><span class="sxs-lookup"><span data-stu-id="2b878-273">In this example, a balloon reports an incorrect input character.</span></span>

-   <span data-ttu-id="2b878-274">Si los datos de entrada tienen un valor o un formato que no es válido, muestre un globo de problema de entrada cuando el cuadro de texto pierda el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b878-274">If the input data has a value or format that isn't valid, display an input problem balloon when the text box loses input focus.</span></span>
-   <span data-ttu-id="2b878-275">Si los datos de entrada son incoherentes con otros controles de la ventana, proporcione un mensaje de error cuando se complete toda la entrada, por ejemplo, cuando los usuarios hacen clic en Aceptar para un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="2b878-275">If the input data is inconsistent with other controls on the window, give an error message when the entire input is complete, such as when users click OK for a modal dialog box.</span></span>

<span data-ttu-id="2b878-276">**No borre los datos de entrada no válidos a menos que los usuarios no puedan corregir los errores fácilmente.**</span><span class="sxs-lookup"><span data-stu-id="2b878-276">**Don't clear invalid input data unless users aren't able to correct errors easily.**</span></span> <span data-ttu-id="2b878-277">Esto permite a los usuarios corregir errores sin necesidad de iniciarse.</span><span class="sxs-lookup"><span data-stu-id="2b878-277">Doing so allows users to correct mistakes without starting over.</span></span> <span data-ttu-id="2b878-278">Por ejemplo, debe borrar las contraseñas y los pin incorrectos, ya que los usuarios no pueden corregirlos fácilmente.</span><span class="sxs-lookup"><span data-stu-id="2b878-278">For example, you should clear incorrect passwords and PINs because users can't correct them easily.</span></span>

<span data-ttu-id="2b878-279">Para obtener más instrucciones y ejemplos, consulte [mensajes de error](mess-error.md) y [globos](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="2b878-279">For more guidelines and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

## <a name="prompts"></a><span data-ttu-id="2b878-280">Mensajes</span><span class="sxs-lookup"><span data-stu-id="2b878-280">Prompts</span></span>

<span data-ttu-id="2b878-281">Un mensaje es una etiqueta o una instrucción corta colocada dentro de un cuadro de texto como su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2b878-281">A prompt is a label or short instruction placed inside a text box as its default value.</span></span> <span data-ttu-id="2b878-282">A diferencia del texto estático, los mensajes desaparecen de la pantalla una vez que los usuarios escriben algo en el cuadro de texto o obtienen el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b878-282">Unlike static text, prompts disappear from the screen once users type something into the text box or it gets input focus.</span></span>

![<span data-ttu-id="2b878-283">captura de pantalla del cuadro de texto prompt con la etiqueta: Search</span><span class="sxs-lookup"><span data-stu-id="2b878-283">screen shot of prompt text box with label: search</span></span> ](images/ctrl-text-boxes-image24.png)

<span data-ttu-id="2b878-284">Un mensaje típico.</span><span class="sxs-lookup"><span data-stu-id="2b878-284">A typical prompt.</span></span>

<span data-ttu-id="2b878-285">Use un símbolo del sistema cuando:</span><span class="sxs-lookup"><span data-stu-id="2b878-285">Use a prompt when:</span></span>

-   <span data-ttu-id="2b878-286">El espacio de la pantalla es tan importante que no se desea usar una etiqueta o instrucción, como en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="2b878-286">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="2b878-287">El mensaje es principalmente para identificar el propósito del cuadro de texto de una manera compacta.</span><span class="sxs-lookup"><span data-stu-id="2b878-287">The prompt is primarily for identifying the purpose of the text box in a compact way.</span></span> <span data-ttu-id="2b878-288">No debe ser información fundamental que el usuario necesite ver mientras usa el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-288">It must not be crucial information that the user needs to see while using the text box.</span></span>

<span data-ttu-id="2b878-289">No use mensajes solo para indicar a los usuarios que escriban algo o haga clic en los botones.</span><span class="sxs-lookup"><span data-stu-id="2b878-289">Don't use prompts just to direct users to type something or to click buttons.</span></span> <span data-ttu-id="2b878-290">Por ejemplo, no escriba el texto del mensaje que dice escriba un nombre de archivo y haga clic en enviar.</span><span class="sxs-lookup"><span data-stu-id="2b878-290">For example, don't write prompt text that says Enter a filename and then click Send.</span></span>

<span data-ttu-id="2b878-291">Cuando se utilizan mensajes:</span><span class="sxs-lookup"><span data-stu-id="2b878-291">When using prompts:</span></span>

-   <span data-ttu-id="2b878-292">Dibuje el texto del mensaje en gris en cursiva y el texto de entrada real en negro normal.</span><span class="sxs-lookup"><span data-stu-id="2b878-292">Draw the prompt text in italic gray and the actual input text in normal black.</span></span> <span data-ttu-id="2b878-293">El texto del mensaje no se debe confundir con el texto real.</span><span class="sxs-lookup"><span data-stu-id="2b878-293">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="2b878-294">Mantenga el texto del mensaje conciso.</span><span class="sxs-lookup"><span data-stu-id="2b878-294">Keep the prompt text concise.</span></span> <span data-ttu-id="2b878-295">Puede usar fragmentos en lugar de oraciones completas.</span><span class="sxs-lookup"><span data-stu-id="2b878-295">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="2b878-296">Use mayúsculas de estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="2b878-296">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="2b878-297">No use signos de puntuación o puntos suspensivos de finalización.</span><span class="sxs-lookup"><span data-stu-id="2b878-297">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="2b878-298">El texto del mensaje no se debe editar y debe desaparecer una vez que los usuarios hacen clic en o en la pestaña en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-298">The prompt text should not be editable and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="2b878-299">**Excepción:** Si el cuadro de texto tiene el foco de entrada predeterminado, se muestra el mensaje y desaparece cuando el usuario comienza a escribir.</span><span class="sxs-lookup"><span data-stu-id="2b878-299">**Exception:** If the text box has default input focus, the prompt is displayed, and it disappears once the user starts typing.</span></span>
-   <span data-ttu-id="2b878-300">El texto del mensaje se restaura si el cuadro de texto todavía está vacío cuando pierde el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b878-300">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="2b878-301">Ajuste de tamaño y espaciado recomendados</span><span class="sxs-lookup"><span data-stu-id="2b878-301">Recommended sizing and spacing</span></span>

![<span data-ttu-id="2b878-302">figura de cuadros de texto de una línea y dos líneas</span><span class="sxs-lookup"><span data-stu-id="2b878-302">figure of one-line and two-line text boxes</span></span> ](images/ctrl-text-boxes-image25.png)

<span data-ttu-id="2b878-303">Ajuste de tamaño y espaciado recomendados para los cuadros de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-303">Recommended sizing and spacing for text boxes.</span></span>

<span data-ttu-id="2b878-304">El ancho de un cuadro de texto es una pista visual del tamaño de entrada esperado.</span><span class="sxs-lookup"><span data-stu-id="2b878-304">The width of a text box is a visual clue of the expected input size.</span></span> <span data-ttu-id="2b878-305">Al ajustar el tamaño de los cuadros de texto:</span><span class="sxs-lookup"><span data-stu-id="2b878-305">When sizing text boxes:</span></span>

-   <span data-ttu-id="2b878-306">**Elija un ancho adecuado para los datos válidos más largos.**</span><span class="sxs-lookup"><span data-stu-id="2b878-306">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="2b878-307">En la mayoría de los casos, los usuarios no deberían tener que desplazarse por la cadena más larga probable que escriban o vean.</span><span class="sxs-lookup"><span data-stu-id="2b878-307">In most situations, users shouldn't have to scroll the longest likely string they'll enter or view.</span></span>
-   <span data-ttu-id="2b878-308">**Incluya un 30% adicional** (hasta el 200 por ciento para el texto más corto) para cualquier texto (pero no para los números) que se traducirá.</span><span class="sxs-lookup"><span data-stu-id="2b878-308">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="2b878-309">**Si la entrada esperada no tiene un tamaño determinado, elija un ancho que sea coherente con los demás cuadros de texto o controles de la ventana.**</span><span class="sxs-lookup"><span data-stu-id="2b878-309">**If the expected input has no particular size, choose a width that is consistent with the other text boxes or controls on the window.**</span></span>
-   <span data-ttu-id="2b878-310">**Cambiar el tamaño de los cuadros de texto multilínea para mostrar un número entero de líneas de texto.**</span><span class="sxs-lookup"><span data-stu-id="2b878-310">**Size multi-line text boxes to display an integral number of lines of text.**</span></span>

## <a name="labels"></a><span data-ttu-id="2b878-311">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="2b878-311">Labels</span></span>

### <a name="text-box-labels"></a><span data-ttu-id="2b878-312">Etiquetas de cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-312">Text box labels</span></span>

-   <span data-ttu-id="2b878-313">Todos los cuadros de texto necesitan etiquetas.</span><span class="sxs-lookup"><span data-stu-id="2b878-313">All text boxes need labels.</span></span> <span data-ttu-id="2b878-314">Escriba la etiqueta como una palabra o frase, no como una frase, terminando con dos puntos y usando [texto estático](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="2b878-314">Write the label as a word or phrase, not as a sentence, ending with a colon, and using [static text](glossary.md).</span></span>

    <span data-ttu-id="2b878-315">**Excepciones:**</span><span class="sxs-lookup"><span data-stu-id="2b878-315">**Exceptions:**</span></span>

    -   <span data-ttu-id="2b878-316">Cuadros de texto con mensajes donde el espacio es Premium.</span><span class="sxs-lookup"><span data-stu-id="2b878-316">Text boxes with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="2b878-317">Para el etiquetado, un grupo de cuadros de texto utilizados para la **entrada de datos con formato** se debe tratar como un solo cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-317">For labeling, a group of text boxes used for **formatted data input** should be treated as a single text box.</span></span>
    -   <span data-ttu-id="2b878-318">Si un cuadro de texto está subordinado a un botón de radio o casilla, y se introduce por la etiqueta que termina con un signo de dos puntos, no incluya una etiqueta adicional en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-318">If a text box is subordinate to a radio button or check box, and is introduced by its label ending with a colon, don't put an additional label on the text box.</span></span>
    -   <span data-ttu-id="2b878-319">**Omita las etiquetas de control que representen la instrucción principal.**</span><span class="sxs-lookup"><span data-stu-id="2b878-319">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="2b878-320">En este caso, la instrucción principal toma el signo de dos puntos (a menos que sea una pregunta) y una clave de acceso.</span><span class="sxs-lookup"><span data-stu-id="2b878-320">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

        <span data-ttu-id="2b878-321">**Aceptable:**</span><span class="sxs-lookup"><span data-stu-id="2b878-321">**Acceptable:**</span></span>

        ![captura de pantalla de un cuadro de texto con la etiqueta redundante resulta](images/ctrl-text-boxes-image26.png)

        <span data-ttu-id="2b878-323">En este ejemplo, la etiqueta del cuadro de texto es simplemente una resituación de la instrucción principal.</span><span class="sxs-lookup"><span data-stu-id="2b878-323">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="2b878-324">**Manera**</span><span class="sxs-lookup"><span data-stu-id="2b878-324">**Better:**</span></span>

        ![<span data-ttu-id="2b878-325">captura de pantalla del cuadro de texto con la instrucción principal únicamente</span><span class="sxs-lookup"><span data-stu-id="2b878-325">screen shot of text box with main instruction only</span></span> ](images/ctrl-text-boxes-image27.png)

        <span data-ttu-id="2b878-326">En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma el signo de dos puntos y la tecla de acceso.</span><span class="sxs-lookup"><span data-stu-id="2b878-326">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="2b878-327">Asigne una clave de acceso única.</span><span class="sxs-lookup"><span data-stu-id="2b878-327">Assign a unique access key.</span></span> <span data-ttu-id="2b878-328">Para obtener instrucciones de asignación de claves de acceso, consulte [teclado](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="2b878-328">For access key assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="2b878-329">Use mayúsculas de estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="2b878-329">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="2b878-330">Coloque la etiqueta a la izquierda o encima del cuadro de texto y alinee la etiqueta con el borde izquierdo del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-330">Position the label either to the left of or above the text box, and align the label with the left edge of the text box.</span></span> <span data-ttu-id="2b878-331">Si la etiqueta está a la izquierda, alinee verticalmente el texto de la etiqueta con el texto del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-331">If the label is on the left, vertically align the label text with the text box text.</span></span>

    <span data-ttu-id="2b878-332">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-332">**Correct:**</span></span>

    ![<span data-ttu-id="2b878-333">captura de pantalla de la etiqueta alineada a la izquierda sobre el cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-333">screen shot of left-aligned label above text box</span></span> ](images/ctrl-text-boxes-image28.png)

    ![<span data-ttu-id="2b878-334">captura de pantalla de la etiqueta alineada de texto a la izquierda del cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-334">screen shot of text-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image29.png)

    <span data-ttu-id="2b878-335">En estos ejemplos, la etiqueta en la parte superior se alinea con el borde izquierdo del cuadro de texto y la etiqueta de la izquierda se alinea con el texto del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-335">In these examples, the label on top aligns with the left edge of the text box, and the label on the left aligns with the text in the text box.</span></span>

    <span data-ttu-id="2b878-336">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-336">**Incorrect:**</span></span>

    ![<span data-ttu-id="2b878-337">captura de pantalla de la etiqueta alineada de texto sobre el cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-337">screen shot of text-aligned label above text box</span></span> ](images/ctrl-text-boxes-image30.png)

    ![<span data-ttu-id="2b878-338">captura de pantalla de la etiqueta alineada en la parte izquierda del cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-338">screen shot of top-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image31.png)

    <span data-ttu-id="2b878-339">En estos ejemplos incorrectos, la etiqueta en la parte superior se alinea con el texto del cuadro de texto y la etiqueta de la izquierda se alinea con la parte superior del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-339">In these incorrect examples, the label on top aligns with the text in the text box, and the label on the left aligns with the top of the text box.</span></span>

-   <span data-ttu-id="2b878-340">Puede especificar unidades (por ejemplo, segundos o conexiones) entre paréntesis después de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2b878-340">You may specify units (for example, seconds or connections) in parentheses after the label.</span></span>
-   <span data-ttu-id="2b878-341">Si un cuadro de texto acepta un número máximo de caracteres arbitrariamente pequeño, puede indicar la entrada máxima en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2b878-341">If a text box accepts an arbitrarily small maximum number of characters, you can state the maximum input in the label.</span></span> <span data-ttu-id="2b878-342">El ancho del cuadro de texto también debe sugerir el tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="2b878-342">The text box width should also suggest the maximum size.</span></span>

    ![<span data-ttu-id="2b878-343">captura de pantalla del cuadro de texto de contraseña</span><span class="sxs-lookup"><span data-stu-id="2b878-343">screen shot of password text box</span></span> ](images/ctrl-text-boxes-image32.png)

    <span data-ttu-id="2b878-344">En este ejemplo, la etiqueta proporciona el número máximo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2b878-344">In this example, the label gives the maximum number of characters.</span></span>

-   <span data-ttu-id="2b878-345">No haga que el contenido del cuadro de texto (o su etiqueta de unidades) forme parte de una frase, ya que no es localizable.</span><span class="sxs-lookup"><span data-stu-id="2b878-345">Don't make the content of the text box (or its units label) part of a sentence, because this is not localizable.</span></span>
-   <span data-ttu-id="2b878-346">Si el cuadro de texto se puede usar para escribir varios elementos, deje claro cómo debe separar los elementos de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2b878-346">If the text box can be used to enter several items, make it clear how to separate the items in the label.</span></span>

    ![<span data-ttu-id="2b878-347">captura de pantalla de nombres independientes de etiqueta con punto y coma</span><span class="sxs-lookup"><span data-stu-id="2b878-347">screen shot of label separate names with semicolon</span></span> ](images/ctrl-text-boxes-image33.png)

    <span data-ttu-id="2b878-348">En este ejemplo, el separador de elementos se proporciona en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2b878-348">In this example, the item separator is given in the label.</span></span>

-   <span data-ttu-id="2b878-349">Para obtener instrucciones sobre cómo indicar la entrada necesaria, consulte la entrada necesaria en los [cuadros de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="2b878-349">For guidelines on indicating required input, see Required input in [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="instruction-labels"></a><span data-ttu-id="2b878-350">Etiquetas de instrucción</span><span class="sxs-lookup"><span data-stu-id="2b878-350">Instruction labels</span></span>

-   <span data-ttu-id="2b878-351">Si necesita agregar texto informativo sobre un cuadro de texto, agréguelo encima de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2b878-351">If you need to add instructional text about a text box, add it above the label.</span></span> <span data-ttu-id="2b878-352">Use frases completas con una puntuación final.</span><span class="sxs-lookup"><span data-stu-id="2b878-352">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="2b878-353">Use mayúsculas de estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="2b878-353">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="2b878-354">La información adicional que sea útil pero no necesaria debe mantenerse en breve.</span><span class="sxs-lookup"><span data-stu-id="2b878-354">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="2b878-355">Coloque esta información entre paréntesis entre la etiqueta y el signo de dos puntos, o sin paréntesis debajo del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-355">Place this information either in parentheses between the label and colon, or without parentheses below the text box.</span></span>

    ![<span data-ttu-id="2b878-356">captura de pantalla de la información agregada debajo del cuadro de texto</span><span class="sxs-lookup"><span data-stu-id="2b878-356">screen shot of added information below text box</span></span> ](images/ctrl-text-boxes-image34.png)

    <span data-ttu-id="2b878-357">En este ejemplo, se coloca información adicional debajo del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-357">In this example, additional information is placed below the text box.</span></span>

### <a name="prompt-labels"></a><span data-ttu-id="2b878-358">Etiquetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="2b878-358">Prompt labels</span></span>

-   <span data-ttu-id="2b878-359">Mantenga el texto del mensaje conciso.</span><span class="sxs-lookup"><span data-stu-id="2b878-359">Keep the prompt text concise.</span></span> <span data-ttu-id="2b878-360">Puede usar fragmentos en lugar de oraciones completas.</span><span class="sxs-lookup"><span data-stu-id="2b878-360">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="2b878-361">Use mayúsculas de estilo de frase.</span><span class="sxs-lookup"><span data-stu-id="2b878-361">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="2b878-362">No use signos de puntuación o puntos suspensivos de finalización.</span><span class="sxs-lookup"><span data-stu-id="2b878-362">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="2b878-363">Si el símbolo del sistema indica a los usuarios que escriban información sobre la que se actuará con un botón situado junto al cuadro de texto, simplemente coloque el botón junto al cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2b878-363">If the prompt directs users to enter information that will be acted upon by a button next to the text box, simply place the button next to the text box.</span></span> <span data-ttu-id="2b878-364">No utilice el símbolo del sistema para indicar a los usuarios que haga clic en el botón (por ejemplo, no escriba el texto del mensaje que dice, arrastre un archivo y, a continuación, haga clic en enviar).</span><span class="sxs-lookup"><span data-stu-id="2b878-364">Don't use the prompt to direct users to click the button (for example, don't write prompt text that says, Drag a file and then click Send).</span></span>

## <a name="documentation"></a><span data-ttu-id="2b878-365">Documentación</span><span class="sxs-lookup"><span data-stu-id="2b878-365">Documentation</span></span>

<span data-ttu-id="2b878-366">Al hacer referencia a los cuadros de texto:</span><span class="sxs-lookup"><span data-stu-id="2b878-366">When referring to text boxes:</span></span>

-   <span data-ttu-id="2b878-367">Use Type para hacer referencia a interacciones de usuario que requieren escribir o pegar; de lo contrario, use entrar si los usuarios pueden colocar información en el cuadro de texto mediante otros medios, como seleccionar el valor de una lista o utilizar un botón examinar.</span><span class="sxs-lookup"><span data-stu-id="2b878-367">Use type to refer to user interactions that require typing or pasting; otherwise use enter if users can put information into the text box using other means, such as selecting the value from a list or using a Browse button.</span></span>
-   <span data-ttu-id="2b878-368">Use SELECT para hacer referencia a una entrada en un cuadro de texto de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2b878-368">Use select to refer to an entry in a read-only text box.</span></span>
-   <span data-ttu-id="2b878-369">Use el texto exacto de la etiqueta, incluido el uso de mayúsculas, e incluya el cuadro palabra.</span><span class="sxs-lookup"><span data-stu-id="2b878-369">Use the exact label text, including its capitalization, and include the word box.</span></span> <span data-ttu-id="2b878-370">No incluya el carácter de subrayado o el signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="2b878-370">Don't include the access key underscore or colon.</span></span> <span data-ttu-id="2b878-371">No haga referencia a un cuadro de texto como un cuadro de texto o un campo.</span><span class="sxs-lookup"><span data-stu-id="2b878-371">Don't refer to a text box as a text box or a field.</span></span>
-   <span data-ttu-id="2b878-372">Siempre que sea posible, dé formato a la etiqueta usando texto en negrita.</span><span class="sxs-lookup"><span data-stu-id="2b878-372">When possible, format the label using bold text.</span></span> <span data-ttu-id="2b878-373">De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.</span><span class="sxs-lookup"><span data-stu-id="2b878-373">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="2b878-374">Ejemplo: escriba la contraseña en el cuadro **contraseña** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2b878-374">Example: Type your password into the **Password** box, and then click **OK**.</span></span>

-   <span data-ttu-id="2b878-375">Si el cuadro de texto requiere un formato específico, documente solo el formato aceptable que se usa con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="2b878-375">If the text box requires a specific format, document only the most commonly used acceptable format.</span></span> <span data-ttu-id="2b878-376">Permita a los usuarios detectar otros formatos por su cuenta.</span><span class="sxs-lookup"><span data-stu-id="2b878-376">Let users discover any other formats on their own.</span></span> <span data-ttu-id="2b878-377">Quiere ser flexible con formatos de datos, pero si lo hace, no debería producirse una documentación compleja.</span><span class="sxs-lookup"><span data-stu-id="2b878-377">You want to be flexible with data formats, but doing so should not result in complex documentation.</span></span>

    <span data-ttu-id="2b878-378">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-378">**Correct:**</span></span>

    <span data-ttu-id="2b878-379">Escriba el número de serie del elemento con el formato 1234-56-7890.</span><span class="sxs-lookup"><span data-stu-id="2b878-379">Enter the part's serial number using the 1234-56-7890 format.</span></span>

    <span data-ttu-id="2b878-380">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="2b878-380">**Incorrect:**</span></span>

    <span data-ttu-id="2b878-381">Escriba el número de serie del elemento con cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="2b878-381">Enter the part's serial number using any of the following formats:</span></span>

    <span data-ttu-id="2b878-382">1234567890</span><span class="sxs-lookup"><span data-stu-id="2b878-382">1234567890</span></span>

    <span data-ttu-id="2b878-383">1234-56-7890</span><span class="sxs-lookup"><span data-stu-id="2b878-383">1234-56-7890</span></span>

    <span data-ttu-id="2b878-384">1234 56 7890</span><span class="sxs-lookup"><span data-stu-id="2b878-384">1234 56 7890</span></span>

