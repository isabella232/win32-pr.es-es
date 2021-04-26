---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba727cfa1c11850b62a883b95ab78a6dfae50
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996262"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="fdb76-104">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="fdb76-104">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="fdb76-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="fdb76-105">This topic is not current.</span></span> <span data-ttu-id="fdb76-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fdb76-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fdb76-107">Especifica el comportamiento de generación de negro para las separaciones de CONDUCT.</span><span class="sxs-lookup"><span data-stu-id="fdb76-107">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="fdb76-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fdb76-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fdb76-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="fdb76-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fdb76-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fdb76-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fdb76-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fdb76-111">Element Information</span></span>



| <span data-ttu-id="fdb76-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="fdb76-112">Name</span></span> | <span data-ttu-id="fdb76-113">Value</span><span class="sxs-lookup"><span data-stu-id="fdb76-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="fdb76-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="fdb76-114">Element Type</span></span> <br/>   | <span data-ttu-id="fdb76-115">Característica</span><span class="sxs-lookup"><span data-stu-id="fdb76-115">Feature</span></span><br/> |
| <span data-ttu-id="fdb76-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="fdb76-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fdb76-117">Página</span><span class="sxs-lookup"><span data-stu-id="fdb76-117">Page</span></span><br/>    |
| <span data-ttu-id="fdb76-118">Notas</span><span class="sxs-lookup"><span data-stu-id="fdb76-118">Notes</span></span> <br/>          | <span data-ttu-id="fdb76-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fdb76-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="fdb76-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="fdb76-120">Structural Content</span></span>

<span data-ttu-id="fdb76-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="fdb76-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="fdb76-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="fdb76-122">Structure Variables</span></span>

<span data-ttu-id="fdb76-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="fdb76-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fdb76-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="fdb76-124">Name</span></span>                               | <span data-ttu-id="fdb76-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fdb76-125">Data type</span></span>         | <span data-ttu-id="fdb76-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="fdb76-126">Unit</span></span>                  | <span data-ttu-id="fdb76-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="fdb76-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fdb76-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="fdb76-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fdb76-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fdb76-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="fdb76-130">string</span><span class="sxs-lookup"><span data-stu-id="fdb76-130">string</span></span><br/> | <span data-ttu-id="fdb76-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="fdb76-131">characters</span></span><br/> | <span data-ttu-id="fdb76-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fdb76-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fdb76-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fdb76-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fdb76-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="fdb76-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="fdb76-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="fdb76-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="fdb76-136">string</span><span class="sxs-lookup"><span data-stu-id="fdb76-136">string</span></span><br/> | <span data-ttu-id="fdb76-137">N/D</span><span class="sxs-lookup"><span data-stu-id="fdb76-137">n/a</span></span><br/>        | <span data-ttu-id="fdb76-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="fdb76-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fdb76-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="fdb76-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fdb76-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fdb76-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fdb76-141">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="fdb76-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fdb76-142">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="fdb76-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fdb76-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fdb76-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdb76-144">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="fdb76-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




