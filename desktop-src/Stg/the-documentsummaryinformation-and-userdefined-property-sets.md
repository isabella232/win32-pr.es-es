---
title: Los conjuntos de propiedades DocumentSummaryInformation y UserDefined
description: Un conjunto de propiedades DocumentSummaryInformation y UserDefined es una extensión del conjunto de propiedades de información de resumen. Ambos conjuntos de propiedades pueden existir simultáneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Conjuntos de propiedades UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532104"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a><span data-ttu-id="af477-106">Los conjuntos de propiedades DocumentSummaryInformation y UserDefined</span><span class="sxs-lookup"><span data-stu-id="af477-106">The DocumentSummaryInformation and UserDefined Property Sets</span></span>

<span data-ttu-id="af477-107">Un conjunto de propiedades **DocumentSummaryInformation** y **UserDefined** es una extensión [del conjunto de propiedades de información de Resumen](the-summary-information-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="af477-107">A **DocumentSummaryInformation** and **UserDefined** property set is an extension to [the Summary Information property set](the-summary-information-property-set.md).</span></span> <span data-ttu-id="af477-108">Ambos conjuntos de propiedades pueden existir simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="af477-108">Both property sets can exist simultaneously.</span></span>

<span data-ttu-id="af477-109">El nombre de la secuencia que contiene el conjunto de propiedades **DocumentSummaryInformation** es **" \\ 005DocumentSummaryInformation"**.</span><span class="sxs-lookup"><span data-stu-id="af477-109">The name of the stream that contains the **DocumentSummaryInformation** property set is **"\\005DocumentSummaryInformation"**.</span></span> <span data-ttu-id="af477-110">El identificador de formato (FMTID) del conjunto de propiedades **DocumentSummaryInformation** es **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="af477-110">The format identifier (FMTID) for the **DocumentSummaryInformation** property set is **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="af477-111">La declaración para este valor está disponible en los archivos de encabezado proporcionados como **FMTID \_ DocSummaryInformation**.</span><span class="sxs-lookup"><span data-stu-id="af477-111">The declaration for this value is available in the provided header files as **FMTID\_DocSummaryInformation**.</span></span> <span data-ttu-id="af477-112">Para obtener más información, vea [nombres en IStorage](names-in-istorage.md), [el conjunto de propiedades de información de Resumen](the-summary-information-property-set.md), [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) y [Format Identifiers](format-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="af477-112">For more information, see [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).</span></span>

<span data-ttu-id="af477-113">Esta secuencia también tiene una sección independiente para las propiedades personalizadas definidas por el usuario como en los conjuntos de propiedades **DocumentSummaryInformation** y **UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="af477-113">This stream also has a separate section for the custom-user-defined properties as in the **DocumentSummaryInformation** and **UserDefined** property sets.</span></span> <span data-ttu-id="af477-114">Esta sección aparece en la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) como un conjunto de propiedades independiente, con el siguiente FMTID (disponible como **FMTID \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="af477-114">This section appears in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface as a separate property set, with the following FMTID (available as **FMTID\_UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="af477-115">Estos dos conjuntos de propiedades son los únicos para los que una sola secuencia puede contener varios conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="af477-115">These two property sets are the only ones for which a single stream can hold multiple property sets.</span></span> <span data-ttu-id="af477-116">El hecho de que estos dos conjuntos de propiedades se encuentren en un solo flujo afecta al comportamiento de la interfaz **IPropertySetStorage** .</span><span class="sxs-lookup"><span data-stu-id="af477-116">The fact that these two property sets are in a single stream affects the behavior of the **IPropertySetStorage** interface.</span></span> <span data-ttu-id="af477-117">Para obtener más información, vea [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span><span class="sxs-lookup"><span data-stu-id="af477-117">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

<span data-ttu-id="af477-118">En la tabla siguiente se enumeran las propiedades agregadas al conjunto de propiedades **DocumentSummaryInformation** y **UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="af477-118">The following table lists the added properties to the **DocumentSummaryInformation** and **UserDefined** property set.</span></span> <span data-ttu-id="af477-119">Como en el conjunto de propiedades **SummaryInformation** , los nombres normalmente no se almacenan en el conjunto de propiedades, pero se deducen a partir del identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="af477-119">As in the **SummaryInformation** property set, the names are not typically stored in the property set, but are inferred from the property identifier.</span></span>



| <span data-ttu-id="af477-120">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="af477-120">Property name</span></span>      | <span data-ttu-id="af477-121">Identificador de la propiedad</span><span class="sxs-lookup"><span data-stu-id="af477-121">Property identifier</span></span>     | <span data-ttu-id="af477-122">Valor del identificador de propiedad</span><span class="sxs-lookup"><span data-stu-id="af477-122">Property identifier value</span></span> | <span data-ttu-id="af477-123">Tipo VARIANT</span><span class="sxs-lookup"><span data-stu-id="af477-123">VARIANT type</span></span>                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| <span data-ttu-id="af477-124">Category</span><span class="sxs-lookup"><span data-stu-id="af477-124">Category</span></span>           | <span data-ttu-id="af477-125">**\_categoría PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="af477-125">**PIDDSI\_CATEGORY**</span></span>    | <span data-ttu-id="af477-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="af477-126">0x00000002</span></span>                | <span data-ttu-id="af477-127">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="af477-127">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="af477-128">PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="af477-128">PresentationTarget</span></span> | <span data-ttu-id="af477-129">**PIDDSI \_ PRESFORMAT**</span><span class="sxs-lookup"><span data-stu-id="af477-129">**PIDDSI\_PRESFORMAT**</span></span>  | <span data-ttu-id="af477-130">0x00000003</span><span class="sxs-lookup"><span data-stu-id="af477-130">0x00000003</span></span>                | <span data-ttu-id="af477-131">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="af477-131">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="af477-132">Bytes</span><span class="sxs-lookup"><span data-stu-id="af477-132">Bytes</span></span>              | <span data-ttu-id="af477-133">**PIDDSI \_ BYTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="af477-133">**PIDDSI\_BYTECOUNT**</span></span>   | <span data-ttu-id="af477-134">0x00000004</span><span class="sxs-lookup"><span data-stu-id="af477-134">0x00000004</span></span>                | <span data-ttu-id="af477-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="af477-135">**VT\_I4**</span></span>                        |
| <span data-ttu-id="af477-136">Líneas</span><span class="sxs-lookup"><span data-stu-id="af477-136">Lines</span></span>              | <span data-ttu-id="af477-137">**PIDDSI \_ LINECOUNT**</span><span class="sxs-lookup"><span data-stu-id="af477-137">**PIDDSI\_LINECOUNT**</span></span>   | <span data-ttu-id="af477-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="af477-138">0x00000005</span></span>                | <span data-ttu-id="af477-139">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="af477-139">**VT\_I4**</span></span>                        |
| <span data-ttu-id="af477-140">Párrafos</span><span class="sxs-lookup"><span data-stu-id="af477-140">Paragraphs</span></span>         | <span data-ttu-id="af477-141">**PIDDSI \_ PARCOUNT**</span><span class="sxs-lookup"><span data-stu-id="af477-141">**PIDDSI\_PARCOUNT**</span></span>    | <span data-ttu-id="af477-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="af477-142">0x00000006</span></span>                | <span data-ttu-id="af477-143">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="af477-143">**VT\_I4**</span></span>                        |
| <span data-ttu-id="af477-144">Diapositivas</span><span class="sxs-lookup"><span data-stu-id="af477-144">Slides</span></span>             | <span data-ttu-id="af477-145">**PIDDSI \_ SLIDECOUNT**</span><span class="sxs-lookup"><span data-stu-id="af477-145">**PIDDSI\_SLIDECOUNT**</span></span>  | <span data-ttu-id="af477-146">0x00000007</span><span class="sxs-lookup"><span data-stu-id="af477-146">0x00000007</span></span>                | <span data-ttu-id="af477-147">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="af477-147">**VT\_I4**</span></span>                        |
| <span data-ttu-id="af477-148">Notas</span><span class="sxs-lookup"><span data-stu-id="af477-148">Notes</span></span>              | <span data-ttu-id="af477-149">**PIDDSI \_ NOTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="af477-149">**PIDDSI\_NOTECOUNT**</span></span>   | <span data-ttu-id="af477-150">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af477-150">0x00000008</span></span>                | <span data-ttu-id="af477-151">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="af477-151">**VT\_I4**</span></span>                        |
| <span data-ttu-id="af477-152">HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="af477-152">HiddenSlides</span></span>       | <span data-ttu-id="af477-153">**PIDDSI \_ HIDDENCOUNT**</span><span class="sxs-lookup"><span data-stu-id="af477-153">**PIDDSI\_HIDDENCOUNT**</span></span> | <span data-ttu-id="af477-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="af477-154">0x00000009</span></span>                | <span data-ttu-id="af477-155">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="af477-155">**VT\_I4**</span></span>                        |
| <span data-ttu-id="af477-156">MMClips</span><span class="sxs-lookup"><span data-stu-id="af477-156">MMClips</span></span>            | <span data-ttu-id="af477-157">**PIDDSI \_ MMCLIPCOUNT**</span><span class="sxs-lookup"><span data-stu-id="af477-157">**PIDDSI\_MMCLIPCOUNT**</span></span> | <span data-ttu-id="af477-158">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="af477-158">0x0000000A</span></span>                | <span data-ttu-id="af477-159">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="af477-159">**VT\_I4**</span></span>                        |
| <span data-ttu-id="af477-160">ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="af477-160">ScaleCrop</span></span>          | <span data-ttu-id="af477-161">**\_escala PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="af477-161">**PIDDSI\_SCALE**</span></span>       | <span data-ttu-id="af477-162">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="af477-162">0x0000000B</span></span>                | <span data-ttu-id="af477-163">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="af477-163">**VT\_BOOL**</span></span>                      |
| <span data-ttu-id="af477-164">HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="af477-164">HeadingPairs</span></span>       | <span data-ttu-id="af477-165">**PIDDSI \_ HEADINGPAIR**</span><span class="sxs-lookup"><span data-stu-id="af477-165">**PIDDSI\_HEADINGPAIR**</span></span> | <span data-ttu-id="af477-166">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="af477-166">0x0000000C</span></span>                | <span data-ttu-id="af477-167">**VT \_** \| **\_ Vector** de variante VT</span><span class="sxs-lookup"><span data-stu-id="af477-167">**VT\_VARIANT** \| **VT\_VECTOR**</span></span> |
| <span data-ttu-id="af477-168">TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="af477-168">TitlesofParts</span></span>      | <span data-ttu-id="af477-169">**PIDDSI \_ DOCPARTS**</span><span class="sxs-lookup"><span data-stu-id="af477-169">**PIDDSI\_DOCPARTS**</span></span>    | <span data-ttu-id="af477-170">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="af477-170">0x0000000D</span></span>                | <span data-ttu-id="af477-171">**VT \_ Vector** \| **VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="af477-171">**VT\_VECTOR** \| **VT\_LPSTR**</span></span>   |
| <span data-ttu-id="af477-172">Manager</span><span class="sxs-lookup"><span data-stu-id="af477-172">Manager</span></span>            | <span data-ttu-id="af477-173">**Administrador de PIDDSI \_**</span><span class="sxs-lookup"><span data-stu-id="af477-173">**PIDDSI\_MANAGER**</span></span>     | <span data-ttu-id="af477-174">0x0000000E</span><span class="sxs-lookup"><span data-stu-id="af477-174">0x0000000E</span></span>                | <span data-ttu-id="af477-175">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="af477-175">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="af477-176">Compañía</span><span class="sxs-lookup"><span data-stu-id="af477-176">Company</span></span>            | <span data-ttu-id="af477-177">**\_empresa PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="af477-177">**PIDDSI\_COMPANY**</span></span>     | <span data-ttu-id="af477-178">0x0000000F</span><span class="sxs-lookup"><span data-stu-id="af477-178">0x0000000F</span></span>                | <span data-ttu-id="af477-179">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="af477-179">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="af477-180">LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="af477-180">LinksUpToDate</span></span>      | <span data-ttu-id="af477-181">**PIDDSI \_ LINKSDIRTY**</span><span class="sxs-lookup"><span data-stu-id="af477-181">**PIDDSI\_LINKSDIRTY**</span></span>  | <span data-ttu-id="af477-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af477-182">0x00000010</span></span>                | <span data-ttu-id="af477-183">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="af477-183">**VT\_BOOL**</span></span>                      |



 

<span data-ttu-id="af477-184">Estas propiedades tienen los siguientes usos:</span><span class="sxs-lookup"><span data-stu-id="af477-184">These properties have the following uses:</span></span>

<dl> <dt>

<span data-ttu-id="af477-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría</span><span class="sxs-lookup"><span data-stu-id="af477-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="af477-186">Cadena de texto escrita por el usuario que indica a qué categoría pertenece el archivo (memorando, propuesta, etc.).</span><span class="sxs-lookup"><span data-stu-id="af477-186">A text string typed by the user that indicates what category the file belongs to (memo, proposal, and so on).</span></span> <span data-ttu-id="af477-187">Es útil para buscar archivos del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="af477-187">It is useful for finding files of same type.</span></span>

</dd> <dt>

<span data-ttu-id="af477-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="af477-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span></span>
</dt> <dd>

<span data-ttu-id="af477-189">Formato de destino para la presentación (35mm, impresora, vídeo, etc.).</span><span class="sxs-lookup"><span data-stu-id="af477-189">Target format for presentation (35mm, printer, video, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="af477-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span><span class="sxs-lookup"><span data-stu-id="af477-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span></span>
</dt> <dd>

<span data-ttu-id="af477-191">Número de bytes.</span><span class="sxs-lookup"><span data-stu-id="af477-191">Number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="af477-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Cuadrícula</span><span class="sxs-lookup"><span data-stu-id="af477-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Lines</span></span>
</dt> <dd>

<span data-ttu-id="af477-193">Número de líneas.</span><span class="sxs-lookup"><span data-stu-id="af477-193">Number of lines.</span></span>

</dd> <dt>

<span data-ttu-id="af477-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Párrafos</span><span class="sxs-lookup"><span data-stu-id="af477-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragraphs</span></span>
</dt> <dd>

<span data-ttu-id="af477-195">Número de párrafos.</span><span class="sxs-lookup"><span data-stu-id="af477-195">Number of paragraphs.</span></span>

</dd> <dt>

<span data-ttu-id="af477-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Quedar</span><span class="sxs-lookup"><span data-stu-id="af477-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span></span>
</dt> <dd>

<span data-ttu-id="af477-197">Número de diapositivas.</span><span class="sxs-lookup"><span data-stu-id="af477-197">Number of slides.</span></span>

</dd> <dt>

<span data-ttu-id="af477-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Apunte</span><span class="sxs-lookup"><span data-stu-id="af477-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span></span>
</dt> <dd>

<span data-ttu-id="af477-199">Número de páginas que contienen notas.</span><span class="sxs-lookup"><span data-stu-id="af477-199">Number of pages that contain notes.</span></span>

</dd> <dt>

<span data-ttu-id="af477-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="af477-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span></span>
</dt> <dd>

<span data-ttu-id="af477-201">Número de diapositivas que están ocultas.</span><span class="sxs-lookup"><span data-stu-id="af477-201">Number of slides that are hidden.</span></span>

</dd> <dt>

<span data-ttu-id="af477-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span><span class="sxs-lookup"><span data-stu-id="af477-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span></span>
</dt> <dd>

<span data-ttu-id="af477-203">Número de clips de sonido o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="af477-203">Number of sound or video clips.</span></span>

</dd> <dt>

<span data-ttu-id="af477-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="af477-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span></span>
</dt> <dd>

<span data-ttu-id="af477-205">Se establece en true (-1) cuando se desea el escalado de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="af477-205">Set to True (-1) when scaling of the thumbnail is desired.</span></span> <span data-ttu-id="af477-206">Si no se establece, se desea un recorte.</span><span class="sxs-lookup"><span data-stu-id="af477-206">If not set, cropping is desired.</span></span>

</dd> <dt>

<span data-ttu-id="af477-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="af477-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span></span>
</dt> <dd>

<span data-ttu-id="af477-208">Propiedad usada internamente que indica la agrupación de diferentes partes del documento y el número de elementos de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="af477-208">Internally used property indicating the grouping of different document parts and the number of items in each group.</span></span> <span data-ttu-id="af477-209">Los títulos de las partes del documento se almacenan en la propiedad **TitlesofParts** .</span><span class="sxs-lookup"><span data-stu-id="af477-209">The titles of the document parts are stored in the **TitlesofParts** property.</span></span> <span data-ttu-id="af477-210">La propiedad **HeadingPairs** se almacena como un vector de variantes, en los pares de repetición de los valores **VT \_ LPSTR** (o **VT \_ LPWStr**) y **VT \_ I4** .</span><span class="sxs-lookup"><span data-stu-id="af477-210">The **HeadingPairs** property is stored as a vector of variants, in repeating pairs of **VT\_LPSTR** (or **VT\_LPWSTR**) and **VT\_I4** values.</span></span> <span data-ttu-id="af477-211">El valor de **VT \_ LPSTR** representa un nombre de encabezado y el valor de **VT \_ I4** indica el recuento de elementos de documento bajo ese encabezado.</span><span class="sxs-lookup"><span data-stu-id="af477-211">The **VT\_LPSTR** value represents a heading name, and the **VT\_I4** value indicates the count of document parts under that heading.</span></span>

</dd> <dt>

<span data-ttu-id="af477-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="af477-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span></span>
</dt> <dd>

<span data-ttu-id="af477-213">Nombres de los elementos del documento.</span><span class="sxs-lookup"><span data-stu-id="af477-213">Names of document parts.</span></span>

</dd> <dt>

<span data-ttu-id="af477-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span><span class="sxs-lookup"><span data-stu-id="af477-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span></span>
</dt> <dd>

<span data-ttu-id="af477-215">Administrador del proyecto.</span><span class="sxs-lookup"><span data-stu-id="af477-215">Manager of the project.</span></span>

</dd> <dt>

<span data-ttu-id="af477-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Recíproca</span><span class="sxs-lookup"><span data-stu-id="af477-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="af477-217">Nombre de la compañía.</span><span class="sxs-lookup"><span data-stu-id="af477-217">Company name.</span></span>

</dd> <dt>

<span data-ttu-id="af477-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="af477-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span></span>
</dt> <dd>

<span data-ttu-id="af477-219">Valor booleano que indica si los vínculos personalizados están obstaculizados por ruido excesivo en todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="af477-219">Boolean value to indicate whether the custom links are hampered by excessive noise, for all applications.</span></span>

> [!Note]  
> <span data-ttu-id="af477-220">Tal y como se describe en 12,3.</span><span class="sxs-lookup"><span data-stu-id="af477-220">As described in 12.3.</span></span> <span data-ttu-id="af477-221">Formato serializado para los conjuntos de propiedades de la especificación de diseño OLE 2,0, los elementos vectoriales de las propiedades **HeadingPairs** y **TitlesofParts** deben estar alineados en los límites de 32 bits en el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="af477-221">Serialized Format for Property Sets of the OLE 2.0 Design Specification, vector elements in the **HeadingPairs** and **TitlesofParts** properties should be aligned on 32 bit boundaries within the property set.</span></span> <span data-ttu-id="af477-222">Sin embargo, en los conjuntos de propiedades **DocumentSummaryInformation** y **UserDefined** , cuando la página de códigos de la propiedad establecida no es Unicode, estos elementos deben estar empaquetados.</span><span class="sxs-lookup"><span data-stu-id="af477-222">However, in the **DocumentSummaryInformation** and **UserDefined** property sets, when the code page of the property set is not Unicode, these elements must be packed.</span></span>

 

</dd> </dl>

<span data-ttu-id="af477-223">El conjunto de propiedades **UserDefined** se puede usar para contener cualquier propiedad.</span><span class="sxs-lookup"><span data-stu-id="af477-223">The **UserDefined** property set can be used to hold any properties.</span></span> <span data-ttu-id="af477-224">Normalmente, se usa para almacenar las propiedades con nombre creadas por un usuario.</span><span class="sxs-lookup"><span data-stu-id="af477-224">Typically, it is used to store named properties created by a user.</span></span>

 

 




