---
description: Obtenga información sobre el elemento configurable por el usuario PageResolution. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394829"
---
# <a name="pageresolution"></a><span data-ttu-id="987f6-105">PageResolution</span><span class="sxs-lookup"><span data-stu-id="987f6-105">PageResolution</span></span>

<span data-ttu-id="987f6-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="987f6-106">This topic is not current.</span></span> <span data-ttu-id="987f6-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="987f6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="987f6-108">Define la resolución de página de la impresión, ya sea como un valor cualitativo, como puntos por pulgada o ambos.</span><span class="sxs-lookup"><span data-stu-id="987f6-108">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="987f6-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="987f6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="987f6-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="987f6-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="987f6-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="987f6-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="987f6-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="987f6-112">Element Information</span></span>



| <span data-ttu-id="987f6-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="987f6-113">Name</span></span> | <span data-ttu-id="987f6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="987f6-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="987f6-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="987f6-115">Element Type</span></span> <br/>   | <span data-ttu-id="987f6-116">Característica</span><span class="sxs-lookup"><span data-stu-id="987f6-116">Feature</span></span><br/> |
| <span data-ttu-id="987f6-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="987f6-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="987f6-118">Página</span><span class="sxs-lookup"><span data-stu-id="987f6-118">Page</span></span><br/>    |
| <span data-ttu-id="987f6-119">Notas</span><span class="sxs-lookup"><span data-stu-id="987f6-119">Notes</span></span> <br/>          | <span data-ttu-id="987f6-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="987f6-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="987f6-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="987f6-121">Structural Content</span></span>

<span data-ttu-id="987f6-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="987f6-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="987f6-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="987f6-123">Structure Variables</span></span>

<span data-ttu-id="987f6-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="987f6-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="987f6-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="987f6-125">Name</span></span>                                      | <span data-ttu-id="987f6-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="987f6-126">Data type</span></span>          | <span data-ttu-id="987f6-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="987f6-127">Unit</span></span>                  | <span data-ttu-id="987f6-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="987f6-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="987f6-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="987f6-129">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="987f6-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="987f6-130">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="987f6-131">string</span><span class="sxs-lookup"><span data-stu-id="987f6-131">string</span></span><br/>  | <span data-ttu-id="987f6-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="987f6-132">characters</span></span><br/> | <span data-ttu-id="987f6-133">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="987f6-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="987f6-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="987f6-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="987f6-135">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="987f6-135">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="987f6-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="987f6-136">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="987f6-137">string</span><span class="sxs-lookup"><span data-stu-id="987f6-137">string</span></span><br/>  | <span data-ttu-id="987f6-138">N/D</span><span class="sxs-lookup"><span data-stu-id="987f6-138">n/a</span></span><br/>        | <span data-ttu-id="987f6-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="987f6-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="987f6-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="987f6-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="987f6-141">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="987f6-141">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="987f6-142">integer</span><span class="sxs-lookup"><span data-stu-id="987f6-142">integer</span></span><br/> | <span data-ttu-id="987f6-143">ppp</span><span class="sxs-lookup"><span data-stu-id="987f6-143">DPI</span></span><br/>        | <span data-ttu-id="987f6-144">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="987f6-144">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="987f6-145">Especifica el componente x de la resolución con respecto a PageImageableSize en PPP (en relación con PageMediaSize y la dirección de fuente de los medios).</span><span class="sxs-lookup"><span data-stu-id="987f6-145">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="987f6-146">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="987f6-146">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="987f6-147">integer</span><span class="sxs-lookup"><span data-stu-id="987f6-147">integer</span></span><br/> | <span data-ttu-id="987f6-148">ppp</span><span class="sxs-lookup"><span data-stu-id="987f6-148">DPI</span></span><br/>        | <span data-ttu-id="987f6-149">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="987f6-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="987f6-150">Especifica el componente y de la resolución con respecto a PageImageableSize en PPP (en relación con PageMediaSize y la dirección de fuente de los medios).</span><span class="sxs-lookup"><span data-stu-id="987f6-150">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="987f6-151">\_CualitativoResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="987f6-151">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="987f6-152">string</span><span class="sxs-lookup"><span data-stu-id="987f6-152">string</span></span><br/>  | <span data-ttu-id="987f6-153">N/D</span><span class="sxs-lookup"><span data-stu-id="987f6-153">n/a</span></span><br/>        | <span data-ttu-id="987f6-154">Default, Draft, High, Normal, Other.</span><span class="sxs-lookup"><span data-stu-id="987f6-154">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="987f6-155">Especifica una etiqueta de calidad para la resolución.</span><span class="sxs-lookup"><span data-stu-id="987f6-155">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="987f6-156">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="987f6-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="987f6-157">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="987f6-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="987f6-158">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="987f6-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="987f6-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="987f6-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="987f6-160">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="987f6-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




