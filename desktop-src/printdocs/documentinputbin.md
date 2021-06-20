---
description: Obtenga información sobre el elemento DocumentInputBin, que describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 452e2f94b3e75a2b0555610db26d69e2a2f7548b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409308"
---
# <a name="documentinputbin"></a><span data-ttu-id="1924b-103">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="1924b-103">DocumentInputBin</span></span>

<span data-ttu-id="1924b-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1924b-104">This topic is not current.</span></span> <span data-ttu-id="1924b-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1924b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1924b-106">Describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1924b-106">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="1924b-107">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="1924b-107">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="1924b-108">Ambos no deben especificarse simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="1924b-108">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1924b-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1924b-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="1924b-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1924b-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="1924b-111">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="1924b-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1924b-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1924b-112">Element Information</span></span>



| <span data-ttu-id="1924b-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="1924b-113">Name</span></span> | <span data-ttu-id="1924b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1924b-114">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1924b-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1924b-115">Element Type</span></span> <br/>   | <span data-ttu-id="1924b-116">Característica</span><span class="sxs-lookup"><span data-stu-id="1924b-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="1924b-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1924b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1924b-118">Documento</span><span class="sxs-lookup"><span data-stu-id="1924b-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="1924b-119">Notas</span><span class="sxs-lookup"><span data-stu-id="1924b-119">Notes</span></span> <br/>          | <span data-ttu-id="1924b-120">Los contenedores admitidos que no están instalados actualmente deben marcarse como restringidos en el documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="1924b-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1924b-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1924b-121">Structural Content</span></span>

<span data-ttu-id="1924b-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="1924b-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1924b-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="1924b-123">Structure Variables</span></span>

<span data-ttu-id="1924b-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1924b-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1924b-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="1924b-125">Name</span></span>                                   | <span data-ttu-id="1924b-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1924b-126">Data type</span></span>          | <span data-ttu-id="1924b-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="1924b-127">Unit</span></span>                  | <span data-ttu-id="1924b-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="1924b-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1924b-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="1924b-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1924b-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1924b-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="1924b-131">string</span><span class="sxs-lookup"><span data-stu-id="1924b-131">string</span></span><br/>  | <span data-ttu-id="1924b-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="1924b-132">characters</span></span><br/> | <span data-ttu-id="1924b-133">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1924b-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1924b-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1924b-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1924b-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1924b-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="1924b-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="1924b-137">string</span><span class="sxs-lookup"><span data-stu-id="1924b-137">string</span></span><br/>  | <span data-ttu-id="1924b-138">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-138">n/a</span></span><br/>        | <span data-ttu-id="1924b-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="1924b-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1924b-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1924b-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1924b-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="1924b-142">string</span><span class="sxs-lookup"><span data-stu-id="1924b-142">string</span></span><br/>  | <span data-ttu-id="1924b-143">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-143">n/a</span></span><br/>        | <span data-ttu-id="1924b-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="1924b-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1924b-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1924b-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1924b-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="1924b-147">string</span><span class="sxs-lookup"><span data-stu-id="1924b-147">string</span></span><br/>  | <span data-ttu-id="1924b-148">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-148">n/a</span></span><br/>        | <span data-ttu-id="1924b-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="1924b-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="1924b-150">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="1924b-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="1924b-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="1924b-152">string</span><span class="sxs-lookup"><span data-stu-id="1924b-152">string</span></span><br/>  | <span data-ttu-id="1924b-153">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-153">n/a</span></span><br/>        | <span data-ttu-id="1924b-154">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="1924b-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="1924b-155">Especifica el mecanismo de fuente de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="1924b-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="1924b-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="1924b-157">integer</span><span class="sxs-lookup"><span data-stu-id="1924b-157">integer</span></span><br/> | <span data-ttu-id="1924b-158">Hojas</span><span class="sxs-lookup"><span data-stu-id="1924b-158">sheets</span></span><br/>     | <span data-ttu-id="1924b-159">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1924b-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="1924b-160">Especifica si la ubicación es un cubo de alta capacidad (cualitativo).</span><span class="sxs-lookup"><span data-stu-id="1924b-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="1924b-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1924b-162">string</span><span class="sxs-lookup"><span data-stu-id="1924b-162">string</span></span><br/>  | <span data-ttu-id="1924b-163">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-163">n/a</span></span><br/>        | <span data-ttu-id="1924b-164">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1924b-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1924b-165">Especifica la funcionalidad de detección automática del tamaño del medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1924b-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="1924b-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1924b-167">string</span><span class="sxs-lookup"><span data-stu-id="1924b-167">string</span></span><br/>  | <span data-ttu-id="1924b-168">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-168">n/a</span></span><br/>        | <span data-ttu-id="1924b-169">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1924b-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1924b-170">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="1924b-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="1924b-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="1924b-172">string</span><span class="sxs-lookup"><span data-stu-id="1924b-172">string</span></span><br/>  | <span data-ttu-id="1924b-173">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-173">n/a</span></span><br/>        | <span data-ttu-id="1924b-174">Recta, íntea.</span><span class="sxs-lookup"><span data-stu-id="1924b-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="1924b-175">Especifica las características de la ruta de acceso del medio.</span><span class="sxs-lookup"><span data-stu-id="1924b-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="1924b-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="1924b-177">string</span><span class="sxs-lookup"><span data-stu-id="1924b-177">string</span></span><br/>  | <span data-ttu-id="1924b-178">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-178">n/a</span></span><br/>        | <span data-ttu-id="1924b-179">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="1924b-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1924b-180">Especifica si los medios se imprimirán de cara hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="1924b-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="1924b-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="1924b-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="1924b-182">string</span><span class="sxs-lookup"><span data-stu-id="1924b-182">string</span></span><br/>  | <span data-ttu-id="1924b-183">N/D</span><span class="sxs-lookup"><span data-stu-id="1924b-183">n/a</span></span><br/>        | <span data-ttu-id="1924b-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="1924b-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="1924b-185">Especifica si los medios se alimentan primero con un borde largo o con un borde corto.</span><span class="sxs-lookup"><span data-stu-id="1924b-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1924b-186">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1924b-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1924b-187">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="1924b-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1924b-188">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="1924b-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1924b-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1924b-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1924b-190">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1924b-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




