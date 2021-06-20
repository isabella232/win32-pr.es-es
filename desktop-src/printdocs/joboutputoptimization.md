---
description: Obtenga información sobre JobOutputOptimization, que describe el procesamiento del trabajo, diseñado para optimizar la salida para escenarios de uso determinados, tal como se indica en la opción especificada.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbb65f86b5ed4fd30c056e234b88197d4ab475d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408798"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="46676-103">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="46676-103">JobOutputOptimization</span></span>

<span data-ttu-id="46676-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="46676-104">This topic is not current.</span></span> <span data-ttu-id="46676-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="46676-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="46676-106">Describe el procesamiento del trabajo, diseñado para optimizar la salida para escenarios de uso concretos, tal como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="46676-106">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="46676-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="46676-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="46676-108">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="46676-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="46676-109">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="46676-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="46676-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="46676-110">Element Information</span></span>



| <span data-ttu-id="46676-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="46676-111">Name</span></span> | <span data-ttu-id="46676-112">Valor</span><span class="sxs-lookup"><span data-stu-id="46676-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="46676-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="46676-113">Element Type</span></span> <br/>   | <span data-ttu-id="46676-114">Característica</span><span class="sxs-lookup"><span data-stu-id="46676-114">Feature</span></span><br/> |
| <span data-ttu-id="46676-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="46676-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="46676-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="46676-116">Job</span></span><br/>     |
| <span data-ttu-id="46676-117">Notas</span><span class="sxs-lookup"><span data-stu-id="46676-117">Notes</span></span> <br/>          | <span data-ttu-id="46676-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="46676-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="46676-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="46676-119">Structural Content</span></span>

<span data-ttu-id="46676-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="46676-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="46676-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="46676-121">Structure Variables</span></span>

<span data-ttu-id="46676-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="46676-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="46676-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="46676-123">Name</span></span>                               | <span data-ttu-id="46676-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="46676-124">Data type</span></span>         | <span data-ttu-id="46676-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="46676-125">Unit</span></span>                  | <span data-ttu-id="46676-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="46676-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="46676-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="46676-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="46676-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="46676-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="46676-129">string</span><span class="sxs-lookup"><span data-stu-id="46676-129">string</span></span><br/> | <span data-ttu-id="46676-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="46676-130">characters</span></span><br/> | <span data-ttu-id="46676-131">Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="46676-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="46676-132">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="46676-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="46676-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="46676-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="46676-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="46676-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="46676-135">string</span><span class="sxs-lookup"><span data-stu-id="46676-135">string</span></span><br/> | <span data-ttu-id="46676-136">N/D</span><span class="sxs-lookup"><span data-stu-id="46676-136">n/a</span></span><br/>        | <span data-ttu-id="46676-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="46676-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="46676-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="46676-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="46676-139">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="46676-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="46676-140">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="46676-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="46676-141">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="46676-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="46676-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46676-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46676-143">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="46676-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




