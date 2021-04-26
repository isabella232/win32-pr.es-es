---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf26811bc8c008fa06d647b25e48914a6e724d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999182"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="fbdf7-104">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="fbdf7-104">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="fbdf7-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-105">This topic is not current.</span></span> <span data-ttu-id="fbdf7-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fbdf7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fbdf7-107">Junto con el parámetro PageDeviceColorSpaceProfileURI, este parámetro define el comportamiento de representación de los elementos presentados en un espacio de color del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-107">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="fbdf7-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fbdf7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fbdf7-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="fbdf7-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fbdf7-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fbdf7-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fbdf7-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fbdf7-111">Element Information</span></span>



| <span data-ttu-id="fbdf7-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbdf7-112">Name</span></span> | <span data-ttu-id="fbdf7-113">Value</span><span class="sxs-lookup"><span data-stu-id="fbdf7-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbdf7-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="fbdf7-114">Element Type</span></span> <br/>   | <span data-ttu-id="fbdf7-115">Característica</span><span class="sxs-lookup"><span data-stu-id="fbdf7-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fbdf7-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="fbdf7-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fbdf7-117">Página</span><span class="sxs-lookup"><span data-stu-id="fbdf7-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fbdf7-118">Notas</span><span class="sxs-lookup"><span data-stu-id="fbdf7-118">Notes</span></span> <br/>          | <span data-ttu-id="fbdf7-119">Esto solo se aplica a los documentos XPS y no se debe usar en PrintTickets arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="fbdf7-120">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="fbdf7-121">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="fbdf7-122">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="fbdf7-123">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="fbdf7-124">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="fbdf7-125">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="fbdf7-125">Structural Content</span></span>

<span data-ttu-id="fbdf7-126">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="fbdf7-126">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
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

## <a name="structure-variables"></a><span data-ttu-id="fbdf7-127">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="fbdf7-127">Structure Variables</span></span>

<span data-ttu-id="fbdf7-128">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fbdf7-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbdf7-129">Name</span></span>                               | <span data-ttu-id="fbdf7-130">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fbdf7-130">Data type</span></span>         | <span data-ttu-id="fbdf7-131">Unidad</span><span class="sxs-lookup"><span data-stu-id="fbdf7-131">Unit</span></span>                  | <span data-ttu-id="fbdf7-132">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="fbdf7-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fbdf7-133">Resumen</span><span class="sxs-lookup"><span data-stu-id="fbdf7-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fbdf7-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fbdf7-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="fbdf7-135">string</span><span class="sxs-lookup"><span data-stu-id="fbdf7-135">string</span></span><br/> | <span data-ttu-id="fbdf7-136">caracteres</span><span class="sxs-lookup"><span data-stu-id="fbdf7-136">characters</span></span><br/> | <span data-ttu-id="fbdf7-137">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fbdf7-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fbdf7-138">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fbdf7-139">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="fbdf7-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="fbdf7-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="fbdf7-141">string</span><span class="sxs-lookup"><span data-stu-id="fbdf7-141">string</span></span><br/> | <span data-ttu-id="fbdf7-142">N/D</span><span class="sxs-lookup"><span data-stu-id="fbdf7-142">n/a</span></span><br/>        | <span data-ttu-id="fbdf7-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fbdf7-144">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fbdf7-145">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fbdf7-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fbdf7-146">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="fbdf7-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fbdf7-147">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="fbdf7-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- If the device determines that the profile specified by the PageDeviceColorSpaceProfileURI parameter can be used as a device color space profile, all elements using the same profile are treated as already being specified in device color space. All other elements MUST use the profile specified for that element.
If the profile cannot be used as a device color space profile, elements using the profile MUST be color managed like any other element using the color profile. -->
  <psf:Option name="psk:MatchToDefault" />
  <!-- If the profile specified by the PageDeviceColorSpaceProfileURI parameter has a number of channels matching the number of primaries of the device, it SHOULD be used instead of the devices internal color management for all elements. Elements using this profile are assumed to be in device color space and will not be color managed further. -->
  <psf:Option name="psk:OverrideDeviceDefault" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="fbdf7-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fbdf7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbdf7-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="fbdf7-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




