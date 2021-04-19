---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf68660929839fad79be26daebf32b9bc0f7ea5
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707641"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="e0cb0-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="e0cb0-104">PageBlendColorSpace</span></span>

<span data-ttu-id="e0cb0-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-105">This topic is not current.</span></span> <span data-ttu-id="e0cb0-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e0cb0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e0cb0-107">Describe el espacio de colores que se debe usar para las operaciones de mezcla.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="e0cb0-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e0cb0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e0cb0-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e0cb0-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e0cb0-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="e0cb0-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e0cb0-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e0cb0-111">Element Information</span></span>



| <span data-ttu-id="e0cb0-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0cb0-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0cb0-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e0cb0-113">Element Type</span></span> <br/>   | <span data-ttu-id="e0cb0-114">Característica</span><span class="sxs-lookup"><span data-stu-id="e0cb0-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e0cb0-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e0cb0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e0cb0-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="e0cb0-116">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e0cb0-117">Notas</span><span class="sxs-lookup"><span data-stu-id="e0cb0-117">Notes</span></span> <br/>          | <span data-ttu-id="e0cb0-118">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-118">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="e0cb0-119">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-119">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="e0cb0-120">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-120">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="e0cb0-121">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-121">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="e0cb0-122">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-122">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e0cb0-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e0cb0-123">Structural Content</span></span>

<span data-ttu-id="e0cb0-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e0cb0-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e0cb0-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="e0cb0-125">Structure Variables</span></span>

<span data-ttu-id="e0cb0-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e0cb0-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0cb0-127">Name</span></span>                               | <span data-ttu-id="e0cb0-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e0cb0-128">Data type</span></span>         | <span data-ttu-id="e0cb0-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="e0cb0-129">Unit</span></span>                  | <span data-ttu-id="e0cb0-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="e0cb0-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e0cb0-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="e0cb0-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e0cb0-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e0cb0-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e0cb0-133">string</span><span class="sxs-lookup"><span data-stu-id="e0cb0-133">string</span></span><br/> | <span data-ttu-id="e0cb0-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="e0cb0-134">characters</span></span><br/> | <span data-ttu-id="e0cb0-135">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e0cb0-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e0cb0-136">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e0cb0-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e0cb0-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e0cb0-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e0cb0-139">string</span><span class="sxs-lookup"><span data-stu-id="e0cb0-139">string</span></span><br/> | <span data-ttu-id="e0cb0-140">N/D</span><span class="sxs-lookup"><span data-stu-id="e0cb0-140">n/a</span></span><br/>        | <span data-ttu-id="e0cb0-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e0cb0-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e0cb0-143">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="e0cb0-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e0cb0-144">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e0cb0-145">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="e0cb0-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e0cb0-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0cb0-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0cb0-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e0cb0-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




