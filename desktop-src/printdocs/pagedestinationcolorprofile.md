---
description: Revise el elemento configurable por el usuario PageDestinationColorProfile. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c12e8b6e322f024c3603abc97b0e4e0413d5b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549223"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="a1006-105">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="a1006-105">PageDestinationColorProfile</span></span>

<span data-ttu-id="a1006-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="a1006-106">This topic is not current.</span></span> <span data-ttu-id="a1006-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a1006-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a1006-108">Define las características del perfil de color de destino.</span><span class="sxs-lookup"><span data-stu-id="a1006-108">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="a1006-109">Describe si la aplicación o el controlador selecciona el perfil de color de destino que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a1006-109">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="a1006-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a1006-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a1006-111">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="a1006-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a1006-112">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a1006-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a1006-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a1006-113">Element Information</span></span>



| <span data-ttu-id="a1006-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="a1006-114">Name</span></span> | <span data-ttu-id="a1006-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a1006-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1006-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a1006-116">Element Type</span></span> <br/>   | <span data-ttu-id="a1006-117">Característica</span><span class="sxs-lookup"><span data-stu-id="a1006-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a1006-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="a1006-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a1006-119">Página</span><span class="sxs-lookup"><span data-stu-id="a1006-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a1006-120">Notas</span><span class="sxs-lookup"><span data-stu-id="a1006-120">Notes</span></span> <br/>          | <span data-ttu-id="a1006-121">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="a1006-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="a1006-122">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="a1006-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="a1006-123">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="a1006-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="a1006-124">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="a1006-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="a1006-125">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a1006-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a1006-126">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="a1006-126">Structural Content</span></span>

<span data-ttu-id="a1006-127">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="a1006-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a1006-128">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="a1006-128">Structure Variables</span></span>

<span data-ttu-id="a1006-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="a1006-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a1006-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="a1006-130">Name</span></span>                               | <span data-ttu-id="a1006-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a1006-131">Data type</span></span>         | <span data-ttu-id="a1006-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="a1006-132">Unit</span></span>                  | <span data-ttu-id="a1006-133">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="a1006-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a1006-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="a1006-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a1006-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a1006-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a1006-136">string</span><span class="sxs-lookup"><span data-stu-id="a1006-136">string</span></span><br/> | <span data-ttu-id="a1006-137">caracteres</span><span class="sxs-lookup"><span data-stu-id="a1006-137">characters</span></span><br/> | <span data-ttu-id="a1006-138">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a1006-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a1006-139">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a1006-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a1006-140">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="a1006-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a1006-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a1006-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a1006-142">string</span><span class="sxs-lookup"><span data-stu-id="a1006-142">string</span></span><br/> | <span data-ttu-id="a1006-143">N/D</span><span class="sxs-lookup"><span data-stu-id="a1006-143">n/a</span></span><br/>        | <span data-ttu-id="a1006-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="a1006-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a1006-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="a1006-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a1006-146">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a1006-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a1006-147">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="a1006-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a1006-148">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="a1006-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a1006-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1006-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1006-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="a1006-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




