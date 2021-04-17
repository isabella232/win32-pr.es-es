---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac772fdbd9bf378716c42362dc1657a100f1231
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717435"
---
# <a name="documentbannersheet"></a><span data-ttu-id="204dd-104">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="204dd-104">DocumentBannerSheet</span></span>

<span data-ttu-id="204dd-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="204dd-105">This topic is not current.</span></span> <span data-ttu-id="204dd-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="204dd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="204dd-107">Describe la hoja de pancarta que se va a mostrar para un documento determinado.</span><span class="sxs-lookup"><span data-stu-id="204dd-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="204dd-108">La hoja de pancarta se debe mostrar en el valor predeterminado de PageMediaSize, con el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="204dd-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="204dd-109">La hoja de pancarta también debe aislarse del resto del documento.</span><span class="sxs-lookup"><span data-stu-id="204dd-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="204dd-110">Esto significa que las opciones de finalización de documentos o de procesamiento (como DocumentDuplex, DocumentStaple o DocumentBinding) no deben incluir la hoja de pancarta.</span><span class="sxs-lookup"><span data-stu-id="204dd-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="204dd-111">La hoja de pancarta puede estar aislada o no del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="204dd-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="204dd-112">Esto significa que las opciones de finalización de trabajo o procesamiento pueden incluir la hoja de pancarta del documento.</span><span class="sxs-lookup"><span data-stu-id="204dd-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="204dd-113">La hoja de pancarta debe aparecer como la primera hoja del documento.</span><span class="sxs-lookup"><span data-stu-id="204dd-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="204dd-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="204dd-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="204dd-115">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="204dd-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="204dd-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="204dd-116">Element Information</span></span>



| <span data-ttu-id="204dd-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="204dd-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="204dd-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="204dd-118">Element Type</span></span> <br/>   | <span data-ttu-id="204dd-119">Característica</span><span class="sxs-lookup"><span data-stu-id="204dd-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="204dd-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="204dd-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="204dd-121">Documento</span><span class="sxs-lookup"><span data-stu-id="204dd-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="204dd-122">Notas</span><span class="sxs-lookup"><span data-stu-id="204dd-122">Notes</span></span> <br/>          | <span data-ttu-id="204dd-123">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="204dd-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="204dd-124">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="204dd-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="204dd-125">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="204dd-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="204dd-126">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="204dd-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="204dd-127">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="204dd-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="204dd-128">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="204dd-128">Structural Content</span></span>

<span data-ttu-id="204dd-129">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="204dd-129">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="204dd-130">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="204dd-130">Structure Variables</span></span>

<span data-ttu-id="204dd-131">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="204dd-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="204dd-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="204dd-132">Name</span></span>                               | <span data-ttu-id="204dd-133">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="204dd-133">Data type</span></span>         | <span data-ttu-id="204dd-134">Unidad</span><span class="sxs-lookup"><span data-stu-id="204dd-134">Unit</span></span>                   | <span data-ttu-id="204dd-135">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="204dd-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="204dd-136">Resumen</span><span class="sxs-lookup"><span data-stu-id="204dd-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="204dd-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="204dd-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="204dd-138">string</span><span class="sxs-lookup"><span data-stu-id="204dd-138">string</span></span><br/> | <span data-ttu-id="204dd-139">caracteres</span><span class="sxs-lookup"><span data-stu-id="204dd-139">characters</span></span> <br/> | <span data-ttu-id="204dd-140">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="204dd-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="204dd-141">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="204dd-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="204dd-142">El nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="204dd-142">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="204dd-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="204dd-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="204dd-144">string</span><span class="sxs-lookup"><span data-stu-id="204dd-144">string</span></span><br/> | <span data-ttu-id="204dd-145">N/D</span><span class="sxs-lookup"><span data-stu-id="204dd-145">n/a</span></span><br/>         | <span data-ttu-id="204dd-146">True, False</span><span class="sxs-lookup"><span data-stu-id="204dd-146">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="204dd-147">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="204dd-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="204dd-148">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="204dd-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="204dd-149">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="204dd-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="204dd-150">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="204dd-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="204dd-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="204dd-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="204dd-152">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="204dd-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




