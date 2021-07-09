---
description: Obtenga información sobre el elemento configurable por el usuario PageBlendColorSpace. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36ce3a1def74058014fc396d9ef53aed6a32302
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549343"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="137b6-105">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="137b6-105">PageBlendColorSpace</span></span>

<span data-ttu-id="137b6-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="137b6-106">This topic is not current.</span></span> <span data-ttu-id="137b6-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="137b6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="137b6-108">Describe el espacio de color que se debe usar para las operaciones de combinación.</span><span class="sxs-lookup"><span data-stu-id="137b6-108">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="137b6-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="137b6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="137b6-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="137b6-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="137b6-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="137b6-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="137b6-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="137b6-112">Element Information</span></span>



| <span data-ttu-id="137b6-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="137b6-113">Name</span></span> | <span data-ttu-id="137b6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="137b6-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="137b6-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="137b6-115">Element Type</span></span> <br/>   | <span data-ttu-id="137b6-116">Característica</span><span class="sxs-lookup"><span data-stu-id="137b6-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="137b6-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="137b6-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="137b6-118">Trabajo</span><span class="sxs-lookup"><span data-stu-id="137b6-118">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="137b6-119">Notas</span><span class="sxs-lookup"><span data-stu-id="137b6-119">Notes</span></span> <br/>          | <span data-ttu-id="137b6-120">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso como una imagen o un perfil de color en un documento de capacidades de impresión o PrintTicket DEBE hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="137b6-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="137b6-121">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="137b6-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="137b6-122">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="137b6-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="137b6-123">Los URI a los que se hace referencia en un documento de capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="137b6-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="137b6-124">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y puedan crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="137b6-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="137b6-125">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="137b6-125">Structural Content</span></span>

<span data-ttu-id="137b6-126">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="137b6-126">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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

## <a name="structure-variables"></a><span data-ttu-id="137b6-127">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="137b6-127">Structure Variables</span></span>

<span data-ttu-id="137b6-128">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="137b6-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="137b6-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="137b6-129">Name</span></span>                               | <span data-ttu-id="137b6-130">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="137b6-130">Data type</span></span>         | <span data-ttu-id="137b6-131">Unidad</span><span class="sxs-lookup"><span data-stu-id="137b6-131">Unit</span></span>                  | <span data-ttu-id="137b6-132">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="137b6-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="137b6-133">Resumen</span><span class="sxs-lookup"><span data-stu-id="137b6-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="137b6-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="137b6-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="137b6-135">string</span><span class="sxs-lookup"><span data-stu-id="137b6-135">string</span></span><br/> | <span data-ttu-id="137b6-136">caracteres</span><span class="sxs-lookup"><span data-stu-id="137b6-136">characters</span></span><br/> | <span data-ttu-id="137b6-137">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="137b6-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="137b6-138">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="137b6-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="137b6-139">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="137b6-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="137b6-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="137b6-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="137b6-141">string</span><span class="sxs-lookup"><span data-stu-id="137b6-141">string</span></span><br/> | <span data-ttu-id="137b6-142">N/D</span><span class="sxs-lookup"><span data-stu-id="137b6-142">n/a</span></span><br/>        | <span data-ttu-id="137b6-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="137b6-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="137b6-144">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="137b6-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="137b6-145">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="137b6-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="137b6-146">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="137b6-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="137b6-147">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="137b6-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="137b6-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="137b6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="137b6-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="137b6-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




