---
description: Obtenga información sobre el elemento PageSourceColorProfile. Este elemento define las características del perfil de color de origen.
ms.assetid: aa4f5425-6ca1-4820-b15d-bbead1f6d735
title: PageSourceColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709d44f8af7ea6c2709201e57bc047fe9b2d21b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119000"
---
# <a name="pagesourcecolorprofile"></a><span data-ttu-id="6fe04-104">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="6fe04-104">PageSourceColorProfile</span></span>

<span data-ttu-id="6fe04-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="6fe04-105">This topic is not current.</span></span> <span data-ttu-id="6fe04-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6fe04-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6fe04-107">Define las características del perfil de color de origen.</span><span class="sxs-lookup"><span data-stu-id="6fe04-107">Defines the characteristics of the source color profile.</span></span>

-   [<span data-ttu-id="6fe04-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6fe04-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6fe04-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6fe04-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6fe04-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fe04-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6fe04-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6fe04-111">Element Information</span></span>



| <span data-ttu-id="6fe04-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="6fe04-112">Name</span></span>                       | <span data-ttu-id="6fe04-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6fe04-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe04-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6fe04-114">Element Type</span></span> <br/>   | <span data-ttu-id="6fe04-115">Característica</span><span class="sxs-lookup"><span data-stu-id="6fe04-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6fe04-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="6fe04-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6fe04-117">Página</span><span class="sxs-lookup"><span data-stu-id="6fe04-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6fe04-118">Notas</span><span class="sxs-lookup"><span data-stu-id="6fe04-118">Notes</span></span> <br/>          | <span data-ttu-id="6fe04-119">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso como una imagen o un perfil de color en un documento de capacidades de impresión o PrintTicket DEBE hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="6fe04-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="6fe04-120">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="6fe04-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="6fe04-121">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="6fe04-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="6fe04-122">Los URI a los que se hace referencia en un documento de capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="6fe04-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="6fe04-123">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6fe04-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6fe04-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6fe04-124">Structural Content</span></span>

<span data-ttu-id="6fe04-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="6fe04-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="6fe04-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="6fe04-126">Structure Variables</span></span>

<span data-ttu-id="6fe04-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="6fe04-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6fe04-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="6fe04-128">Name</span></span>                               | <span data-ttu-id="6fe04-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6fe04-129">Data type</span></span>         | <span data-ttu-id="6fe04-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="6fe04-130">Unit</span></span>                  | <span data-ttu-id="6fe04-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="6fe04-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6fe04-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="6fe04-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6fe04-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6fe04-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6fe04-134">string</span><span class="sxs-lookup"><span data-stu-id="6fe04-134">string</span></span><br/> | <span data-ttu-id="6fe04-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="6fe04-135">characters</span></span><br/> | <span data-ttu-id="6fe04-136">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6fe04-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6fe04-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6fe04-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6fe04-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="6fe04-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6fe04-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6fe04-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6fe04-140">string</span><span class="sxs-lookup"><span data-stu-id="6fe04-140">string</span></span><br/> | <span data-ttu-id="6fe04-141">N/D</span><span class="sxs-lookup"><span data-stu-id="6fe04-141">n/a</span></span><br/>        | <span data-ttu-id="6fe04-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="6fe04-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6fe04-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="6fe04-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6fe04-144">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fe04-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6fe04-145">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="6fe04-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6fe04-146">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="6fe04-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Option name="psk:RGB">
    <!-- Source profile used to perform color management for untagged RGB data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CMYK">
    <!-- Source profile used to perform color management for untagged CMYK data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6fe04-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fe04-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fe04-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6fe04-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




