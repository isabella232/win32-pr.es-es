---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde6077bc2bae611c2a791ecf041cb52588c2ebb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707637"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="bd8c3-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="bd8c3-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="bd8c3-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-105">This topic is not current.</span></span> <span data-ttu-id="bd8c3-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bd8c3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bd8c3-107">Define las características del perfil de color de destino.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="bd8c3-108">Describe si la aplicación o el controlador selecciona el perfil de color de destino que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="bd8c3-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bd8c3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bd8c3-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="bd8c3-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bd8c3-111">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="bd8c3-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bd8c3-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bd8c3-112">Element Information</span></span>



| <span data-ttu-id="bd8c3-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd8c3-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd8c3-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bd8c3-114">Element Type</span></span> <br/>   | <span data-ttu-id="bd8c3-115">Característica</span><span class="sxs-lookup"><span data-stu-id="bd8c3-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bd8c3-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="bd8c3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bd8c3-117">Página</span><span class="sxs-lookup"><span data-stu-id="bd8c3-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bd8c3-118">Notas</span><span class="sxs-lookup"><span data-stu-id="bd8c3-118">Notes</span></span> <br/>          | <span data-ttu-id="bd8c3-119">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="bd8c3-120">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="bd8c3-121">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="bd8c3-122">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="bd8c3-123">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="bd8c3-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="bd8c3-124">Structural Content</span></span>

<span data-ttu-id="bd8c3-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="bd8c3-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="bd8c3-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="bd8c3-126">Structure Variables</span></span>

<span data-ttu-id="bd8c3-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bd8c3-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd8c3-128">Name</span></span>                               | <span data-ttu-id="bd8c3-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bd8c3-129">Data type</span></span>         | <span data-ttu-id="bd8c3-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="bd8c3-130">Unit</span></span>                  | <span data-ttu-id="bd8c3-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="bd8c3-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bd8c3-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="bd8c3-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bd8c3-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="bd8c3-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bd8c3-134">string</span><span class="sxs-lookup"><span data-stu-id="bd8c3-134">string</span></span><br/> | <span data-ttu-id="bd8c3-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="bd8c3-135">characters</span></span><br/> | <span data-ttu-id="bd8c3-136">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="bd8c3-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bd8c3-137">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bd8c3-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="bd8c3-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bd8c3-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bd8c3-140">string</span><span class="sxs-lookup"><span data-stu-id="bd8c3-140">string</span></span><br/> | <span data-ttu-id="bd8c3-141">N/D</span><span class="sxs-lookup"><span data-stu-id="bd8c3-141">n/a</span></span><br/>        | <span data-ttu-id="bd8c3-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bd8c3-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bd8c3-144">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="bd8c3-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bd8c3-145">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="bd8c3-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bd8c3-146">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="bd8c3-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bd8c3-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd8c3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd8c3-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="bd8c3-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




