---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a94fb97ad1e64c7f55fd9520ed8a648a74f550
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997542"
---
# <a name="pageorientation"></a><span data-ttu-id="600bc-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="600bc-104">PageOrientation</span></span>

<span data-ttu-id="600bc-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="600bc-105">This topic is not current.</span></span> <span data-ttu-id="600bc-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="600bc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="600bc-107">Describe la orientación de la hoja de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="600bc-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="600bc-108">Opción</span><span class="sxs-lookup"><span data-stu-id="600bc-108">Option</span></span>                       | <span data-ttu-id="600bc-109">Definición</span><span class="sxs-lookup"><span data-stu-id="600bc-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600bc-110">Horizontal</span><span class="sxs-lookup"><span data-stu-id="600bc-110">Landscape</span></span> <br/>        | <span data-ttu-id="600bc-111">¿El contenido se gira en la página 90?? grados CCW con respecto a la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="600bc-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="600bc-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="600bc-112">Portrait</span></span> <br/>         | <span data-ttu-id="600bc-113">Orientación estándar.</span><span class="sxs-lookup"><span data-stu-id="600bc-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="600bc-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="600bc-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="600bc-115">¿El contenido se gira en la página 270?? grados CCW con respecto a la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="600bc-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="600bc-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="600bc-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="600bc-117">¿El contenido se gira en la página 180?? grados relativos a la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="600bc-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="600bc-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="600bc-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="600bc-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="600bc-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="600bc-120">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="600bc-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="600bc-121">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="600bc-121">Element Information</span></span>



| <span data-ttu-id="600bc-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="600bc-122">Name</span></span> | <span data-ttu-id="600bc-123">Value</span><span class="sxs-lookup"><span data-stu-id="600bc-123">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600bc-124">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="600bc-124">Element Type</span></span> <br/>   | <span data-ttu-id="600bc-125">Característica</span><span class="sxs-lookup"><span data-stu-id="600bc-125">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="600bc-126">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="600bc-126">Scoping Prefix</span></span> <br/> | <span data-ttu-id="600bc-127">Página</span><span class="sxs-lookup"><span data-stu-id="600bc-127">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="600bc-128">Notas</span><span class="sxs-lookup"><span data-stu-id="600bc-128">Notes</span></span> <br/>          | <span data-ttu-id="600bc-129">Si un dispositivo de impresora solo puede admitir una dirección horizontal y esta dirección se conoce como "Horizontal inverso", la orientación de la página todavía se considerará como "Horizontal".</span><span class="sxs-lookup"><span data-stu-id="600bc-129">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="600bc-130">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="600bc-130">Structural Content</span></span>

<span data-ttu-id="600bc-131">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="600bc-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="600bc-132">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="600bc-132">Structure Variables</span></span>

<span data-ttu-id="600bc-133">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="600bc-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="600bc-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="600bc-134">Name</span></span>                               | <span data-ttu-id="600bc-135">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="600bc-135">Data type</span></span>         | <span data-ttu-id="600bc-136">Unidad</span><span class="sxs-lookup"><span data-stu-id="600bc-136">Unit</span></span>                  | <span data-ttu-id="600bc-137">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="600bc-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="600bc-138">Resumen</span><span class="sxs-lookup"><span data-stu-id="600bc-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="600bc-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="600bc-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="600bc-140">string</span><span class="sxs-lookup"><span data-stu-id="600bc-140">string</span></span><br/> | <span data-ttu-id="600bc-141">caracteres</span><span class="sxs-lookup"><span data-stu-id="600bc-141">characters</span></span><br/> | <span data-ttu-id="600bc-142">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="600bc-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="600bc-143">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="600bc-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="600bc-144">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="600bc-144">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="600bc-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="600bc-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="600bc-146">string</span><span class="sxs-lookup"><span data-stu-id="600bc-146">string</span></span><br/> | <span data-ttu-id="600bc-147">N/D</span><span class="sxs-lookup"><span data-stu-id="600bc-147">n/a</span></span><br/>        | <span data-ttu-id="600bc-148">True, False.</span><span class="sxs-lookup"><span data-stu-id="600bc-148">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="600bc-149">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="600bc-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="600bc-150">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="600bc-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="600bc-151">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="600bc-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="600bc-152">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="600bc-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="600bc-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="600bc-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="600bc-154">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="600bc-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




