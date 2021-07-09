---
description: Obtenga información sobre el elemento configurable por el usuario PageInputBin. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc53d377106b95b26e694d531af2952cea98a8b1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549173"
---
# <a name="pageinputbin"></a><span data-ttu-id="33c38-105">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="33c38-105">PageInputBin</span></span>

<span data-ttu-id="33c38-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="33c38-106">This topic is not current.</span></span> <span data-ttu-id="33c38-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="33c38-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="33c38-108">Describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33c38-108">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="33c38-109">Permite la especificación de la ubicación de entrada por página.</span><span class="sxs-lookup"><span data-stu-id="33c38-109">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="33c38-110">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="33c38-110">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="33c38-111">Ambos no se deben especificar simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="33c38-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="33c38-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="33c38-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="33c38-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="33c38-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="33c38-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="33c38-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="33c38-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="33c38-115">Element Information</span></span>



| <span data-ttu-id="33c38-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="33c38-116">Name</span></span> | <span data-ttu-id="33c38-117">Valor</span><span class="sxs-lookup"><span data-stu-id="33c38-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="33c38-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="33c38-118">Element Type</span></span> <br/>   | <span data-ttu-id="33c38-119">Característica</span><span class="sxs-lookup"><span data-stu-id="33c38-119">Feature</span></span><br/> |
| <span data-ttu-id="33c38-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="33c38-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="33c38-121">Página</span><span class="sxs-lookup"><span data-stu-id="33c38-121">Page</span></span><br/>    |
| <span data-ttu-id="33c38-122">Notas</span><span class="sxs-lookup"><span data-stu-id="33c38-122">Notes</span></span> <br/>          | <span data-ttu-id="33c38-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="33c38-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="33c38-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="33c38-124">Structural Content</span></span>

<span data-ttu-id="33c38-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="33c38-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psf:_EnvelopeOptionValue_">
      <psf:Value xsi:type="xs:string">_EnvelopeOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_FeedTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_MediaCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaSizeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaTypeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_MediaPathValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_FeedFaceValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_FeedDirectionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="33c38-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="33c38-126">Structure Variables</span></span>

<span data-ttu-id="33c38-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="33c38-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="33c38-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="33c38-128">Name</span></span>                                   | <span data-ttu-id="33c38-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="33c38-129">Data type</span></span>          | <span data-ttu-id="33c38-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="33c38-130">Unit</span></span>                  | <span data-ttu-id="33c38-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="33c38-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="33c38-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="33c38-132">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33c38-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="33c38-133">\_OptionName\_</span></span><br/>              | <span data-ttu-id="33c38-134">string</span><span class="sxs-lookup"><span data-stu-id="33c38-134">string</span></span><br/>  | <span data-ttu-id="33c38-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="33c38-135">characters</span></span><br/> | <span data-ttu-id="33c38-136">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="33c38-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="33c38-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="33c38-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="33c38-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="33c38-138">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="33c38-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-139">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="33c38-140">string</span><span class="sxs-lookup"><span data-stu-id="33c38-140">string</span></span><br/>  | <span data-ttu-id="33c38-141">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-141">n/a</span></span><br/>        | <span data-ttu-id="33c38-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="33c38-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="33c38-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="33c38-143">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="33c38-144">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-144">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="33c38-145">string</span><span class="sxs-lookup"><span data-stu-id="33c38-145">string</span></span><br/>  | <span data-ttu-id="33c38-146">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-146">n/a</span></span><br/>        | <span data-ttu-id="33c38-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="33c38-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="33c38-148">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="33c38-148">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="33c38-149">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-149">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="33c38-150">string</span><span class="sxs-lookup"><span data-stu-id="33c38-150">string</span></span><br/>  | <span data-ttu-id="33c38-151">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-151">n/a</span></span><br/>        | <span data-ttu-id="33c38-152">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="33c38-152">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="33c38-153">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="33c38-153">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="33c38-154">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-154">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="33c38-155">string</span><span class="sxs-lookup"><span data-stu-id="33c38-155">string</span></span><br/>  | <span data-ttu-id="33c38-156">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-156">n/a</span></span><br/>        | <span data-ttu-id="33c38-157">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="33c38-157">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="33c38-158">Especifica el mecanismo de fuente de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="33c38-158">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="33c38-159">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-159">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="33c38-160">string</span><span class="sxs-lookup"><span data-stu-id="33c38-160">string</span></span><br/>  | <span data-ttu-id="33c38-161">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-161">n/a</span></span><br/>        | <span data-ttu-id="33c38-162">Alto, Estándar.</span><span class="sxs-lookup"><span data-stu-id="33c38-162">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="33c38-163">Especifica si el cubo es un cubo de alta capacidad (cualitativo).</span><span class="sxs-lookup"><span data-stu-id="33c38-163">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="33c38-164">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-164">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="33c38-165">string</span><span class="sxs-lookup"><span data-stu-id="33c38-165">string</span></span><br/>  | <span data-ttu-id="33c38-166">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-166">n/a</span></span><br/>        | <span data-ttu-id="33c38-167">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="33c38-167">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="33c38-168">Especifica la funcionalidad de detección automática del tamaño del medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33c38-168">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="33c38-169">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-169">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="33c38-170">string</span><span class="sxs-lookup"><span data-stu-id="33c38-170">string</span></span><br/>  | <span data-ttu-id="33c38-171">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-171">n/a</span></span><br/>        | <span data-ttu-id="33c38-172">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="33c38-172">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="33c38-173">Especifica la funcionalidad de detección automática del tipo de medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33c38-173">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="33c38-174">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-174">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="33c38-175">integer</span><span class="sxs-lookup"><span data-stu-id="33c38-175">integer</span></span><br/> | <span data-ttu-id="33c38-176">Hojas</span><span class="sxs-lookup"><span data-stu-id="33c38-176">sheets</span></span><br/>     | <span data-ttu-id="33c38-177">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33c38-177">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="33c38-178">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="33c38-178">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="33c38-179">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-179">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="33c38-180">string</span><span class="sxs-lookup"><span data-stu-id="33c38-180">string</span></span><br/>  | <span data-ttu-id="33c38-181">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-181">n/a</span></span><br/>        | <span data-ttu-id="33c38-182">Recta, Tieneine.</span><span class="sxs-lookup"><span data-stu-id="33c38-182">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="33c38-183">Especifica las características de la ruta de acceso multimedia.</span><span class="sxs-lookup"><span data-stu-id="33c38-183">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="33c38-184">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-184">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="33c38-185">string</span><span class="sxs-lookup"><span data-stu-id="33c38-185">string</span></span><br/>  | <span data-ttu-id="33c38-186">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-186">n/a</span></span><br/>        | <span data-ttu-id="33c38-187">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="33c38-187">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="33c38-188">Especifica si los medios se imprimirán de cara hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="33c38-188">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="33c38-189">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="33c38-189">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="33c38-190">string</span><span class="sxs-lookup"><span data-stu-id="33c38-190">string</span></span><br/>  | <span data-ttu-id="33c38-191">N/D</span><span class="sxs-lookup"><span data-stu-id="33c38-191">n/a</span></span><br/>        | <span data-ttu-id="33c38-192">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="33c38-192">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="33c38-193">Especifica si los medios se alimentan primero con un borde largo o con un borde corto.</span><span class="sxs-lookup"><span data-stu-id="33c38-193">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="33c38-194">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="33c38-194">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="33c38-195">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="33c38-195">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="33c38-196">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="33c38-196">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Device will automatically choose best option based on configuration -->
  <psf:Option name="psk:AutoSelect">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the default manual feed bin -->
  <psf:Option name="psk:Manual">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">Manual</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a cassette-->
  <psf:Option name="psk:Cassette">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">SheetFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a tractor-->
  <psf:Option name="psk:Tractor">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">ContinuousFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!-- Device Input tray for Inkjet Printers -->
  <psf:Option name="psk:AutoSheetFeeder">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="33c38-197">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33c38-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c38-198">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="33c38-198">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




