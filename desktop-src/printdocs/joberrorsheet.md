---
description: Obtenga información sobre el elemento JobErrorSheet, que describe la salida de la hoja de errores. Todo el trabajo tendrá una sola hoja de errores.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcee6c50d482793eeef96e29ad98385da11a4e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408908"
---
# <a name="joberrorsheet"></a><span data-ttu-id="0a2bd-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="0a2bd-104">JobErrorSheet</span></span>

<span data-ttu-id="0a2bd-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-105">This topic is not current.</span></span> <span data-ttu-id="0a2bd-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0a2bd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0a2bd-107">Describe la salida de la hoja de errores.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-107">Describes the error sheet output.</span></span> <span data-ttu-id="0a2bd-108">Todo el trabajo tendrá una sola hoja de errores.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="0a2bd-109">La hoja de errores debe generarse en el valor predeterminado PageMediaSize y usar el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="0a2bd-110">La hoja de errores debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="0a2bd-111">Esto significa que las opciones de finalización o procesamiento (como JobDuplex, JobStaple o JobBinding) no deben incluir la hoja de errores.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="0a2bd-112">La hoja de errores debe producirse como hoja final del trabajo.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="0a2bd-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0a2bd-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0a2bd-114">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0a2bd-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0a2bd-115">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0a2bd-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0a2bd-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0a2bd-116">Element Information</span></span>



| <span data-ttu-id="0a2bd-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a2bd-117">Name</span></span> | <span data-ttu-id="0a2bd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0a2bd-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2bd-119">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0a2bd-119">Element Type</span></span> <br/>   | <span data-ttu-id="0a2bd-120">Característica</span><span class="sxs-lookup"><span data-stu-id="0a2bd-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="0a2bd-121">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="0a2bd-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0a2bd-122">Trabajo</span><span class="sxs-lookup"><span data-stu-id="0a2bd-122">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0a2bd-123">Notas</span><span class="sxs-lookup"><span data-stu-id="0a2bd-123">Notes</span></span> <br/>          | <span data-ttu-id="0a2bd-124">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="0a2bd-125">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="0a2bd-126">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="0a2bd-127">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="0a2bd-128">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0a2bd-129">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="0a2bd-129">Structural Content</span></span>

<span data-ttu-id="0a2bd-130">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="0a2bd-130">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0a2bd-131">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="0a2bd-131">Structure Variables</span></span>

<span data-ttu-id="0a2bd-132">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0a2bd-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a2bd-133">Name</span></span>                                             | <span data-ttu-id="0a2bd-134">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0a2bd-134">Data type</span></span>         | <span data-ttu-id="0a2bd-135">Unidad</span><span class="sxs-lookup"><span data-stu-id="0a2bd-135">Unit</span></span>                  | <span data-ttu-id="0a2bd-136">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="0a2bd-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0a2bd-137">Resumen</span><span class="sxs-lookup"><span data-stu-id="0a2bd-137">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0a2bd-138">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="0a2bd-138">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="0a2bd-139">string</span><span class="sxs-lookup"><span data-stu-id="0a2bd-139">string</span></span><br/> | <span data-ttu-id="0a2bd-140">caracteres</span><span class="sxs-lookup"><span data-stu-id="0a2bd-140">characters</span></span><br/> | <span data-ttu-id="0a2bd-141">Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0a2bd-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0a2bd-142">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0a2bd-143">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0a2bd-144">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0a2bd-144">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0a2bd-145">string</span><span class="sxs-lookup"><span data-stu-id="0a2bd-145">string</span></span><br/> | <span data-ttu-id="0a2bd-146">N/D</span><span class="sxs-lookup"><span data-stu-id="0a2bd-146">n/a</span></span><br/>        | <span data-ttu-id="0a2bd-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0a2bd-148">Define los criterios de selección de la interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="0a2bd-148">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="0a2bd-149">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0a2bd-149">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="0a2bd-150">string</span><span class="sxs-lookup"><span data-stu-id="0a2bd-150">string</span></span><br/> | <span data-ttu-id="0a2bd-151">N/D</span><span class="sxs-lookup"><span data-stu-id="0a2bd-151">n/a</span></span><br/>        | <span data-ttu-id="0a2bd-152">Nombre completo válido tal y como se define en https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="0a2bd-152">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="0a2bd-153">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-153">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="0a2bd-154">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-154">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0a2bd-155">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0a2bd-155">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="0a2bd-156">string</span><span class="sxs-lookup"><span data-stu-id="0a2bd-156">string</span></span><br/> | <span data-ttu-id="0a2bd-157">N/D</span><span class="sxs-lookup"><span data-stu-id="0a2bd-157">n/a</span></span><br/>        | <span data-ttu-id="0a2bd-158">True, False.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-158">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0a2bd-159">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="0a2bd-159">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0a2bd-160">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0a2bd-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0a2bd-161">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="0a2bd-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0a2bd-162">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="0a2bd-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0a2bd-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a2bd-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a2bd-164">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0a2bd-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




