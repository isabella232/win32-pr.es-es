---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef9d613bf3b3af980b5cb8e916eac115cd1a0cb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "103914286"
---
# <a name="joberrorsheet"></a><span data-ttu-id="0d458-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="0d458-104">JobErrorSheet</span></span>

<span data-ttu-id="0d458-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="0d458-105">This topic is not current.</span></span> <span data-ttu-id="0d458-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0d458-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0d458-107">Describe la salida de la hoja de errores.</span><span class="sxs-lookup"><span data-stu-id="0d458-107">Describes the error sheet output.</span></span> <span data-ttu-id="0d458-108">Todo el trabajo tendrá una sola hoja de error.</span><span class="sxs-lookup"><span data-stu-id="0d458-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="0d458-109">La hoja de error se debe mostrar en el PageMediaSize predeterminado y usar el valor predeterminado de PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="0d458-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="0d458-110">La hoja de error debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d458-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="0d458-111">Esto significa que las opciones de finalización o procesamiento (como JobDuplex, JobStaple o JobBinding) no deben incluir la hoja de error.</span><span class="sxs-lookup"><span data-stu-id="0d458-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="0d458-112">La hoja de error debe aparecer como la última hoja del trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d458-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="0d458-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0d458-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0d458-114">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0d458-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0d458-115">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="0d458-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0d458-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0d458-116">Element Information</span></span>



| <span data-ttu-id="0d458-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="0d458-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d458-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0d458-118">Element Type</span></span> <br/>   | <span data-ttu-id="0d458-119">Característica</span><span class="sxs-lookup"><span data-stu-id="0d458-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="0d458-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="0d458-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0d458-121">Trabajo</span><span class="sxs-lookup"><span data-stu-id="0d458-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0d458-122">Notas</span><span class="sxs-lookup"><span data-stu-id="0d458-122">Notes</span></span> <br/>          | <span data-ttu-id="0d458-123">Los consumidores compatibles con XPS deben exigir que una referencia de URI a un recurso como un perfil de imagen o de color en un documento de funcionalidades de impresión o en PrintTicket deban hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="0d458-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="0d458-124">Un consumidor XPS compatible no debe usar un URI que no sea compatible con la sintaxis del nombre de la parte.</span><span class="sxs-lookup"><span data-stu-id="0d458-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="0d458-125">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="0d458-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="0d458-126">Los URI a los que se hace referencia en un documento de funcionalidades de impresión o en PrintTicket no se deben resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="0d458-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="0d458-127">Esto no es seguro ya que es posible que no se resuelvan según lo previsto y puede crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0d458-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0d458-128">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0d458-128">Structural Content</span></span>

<span data-ttu-id="0d458-129">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="0d458-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="0d458-130">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="0d458-130">Structure Variables</span></span>

<span data-ttu-id="0d458-131">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="0d458-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0d458-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="0d458-132">Name</span></span>                                             | <span data-ttu-id="0d458-133">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0d458-133">Data type</span></span>         | <span data-ttu-id="0d458-134">Unidad</span><span class="sxs-lookup"><span data-stu-id="0d458-134">Unit</span></span>                  | <span data-ttu-id="0d458-135">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="0d458-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0d458-136">Resumen</span><span class="sxs-lookup"><span data-stu-id="0d458-136">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0d458-137">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="0d458-137">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="0d458-138">string</span><span class="sxs-lookup"><span data-stu-id="0d458-138">string</span></span><br/> | <span data-ttu-id="0d458-139">caracteres</span><span class="sxs-lookup"><span data-stu-id="0d458-139">characters</span></span><br/> | <span data-ttu-id="0d458-140">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0d458-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0d458-141">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0d458-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0d458-142">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="0d458-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0d458-143">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0d458-143">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0d458-144">string</span><span class="sxs-lookup"><span data-stu-id="0d458-144">string</span></span><br/> | <span data-ttu-id="0d458-145">N/D</span><span class="sxs-lookup"><span data-stu-id="0d458-145">n/a</span></span><br/>        | <span data-ttu-id="0d458-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="0d458-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0d458-147">Define los criterios de selección de la interfaz de usuario (IU).</span><span class="sxs-lookup"><span data-stu-id="0d458-147">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="0d458-148">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0d458-148">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="0d458-149">string</span><span class="sxs-lookup"><span data-stu-id="0d458-149">string</span></span><br/> | <span data-ttu-id="0d458-150">N/D</span><span class="sxs-lookup"><span data-stu-id="0d458-150">n/a</span></span><br/>        | <span data-ttu-id="0d458-151">Nombre completo válido, tal y como se define en https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="0d458-151">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="0d458-152">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0d458-152">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="0d458-153">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="0d458-153">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0d458-154">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0d458-154">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="0d458-155">string</span><span class="sxs-lookup"><span data-stu-id="0d458-155">string</span></span><br/> | <span data-ttu-id="0d458-156">N/D</span><span class="sxs-lookup"><span data-stu-id="0d458-156">n/a</span></span><br/>        | <span data-ttu-id="0d458-157">True, False.</span><span class="sxs-lookup"><span data-stu-id="0d458-157">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0d458-158">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="0d458-158">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0d458-159">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="0d458-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0d458-160">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0d458-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0d458-161">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="0d458-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="0d458-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d458-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d458-163">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0d458-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




