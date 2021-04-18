---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4459f621ac4455a69e891c2eeda6f785b6d8b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717445"
---
# <a name="documentinputbin"></a><span data-ttu-id="3c69a-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="3c69a-104">DocumentInputBin</span></span>

<span data-ttu-id="3c69a-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="3c69a-105">This topic is not current.</span></span> <span data-ttu-id="3c69a-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3c69a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3c69a-107">Describe la bandeja de entrada instalada en un dispositivo o la lista completa de ubicaciones compatibles para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c69a-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="3c69a-108">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="3c69a-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="3c69a-109">Ambos no se deben especificar simultáneamente en un documento de capacidades de impresión o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="3c69a-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="3c69a-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3c69a-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="3c69a-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3c69a-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="3c69a-112">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="3c69a-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3c69a-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3c69a-113">Element Information</span></span>



| <span data-ttu-id="3c69a-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="3c69a-114">Name</span></span>                       |                                                                                                                                |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c69a-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3c69a-115">Element Type</span></span> <br/>   | <span data-ttu-id="3c69a-116">Característica</span><span class="sxs-lookup"><span data-stu-id="3c69a-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c69a-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="3c69a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3c69a-118">Documento</span><span class="sxs-lookup"><span data-stu-id="3c69a-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="3c69a-119">Notas</span><span class="sxs-lookup"><span data-stu-id="3c69a-119">Notes</span></span> <br/>          | <span data-ttu-id="3c69a-120">Las ubicaciones admitidas que no están instaladas se deben marcar como restringidas en el documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3c69a-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="3c69a-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3c69a-121">Structural Content</span></span>

<span data-ttu-id="3c69a-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="3c69a-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3c69a-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="3c69a-123">Structure Variables</span></span>

<span data-ttu-id="3c69a-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="3c69a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3c69a-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="3c69a-125">Name</span></span>                                   | <span data-ttu-id="3c69a-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3c69a-126">Data type</span></span>          | <span data-ttu-id="3c69a-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="3c69a-127">Unit</span></span>                  | <span data-ttu-id="3c69a-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="3c69a-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3c69a-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="3c69a-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c69a-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="3c69a-131">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-131">string</span></span><br/>  | <span data-ttu-id="3c69a-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="3c69a-132">characters</span></span><br/> | <span data-ttu-id="3c69a-133">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="3c69a-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3c69a-134">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3c69a-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3c69a-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="3c69a-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="3c69a-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="3c69a-137">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-137">string</span></span><br/>  | <span data-ttu-id="3c69a-138">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-138">n/a</span></span><br/>        | <span data-ttu-id="3c69a-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="3c69a-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3c69a-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="3c69a-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="3c69a-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="3c69a-142">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-142">string</span></span><br/>  | <span data-ttu-id="3c69a-143">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-143">n/a</span></span><br/>        | <span data-ttu-id="3c69a-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="3c69a-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3c69a-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="3c69a-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="3c69a-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="3c69a-147">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-147">string</span></span><br/>  | <span data-ttu-id="3c69a-148">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-148">n/a</span></span><br/>        | <span data-ttu-id="3c69a-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="3c69a-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="3c69a-150">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="3c69a-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="3c69a-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="3c69a-152">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-152">string</span></span><br/>  | <span data-ttu-id="3c69a-153">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-153">n/a</span></span><br/>        | <span data-ttu-id="3c69a-154">Automática, manual.</span><span class="sxs-lookup"><span data-stu-id="3c69a-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="3c69a-155">Especifica el mecanismo de alimentación de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="3c69a-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="3c69a-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="3c69a-157">integer</span><span class="sxs-lookup"><span data-stu-id="3c69a-157">integer</span></span><br/> | <span data-ttu-id="3c69a-158">Sheet</span><span class="sxs-lookup"><span data-stu-id="3c69a-158">sheets</span></span><br/>     | <span data-ttu-id="3c69a-159">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c69a-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="3c69a-160">Especifica si la ubicación es una ubicación de alta capacidad (cualitativa).</span><span class="sxs-lookup"><span data-stu-id="3c69a-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="3c69a-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="3c69a-162">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-162">string</span></span><br/>  | <span data-ttu-id="3c69a-163">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-163">n/a</span></span><br/>        | <span data-ttu-id="3c69a-164">Compatible, ninguno.</span><span class="sxs-lookup"><span data-stu-id="3c69a-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="3c69a-165">Especifica la capacidad de detección automática del tamaño del medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c69a-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="3c69a-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="3c69a-167">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-167">string</span></span><br/>  | <span data-ttu-id="3c69a-168">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-168">n/a</span></span><br/>        | <span data-ttu-id="3c69a-169">Compatible, ninguno.</span><span class="sxs-lookup"><span data-stu-id="3c69a-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="3c69a-170">Especifica la capacidad de los medios en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="3c69a-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="3c69a-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="3c69a-172">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-172">string</span></span><br/>  | <span data-ttu-id="3c69a-173">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-173">n/a</span></span><br/>        | <span data-ttu-id="3c69a-174">Straight, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="3c69a-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="3c69a-175">Especifica las características de la ruta de acceso del medio.</span><span class="sxs-lookup"><span data-stu-id="3c69a-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="3c69a-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="3c69a-177">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-177">string</span></span><br/>  | <span data-ttu-id="3c69a-178">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-178">n/a</span></span><br/>        | <span data-ttu-id="3c69a-179">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="3c69a-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="3c69a-180">Especifica si los medios se van a imprimir en una superficie arriba o abajo.</span><span class="sxs-lookup"><span data-stu-id="3c69a-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="3c69a-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="3c69a-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="3c69a-182">string</span><span class="sxs-lookup"><span data-stu-id="3c69a-182">string</span></span><br/>  | <span data-ttu-id="3c69a-183">N/D</span><span class="sxs-lookup"><span data-stu-id="3c69a-183">n/a</span></span><br/>        | <span data-ttu-id="3c69a-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="3c69a-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="3c69a-185">Especifica si los medios se alimentan primero hacia el borde largo o el borde corto.</span><span class="sxs-lookup"><span data-stu-id="3c69a-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3c69a-186">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="3c69a-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3c69a-187">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="3c69a-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3c69a-188">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="3c69a-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3c69a-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c69a-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c69a-190">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="3c69a-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




