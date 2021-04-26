---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e44a7ff73c03929d3dfc8bc9f7c31c878ad039c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993722"
---
# <a name="pageresolution"></a><span data-ttu-id="e9ed8-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="e9ed8-104">PageResolution</span></span>

<span data-ttu-id="e9ed8-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-105">This topic is not current.</span></span> <span data-ttu-id="e9ed8-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e9ed8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e9ed8-107">Define la resolución de página de la impresión, ya sea como un valor cualitativo, como puntos por pulgada o ambos.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="e9ed8-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e9ed8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e9ed8-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e9ed8-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e9ed8-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e9ed8-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e9ed8-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e9ed8-111">Element Information</span></span>



| <span data-ttu-id="e9ed8-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9ed8-112">Name</span></span> | <span data-ttu-id="e9ed8-113">Value</span><span class="sxs-lookup"><span data-stu-id="e9ed8-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="e9ed8-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e9ed8-114">Element Type</span></span> <br/>   | <span data-ttu-id="e9ed8-115">Característica</span><span class="sxs-lookup"><span data-stu-id="e9ed8-115">Feature</span></span><br/> |
| <span data-ttu-id="e9ed8-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e9ed8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e9ed8-117">Página</span><span class="sxs-lookup"><span data-stu-id="e9ed8-117">Page</span></span><br/>    |
| <span data-ttu-id="e9ed8-118">Notas</span><span class="sxs-lookup"><span data-stu-id="e9ed8-118">Notes</span></span> <br/>          | <span data-ttu-id="e9ed8-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e9ed8-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e9ed8-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e9ed8-120">Structural Content</span></span>

<span data-ttu-id="e9ed8-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e9ed8-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e9ed8-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="e9ed8-122">Structure Variables</span></span>

<span data-ttu-id="e9ed8-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e9ed8-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9ed8-124">Name</span></span>                                      | <span data-ttu-id="e9ed8-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e9ed8-125">Data type</span></span>          | <span data-ttu-id="e9ed8-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="e9ed8-126">Unit</span></span>                  | <span data-ttu-id="e9ed8-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="e9ed8-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e9ed8-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="e9ed8-128">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ed8-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e9ed8-129">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="e9ed8-130">string</span><span class="sxs-lookup"><span data-stu-id="e9ed8-130">string</span></span><br/>  | <span data-ttu-id="e9ed8-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="e9ed8-131">characters</span></span><br/> | <span data-ttu-id="e9ed8-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e9ed8-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e9ed8-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e9ed8-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-134">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="e9ed8-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e9ed8-135">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="e9ed8-136">string</span><span class="sxs-lookup"><span data-stu-id="e9ed8-136">string</span></span><br/>  | <span data-ttu-id="e9ed8-137">N/D</span><span class="sxs-lookup"><span data-stu-id="e9ed8-137">n/a</span></span><br/>        | <span data-ttu-id="e9ed8-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e9ed8-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="e9ed8-140">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="e9ed8-140">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="e9ed8-141">integer</span><span class="sxs-lookup"><span data-stu-id="e9ed8-141">integer</span></span><br/> | <span data-ttu-id="e9ed8-142">ppp</span><span class="sxs-lookup"><span data-stu-id="e9ed8-142">DPI</span></span><br/>        | <span data-ttu-id="e9ed8-143">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-143">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e9ed8-144">Especifica el componente x de la resolución en relación con PageImageableSize en PPP (en relación con PageMediaSize y la dirección de fuente del medio).</span><span class="sxs-lookup"><span data-stu-id="e9ed8-144">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="e9ed8-145">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="e9ed8-145">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="e9ed8-146">integer</span><span class="sxs-lookup"><span data-stu-id="e9ed8-146">integer</span></span><br/> | <span data-ttu-id="e9ed8-147">ppp</span><span class="sxs-lookup"><span data-stu-id="e9ed8-147">DPI</span></span><br/>        | <span data-ttu-id="e9ed8-148">Mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-148">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e9ed8-149">Especifica el componente y de la resolución con respecto a PageImageableSize en PPP (en relación con PageMediaSize y la dirección de fuente de los medios).</span><span class="sxs-lookup"><span data-stu-id="e9ed8-149">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="e9ed8-150">\_CualitativoResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="e9ed8-150">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="e9ed8-151">string</span><span class="sxs-lookup"><span data-stu-id="e9ed8-151">string</span></span><br/>  | <span data-ttu-id="e9ed8-152">N/D</span><span class="sxs-lookup"><span data-stu-id="e9ed8-152">n/a</span></span><br/>        | <span data-ttu-id="e9ed8-153">Predeterminado, Borrador, Alto, Normal, Otro.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-153">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="e9ed8-154">Especifica una etiqueta de calidad para la resolución.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-154">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e9ed8-155">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e9ed8-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e9ed8-156">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="e9ed8-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e9ed8-157">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="e9ed8-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e9ed8-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9ed8-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ed8-159">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e9ed8-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




