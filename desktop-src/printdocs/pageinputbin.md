---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74e75653f7c6cbc6a586b80b3e8217286ce7c36
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993772"
---
# <a name="pageinputbin"></a><span data-ttu-id="848b0-104">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="848b0-104">PageInputBin</span></span>

<span data-ttu-id="848b0-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="848b0-105">This topic is not current.</span></span> <span data-ttu-id="848b0-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="848b0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="848b0-107">Describe la ubicación de entrada instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="848b0-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="848b0-108">Permite la especificación de la ubicación de entrada por página.</span><span class="sxs-lookup"><span data-stu-id="848b0-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="848b0-109">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="848b0-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="848b0-110">Ambos no se deben especificar simultáneamente en un documento PrintTicket o Capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="848b0-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="848b0-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="848b0-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="848b0-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="848b0-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="848b0-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="848b0-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="848b0-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="848b0-114">Element Information</span></span>



| <span data-ttu-id="848b0-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="848b0-115">Name</span></span> | <span data-ttu-id="848b0-116">Value</span><span class="sxs-lookup"><span data-stu-id="848b0-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="848b0-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="848b0-117">Element Type</span></span> <br/>   | <span data-ttu-id="848b0-118">Característica</span><span class="sxs-lookup"><span data-stu-id="848b0-118">Feature</span></span><br/> |
| <span data-ttu-id="848b0-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="848b0-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="848b0-120">Página</span><span class="sxs-lookup"><span data-stu-id="848b0-120">Page</span></span><br/>    |
| <span data-ttu-id="848b0-121">Notas</span><span class="sxs-lookup"><span data-stu-id="848b0-121">Notes</span></span> <br/>          | <span data-ttu-id="848b0-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="848b0-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="848b0-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="848b0-123">Structural Content</span></span>

<span data-ttu-id="848b0-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="848b0-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="848b0-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="848b0-125">Structure Variables</span></span>

<span data-ttu-id="848b0-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="848b0-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="848b0-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="848b0-127">Name</span></span>                                   | <span data-ttu-id="848b0-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="848b0-128">Data type</span></span>          | <span data-ttu-id="848b0-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="848b0-129">Unit</span></span>                  | <span data-ttu-id="848b0-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="848b0-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="848b0-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="848b0-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="848b0-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="848b0-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="848b0-133">string</span><span class="sxs-lookup"><span data-stu-id="848b0-133">string</span></span><br/>  | <span data-ttu-id="848b0-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="848b0-134">characters</span></span><br/> | <span data-ttu-id="848b0-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="848b0-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="848b0-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="848b0-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="848b0-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="848b0-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="848b0-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="848b0-139">string</span><span class="sxs-lookup"><span data-stu-id="848b0-139">string</span></span><br/>  | <span data-ttu-id="848b0-140">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-140">n/a</span></span><br/>        | <span data-ttu-id="848b0-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="848b0-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="848b0-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="848b0-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="848b0-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="848b0-144">string</span><span class="sxs-lookup"><span data-stu-id="848b0-144">string</span></span><br/>  | <span data-ttu-id="848b0-145">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-145">n/a</span></span><br/>        | <span data-ttu-id="848b0-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="848b0-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="848b0-147">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="848b0-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="848b0-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="848b0-149">string</span><span class="sxs-lookup"><span data-stu-id="848b0-149">string</span></span><br/>  | <span data-ttu-id="848b0-150">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-150">n/a</span></span><br/>        | <span data-ttu-id="848b0-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="848b0-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="848b0-152">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="848b0-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="848b0-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="848b0-154">string</span><span class="sxs-lookup"><span data-stu-id="848b0-154">string</span></span><br/>  | <span data-ttu-id="848b0-155">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-155">n/a</span></span><br/>        | <span data-ttu-id="848b0-156">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="848b0-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="848b0-157">Especifica el mecanismo de fuente de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="848b0-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="848b0-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="848b0-159">string</span><span class="sxs-lookup"><span data-stu-id="848b0-159">string</span></span><br/>  | <span data-ttu-id="848b0-160">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-160">n/a</span></span><br/>        | <span data-ttu-id="848b0-161">Alto, Estándar.</span><span class="sxs-lookup"><span data-stu-id="848b0-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="848b0-162">Especifica si la ubicación es un cubo de alta capacidad (cualitativo).</span><span class="sxs-lookup"><span data-stu-id="848b0-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="848b0-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="848b0-164">string</span><span class="sxs-lookup"><span data-stu-id="848b0-164">string</span></span><br/>  | <span data-ttu-id="848b0-165">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-165">n/a</span></span><br/>        | <span data-ttu-id="848b0-166">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="848b0-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="848b0-167">Especifica la funcionalidad de detección automática de tamaño de medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="848b0-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="848b0-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="848b0-169">string</span><span class="sxs-lookup"><span data-stu-id="848b0-169">string</span></span><br/>  | <span data-ttu-id="848b0-170">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-170">n/a</span></span><br/>        | <span data-ttu-id="848b0-171">Compatible, Ninguno.</span><span class="sxs-lookup"><span data-stu-id="848b0-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="848b0-172">Especifica la funcionalidad de detección automática del tipo de medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="848b0-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="848b0-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="848b0-174">integer</span><span class="sxs-lookup"><span data-stu-id="848b0-174">integer</span></span><br/> | <span data-ttu-id="848b0-175">Hojas</span><span class="sxs-lookup"><span data-stu-id="848b0-175">sheets</span></span><br/>     | <span data-ttu-id="848b0-176">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="848b0-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="848b0-177">Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="848b0-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="848b0-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="848b0-179">string</span><span class="sxs-lookup"><span data-stu-id="848b0-179">string</span></span><br/>  | <span data-ttu-id="848b0-180">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-180">n/a</span></span><br/>        | <span data-ttu-id="848b0-181">Recta, Tieneine.</span><span class="sxs-lookup"><span data-stu-id="848b0-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="848b0-182">Especifica las características de la ruta de acceso multimedia.</span><span class="sxs-lookup"><span data-stu-id="848b0-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="848b0-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="848b0-184">string</span><span class="sxs-lookup"><span data-stu-id="848b0-184">string</span></span><br/>  | <span data-ttu-id="848b0-185">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-185">n/a</span></span><br/>        | <span data-ttu-id="848b0-186">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="848b0-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="848b0-187">Especifica si los medios se imprimirán de cara hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="848b0-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="848b0-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="848b0-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="848b0-189">string</span><span class="sxs-lookup"><span data-stu-id="848b0-189">string</span></span><br/>  | <span data-ttu-id="848b0-190">N/D</span><span class="sxs-lookup"><span data-stu-id="848b0-190">n/a</span></span><br/>        | <span data-ttu-id="848b0-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="848b0-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="848b0-192">Especifica si los medios se alimentan primero con un borde largo o con un borde corto.</span><span class="sxs-lookup"><span data-stu-id="848b0-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="848b0-193">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="848b0-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="848b0-194">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="848b0-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="848b0-195">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="848b0-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="848b0-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="848b0-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="848b0-197">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="848b0-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




