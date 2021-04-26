---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92845b635aa7db1f44394cb6ef76b32292ea0dd4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996142"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="6d288-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="6d288-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="6d288-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="6d288-105">This topic is not current.</span></span> <span data-ttu-id="6d288-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6d288-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6d288-107">Define las características del perfil de color de destino.</span><span class="sxs-lookup"><span data-stu-id="6d288-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="6d288-108">Describe si la aplicación o el controlador selecciona el perfil de color de destino que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6d288-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="6d288-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6d288-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6d288-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6d288-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6d288-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6d288-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6d288-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6d288-112">Element Information</span></span>



| <span data-ttu-id="6d288-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d288-113">Name</span></span> | <span data-ttu-id="6d288-114">Value</span><span class="sxs-lookup"><span data-stu-id="6d288-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d288-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6d288-115">Element Type</span></span> <br/>   | <span data-ttu-id="6d288-116">Característica</span><span class="sxs-lookup"><span data-stu-id="6d288-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6d288-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="6d288-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6d288-118">Página</span><span class="sxs-lookup"><span data-stu-id="6d288-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6d288-119">Notas</span><span class="sxs-lookup"><span data-stu-id="6d288-119">Notes</span></span> <br/>          | <span data-ttu-id="6d288-120">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="6d288-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="6d288-121">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="6d288-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="6d288-122">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="6d288-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="6d288-123">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="6d288-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="6d288-124">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6d288-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6d288-125">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6d288-125">Structural Content</span></span>

<span data-ttu-id="6d288-126">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="6d288-126">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="6d288-127">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="6d288-127">Structure Variables</span></span>

<span data-ttu-id="6d288-128">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="6d288-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6d288-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d288-129">Name</span></span>                               | <span data-ttu-id="6d288-130">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6d288-130">Data type</span></span>         | <span data-ttu-id="6d288-131">Unidad</span><span class="sxs-lookup"><span data-stu-id="6d288-131">Unit</span></span>                  | <span data-ttu-id="6d288-132">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="6d288-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6d288-133">Resumen</span><span class="sxs-lookup"><span data-stu-id="6d288-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6d288-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6d288-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6d288-135">string</span><span class="sxs-lookup"><span data-stu-id="6d288-135">string</span></span><br/> | <span data-ttu-id="6d288-136">caracteres</span><span class="sxs-lookup"><span data-stu-id="6d288-136">characters</span></span><br/> | <span data-ttu-id="6d288-137">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6d288-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6d288-138">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6d288-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6d288-139">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="6d288-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6d288-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6d288-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6d288-141">string</span><span class="sxs-lookup"><span data-stu-id="6d288-141">string</span></span><br/> | <span data-ttu-id="6d288-142">N/D</span><span class="sxs-lookup"><span data-stu-id="6d288-142">n/a</span></span><br/>        | <span data-ttu-id="6d288-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="6d288-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6d288-144">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="6d288-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6d288-145">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6d288-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6d288-146">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="6d288-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6d288-147">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="6d288-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6d288-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d288-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d288-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6d288-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




