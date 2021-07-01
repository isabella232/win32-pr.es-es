---
description: Obtenga información sobre el elemento configurable por el usuario DocumentCoverFront. Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301b67c9a741caa48024646854b208ac5dffbb20
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119830"
---
# <a name="documentcoverfront"></a><span data-ttu-id="4d639-105">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="4d639-105">DocumentCoverFront</span></span>

<span data-ttu-id="4d639-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4d639-106">This topic is not current.</span></span> <span data-ttu-id="4d639-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4d639-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4d639-108">Describe la hoja de cobertura frontal (inicial).</span><span class="sxs-lookup"><span data-stu-id="4d639-108">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="4d639-109">Cada documento tendrá una hoja independiente.</span><span class="sxs-lookup"><span data-stu-id="4d639-109">Each document will have a separate sheet.</span></span> <span data-ttu-id="4d639-110">La hoja de cobertura debe imprimirse en PageMediaSize y PageMediaType usados para la primera página del documento.</span><span class="sxs-lookup"><span data-stu-id="4d639-110">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="4d639-111">La hoja de cobertura debe integrarse en las opciones de procesamiento (como DocumentDuplex o DocumentNUp), tal como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="4d639-111">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="4d639-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4d639-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4d639-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="4d639-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4d639-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4d639-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4d639-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4d639-115">Element Information</span></span>



| <span data-ttu-id="4d639-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d639-116">Name</span></span> | <span data-ttu-id="4d639-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4d639-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d639-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4d639-118">Element Type</span></span> <br/>   | <span data-ttu-id="4d639-119">Característica</span><span class="sxs-lookup"><span data-stu-id="4d639-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4d639-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="4d639-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4d639-121">Documento</span><span class="sxs-lookup"><span data-stu-id="4d639-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4d639-122">Notas</span><span class="sxs-lookup"><span data-stu-id="4d639-122">Notes</span></span> <br/>          | <span data-ttu-id="4d639-123">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="4d639-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="4d639-124">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="4d639-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="4d639-125">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="4d639-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="4d639-126">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="4d639-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="4d639-127">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4d639-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="4d639-128">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="4d639-128">Structural Content</span></span>

<span data-ttu-id="4d639-129">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="4d639-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="4d639-130">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="4d639-130">Structure Variables</span></span>

<span data-ttu-id="4d639-131">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="4d639-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4d639-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d639-132">Name</span></span>                               | <span data-ttu-id="4d639-133">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4d639-133">Data type</span></span>         | <span data-ttu-id="4d639-134">Unidad</span><span class="sxs-lookup"><span data-stu-id="4d639-134">Unit</span></span>                  | <span data-ttu-id="4d639-135">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="4d639-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4d639-136">Resumen</span><span class="sxs-lookup"><span data-stu-id="4d639-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4d639-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="4d639-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4d639-138">string</span><span class="sxs-lookup"><span data-stu-id="4d639-138">string</span></span><br/> | <span data-ttu-id="4d639-139">caracteres</span><span class="sxs-lookup"><span data-stu-id="4d639-139">characters</span></span><br/> | <span data-ttu-id="4d639-140">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="4d639-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4d639-141">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4d639-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4d639-142">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="4d639-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4d639-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4d639-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4d639-144">string</span><span class="sxs-lookup"><span data-stu-id="4d639-144">string</span></span><br/> | <span data-ttu-id="4d639-145">N/D</span><span class="sxs-lookup"><span data-stu-id="4d639-145">n/a</span></span><br/>        | <span data-ttu-id="4d639-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="4d639-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4d639-147">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="4d639-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4d639-148">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4d639-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4d639-149">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="4d639-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4d639-150">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="4d639-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="4d639-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d639-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d639-152">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4d639-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




