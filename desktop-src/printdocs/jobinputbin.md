---
description: Obtenga información sobre el elemento JobInputBin, que describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: JobInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929df4cb4871e5a8d2ebacfe533b5da3ad9babf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408898"
---
# <a name="jobinputbin"></a><span data-ttu-id="1b733-103">JobInputBin</span><span class="sxs-lookup"><span data-stu-id="1b733-103">JobInputBin</span></span>

<span data-ttu-id="1b733-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1b733-104">This topic is not current.</span></span> <span data-ttu-id="1b733-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1b733-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1b733-106">Describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b733-106">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="1b733-107">Permite la especificación de la ubicación de entrada por trabajo.</span><span class="sxs-lookup"><span data-stu-id="1b733-107">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="1b733-108">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="1b733-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="1b733-109">Ambos no se deben especificar simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="1b733-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1b733-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1b733-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1b733-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1b733-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1b733-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1b733-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1b733-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1b733-113">Element Information</span></span>



| <span data-ttu-id="1b733-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b733-114">Name</span></span> | <span data-ttu-id="1b733-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1b733-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1b733-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1b733-116">Element Type</span></span> <br/>   | <span data-ttu-id="1b733-117">Característica</span><span class="sxs-lookup"><span data-stu-id="1b733-117">Feature</span></span><br/> |
| <span data-ttu-id="1b733-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1b733-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1b733-119">Trabajo</span><span class="sxs-lookup"><span data-stu-id="1b733-119">Job</span></span><br/>     |
| <span data-ttu-id="1b733-120">Notas</span><span class="sxs-lookup"><span data-stu-id="1b733-120">Notes</span></span> <br/>          | <span data-ttu-id="1b733-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1b733-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1b733-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="1b733-122">Structural Content</span></span>

<span data-ttu-id="1b733-123">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="1b733-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1b733-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="1b733-124">Structure Variables</span></span>

<span data-ttu-id="1b733-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1b733-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1b733-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b733-126">Name</span></span>                                   | <span data-ttu-id="1b733-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1b733-127">Data type</span></span>          | <span data-ttu-id="1b733-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="1b733-128">Unit</span></span>                  | <span data-ttu-id="1b733-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="1b733-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1b733-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="1b733-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b733-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1b733-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="1b733-132">string</span><span class="sxs-lookup"><span data-stu-id="1b733-132">string</span></span><br/>  | <span data-ttu-id="1b733-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="1b733-133">characters</span></span><br/> | <span data-ttu-id="1b733-134">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="1b733-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1b733-135">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1b733-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1b733-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="1b733-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="1b733-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="1b733-138">string</span><span class="sxs-lookup"><span data-stu-id="1b733-138">string</span></span><br/>  | <span data-ttu-id="1b733-139">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-139">n/a</span></span><br/>        | <span data-ttu-id="1b733-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="1b733-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1b733-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1b733-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1b733-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="1b733-143">string</span><span class="sxs-lookup"><span data-stu-id="1b733-143">string</span></span><br/>  | <span data-ttu-id="1b733-144">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-144">n/a</span></span><br/>        | <span data-ttu-id="1b733-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="1b733-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1b733-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="1b733-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1b733-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="1b733-148">string</span><span class="sxs-lookup"><span data-stu-id="1b733-148">string</span></span><br/>  | <span data-ttu-id="1b733-149">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-149">n/a</span></span><br/>        | <span data-ttu-id="1b733-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="1b733-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="1b733-151">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="1b733-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="1b733-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="1b733-153">string</span><span class="sxs-lookup"><span data-stu-id="1b733-153">string</span></span><br/>  | <span data-ttu-id="1b733-154">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-154">n/a</span></span><br/>        | <span data-ttu-id="1b733-155">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="1b733-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="1b733-156">Especifica el mecanismo de fuente de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="1b733-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="1b733-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="1b733-158">string</span><span class="sxs-lookup"><span data-stu-id="1b733-158">string</span></span><br/>  | <span data-ttu-id="1b733-159">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-159">n/a</span></span><br/>        | <span data-ttu-id="1b733-160">Alto, Estándar.</span><span class="sxs-lookup"><span data-stu-id="1b733-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="1b733-161">Especifica si el cubo es un cubo de alta capacidad (cualitativo).</span><span class="sxs-lookup"><span data-stu-id="1b733-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="1b733-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1b733-163">string</span><span class="sxs-lookup"><span data-stu-id="1b733-163">string</span></span><br/>  | <span data-ttu-id="1b733-164">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-164">n/a</span></span><br/>        | <span data-ttu-id="1b733-165">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1b733-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1b733-166">Especifica la funcionalidad de detección automática del tamaño del medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b733-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1b733-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1b733-168">string</span><span class="sxs-lookup"><span data-stu-id="1b733-168">string</span></span><br/>  | <span data-ttu-id="1b733-169">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-169">n/a</span></span><br/>        | <span data-ttu-id="1b733-170">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1b733-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1b733-171">Especifica la funcionalidad de detección automática del tipo de medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b733-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1b733-172">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="1b733-173">integer</span><span class="sxs-lookup"><span data-stu-id="1b733-173">integer</span></span><br/> | <span data-ttu-id="1b733-174">Hojas</span><span class="sxs-lookup"><span data-stu-id="1b733-174">sheets</span></span><br/>     | <span data-ttu-id="1b733-175">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b733-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="1b733-176">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="1b733-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="1b733-177">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="1b733-178">string</span><span class="sxs-lookup"><span data-stu-id="1b733-178">string</span></span><br/>  | <span data-ttu-id="1b733-179">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-179">n/a</span></span><br/>        | <span data-ttu-id="1b733-180">Recta, Tieneine.</span><span class="sxs-lookup"><span data-stu-id="1b733-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="1b733-181">Especifica las características de la ruta de acceso multimedia.</span><span class="sxs-lookup"><span data-stu-id="1b733-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="1b733-182">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="1b733-183">string</span><span class="sxs-lookup"><span data-stu-id="1b733-183">string</span></span><br/>  | <span data-ttu-id="1b733-184">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-184">n/a</span></span><br/>        | <span data-ttu-id="1b733-185">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="1b733-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1b733-186">Especifica si los medios se imprimirán de cara hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="1b733-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="1b733-187">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="1b733-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="1b733-188">string</span><span class="sxs-lookup"><span data-stu-id="1b733-188">string</span></span><br/>  | <span data-ttu-id="1b733-189">N/D</span><span class="sxs-lookup"><span data-stu-id="1b733-189">n/a</span></span><br/>        | <span data-ttu-id="1b733-190">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="1b733-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="1b733-191">Especifica si los medios se alimentan primero con un borde largo o con un borde corto.</span><span class="sxs-lookup"><span data-stu-id="1b733-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1b733-192">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1b733-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1b733-193">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="1b733-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1b733-194">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="1b733-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1b733-195">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b733-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b733-196">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1b733-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




