---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76364aca1a9b6c8019a709c1cd0b7b1ad03020c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997752"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="ccf23-104">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="ccf23-104">JobOutputOptimization</span></span>

<span data-ttu-id="ccf23-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ccf23-105">This topic is not current.</span></span> <span data-ttu-id="ccf23-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ccf23-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ccf23-107">Describe el procesamiento del trabajo, diseñado para optimizar la salida para escenarios de uso concretos, tal como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="ccf23-107">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="ccf23-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ccf23-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ccf23-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ccf23-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ccf23-110">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ccf23-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ccf23-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ccf23-111">Element Information</span></span>



| <span data-ttu-id="ccf23-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccf23-112">Name</span></span> | <span data-ttu-id="ccf23-113">Value</span><span class="sxs-lookup"><span data-stu-id="ccf23-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ccf23-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ccf23-114">Element Type</span></span> <br/>   | <span data-ttu-id="ccf23-115">Característica</span><span class="sxs-lookup"><span data-stu-id="ccf23-115">Feature</span></span><br/> |
| <span data-ttu-id="ccf23-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ccf23-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ccf23-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="ccf23-117">Job</span></span><br/>     |
| <span data-ttu-id="ccf23-118">Notas</span><span class="sxs-lookup"><span data-stu-id="ccf23-118">Notes</span></span> <br/>          | <span data-ttu-id="ccf23-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ccf23-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ccf23-120">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="ccf23-120">Structural Content</span></span>

<span data-ttu-id="ccf23-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="ccf23-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
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

## <a name="structure-variables"></a><span data-ttu-id="ccf23-122">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="ccf23-122">Structure Variables</span></span>

<span data-ttu-id="ccf23-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ccf23-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ccf23-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccf23-124">Name</span></span>                               | <span data-ttu-id="ccf23-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ccf23-125">Data type</span></span>         | <span data-ttu-id="ccf23-126">Unidad</span><span class="sxs-lookup"><span data-stu-id="ccf23-126">Unit</span></span>                  | <span data-ttu-id="ccf23-127">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="ccf23-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ccf23-128">Resumen</span><span class="sxs-lookup"><span data-stu-id="ccf23-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ccf23-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ccf23-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ccf23-130">string</span><span class="sxs-lookup"><span data-stu-id="ccf23-130">string</span></span><br/> | <span data-ttu-id="ccf23-131">caracteres</span><span class="sxs-lookup"><span data-stu-id="ccf23-131">characters</span></span><br/> | <span data-ttu-id="ccf23-132">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ccf23-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ccf23-133">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ccf23-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ccf23-134">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="ccf23-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ccf23-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ccf23-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ccf23-136">string</span><span class="sxs-lookup"><span data-stu-id="ccf23-136">string</span></span><br/> | <span data-ttu-id="ccf23-137">N/D</span><span class="sxs-lookup"><span data-stu-id="ccf23-137">n/a</span></span><br/>        | <span data-ttu-id="ccf23-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="ccf23-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ccf23-139">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="ccf23-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ccf23-140">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ccf23-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ccf23-141">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="ccf23-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ccf23-142">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="ccf23-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="ccf23-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccf23-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccf23-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ccf23-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




