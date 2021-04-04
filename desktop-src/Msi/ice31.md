---
description: ICE31 valida los estilos de fuente predefinidos que se usan en los controles que muestran texto. También valida que la propiedad DefaultUIFont hace referencia a un estilo de fuente válido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277548"
---
# <a name="ice31"></a><span data-ttu-id="82e32-104">ICE31</span><span class="sxs-lookup"><span data-stu-id="82e32-104">ICE31</span></span>

<span data-ttu-id="82e32-105">ICE31 valida los estilos de fuente predefinidos que se usan en [los controles](controls.md) que muestran texto.</span><span class="sxs-lookup"><span data-stu-id="82e32-105">ICE31 validates any predefined font styles used in [controls](controls.md) that display text.</span></span> <span data-ttu-id="82e32-106">También valida que la propiedad [**DefaultUIFont**](defaultuifont.md) hace referencia a un estilo de fuente válido.</span><span class="sxs-lookup"><span data-stu-id="82e32-106">It also validates that the [**DefaultUIFont**](defaultuifont.md) property refers to a valid font style.</span></span>

<span data-ttu-id="82e32-107">Los controles pueden tener un estilo de fuente predefinido, tal y como se describe en [Agregar controles y texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="82e32-107">Controls can have a predefined font style as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="82e32-108">Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&*Style*}.</span><span class="sxs-lookup"><span data-stu-id="82e32-108">To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&*style*}.</span></span> <span data-ttu-id="82e32-109">Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="82e32-109">Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="82e32-110">Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente.</span><span class="sxs-lookup"><span data-stu-id="82e32-110">If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.</span></span>

<span data-ttu-id="82e32-111">ICE31 comprueba la columna de texto de cada control de la [tabla de control](control-table.md) para comprobar que existe una entrada válida en la [tabla TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="82e32-111">ICE31 checks the Text column for each control in the [Control Table](control-table.md) to verifies that a valid entry exist in the [TextStyle table](textstyle-table.md).</span></span>

<span data-ttu-id="82e32-112">ICE31 omite el [control ScrollableText](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="82e32-112">ICE31 ignores the [ScrollableText Control](scrollabletext-control.md).</span></span>

## <a name="results"></a><span data-ttu-id="82e32-113">Results</span><span class="sxs-lookup"><span data-stu-id="82e32-113">Results</span></span>

<span data-ttu-id="82e32-114">ICE31 expone un mensaje de error para estilos no definidos, nombres de estilo que son demasiado largos, una tabla de TextStyle que falta y etiquetas de estilo sin llave de cierre.</span><span class="sxs-lookup"><span data-stu-id="82e32-114">ICE31 posts an error message for undefined styles, style names that are too long, a missing TextStyle table, and style tags with no closing brace.</span></span>

<span data-ttu-id="82e32-115">ICE31 expone una advertencia si la etiqueta de estilo no está al principio de la línea o si un control tiene varias etiquetas de estilo.</span><span class="sxs-lookup"><span data-stu-id="82e32-115">ICE31 posts a warning if the style tag is not at the beginning of the line, or if a control has multiple style tags.</span></span>

## <a name="example"></a><span data-ttu-id="82e32-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82e32-116">Example</span></span>

<span data-ttu-id="82e32-117">ICE31 expone los siguientes errores para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="82e32-117">ICE31 posts the following errors for the example shown:</span></span>

-   <span data-ttu-id="82e32-118">El control DialogB. Control1 usa BadStyle de TextStyle sin definir.</span><span class="sxs-lookup"><span data-stu-id="82e32-118">Control DialogB.Control1 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="82e32-119">El control DialogB. Control2 usa BadStyle de TextStyle sin definir.</span><span class="sxs-lookup"><span data-stu-id="82e32-119">Control DialogB.Control2 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="82e32-120">El control DialogB. Control6 no tiene llave de cierre en el estilo de texto.</span><span class="sxs-lookup"><span data-stu-id="82e32-120">Control DialogB.Control6 is missing closing brace in text style.</span></span>
-   <span data-ttu-id="82e32-121">El control DialogB. Control3 especifica un estilo de texto que es demasiado largo para ser válido.</span><span class="sxs-lookup"><span data-stu-id="82e32-121">Control DialogB.Control3 specifies a text style that is too long to be valid.</span></span>

<span data-ttu-id="82e32-122">ICE31 envía la siguiente advertencia para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="82e32-122">ICE31 posts the following warning for the example shown:</span></span>

-   <span data-ttu-id="82e32-123">La etiqueta de estilo de texto de DialogB. Control4 no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="82e32-123">Text Style tag in DialogB.Control4 has no effect.</span></span> <span data-ttu-id="82e32-124">¿Realmente desea que aparezca como texto?</span><span class="sxs-lookup"><span data-stu-id="82e32-124">Do you really want it to appear as text?</span></span>

<span data-ttu-id="82e32-125">[Tabla de control](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="82e32-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="82e32-126">Diálogo</span><span class="sxs-lookup"><span data-stu-id="82e32-126">Dialog</span></span>  | <span data-ttu-id="82e32-127">Control</span><span class="sxs-lookup"><span data-stu-id="82e32-127">Control</span></span>  | <span data-ttu-id="82e32-128">Texto</span><span class="sxs-lookup"><span data-stu-id="82e32-128">Text</span></span>                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e32-129">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="82e32-129">DialogA</span></span> | <span data-ttu-id="82e32-130">Control0</span><span class="sxs-lookup"><span data-stu-id="82e32-130">Control0</span></span> | <span data-ttu-id="82e32-131">{ \\ OKStyle} este es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-131">{\\OKStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="82e32-132">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="82e32-132">DialogA</span></span> | <span data-ttu-id="82e32-133">Control1</span><span class="sxs-lookup"><span data-stu-id="82e32-133">Control1</span></span> | <span data-ttu-id="82e32-134">{&OKStyle} Este es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-134">{&OKStyle}This is the text to display.</span></span>                                                                                                                              |
| <span data-ttu-id="82e32-135">DialogB</span><span class="sxs-lookup"><span data-stu-id="82e32-135">DialogB</span></span> | <span data-ttu-id="82e32-136">Control1</span><span class="sxs-lookup"><span data-stu-id="82e32-136">Control1</span></span> | <span data-ttu-id="82e32-137">{&BadStyle} Este es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-137">{&BadStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="82e32-138">DialogB</span><span class="sxs-lookup"><span data-stu-id="82e32-138">DialogB</span></span> | <span data-ttu-id="82e32-139">Control2</span><span class="sxs-lookup"><span data-stu-id="82e32-139">Control2</span></span> | <span data-ttu-id="82e32-140">{ \\ BadStyle} este es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-140">{\\BadStyle}This is the text to display.</span></span>                                                                                                                            |
| <span data-ttu-id="82e32-141">DialogB</span><span class="sxs-lookup"><span data-stu-id="82e32-141">DialogB</span></span> | <span data-ttu-id="82e32-142">Control3</span><span class="sxs-lookup"><span data-stu-id="82e32-142">Control3</span></span> | <span data-ttu-id="82e32-143">{&estilo que está por encima de 72 caracteres y, por lo tanto, no puede ser un estilo aunque de algún modo se hubiera administrado para obtenerlo en la tabla de TextStyle} Este es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-143">{&Style that is over 72 chars and therefore cannot possibly be a style even if somehow you did manage to get it in the TextStyle table}This is the text to display.</span></span> |
| <span data-ttu-id="82e32-144">DialogB</span><span class="sxs-lookup"><span data-stu-id="82e32-144">DialogB</span></span> | <span data-ttu-id="82e32-145">Control4</span><span class="sxs-lookup"><span data-stu-id="82e32-145">Control4</span></span> | <span data-ttu-id="82e32-146">ADVERTENCIA { \\ OKStyle} este es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-146">Warning {\\OKStyle}This is the text to display.</span></span>                                                                                                                     |
| <span data-ttu-id="82e32-147">DialogB</span><span class="sxs-lookup"><span data-stu-id="82e32-147">DialogB</span></span> | <span data-ttu-id="82e32-148">Control5</span><span class="sxs-lookup"><span data-stu-id="82e32-148">Control5</span></span> | <span data-ttu-id="82e32-149">{ \\ OKStyle} {&OKStyle} este es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-149">{\\OKStyle}{&OKStyle}This is the text to display.</span></span>                                                                                                                   |
| <span data-ttu-id="82e32-150">DialogB</span><span class="sxs-lookup"><span data-stu-id="82e32-150">DialogB</span></span> | <span data-ttu-id="82e32-151">Control6</span><span class="sxs-lookup"><span data-stu-id="82e32-151">Control6</span></span> | <span data-ttu-id="82e32-152">{ \\ OKStyle es el texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="82e32-152">{\\OKStyle This is the text to display.</span></span>                                                                                                                             |



 

<span data-ttu-id="82e32-153">[Tabla TextStyle](textstyle-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="82e32-153">[TextStyle table](textstyle-table.md) (partial)</span></span>



| <span data-ttu-id="82e32-154">Estilo]</span><span class="sxs-lookup"><span data-stu-id="82e32-154">TextStyle</span></span> |
|-----------|
| <span data-ttu-id="82e32-155">OkStyle</span><span class="sxs-lookup"><span data-stu-id="82e32-155">OkStyle</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="82e32-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82e32-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e32-157">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="82e32-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



