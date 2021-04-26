---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c438cd0f33bc7b3a80fc3e654e0d64831e3b6777
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996932"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="9b7c4-104">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="9b7c4-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="9b7c4-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-105">This topic is not current.</span></span> <span data-ttu-id="9b7c4-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9b7c4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9b7c4-107">Describe la hoja de banners que se va a generar para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="9b7c4-108">La hoja de banners debe generarse en el valor predeterminado PageMediaSize y usar el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="9b7c4-109">La hoja de banners debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="9b7c4-110">Esto significa que las opciones de finalización o procesamiento (como JobDuplexAllDocumentsContiguously, JobStapleAllDocuments o JobBindAllDocuments) no deben incluir la hoja de banners.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="9b7c4-111">La hoja de banners debe aparecer como la primera hoja del trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="9b7c4-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9b7c4-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9b7c4-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9b7c4-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9b7c4-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9b7c4-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9b7c4-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9b7c4-115">Element Information</span></span>



| <span data-ttu-id="9b7c4-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b7c4-116">Name</span></span> | <span data-ttu-id="9b7c4-117">Value</span><span class="sxs-lookup"><span data-stu-id="9b7c4-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7c4-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9b7c4-118">Element Type</span></span> <br/>   | <span data-ttu-id="9b7c4-119">Característica</span><span class="sxs-lookup"><span data-stu-id="9b7c4-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9b7c4-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9b7c4-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9b7c4-121">Trabajo</span><span class="sxs-lookup"><span data-stu-id="9b7c4-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9b7c4-122">Notas</span><span class="sxs-lookup"><span data-stu-id="9b7c4-122">Notes</span></span> <br/>          | <span data-ttu-id="9b7c4-123">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="9b7c4-124">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="9b7c4-125">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="9b7c4-126">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="9b7c4-127">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9b7c4-128">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9b7c4-128">Structural Content</span></span>

<span data-ttu-id="9b7c4-129">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9b7c4-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="9b7c4-130">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9b7c4-130">Structure Variables</span></span>

<span data-ttu-id="9b7c4-131">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9b7c4-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b7c4-132">Name</span></span>                               | <span data-ttu-id="9b7c4-133">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9b7c4-133">Data type</span></span>         | <span data-ttu-id="9b7c4-134">Unidad</span><span class="sxs-lookup"><span data-stu-id="9b7c4-134">Unit</span></span>                  | <span data-ttu-id="9b7c4-135">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9b7c4-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9b7c4-136">Resumen</span><span class="sxs-lookup"><span data-stu-id="9b7c4-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9b7c4-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9b7c4-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9b7c4-138">string</span><span class="sxs-lookup"><span data-stu-id="9b7c4-138">string</span></span><br/> | <span data-ttu-id="9b7c4-139">caracteres</span><span class="sxs-lookup"><span data-stu-id="9b7c4-139">characters</span></span><br/> | <span data-ttu-id="9b7c4-140">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9b7c4-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9b7c4-141">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9b7c4-142">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9b7c4-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9b7c4-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9b7c4-144">string</span><span class="sxs-lookup"><span data-stu-id="9b7c4-144">string</span></span><br/> | <span data-ttu-id="9b7c4-145">N/D</span><span class="sxs-lookup"><span data-stu-id="9b7c4-145">n/a</span></span><br/>        | <span data-ttu-id="9b7c4-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9b7c4-147">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9b7c4-148">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9b7c4-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9b7c4-149">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="9b7c4-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9b7c4-150">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9b7c4-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="9b7c4-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b7c4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b7c4-152">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9b7c4-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




