---
description: Obtenga información sobre el elemento PageBlackGenerationProcessing, que especifica el comportamiento de generación de negro para las separaciones de PROCESAMIENTO.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21861595917b67390857b380a416e441d454081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408518"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="10b98-103">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="10b98-103">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="10b98-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="10b98-104">This topic is not current.</span></span> <span data-ttu-id="10b98-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="10b98-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="10b98-106">Especifica el comportamiento de generación de negro para las separaciones de NTES.</span><span class="sxs-lookup"><span data-stu-id="10b98-106">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="10b98-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="10b98-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="10b98-108">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="10b98-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="10b98-109">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="10b98-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="10b98-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="10b98-110">Element Information</span></span>



| <span data-ttu-id="10b98-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="10b98-111">Name</span></span> | <span data-ttu-id="10b98-112">Valor</span><span class="sxs-lookup"><span data-stu-id="10b98-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="10b98-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="10b98-113">Element Type</span></span> <br/>   | <span data-ttu-id="10b98-114">Característica</span><span class="sxs-lookup"><span data-stu-id="10b98-114">Feature</span></span><br/> |
| <span data-ttu-id="10b98-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="10b98-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="10b98-116">Página</span><span class="sxs-lookup"><span data-stu-id="10b98-116">Page</span></span><br/>    |
| <span data-ttu-id="10b98-117">Notas</span><span class="sxs-lookup"><span data-stu-id="10b98-117">Notes</span></span> <br/>          | <span data-ttu-id="10b98-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="10b98-118">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="10b98-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="10b98-119">Structural Content</span></span>

<span data-ttu-id="10b98-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="10b98-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="10b98-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="10b98-121">Structure Variables</span></span>

<span data-ttu-id="10b98-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="10b98-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="10b98-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="10b98-123">Name</span></span>                               | <span data-ttu-id="10b98-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="10b98-124">Data type</span></span>         | <span data-ttu-id="10b98-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="10b98-125">Unit</span></span>                  | <span data-ttu-id="10b98-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="10b98-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="10b98-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="10b98-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="10b98-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="10b98-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="10b98-129">string</span><span class="sxs-lookup"><span data-stu-id="10b98-129">string</span></span><br/> | <span data-ttu-id="10b98-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="10b98-130">characters</span></span><br/> | <span data-ttu-id="10b98-131">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="10b98-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="10b98-132">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="10b98-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="10b98-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="10b98-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="10b98-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="10b98-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="10b98-135">string</span><span class="sxs-lookup"><span data-stu-id="10b98-135">string</span></span><br/> | <span data-ttu-id="10b98-136">N/D</span><span class="sxs-lookup"><span data-stu-id="10b98-136">n/a</span></span><br/>        | <span data-ttu-id="10b98-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="10b98-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="10b98-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="10b98-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="10b98-139">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="10b98-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="10b98-140">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="10b98-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="10b98-141">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="10b98-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a><span data-ttu-id="10b98-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10b98-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b98-143">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="10b98-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




