---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b143ea6a3e1edd667d56619c190d99d1de93496f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717441"
---
# <a name="documentcoverfront"></a><span data-ttu-id="40d0c-104">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="40d0c-104">DocumentCoverFront</span></span>

<span data-ttu-id="40d0c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="40d0c-105">This topic is not current.</span></span> <span data-ttu-id="40d0c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="40d0c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="40d0c-107">Describe la portada delantera (a partir de).</span><span class="sxs-lookup"><span data-stu-id="40d0c-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="40d0c-108">Cada documento tendrá una hoja independiente.</span><span class="sxs-lookup"><span data-stu-id="40d0c-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="40d0c-109">La portada debe imprimirse en los PageMediaSize y PageMediaType usados para la primera página del documento.</span><span class="sxs-lookup"><span data-stu-id="40d0c-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="40d0c-110">La portada debe integrarse en las opciones de procesamiento (como DocumentDuplex, DocumentNUp) tal y como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="40d0c-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="40d0c-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="40d0c-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="40d0c-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="40d0c-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="40d0c-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="40d0c-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="40d0c-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="40d0c-114">Element Information</span></span>



| <span data-ttu-id="40d0c-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="40d0c-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40d0c-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="40d0c-116">Element Type</span></span> <br/>   | <span data-ttu-id="40d0c-117">Característica</span><span class="sxs-lookup"><span data-stu-id="40d0c-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="40d0c-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="40d0c-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="40d0c-119">Documento</span><span class="sxs-lookup"><span data-stu-id="40d0c-119">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="40d0c-120">Notas</span><span class="sxs-lookup"><span data-stu-id="40d0c-120">Notes</span></span> <br/>          | <span data-ttu-id="40d0c-121">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="40d0c-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="40d0c-122">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="40d0c-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="40d0c-123">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="40d0c-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="40d0c-124">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="40d0c-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="40d0c-125">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="40d0c-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="40d0c-126">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="40d0c-126">Structural Content</span></span>

<span data-ttu-id="40d0c-127">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="40d0c-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="40d0c-128">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="40d0c-128">Structure Variables</span></span>

<span data-ttu-id="40d0c-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="40d0c-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="40d0c-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="40d0c-130">Name</span></span>                               | <span data-ttu-id="40d0c-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="40d0c-131">Data type</span></span>         | <span data-ttu-id="40d0c-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="40d0c-132">Unit</span></span>                  | <span data-ttu-id="40d0c-133">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="40d0c-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="40d0c-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="40d0c-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="40d0c-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="40d0c-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="40d0c-136">string</span><span class="sxs-lookup"><span data-stu-id="40d0c-136">string</span></span><br/> | <span data-ttu-id="40d0c-137">caracteres</span><span class="sxs-lookup"><span data-stu-id="40d0c-137">characters</span></span><br/> | <span data-ttu-id="40d0c-138">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="40d0c-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="40d0c-139">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40d0c-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="40d0c-140">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="40d0c-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="40d0c-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="40d0c-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="40d0c-142">string</span><span class="sxs-lookup"><span data-stu-id="40d0c-142">string</span></span><br/> | <span data-ttu-id="40d0c-143">N/D</span><span class="sxs-lookup"><span data-stu-id="40d0c-143">n/a</span></span><br/>        | <span data-ttu-id="40d0c-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="40d0c-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="40d0c-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="40d0c-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="40d0c-146">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="40d0c-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="40d0c-147">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="40d0c-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="40d0c-148">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="40d0c-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="40d0c-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40d0c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40d0c-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="40d0c-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




