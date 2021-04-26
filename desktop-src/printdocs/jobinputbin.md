---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: JobInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f87782d6cf9aae5c34d36603f025e803f47db3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998102"
---
# <a name="jobinputbin"></a><span data-ttu-id="06568-104">JobInputBin</span><span class="sxs-lookup"><span data-stu-id="06568-104">JobInputBin</span></span>

<span data-ttu-id="06568-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="06568-105">This topic is not current.</span></span> <span data-ttu-id="06568-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="06568-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="06568-107">Describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06568-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="06568-108">Permite la especificación de la ubicación de entrada por trabajo.</span><span class="sxs-lookup"><span data-stu-id="06568-108">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="06568-109">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="06568-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="06568-110">Ambos no se deben especificar simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="06568-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="06568-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="06568-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="06568-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="06568-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="06568-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="06568-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="06568-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="06568-114">Element Information</span></span>



| <span data-ttu-id="06568-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="06568-115">Name</span></span> | <span data-ttu-id="06568-116">Value</span><span class="sxs-lookup"><span data-stu-id="06568-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="06568-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="06568-117">Element Type</span></span> <br/>   | <span data-ttu-id="06568-118">Característica</span><span class="sxs-lookup"><span data-stu-id="06568-118">Feature</span></span><br/> |
| <span data-ttu-id="06568-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="06568-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="06568-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="06568-120">Job</span></span><br/>     |
| <span data-ttu-id="06568-121">Notas</span><span class="sxs-lookup"><span data-stu-id="06568-121">Notes</span></span> <br/>          | <span data-ttu-id="06568-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="06568-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="06568-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="06568-123">Structural Content</span></span>

<span data-ttu-id="06568-124">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="06568-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="06568-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="06568-125">Structure Variables</span></span>

<span data-ttu-id="06568-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="06568-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="06568-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="06568-127">Name</span></span>                                   | <span data-ttu-id="06568-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="06568-128">Data type</span></span>          | <span data-ttu-id="06568-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="06568-129">Unit</span></span>                  | <span data-ttu-id="06568-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="06568-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="06568-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="06568-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06568-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="06568-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="06568-133">string</span><span class="sxs-lookup"><span data-stu-id="06568-133">string</span></span><br/>  | <span data-ttu-id="06568-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="06568-134">characters</span></span><br/> | <span data-ttu-id="06568-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="06568-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="06568-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="06568-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="06568-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="06568-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="06568-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="06568-139">string</span><span class="sxs-lookup"><span data-stu-id="06568-139">string</span></span><br/>  | <span data-ttu-id="06568-140">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-140">n/a</span></span><br/>        | <span data-ttu-id="06568-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="06568-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="06568-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="06568-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="06568-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="06568-144">string</span><span class="sxs-lookup"><span data-stu-id="06568-144">string</span></span><br/>  | <span data-ttu-id="06568-145">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-145">n/a</span></span><br/>        | <span data-ttu-id="06568-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="06568-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="06568-147">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="06568-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="06568-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="06568-149">string</span><span class="sxs-lookup"><span data-stu-id="06568-149">string</span></span><br/>  | <span data-ttu-id="06568-150">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-150">n/a</span></span><br/>        | <span data-ttu-id="06568-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="06568-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="06568-152">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="06568-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="06568-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="06568-154">string</span><span class="sxs-lookup"><span data-stu-id="06568-154">string</span></span><br/>  | <span data-ttu-id="06568-155">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-155">n/a</span></span><br/>        | <span data-ttu-id="06568-156">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="06568-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="06568-157">Especifica el mecanismo de fuente de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="06568-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="06568-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="06568-159">string</span><span class="sxs-lookup"><span data-stu-id="06568-159">string</span></span><br/>  | <span data-ttu-id="06568-160">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-160">n/a</span></span><br/>        | <span data-ttu-id="06568-161">Alto, Estándar.</span><span class="sxs-lookup"><span data-stu-id="06568-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="06568-162">Especifica si la ubicación es un cubo de alta capacidad (cualitativo).</span><span class="sxs-lookup"><span data-stu-id="06568-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="06568-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="06568-164">string</span><span class="sxs-lookup"><span data-stu-id="06568-164">string</span></span><br/>  | <span data-ttu-id="06568-165">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-165">n/a</span></span><br/>        | <span data-ttu-id="06568-166">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="06568-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="06568-167">Especifica la funcionalidad de detección automática del tamaño del medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06568-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="06568-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="06568-169">string</span><span class="sxs-lookup"><span data-stu-id="06568-169">string</span></span><br/>  | <span data-ttu-id="06568-170">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-170">n/a</span></span><br/>        | <span data-ttu-id="06568-171">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="06568-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="06568-172">Especifica la funcionalidad de detección automática del tipo de medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06568-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="06568-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="06568-174">integer</span><span class="sxs-lookup"><span data-stu-id="06568-174">integer</span></span><br/> | <span data-ttu-id="06568-175">Hojas</span><span class="sxs-lookup"><span data-stu-id="06568-175">sheets</span></span><br/>     | <span data-ttu-id="06568-176">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06568-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="06568-177">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="06568-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="06568-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="06568-179">string</span><span class="sxs-lookup"><span data-stu-id="06568-179">string</span></span><br/>  | <span data-ttu-id="06568-180">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-180">n/a</span></span><br/>        | <span data-ttu-id="06568-181">Recta, Tieneine.</span><span class="sxs-lookup"><span data-stu-id="06568-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="06568-182">Especifica las características de la ruta de acceso multimedia.</span><span class="sxs-lookup"><span data-stu-id="06568-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="06568-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="06568-184">string</span><span class="sxs-lookup"><span data-stu-id="06568-184">string</span></span><br/>  | <span data-ttu-id="06568-185">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-185">n/a</span></span><br/>        | <span data-ttu-id="06568-186">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="06568-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="06568-187">Especifica si los medios se imprimirán de cara hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="06568-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="06568-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="06568-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="06568-189">string</span><span class="sxs-lookup"><span data-stu-id="06568-189">string</span></span><br/>  | <span data-ttu-id="06568-190">N/D</span><span class="sxs-lookup"><span data-stu-id="06568-190">n/a</span></span><br/>        | <span data-ttu-id="06568-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="06568-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="06568-192">Especifica si los medios se alimentan primero con un borde largo o con un borde corto.</span><span class="sxs-lookup"><span data-stu-id="06568-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="06568-193">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="06568-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="06568-194">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="06568-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="06568-195">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="06568-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="06568-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06568-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06568-197">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="06568-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




