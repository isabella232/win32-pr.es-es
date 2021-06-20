---
description: Obtenga información sobre el elemento JobPrimaryBannerSheet, que describe la hoja de banners que se va a generar para el trabajo.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39922f65d71ea0cc6d6de6103bc159f79467038f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408758"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="d7615-103">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="d7615-103">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="d7615-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d7615-104">This topic is not current.</span></span> <span data-ttu-id="d7615-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d7615-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d7615-106">Describe la hoja de banners que se va a generar para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7615-106">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="d7615-107">La hoja de banners debe generarse en el valor predeterminado PageMediaSize y usar el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="d7615-107">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="d7615-108">La hoja de banners debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7615-108">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="d7615-109">Esto significa que las opciones de finalización o procesamiento (como JobDuplexAllDocumentsContiguously, JobStapleAllDocuments o JobBindAllDocuments) no deben incluir la hoja de banners.</span><span class="sxs-lookup"><span data-stu-id="d7615-109">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="d7615-110">La hoja de banners debe aparecer como la primera hoja del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7615-110">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="d7615-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d7615-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d7615-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d7615-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d7615-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d7615-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d7615-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d7615-114">Element Information</span></span>



| <span data-ttu-id="d7615-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7615-115">Name</span></span> | <span data-ttu-id="d7615-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d7615-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7615-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d7615-117">Element Type</span></span> <br/>   | <span data-ttu-id="d7615-118">Característica</span><span class="sxs-lookup"><span data-stu-id="d7615-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d7615-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d7615-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d7615-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="d7615-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d7615-121">Notas</span><span class="sxs-lookup"><span data-stu-id="d7615-121">Notes</span></span> <br/>          | <span data-ttu-id="d7615-122">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="d7615-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="d7615-123">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="d7615-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="d7615-124">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="d7615-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="d7615-125">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="d7615-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="d7615-126">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d7615-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="d7615-127">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d7615-127">Structural Content</span></span>

<span data-ttu-id="d7615-128">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="d7615-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="d7615-129">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="d7615-129">Structure Variables</span></span>

<span data-ttu-id="d7615-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d7615-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d7615-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7615-131">Name</span></span>                               | <span data-ttu-id="d7615-132">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d7615-132">Data type</span></span>         | <span data-ttu-id="d7615-133">Unidad</span><span class="sxs-lookup"><span data-stu-id="d7615-133">Unit</span></span>                  | <span data-ttu-id="d7615-134">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="d7615-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d7615-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="d7615-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d7615-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d7615-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d7615-137">string</span><span class="sxs-lookup"><span data-stu-id="d7615-137">string</span></span><br/> | <span data-ttu-id="d7615-138">caracteres</span><span class="sxs-lookup"><span data-stu-id="d7615-138">characters</span></span><br/> | <span data-ttu-id="d7615-139">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d7615-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d7615-140">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d7615-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d7615-141">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="d7615-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d7615-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d7615-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d7615-143">string</span><span class="sxs-lookup"><span data-stu-id="d7615-143">string</span></span><br/> | <span data-ttu-id="d7615-144">N/D</span><span class="sxs-lookup"><span data-stu-id="d7615-144">n/a</span></span><br/>        | <span data-ttu-id="d7615-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="d7615-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d7615-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="d7615-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d7615-147">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d7615-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d7615-148">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="d7615-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d7615-149">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="d7615-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="d7615-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7615-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7615-151">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d7615-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




