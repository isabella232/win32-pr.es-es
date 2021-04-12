---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6d906833dc067155c9d98d50ed47e898a446e2
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104361980"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="e400d-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="e400d-104">JobAccountingSheet</span></span>

<span data-ttu-id="e400d-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="e400d-105">This topic is not current.</span></span> <span data-ttu-id="e400d-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e400d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e400d-107">Describe la hoja de contabilidad que se va a mostrar para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="e400d-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="e400d-108">La hoja de contabilidad se debe mostrar en el PageMediaSize predeterminado y usar el valor predeterminado de PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="e400d-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="e400d-109">La hoja de contabilidad debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="e400d-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="e400d-110">Esto significa que las opciones de finalización o procesamiento (como JobDuplex, JobStaple o JobBinding) no deben incluir la hoja de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e400d-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="e400d-111">La hoja de contabilidad puede aparecer como la primera o la última página del trabajo a discreción del implementador.</span><span class="sxs-lookup"><span data-stu-id="e400d-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="e400d-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e400d-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e400d-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e400d-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e400d-114">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="e400d-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e400d-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e400d-115">Element Information</span></span>



| <span data-ttu-id="e400d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e400d-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="e400d-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e400d-117">Element Type</span></span> <br/>   | <span data-ttu-id="e400d-118">Característica</span><span class="sxs-lookup"><span data-stu-id="e400d-118">Feature</span></span><br/> |
| <span data-ttu-id="e400d-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e400d-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e400d-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="e400d-120">Job</span></span><br/>     |
| <span data-ttu-id="e400d-121">Notas</span><span class="sxs-lookup"><span data-stu-id="e400d-121">Notes</span></span> <br/>          | <span data-ttu-id="e400d-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e400d-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e400d-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="e400d-123">Structural Content</span></span>

<span data-ttu-id="e400d-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e400d-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="e400d-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="e400d-125">Structure Variables</span></span>

<span data-ttu-id="e400d-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e400d-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e400d-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e400d-127">Name</span></span>                               | <span data-ttu-id="e400d-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e400d-128">Data type</span></span>         | <span data-ttu-id="e400d-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="e400d-129">Unit</span></span>                  | <span data-ttu-id="e400d-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="e400d-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e400d-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="e400d-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e400d-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e400d-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e400d-133">string</span><span class="sxs-lookup"><span data-stu-id="e400d-133">string</span></span><br/> | <span data-ttu-id="e400d-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="e400d-134">characters</span></span><br/> | <span data-ttu-id="e400d-135">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e400d-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e400d-136">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e400d-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e400d-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="e400d-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e400d-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e400d-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e400d-139">string</span><span class="sxs-lookup"><span data-stu-id="e400d-139">string</span></span><br/> | <span data-ttu-id="e400d-140">N/D</span><span class="sxs-lookup"><span data-stu-id="e400d-140">n/a</span></span><br/>        | <span data-ttu-id="e400d-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="e400d-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e400d-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="e400d-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e400d-143">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="e400d-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e400d-144">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e400d-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e400d-145">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="e400d-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a><span data-ttu-id="e400d-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e400d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e400d-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e400d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




