---
description: Revise el elemento configurable por el usuario PageDeviceColorSpaceUsage. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b81a37d103d3ce5f1cbb1fb8c032a18d495c2c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396670"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="edea9-105">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="edea9-105">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="edea9-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="edea9-106">This topic is not current.</span></span> <span data-ttu-id="edea9-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="edea9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="edea9-108">Junto con el parámetro PageDeviceColorSpaceProfileURI, este parámetro define el comportamiento de representación de los elementos presentados en un espacio de color del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edea9-108">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="edea9-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="edea9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="edea9-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="edea9-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="edea9-111">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="edea9-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="edea9-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="edea9-112">Element Information</span></span>



| <span data-ttu-id="edea9-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="edea9-113">Name</span></span> | <span data-ttu-id="edea9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="edea9-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edea9-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="edea9-115">Element Type</span></span> <br/>   | <span data-ttu-id="edea9-116">Característica</span><span class="sxs-lookup"><span data-stu-id="edea9-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="edea9-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="edea9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="edea9-118">Página</span><span class="sxs-lookup"><span data-stu-id="edea9-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="edea9-119">Notas</span><span class="sxs-lookup"><span data-stu-id="edea9-119">Notes</span></span> <br/>          | <span data-ttu-id="edea9-120">Esto solo se aplica a los documentos XPS y no se debe usar en PrintTickets arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="edea9-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="edea9-121">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso como una imagen o un perfil de color en un documento de capacidades de impresión o PrintTicket DEBE hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="edea9-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="edea9-122">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="edea9-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="edea9-123">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="edea9-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="edea9-124">Los URI a los que se hace referencia en un documento de capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="edea9-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="edea9-125">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y puedan crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="edea9-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="edea9-126">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="edea9-126">Structural Content</span></span>

<span data-ttu-id="edea9-127">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="edea9-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="edea9-128">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="edea9-128">Structure Variables</span></span>

<span data-ttu-id="edea9-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="edea9-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="edea9-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="edea9-130">Name</span></span>                               | <span data-ttu-id="edea9-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="edea9-131">Data type</span></span>         | <span data-ttu-id="edea9-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="edea9-132">Unit</span></span>                  | <span data-ttu-id="edea9-133">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="edea9-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="edea9-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="edea9-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="edea9-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="edea9-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="edea9-136">string</span><span class="sxs-lookup"><span data-stu-id="edea9-136">string</span></span><br/> | <span data-ttu-id="edea9-137">caracteres</span><span class="sxs-lookup"><span data-stu-id="edea9-137">characters</span></span><br/> | <span data-ttu-id="edea9-138">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="edea9-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="edea9-139">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="edea9-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="edea9-140">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="edea9-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="edea9-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="edea9-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="edea9-142">string</span><span class="sxs-lookup"><span data-stu-id="edea9-142">string</span></span><br/> | <span data-ttu-id="edea9-143">N/D</span><span class="sxs-lookup"><span data-stu-id="edea9-143">n/a</span></span><br/>        | <span data-ttu-id="edea9-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="edea9-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="edea9-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="edea9-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="edea9-146">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="edea9-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="edea9-147">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="edea9-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="edea9-148">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="edea9-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="edea9-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edea9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edea9-150">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="edea9-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




