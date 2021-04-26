---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ffb70ba0ac1a78eefc1024d8e93dc642439aed
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998432"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="d0b91-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="d0b91-104">JobAccountingSheet</span></span>

<span data-ttu-id="d0b91-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d0b91-105">This topic is not current.</span></span> <span data-ttu-id="d0b91-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d0b91-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d0b91-107">Describe la hoja de contabilidad que se va a generar para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d0b91-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="d0b91-108">La hoja de contabilidad debe generarse en el valor predeterminado PageMediaSize y usar el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="d0b91-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="d0b91-109">La hoja de contabilidad debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d0b91-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="d0b91-110">Esto significa que las opciones de finalización o procesamiento (como JobDuplex, JobStaple o JobBinding) no deben incluir la hoja de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d0b91-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="d0b91-111">La hoja de contabilidad puede aparecer como la primera o la última página del trabajo a discreción del implementador.</span><span class="sxs-lookup"><span data-stu-id="d0b91-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="d0b91-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d0b91-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d0b91-113">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d0b91-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d0b91-114">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d0b91-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d0b91-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d0b91-115">Element Information</span></span>



| <span data-ttu-id="d0b91-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0b91-116">Name</span></span> | <span data-ttu-id="d0b91-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0b91-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="d0b91-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d0b91-118">Element Type</span></span> <br/>   | <span data-ttu-id="d0b91-119">Característica</span><span class="sxs-lookup"><span data-stu-id="d0b91-119">Feature</span></span><br/> |
| <span data-ttu-id="d0b91-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d0b91-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d0b91-121">Trabajo</span><span class="sxs-lookup"><span data-stu-id="d0b91-121">Job</span></span><br/>     |
| <span data-ttu-id="d0b91-122">Notas</span><span class="sxs-lookup"><span data-stu-id="d0b91-122">Notes</span></span> <br/>          | <span data-ttu-id="d0b91-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d0b91-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d0b91-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="d0b91-124">Structural Content</span></span>

<span data-ttu-id="d0b91-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="d0b91-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="d0b91-126">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="d0b91-126">Structure Variables</span></span>

<span data-ttu-id="d0b91-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d0b91-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d0b91-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0b91-128">Name</span></span>                               | <span data-ttu-id="d0b91-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d0b91-129">Data type</span></span>         | <span data-ttu-id="d0b91-130">Unidad</span><span class="sxs-lookup"><span data-stu-id="d0b91-130">Unit</span></span>                  | <span data-ttu-id="d0b91-131">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="d0b91-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d0b91-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="d0b91-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d0b91-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d0b91-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d0b91-134">string</span><span class="sxs-lookup"><span data-stu-id="d0b91-134">string</span></span><br/> | <span data-ttu-id="d0b91-135">caracteres</span><span class="sxs-lookup"><span data-stu-id="d0b91-135">characters</span></span><br/> | <span data-ttu-id="d0b91-136">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="d0b91-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d0b91-137">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d0b91-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d0b91-138">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="d0b91-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d0b91-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d0b91-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d0b91-140">string</span><span class="sxs-lookup"><span data-stu-id="d0b91-140">string</span></span><br/> | <span data-ttu-id="d0b91-141">N/D</span><span class="sxs-lookup"><span data-stu-id="d0b91-141">n/a</span></span><br/>        | <span data-ttu-id="d0b91-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="d0b91-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d0b91-143">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="d0b91-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d0b91-144">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d0b91-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d0b91-145">Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="d0b91-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d0b91-146">El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="d0b91-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="d0b91-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0b91-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0b91-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d0b91-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




