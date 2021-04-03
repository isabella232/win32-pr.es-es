---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c8d84b099fb11aa97dea6f242f08acdd532105
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "103914282"
---
# <a name="pageinputbin"></a><span data-ttu-id="273ff-104">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="273ff-104">PageInputBin</span></span>

<span data-ttu-id="273ff-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="273ff-105">This topic is not current.</span></span> <span data-ttu-id="273ff-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="273ff-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="273ff-107">Describe la bandeja de entrada instalada en un dispositivo o la lista completa de ubicaciones compatibles para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="273ff-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="273ff-108">Permite especificar la ubicación de entrada en cada página.</span><span class="sxs-lookup"><span data-stu-id="273ff-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="273ff-109">Las palabras clave JobInputBin, DocumentInputBin y PageInputBin se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="273ff-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="273ff-110">Ambos no se deben especificar simultáneamente en un documento de capacidades de impresión o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="273ff-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="273ff-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="273ff-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="273ff-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="273ff-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="273ff-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="273ff-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="273ff-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="273ff-114">Element Information</span></span>



| <span data-ttu-id="273ff-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="273ff-115">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="273ff-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="273ff-116">Element Type</span></span> <br/>   | <span data-ttu-id="273ff-117">Característica</span><span class="sxs-lookup"><span data-stu-id="273ff-117">Feature</span></span><br/> |
| <span data-ttu-id="273ff-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="273ff-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="273ff-119">Página</span><span class="sxs-lookup"><span data-stu-id="273ff-119">Page</span></span><br/>    |
| <span data-ttu-id="273ff-120">Notas</span><span class="sxs-lookup"><span data-stu-id="273ff-120">Notes</span></span> <br/>          | <span data-ttu-id="273ff-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="273ff-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="273ff-122">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="273ff-122">Structural Content</span></span>

<span data-ttu-id="273ff-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="273ff-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="273ff-124">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="273ff-124">Structure Variables</span></span>

<span data-ttu-id="273ff-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="273ff-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="273ff-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="273ff-126">Name</span></span>                                   | <span data-ttu-id="273ff-127">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="273ff-127">Data type</span></span>          | <span data-ttu-id="273ff-128">Unidad</span><span class="sxs-lookup"><span data-stu-id="273ff-128">Unit</span></span>                  | <span data-ttu-id="273ff-129">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="273ff-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="273ff-130">Resumen</span><span class="sxs-lookup"><span data-stu-id="273ff-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="273ff-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="273ff-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="273ff-132">string</span><span class="sxs-lookup"><span data-stu-id="273ff-132">string</span></span><br/>  | <span data-ttu-id="273ff-133">caracteres</span><span class="sxs-lookup"><span data-stu-id="273ff-133">characters</span></span><br/> | <span data-ttu-id="273ff-134">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="273ff-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="273ff-135">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="273ff-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="273ff-136">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="273ff-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="273ff-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="273ff-138">string</span><span class="sxs-lookup"><span data-stu-id="273ff-138">string</span></span><br/>  | <span data-ttu-id="273ff-139">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-139">n/a</span></span><br/>        | <span data-ttu-id="273ff-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="273ff-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="273ff-141">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="273ff-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="273ff-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="273ff-143">string</span><span class="sxs-lookup"><span data-stu-id="273ff-143">string</span></span><br/>  | <span data-ttu-id="273ff-144">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-144">n/a</span></span><br/>        | <span data-ttu-id="273ff-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="273ff-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="273ff-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="273ff-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="273ff-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="273ff-148">string</span><span class="sxs-lookup"><span data-stu-id="273ff-148">string</span></span><br/>  | <span data-ttu-id="273ff-149">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-149">n/a</span></span><br/>        | <span data-ttu-id="273ff-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="273ff-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="273ff-151">Especifica el tipo de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="273ff-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="273ff-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="273ff-153">string</span><span class="sxs-lookup"><span data-stu-id="273ff-153">string</span></span><br/>  | <span data-ttu-id="273ff-154">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-154">n/a</span></span><br/>        | <span data-ttu-id="273ff-155">Automática, manual.</span><span class="sxs-lookup"><span data-stu-id="273ff-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="273ff-156">Especifica el mecanismo de alimentación de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="273ff-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="273ff-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="273ff-158">string</span><span class="sxs-lookup"><span data-stu-id="273ff-158">string</span></span><br/>  | <span data-ttu-id="273ff-159">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-159">n/a</span></span><br/>        | <span data-ttu-id="273ff-160">Alta, estándar.</span><span class="sxs-lookup"><span data-stu-id="273ff-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="273ff-161">Especifica si la ubicación es una ubicación de alta capacidad (cualitativa).</span><span class="sxs-lookup"><span data-stu-id="273ff-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="273ff-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="273ff-163">string</span><span class="sxs-lookup"><span data-stu-id="273ff-163">string</span></span><br/>  | <span data-ttu-id="273ff-164">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-164">n/a</span></span><br/>        | <span data-ttu-id="273ff-165">Compatible, ninguno.</span><span class="sxs-lookup"><span data-stu-id="273ff-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="273ff-166">Especifica la capacidad de detección automática del tamaño de los medios del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="273ff-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="273ff-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="273ff-168">string</span><span class="sxs-lookup"><span data-stu-id="273ff-168">string</span></span><br/>  | <span data-ttu-id="273ff-169">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-169">n/a</span></span><br/>        | <span data-ttu-id="273ff-170">Compatible, ninguno.</span><span class="sxs-lookup"><span data-stu-id="273ff-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="273ff-171">Especifica la capacidad de detección automática de tipos de medios del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="273ff-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="273ff-172">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="273ff-173">integer</span><span class="sxs-lookup"><span data-stu-id="273ff-173">integer</span></span><br/> | <span data-ttu-id="273ff-174">Sheet</span><span class="sxs-lookup"><span data-stu-id="273ff-174">sheets</span></span><br/>     | <span data-ttu-id="273ff-175">Restricción de entero máxima permitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="273ff-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="273ff-176">Especifica la capacidad de los medios en número de páginas (nivel completo) de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="273ff-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="273ff-177">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="273ff-178">string</span><span class="sxs-lookup"><span data-stu-id="273ff-178">string</span></span><br/>  | <span data-ttu-id="273ff-179">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-179">n/a</span></span><br/>        | <span data-ttu-id="273ff-180">Straight, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="273ff-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="273ff-181">Especifica las características de la ruta de acceso del medio.</span><span class="sxs-lookup"><span data-stu-id="273ff-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="273ff-182">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="273ff-183">string</span><span class="sxs-lookup"><span data-stu-id="273ff-183">string</span></span><br/>  | <span data-ttu-id="273ff-184">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-184">n/a</span></span><br/>        | <span data-ttu-id="273ff-185">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="273ff-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="273ff-186">Especifica si los medios se van a imprimir en una superficie arriba o abajo.</span><span class="sxs-lookup"><span data-stu-id="273ff-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="273ff-187">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="273ff-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="273ff-188">string</span><span class="sxs-lookup"><span data-stu-id="273ff-188">string</span></span><br/>  | <span data-ttu-id="273ff-189">N/D</span><span class="sxs-lookup"><span data-stu-id="273ff-189">n/a</span></span><br/>        | <span data-ttu-id="273ff-190">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="273ff-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="273ff-191">Especifica si los medios se alimentan primero hacia el borde largo o el borde corto.</span><span class="sxs-lookup"><span data-stu-id="273ff-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="273ff-192">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="273ff-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="273ff-193">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="273ff-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="273ff-194">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="273ff-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="273ff-195">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="273ff-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="273ff-196">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="273ff-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




