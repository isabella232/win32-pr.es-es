---
description: Obtenga información sobre el elemento configurable por el usuario DocumentBannerSheet. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce05ffae190835e4a8b4082c634b34e26103ab
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548773"
---
# <a name="documentbannersheet"></a><span data-ttu-id="30c89-105">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="30c89-105">DocumentBannerSheet</span></span>

<span data-ttu-id="30c89-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="30c89-106">This topic is not current.</span></span> <span data-ttu-id="30c89-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="30c89-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="30c89-108">Describe la hoja de banners que se va a generar para un documento determinado.</span><span class="sxs-lookup"><span data-stu-id="30c89-108">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="30c89-109">La hoja de banners debe generarse en el valor predeterminado PageMediaSize , utilizando el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="30c89-109">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="30c89-110">La hoja de banners también debe aislarse del resto del documento.</span><span class="sxs-lookup"><span data-stu-id="30c89-110">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="30c89-111">Esto significa que las opciones de finalización o procesamiento de documentos (como DocumentDuplex, DocumentStaple o DocumentBinding) no deben incluir la hoja de banners.</span><span class="sxs-lookup"><span data-stu-id="30c89-111">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="30c89-112">La hoja de banners puede o no estar aislada del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="30c89-112">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="30c89-113">Esto significa que cualquier opción de finalización o procesamiento del trabajo puede incluir la hoja de banners del documento.</span><span class="sxs-lookup"><span data-stu-id="30c89-113">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="30c89-114">La hoja de banners debe aparecer como la primera hoja del documento.</span><span class="sxs-lookup"><span data-stu-id="30c89-114">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="30c89-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="30c89-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="30c89-116">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="30c89-116">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="30c89-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="30c89-117">Element Information</span></span>



| <span data-ttu-id="30c89-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="30c89-118">Name</span></span> | <span data-ttu-id="30c89-119">Valor</span><span class="sxs-lookup"><span data-stu-id="30c89-119">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30c89-120">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="30c89-120">Element Type</span></span> <br/>   | <span data-ttu-id="30c89-121">Característica</span><span class="sxs-lookup"><span data-stu-id="30c89-121">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="30c89-122">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="30c89-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="30c89-123">Documento</span><span class="sxs-lookup"><span data-stu-id="30c89-123">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="30c89-124">Notas</span><span class="sxs-lookup"><span data-stu-id="30c89-124">Notes</span></span> <br/>          | <span data-ttu-id="30c89-125">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="30c89-125">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="30c89-126">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="30c89-126">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="30c89-127">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="30c89-127">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="30c89-128">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="30c89-128">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="30c89-129">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="30c89-129">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="30c89-130">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="30c89-130">Structural Content</span></span>

<span data-ttu-id="30c89-131">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="30c89-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="30c89-132">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="30c89-132">Structure Variables</span></span>

<span data-ttu-id="30c89-133">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="30c89-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="30c89-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="30c89-134">Name</span></span>                               | <span data-ttu-id="30c89-135">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="30c89-135">Data type</span></span>         | <span data-ttu-id="30c89-136">Unidad</span><span class="sxs-lookup"><span data-stu-id="30c89-136">Unit</span></span>                   | <span data-ttu-id="30c89-137">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="30c89-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="30c89-138">Resumen</span><span class="sxs-lookup"><span data-stu-id="30c89-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="30c89-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="30c89-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="30c89-140">string</span><span class="sxs-lookup"><span data-stu-id="30c89-140">string</span></span><br/> | <span data-ttu-id="30c89-141">caracteres</span><span class="sxs-lookup"><span data-stu-id="30c89-141">characters</span></span> <br/> | <span data-ttu-id="30c89-142">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="30c89-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="30c89-143">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="30c89-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="30c89-144">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="30c89-144">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="30c89-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="30c89-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="30c89-146">string</span><span class="sxs-lookup"><span data-stu-id="30c89-146">string</span></span><br/> | <span data-ttu-id="30c89-147">N/D</span><span class="sxs-lookup"><span data-stu-id="30c89-147">n/a</span></span><br/>         | <span data-ttu-id="30c89-148">True, False</span><span class="sxs-lookup"><span data-stu-id="30c89-148">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="30c89-149">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="30c89-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="30c89-150">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="30c89-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="30c89-151">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="30c89-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="30c89-152">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="30c89-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="30c89-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30c89-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30c89-154">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="30c89-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




