---
description: Obtenga información sobre el elemento JobAccountingSheet, que describe la hoja de contabilidad que se va a generar para el trabajo.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499d78db7a967e256ee79cd6e0c35d2f7d59dff4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409099"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="74433-103">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="74433-103">JobAccountingSheet</span></span>

<span data-ttu-id="74433-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="74433-104">This topic is not current.</span></span> <span data-ttu-id="74433-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74433-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74433-106">Describe la hoja de contabilidad que se va a generar para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="74433-106">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="74433-107">La hoja de contabilidad debe generarse en el valor predeterminado PageMediaSize y usar el valor predeterminado PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="74433-107">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="74433-108">La hoja de contabilidad debe aislarse del resto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="74433-108">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="74433-109">Esto significa que las opciones de finalización o procesamiento (como JobDuplex, JobStaple o JobBinding) no deben incluir la hoja de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="74433-109">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="74433-110">La hoja de contabilidad puede aparecer como la primera o la última página del trabajo a discreción del implementador.</span><span class="sxs-lookup"><span data-stu-id="74433-110">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="74433-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="74433-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="74433-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="74433-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="74433-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="74433-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="74433-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="74433-114">Element Information</span></span>



| <span data-ttu-id="74433-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="74433-115">Name</span></span> | <span data-ttu-id="74433-116">Valor</span><span class="sxs-lookup"><span data-stu-id="74433-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="74433-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="74433-117">Element Type</span></span> <br/>   | <span data-ttu-id="74433-118">Característica</span><span class="sxs-lookup"><span data-stu-id="74433-118">Feature</span></span><br/> |
| <span data-ttu-id="74433-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="74433-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="74433-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="74433-120">Job</span></span><br/>     |
| <span data-ttu-id="74433-121">Notas</span><span class="sxs-lookup"><span data-stu-id="74433-121">Notes</span></span> <br/>          | <span data-ttu-id="74433-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="74433-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="74433-123">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="74433-123">Structural Content</span></span>

<span data-ttu-id="74433-124">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="74433-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="74433-125">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="74433-125">Structure Variables</span></span>

<span data-ttu-id="74433-126">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="74433-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="74433-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="74433-127">Name</span></span>                               | <span data-ttu-id="74433-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="74433-128">Data type</span></span>         | <span data-ttu-id="74433-129">Unidad</span><span class="sxs-lookup"><span data-stu-id="74433-129">Unit</span></span>                  | <span data-ttu-id="74433-130">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="74433-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="74433-131">Resumen</span><span class="sxs-lookup"><span data-stu-id="74433-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="74433-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="74433-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="74433-133">string</span><span class="sxs-lookup"><span data-stu-id="74433-133">string</span></span><br/> | <span data-ttu-id="74433-134">caracteres</span><span class="sxs-lookup"><span data-stu-id="74433-134">characters</span></span><br/> | <span data-ttu-id="74433-135">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="74433-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="74433-136">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="74433-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="74433-137">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="74433-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="74433-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="74433-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="74433-139">string</span><span class="sxs-lookup"><span data-stu-id="74433-139">string</span></span><br/> | <span data-ttu-id="74433-140">N/D</span><span class="sxs-lookup"><span data-stu-id="74433-140">n/a</span></span><br/>        | <span data-ttu-id="74433-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="74433-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="74433-142">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="74433-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="74433-143">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="74433-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="74433-144">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="74433-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="74433-145">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="74433-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="74433-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74433-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74433-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="74433-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




