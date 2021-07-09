---
description: Obtenga información sobre el elemento configurable por el usuario PageOrientation. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f0af08fcd29f34bb55bd16b1eac50487e96ffb
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549123"
---
# <a name="pageorientation"></a><span data-ttu-id="2de82-105">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="2de82-105">PageOrientation</span></span>

<span data-ttu-id="2de82-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="2de82-106">This topic is not current.</span></span> <span data-ttu-id="2de82-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2de82-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2de82-108">Describe la orientación de la hoja de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="2de82-108">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="2de82-109">Opción</span><span class="sxs-lookup"><span data-stu-id="2de82-109">Option</span></span>                       | <span data-ttu-id="2de82-110">Definición</span><span class="sxs-lookup"><span data-stu-id="2de82-110">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de82-111">Horizontal</span><span class="sxs-lookup"><span data-stu-id="2de82-111">Landscape</span></span> <br/>        | <span data-ttu-id="2de82-112">¿El contenido se gira en la página 90?? grados CCW con respecto a la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="2de82-112">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="2de82-113">Vertical</span><span class="sxs-lookup"><span data-stu-id="2de82-113">Portrait</span></span> <br/>         | <span data-ttu-id="2de82-114">Orientación estándar.</span><span class="sxs-lookup"><span data-stu-id="2de82-114">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="2de82-115">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="2de82-115">ReverseLandscape</span></span> <br/> | <span data-ttu-id="2de82-116">¿El contenido gira en la página 270?? grados CCW con respecto a la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="2de82-116">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="2de82-117">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="2de82-117">ReversePortrait</span></span> <br/>  | <span data-ttu-id="2de82-118">¿El contenido gira en la página 180?? grados relativos a la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="2de82-118">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="2de82-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2de82-119">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2de82-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="2de82-120">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2de82-121">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2de82-121">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2de82-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2de82-122">Element Information</span></span>



| <span data-ttu-id="2de82-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="2de82-123">Name</span></span> | <span data-ttu-id="2de82-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2de82-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de82-125">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2de82-125">Element Type</span></span> <br/>   | <span data-ttu-id="2de82-126">Característica</span><span class="sxs-lookup"><span data-stu-id="2de82-126">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="2de82-127">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2de82-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2de82-128">Página</span><span class="sxs-lookup"><span data-stu-id="2de82-128">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="2de82-129">Notas</span><span class="sxs-lookup"><span data-stu-id="2de82-129">Notes</span></span> <br/>          | <span data-ttu-id="2de82-130">Si un dispositivo de impresora solo puede admitir una dirección horizontal y esta dirección se conoce como "Horizontal inversa", la orientación de la página se considerará como "Horizontal".</span><span class="sxs-lookup"><span data-stu-id="2de82-130">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="2de82-131">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="2de82-131">Structural Content</span></span>

<span data-ttu-id="2de82-132">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2de82-132">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2de82-133">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="2de82-133">Structure Variables</span></span>

<span data-ttu-id="2de82-134">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2de82-134">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2de82-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="2de82-135">Name</span></span>                               | <span data-ttu-id="2de82-136">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2de82-136">Data type</span></span>         | <span data-ttu-id="2de82-137">Unidad</span><span class="sxs-lookup"><span data-stu-id="2de82-137">Unit</span></span>                  | <span data-ttu-id="2de82-138">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="2de82-138">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2de82-139">Resumen</span><span class="sxs-lookup"><span data-stu-id="2de82-139">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2de82-140">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2de82-140">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2de82-141">string</span><span class="sxs-lookup"><span data-stu-id="2de82-141">string</span></span><br/> | <span data-ttu-id="2de82-142">caracteres</span><span class="sxs-lookup"><span data-stu-id="2de82-142">characters</span></span><br/> | <span data-ttu-id="2de82-143">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="2de82-143">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2de82-144">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2de82-144">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2de82-145">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="2de82-145">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2de82-146">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2de82-146">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2de82-147">string</span><span class="sxs-lookup"><span data-stu-id="2de82-147">string</span></span><br/> | <span data-ttu-id="2de82-148">N/D</span><span class="sxs-lookup"><span data-stu-id="2de82-148">n/a</span></span><br/>        | <span data-ttu-id="2de82-149">True, False.</span><span class="sxs-lookup"><span data-stu-id="2de82-149">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2de82-150">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="2de82-150">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2de82-151">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2de82-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2de82-152">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="2de82-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2de82-153">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="2de82-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2de82-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2de82-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2de82-155">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2de82-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




