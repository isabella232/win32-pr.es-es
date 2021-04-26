---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef61001e45178989d6f89e17d8cc38b82c1354
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996312"
---
# <a name="documentbannersheet"></a><span data-ttu-id="2ccdc-104">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="2ccdc-104">DocumentBannerSheet</span></span>

<span data-ttu-id="2ccdc-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-105">This topic is not current.</span></span> <span data-ttu-id="2ccdc-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2ccdc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2ccdc-107">Describe la hoja de banners que se va a generar para un documento determinado.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="2ccdc-108">La hoja de banners debe generarse en el valor predeterminado PageMediaSize , utilizando el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="2ccdc-109">La hoja de banners también debe aislarse del resto del documento.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="2ccdc-110">Esto significa que las opciones de finalización o procesamiento de documentos (como DocumentDuplex, DocumentStaple o DocumentBinding) no deben incluir la hoja de banners.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="2ccdc-111">La hoja de banners puede o no aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="2ccdc-112">Esto significa que cualquier opción de finalización o procesamiento de trabajos puede incluir la hoja de banners del documento.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="2ccdc-113">La hoja de banners debe aparecer como la primera hoja del documento.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="2ccdc-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2ccdc-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2ccdc-115">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="2ccdc-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="2ccdc-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2ccdc-116">Element Information</span></span>



| <span data-ttu-id="2ccdc-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ccdc-117">Name</span></span> | <span data-ttu-id="2ccdc-118">Value</span><span class="sxs-lookup"><span data-stu-id="2ccdc-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ccdc-119">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2ccdc-119">Element Type</span></span> <br/>   | <span data-ttu-id="2ccdc-120">Característica</span><span class="sxs-lookup"><span data-stu-id="2ccdc-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2ccdc-121">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2ccdc-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2ccdc-122">Documento</span><span class="sxs-lookup"><span data-stu-id="2ccdc-122">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="2ccdc-123">Notas</span><span class="sxs-lookup"><span data-stu-id="2ccdc-123">Notes</span></span> <br/>          | <span data-ttu-id="2ccdc-124">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="2ccdc-125">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="2ccdc-126">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="2ccdc-127">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="2ccdc-128">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="2ccdc-129">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="2ccdc-129">Structural Content</span></span>

<span data-ttu-id="2ccdc-130">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2ccdc-130">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2ccdc-131">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="2ccdc-131">Structure Variables</span></span>

<span data-ttu-id="2ccdc-132">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2ccdc-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ccdc-133">Name</span></span>                               | <span data-ttu-id="2ccdc-134">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2ccdc-134">Data type</span></span>         | <span data-ttu-id="2ccdc-135">Unidad</span><span class="sxs-lookup"><span data-stu-id="2ccdc-135">Unit</span></span>                   | <span data-ttu-id="2ccdc-136">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="2ccdc-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2ccdc-137">Resumen</span><span class="sxs-lookup"><span data-stu-id="2ccdc-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2ccdc-138">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2ccdc-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2ccdc-139">string</span><span class="sxs-lookup"><span data-stu-id="2ccdc-139">string</span></span><br/> | <span data-ttu-id="2ccdc-140">caracteres</span><span class="sxs-lookup"><span data-stu-id="2ccdc-140">characters</span></span> <br/> | <span data-ttu-id="2ccdc-141">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="2ccdc-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2ccdc-142">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2ccdc-143">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="2ccdc-143">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="2ccdc-144">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2ccdc-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2ccdc-145">string</span><span class="sxs-lookup"><span data-stu-id="2ccdc-145">string</span></span><br/> | <span data-ttu-id="2ccdc-146">N/D</span><span class="sxs-lookup"><span data-stu-id="2ccdc-146">n/a</span></span><br/>         | <span data-ttu-id="2ccdc-147">True, False</span><span class="sxs-lookup"><span data-stu-id="2ccdc-147">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="2ccdc-148">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="2ccdc-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2ccdc-149">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2ccdc-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2ccdc-150">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="2ccdc-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2ccdc-151">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="2ccdc-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2ccdc-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ccdc-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ccdc-153">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2ccdc-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




