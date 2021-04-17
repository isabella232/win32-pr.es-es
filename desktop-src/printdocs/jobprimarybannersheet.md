---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc44973b06dc99c86ca9d50717ca9bf2b6335fa
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717439"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="6e6ca-104">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="6e6ca-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="6e6ca-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-105">This topic is not current.</span></span> <span data-ttu-id="6e6ca-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6e6ca-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6e6ca-107">Describe la hoja de pancarta que se va a mostrar para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="6e6ca-108">La hoja de pancarta se debe mostrar en el PageMediaSize predeterminado y usar el valor predeterminado de PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="6e6ca-109">La hoja de pancarta debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="6e6ca-110">Esto significa que las opciones de finalización o procesamiento (como JobDuplexAllDocumentsContiguously, JobStapleAllDocuments o JobBindAllDocuments) no deben incluir la hoja de pancarta.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="6e6ca-111">La hoja de pancarta debe aparecer como la primera hoja del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="6e6ca-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6e6ca-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6e6ca-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6e6ca-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6e6ca-114">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="6e6ca-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6e6ca-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6e6ca-115">Element Information</span></span>



| <span data-ttu-id="6e6ca-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6e6ca-116">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6ca-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6e6ca-117">Element Type</span></span> <br/>   | <span data-ttu-id="6e6ca-118">Característica</span><span class="sxs-lookup"><span data-stu-id="6e6ca-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6e6ca-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="6e6ca-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6e6ca-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="6e6ca-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6e6ca-121">Notas</span><span class="sxs-lookup"><span data-stu-id="6e6ca-121">Notes</span></span> <br/>          | <span data-ttu-id="6e6ca-122">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="6e6ca-123">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="6e6ca-124">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="6e6ca-125">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="6e6ca-126">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6e6ca-127">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="6e6ca-127">Structural Content</span></span>

<span data-ttu-id="6e6ca-128">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="6e6ca-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="6e6ca-129">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="6e6ca-129">Structure Variables</span></span>

<span data-ttu-id="6e6ca-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6e6ca-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="6e6ca-131">Name</span></span>                               | <span data-ttu-id="6e6ca-132">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6e6ca-132">Data type</span></span>         | <span data-ttu-id="6e6ca-133">Unidad</span><span class="sxs-lookup"><span data-stu-id="6e6ca-133">Unit</span></span>                  | <span data-ttu-id="6e6ca-134">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="6e6ca-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6e6ca-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="6e6ca-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6e6ca-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6e6ca-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6e6ca-137">string</span><span class="sxs-lookup"><span data-stu-id="6e6ca-137">string</span></span><br/> | <span data-ttu-id="6e6ca-138">caracteres</span><span class="sxs-lookup"><span data-stu-id="6e6ca-138">characters</span></span><br/> | <span data-ttu-id="6e6ca-139">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6e6ca-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6e6ca-140">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6e6ca-141">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6e6ca-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6e6ca-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6e6ca-143">string</span><span class="sxs-lookup"><span data-stu-id="6e6ca-143">string</span></span><br/> | <span data-ttu-id="6e6ca-144">N/D</span><span class="sxs-lookup"><span data-stu-id="6e6ca-144">n/a</span></span><br/>        | <span data-ttu-id="6e6ca-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6e6ca-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6e6ca-147">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="6e6ca-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6e6ca-148">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="6e6ca-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6e6ca-149">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="6e6ca-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6e6ca-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e6ca-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e6ca-151">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6e6ca-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




