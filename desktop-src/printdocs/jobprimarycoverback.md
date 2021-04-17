---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 83626e3c-1ce8-4c91-b656-9f0c06c5b1ec
title: JobPrimaryCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073e65f80c3bee31423d0cf813d454a32e6f559b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105698036"
---
# <a name="jobprimarycoverback"></a><span data-ttu-id="9d0e9-104">JobPrimaryCoverBack</span><span class="sxs-lookup"><span data-stu-id="9d0e9-104">JobPrimaryCoverBack</span></span>

<span data-ttu-id="9d0e9-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-105">This topic is not current.</span></span> <span data-ttu-id="9d0e9-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9d0e9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9d0e9-107">Describe la portada (final).</span><span class="sxs-lookup"><span data-stu-id="9d0e9-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="9d0e9-108">Cada trabajo tendrá una hoja principal independiente.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-108">Each job will have a separate primary sheet.</span></span> <span data-ttu-id="9d0e9-109">La portada debe imprimirse en las PageMediaSize y PageMediaType que se usan para la página final del trabajo.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the job.</span></span> <span data-ttu-id="9d0e9-110">La portada debe integrarse en las opciones de procesamiento (como JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) tal y como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="9d0e9-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9d0e9-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9d0e9-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9d0e9-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9d0e9-113">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="9d0e9-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9d0e9-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9d0e9-114">Element Information</span></span>



| <span data-ttu-id="9d0e9-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d0e9-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0e9-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9d0e9-116">Element Type</span></span> <br/>   | <span data-ttu-id="9d0e9-117">Característica</span><span class="sxs-lookup"><span data-stu-id="9d0e9-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d0e9-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9d0e9-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9d0e9-119">Trabajo</span><span class="sxs-lookup"><span data-stu-id="9d0e9-119">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d0e9-120">Notas</span><span class="sxs-lookup"><span data-stu-id="9d0e9-120">Notes</span></span> <br/>          | <span data-ttu-id="9d0e9-121">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="9d0e9-122">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="9d0e9-123">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="9d0e9-124">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="9d0e9-125">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="9d0e9-126">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="9d0e9-126">Structural Content</span></span>

<span data-ttu-id="9d0e9-127">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9d0e9-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9d0e9-128">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="9d0e9-128">Structure Variables</span></span>

<span data-ttu-id="9d0e9-129">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9d0e9-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d0e9-130">Name</span></span>                               | <span data-ttu-id="9d0e9-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9d0e9-131">Data type</span></span>         | <span data-ttu-id="9d0e9-132">Unidad</span><span class="sxs-lookup"><span data-stu-id="9d0e9-132">Unit</span></span>                  | <span data-ttu-id="9d0e9-133">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="9d0e9-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9d0e9-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="9d0e9-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9d0e9-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9d0e9-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9d0e9-136">string</span><span class="sxs-lookup"><span data-stu-id="9d0e9-136">string</span></span><br/> | <span data-ttu-id="9d0e9-137">caracteres</span><span class="sxs-lookup"><span data-stu-id="9d0e9-137">characters</span></span><br/> | <span data-ttu-id="9d0e9-138">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9d0e9-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9d0e9-139">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9d0e9-140">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9d0e9-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9d0e9-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9d0e9-142">string</span><span class="sxs-lookup"><span data-stu-id="9d0e9-142">string</span></span><br/> | <span data-ttu-id="9d0e9-143">N/D</span><span class="sxs-lookup"><span data-stu-id="9d0e9-143">n/a</span></span><br/>        | <span data-ttu-id="9d0e9-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9d0e9-145">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9d0e9-146">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="9d0e9-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9d0e9-147">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9d0e9-148">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="9d0e9-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9d0e9-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d0e9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d0e9-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9d0e9-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




