---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12002b25265a66a0aa3a5168f29e1e8e542ce31
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998082"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="4287e-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="4287e-104">PageBlendColorSpace</span></span>

<span data-ttu-id="4287e-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4287e-105">This topic is not current.</span></span> <span data-ttu-id="4287e-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4287e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4287e-107">Describe el espacio de color que se debe usar para las operaciones de combinación.</span><span class="sxs-lookup"><span data-stu-id="4287e-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="4287e-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4287e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4287e-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="4287e-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4287e-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4287e-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4287e-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4287e-111">Element Information</span></span>



| <span data-ttu-id="4287e-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="4287e-112">Name</span></span> | <span data-ttu-id="4287e-113">Value</span><span class="sxs-lookup"><span data-stu-id="4287e-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4287e-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4287e-114">Element Type</span></span> <br/>   | <span data-ttu-id="4287e-115">Característica</span><span class="sxs-lookup"><span data-stu-id="4287e-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4287e-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="4287e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4287e-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="4287e-117">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="4287e-118">Notas</span><span class="sxs-lookup"><span data-stu-id="4287e-118">Notes</span></span> <br/>          | <span data-ttu-id="4287e-119">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso como una imagen o un perfil de color en un documento de capacidades de impresión o PrintTicket DEBE hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="4287e-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="4287e-120">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="4287e-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="4287e-121">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="4287e-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="4287e-122">Los URI a los que se hace referencia en un documento de capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="4287e-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="4287e-123">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y puedan crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4287e-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="4287e-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="4287e-124">Structural Content</span></span>

<span data-ttu-id="4287e-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="4287e-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4287e-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="4287e-126">Structure Variables</span></span>

<span data-ttu-id="4287e-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="4287e-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4287e-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="4287e-128">Name</span></span>                               | <span data-ttu-id="4287e-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4287e-129">Data type</span></span>         | <span data-ttu-id="4287e-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="4287e-130">Unit</span></span>                  | <span data-ttu-id="4287e-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="4287e-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4287e-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="4287e-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4287e-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="4287e-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4287e-134">string</span><span class="sxs-lookup"><span data-stu-id="4287e-134">string</span></span><br/> | <span data-ttu-id="4287e-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="4287e-135">characters</span></span><br/> | <span data-ttu-id="4287e-136">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="4287e-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4287e-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4287e-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4287e-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="4287e-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4287e-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4287e-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4287e-140">string</span><span class="sxs-lookup"><span data-stu-id="4287e-140">string</span></span><br/> | <span data-ttu-id="4287e-141">N/D</span><span class="sxs-lookup"><span data-stu-id="4287e-141">n/a</span></span><br/>        | <span data-ttu-id="4287e-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="4287e-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4287e-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="4287e-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4287e-144">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4287e-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4287e-145">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="4287e-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4287e-146">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="4287e-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4287e-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4287e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4287e-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4287e-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




