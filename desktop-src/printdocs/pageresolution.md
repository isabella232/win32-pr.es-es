---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0fdd16cf3dc0beb6a418b23d8ee6a93e4a6a61
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707646"
---
# <a name="pageresolution"></a><span data-ttu-id="94254-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="94254-104">PageResolution</span></span>

<span data-ttu-id="94254-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="94254-105">This topic is not current.</span></span> <span data-ttu-id="94254-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="94254-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="94254-107">Define la resolución de página de la impresión, ya sea como un valor cualitativo, como puntos por pulgada o ambos.</span><span class="sxs-lookup"><span data-stu-id="94254-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="94254-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="94254-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="94254-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="94254-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="94254-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="94254-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="94254-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="94254-111">Element Information</span></span>



| <span data-ttu-id="94254-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="94254-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="94254-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="94254-113">Element Type</span></span> <br/>   | <span data-ttu-id="94254-114">Característica</span><span class="sxs-lookup"><span data-stu-id="94254-114">Feature</span></span><br/> |
| <span data-ttu-id="94254-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="94254-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="94254-116">Página</span><span class="sxs-lookup"><span data-stu-id="94254-116">Page</span></span><br/>    |
| <span data-ttu-id="94254-117">Notas</span><span class="sxs-lookup"><span data-stu-id="94254-117">Notes</span></span> <br/>          | <span data-ttu-id="94254-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="94254-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="94254-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="94254-119">Structural Content</span></span>

<span data-ttu-id="94254-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="94254-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="94254-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="94254-121">Structure Variables</span></span>

<span data-ttu-id="94254-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="94254-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="94254-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="94254-123">Name</span></span>                                      | <span data-ttu-id="94254-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="94254-124">Data type</span></span>          | <span data-ttu-id="94254-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="94254-125">Unit</span></span>                  | <span data-ttu-id="94254-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="94254-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="94254-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="94254-127">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94254-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="94254-128">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="94254-129">string</span><span class="sxs-lookup"><span data-stu-id="94254-129">string</span></span><br/>  | <span data-ttu-id="94254-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="94254-130">characters</span></span><br/> | <span data-ttu-id="94254-131">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="94254-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="94254-132">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="94254-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="94254-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="94254-133">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="94254-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="94254-134">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="94254-135">string</span><span class="sxs-lookup"><span data-stu-id="94254-135">string</span></span><br/>  | <span data-ttu-id="94254-136">N/D</span><span class="sxs-lookup"><span data-stu-id="94254-136">n/a</span></span><br/>        | <span data-ttu-id="94254-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="94254-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="94254-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="94254-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="94254-139">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="94254-139">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="94254-140">integer</span><span class="sxs-lookup"><span data-stu-id="94254-140">integer</span></span><br/> | <span data-ttu-id="94254-141">ppp</span><span class="sxs-lookup"><span data-stu-id="94254-141">DPI</span></span><br/>        | <span data-ttu-id="94254-142">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="94254-142">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="94254-143">Especifica el componente x de la resolución en relación con el PageImageableSize en PPP (en relación con el PageMediaSize y la dirección de la fuente del medio).</span><span class="sxs-lookup"><span data-stu-id="94254-143">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="94254-144">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="94254-144">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="94254-145">integer</span><span class="sxs-lookup"><span data-stu-id="94254-145">integer</span></span><br/> | <span data-ttu-id="94254-146">ppp</span><span class="sxs-lookup"><span data-stu-id="94254-146">DPI</span></span><br/>        | <span data-ttu-id="94254-147">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="94254-147">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="94254-148">Especifica el componente y de la resolución en relación con el PageImageableSize en PPP (en relación con el PageMediaSize y la dirección de la fuente del medio).</span><span class="sxs-lookup"><span data-stu-id="94254-148">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="94254-149">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="94254-149">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="94254-150">string</span><span class="sxs-lookup"><span data-stu-id="94254-150">string</span></span><br/>  | <span data-ttu-id="94254-151">N/D</span><span class="sxs-lookup"><span data-stu-id="94254-151">n/a</span></span><br/>        | <span data-ttu-id="94254-152">Predeterminado, borrador, alto, normal, otro.</span><span class="sxs-lookup"><span data-stu-id="94254-152">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="94254-153">Especifica una etiqueta de calidad para la resolución.</span><span class="sxs-lookup"><span data-stu-id="94254-153">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="94254-154">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="94254-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="94254-155">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="94254-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="94254-156">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="94254-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="94254-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94254-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94254-158">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="94254-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




