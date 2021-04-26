---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 83626e3c-1ce8-4c91-b656-9f0c06c5b1ec
title: JobPrimaryCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc66aaf769f34eeba943d8a336b3404217f7c2c6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993961"
---
# <a name="jobprimarycoverback"></a><span data-ttu-id="e83f9-104">JobPrimaryCoverBack</span><span class="sxs-lookup"><span data-stu-id="e83f9-104">JobPrimaryCoverBack</span></span>

<span data-ttu-id="e83f9-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e83f9-105">This topic is not current.</span></span> <span data-ttu-id="e83f9-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e83f9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e83f9-107">Describe la hoja de información posterior (final).</span><span class="sxs-lookup"><span data-stu-id="e83f9-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="e83f9-108">Cada trabajo tendrá una hoja principal independiente.</span><span class="sxs-lookup"><span data-stu-id="e83f9-108">Each job will have a separate primary sheet.</span></span> <span data-ttu-id="e83f9-109">La hoja de cobertura se debe imprimir en PageMediaSize y PageMediaType usados para la página final del trabajo.</span><span class="sxs-lookup"><span data-stu-id="e83f9-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the job.</span></span> <span data-ttu-id="e83f9-110">La hoja de cobertura debe integrarse en las opciones de procesamiento (por ejemplo, JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously), como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="e83f9-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="e83f9-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e83f9-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e83f9-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e83f9-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e83f9-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e83f9-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e83f9-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e83f9-114">Element Information</span></span>



| <span data-ttu-id="e83f9-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="e83f9-115">Name</span></span> | <span data-ttu-id="e83f9-116">Value</span><span class="sxs-lookup"><span data-stu-id="e83f9-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e83f9-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e83f9-117">Element Type</span></span> <br/>   | <span data-ttu-id="e83f9-118">Característica</span><span class="sxs-lookup"><span data-stu-id="e83f9-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e83f9-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e83f9-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e83f9-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="e83f9-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e83f9-121">Notas</span><span class="sxs-lookup"><span data-stu-id="e83f9-121">Notes</span></span> <br/>          | <span data-ttu-id="e83f9-122">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="e83f9-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="e83f9-123">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="e83f9-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="e83f9-124">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="e83f9-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="e83f9-125">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="e83f9-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="e83f9-126">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e83f9-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e83f9-127">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e83f9-127">Structural Content</span></span>

<span data-ttu-id="e83f9-128">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e83f9-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
  <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  <!-- Specifies the XPS part name for the back cover sheet. -->
  <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="e83f9-129">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="e83f9-129">Structure Variables</span></span>

<span data-ttu-id="e83f9-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e83f9-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e83f9-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="e83f9-131">Name</span></span>                               | <span data-ttu-id="e83f9-132">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e83f9-132">Data type</span></span>         | <span data-ttu-id="e83f9-133">Unidad</span><span class="sxs-lookup"><span data-stu-id="e83f9-133">Unit</span></span>                  | <span data-ttu-id="e83f9-134">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="e83f9-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e83f9-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="e83f9-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e83f9-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e83f9-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e83f9-137">string</span><span class="sxs-lookup"><span data-stu-id="e83f9-137">string</span></span><br/> | <span data-ttu-id="e83f9-138">caracteres</span><span class="sxs-lookup"><span data-stu-id="e83f9-138">characters</span></span><br/> | <span data-ttu-id="e83f9-139">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e83f9-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e83f9-140">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e83f9-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e83f9-141">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="e83f9-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e83f9-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e83f9-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e83f9-143">string</span><span class="sxs-lookup"><span data-stu-id="e83f9-143">string</span></span><br/> | <span data-ttu-id="e83f9-144">N/D</span><span class="sxs-lookup"><span data-stu-id="e83f9-144">n/a</span></span><br/>        | <span data-ttu-id="e83f9-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="e83f9-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e83f9-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="e83f9-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e83f9-147">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e83f9-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e83f9-148">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="e83f9-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e83f9-149">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="e83f9-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e83f9-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e83f9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e83f9-151">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e83f9-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




