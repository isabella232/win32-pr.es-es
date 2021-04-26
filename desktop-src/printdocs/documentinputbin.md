---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57890492ed5f0b575e6d462351282dd199f34f45
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997772"
---
# <a name="documentinputbin"></a><span data-ttu-id="9367e-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="9367e-104">DocumentInputBin</span></span>

<span data-ttu-id="9367e-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="9367e-105">This topic is not current.</span></span> <span data-ttu-id="9367e-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9367e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9367e-107">Describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9367e-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="9367e-108">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="9367e-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="9367e-109">Ambos no deben especificarse simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="9367e-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="9367e-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9367e-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="9367e-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9367e-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="9367e-112">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="9367e-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9367e-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9367e-113">Element Information</span></span>



| <span data-ttu-id="9367e-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="9367e-114">Name</span></span> | <span data-ttu-id="9367e-115">Value</span><span class="sxs-lookup"><span data-stu-id="9367e-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9367e-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9367e-116">Element Type</span></span> <br/>   | <span data-ttu-id="9367e-117">Característica</span><span class="sxs-lookup"><span data-stu-id="9367e-117">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="9367e-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9367e-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9367e-119">Documento</span><span class="sxs-lookup"><span data-stu-id="9367e-119">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="9367e-120">Notas</span><span class="sxs-lookup"><span data-stu-id="9367e-120">Notes</span></span> <br/>          | <span data-ttu-id="9367e-121">Los contenedores admitidos que no están instalados actualmente deben marcarse como restringidos en el documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9367e-121">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9367e-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9367e-122">Structural Content</span></span>

<span data-ttu-id="9367e-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9367e-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="9367e-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9367e-124">Structure Variables</span></span>

<span data-ttu-id="9367e-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9367e-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9367e-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="9367e-126">Name</span></span>                                   | <span data-ttu-id="9367e-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9367e-127">Data type</span></span>          | <span data-ttu-id="9367e-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="9367e-128">Unit</span></span>                  | <span data-ttu-id="9367e-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9367e-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9367e-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="9367e-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9367e-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9367e-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="9367e-132">string</span><span class="sxs-lookup"><span data-stu-id="9367e-132">string</span></span><br/>  | <span data-ttu-id="9367e-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="9367e-133">characters</span></span><br/> | <span data-ttu-id="9367e-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9367e-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9367e-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9367e-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9367e-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9367e-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="9367e-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="9367e-138">string</span><span class="sxs-lookup"><span data-stu-id="9367e-138">string</span></span><br/>  | <span data-ttu-id="9367e-139">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-139">n/a</span></span><br/>        | <span data-ttu-id="9367e-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="9367e-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9367e-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9367e-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9367e-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="9367e-143">string</span><span class="sxs-lookup"><span data-stu-id="9367e-143">string</span></span><br/>  | <span data-ttu-id="9367e-144">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-144">n/a</span></span><br/>        | <span data-ttu-id="9367e-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="9367e-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9367e-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9367e-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9367e-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="9367e-148">string</span><span class="sxs-lookup"><span data-stu-id="9367e-148">string</span></span><br/>  | <span data-ttu-id="9367e-149">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-149">n/a</span></span><br/>        | <span data-ttu-id="9367e-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="9367e-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="9367e-151">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="9367e-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="9367e-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="9367e-153">string</span><span class="sxs-lookup"><span data-stu-id="9367e-153">string</span></span><br/>  | <span data-ttu-id="9367e-154">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-154">n/a</span></span><br/>        | <span data-ttu-id="9367e-155">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="9367e-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="9367e-156">Especifica el mecanismo de fuente de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="9367e-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="9367e-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="9367e-158">integer</span><span class="sxs-lookup"><span data-stu-id="9367e-158">integer</span></span><br/> | <span data-ttu-id="9367e-159">Hojas</span><span class="sxs-lookup"><span data-stu-id="9367e-159">sheets</span></span><br/>     | <span data-ttu-id="9367e-160">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9367e-160">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="9367e-161">Especifica si el cubo es un cubo de alta capacidad (cualitativo).</span><span class="sxs-lookup"><span data-stu-id="9367e-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="9367e-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="9367e-163">string</span><span class="sxs-lookup"><span data-stu-id="9367e-163">string</span></span><br/>  | <span data-ttu-id="9367e-164">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-164">n/a</span></span><br/>        | <span data-ttu-id="9367e-165">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9367e-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9367e-166">Especifica la funcionalidad de detección automática del tamaño del medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9367e-166">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="9367e-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="9367e-168">string</span><span class="sxs-lookup"><span data-stu-id="9367e-168">string</span></span><br/>  | <span data-ttu-id="9367e-169">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-169">n/a</span></span><br/>        | <span data-ttu-id="9367e-170">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9367e-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9367e-171">Especifica la capacidad de medios en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="9367e-171">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="9367e-172">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-172">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="9367e-173">string</span><span class="sxs-lookup"><span data-stu-id="9367e-173">string</span></span><br/>  | <span data-ttu-id="9367e-174">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-174">n/a</span></span><br/>        | <span data-ttu-id="9367e-175">Recta, íntea.</span><span class="sxs-lookup"><span data-stu-id="9367e-175">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="9367e-176">Especifica las características de la ruta de acceso multimedia.</span><span class="sxs-lookup"><span data-stu-id="9367e-176">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="9367e-177">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-177">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="9367e-178">string</span><span class="sxs-lookup"><span data-stu-id="9367e-178">string</span></span><br/>  | <span data-ttu-id="9367e-179">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-179">n/a</span></span><br/>        | <span data-ttu-id="9367e-180">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="9367e-180">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9367e-181">Especifica si el medio se va a imprimir de cara hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="9367e-181">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="9367e-182">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="9367e-182">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="9367e-183">string</span><span class="sxs-lookup"><span data-stu-id="9367e-183">string</span></span><br/>  | <span data-ttu-id="9367e-184">N/D</span><span class="sxs-lookup"><span data-stu-id="9367e-184">n/a</span></span><br/>        | <span data-ttu-id="9367e-185">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="9367e-185">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="9367e-186">Especifica si los medios se alimentan primero con un borde largo o con un borde corto primero.</span><span class="sxs-lookup"><span data-stu-id="9367e-186">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9367e-187">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9367e-187">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9367e-188">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="9367e-188">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9367e-189">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9367e-189">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="9367e-190">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9367e-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9367e-191">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9367e-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




