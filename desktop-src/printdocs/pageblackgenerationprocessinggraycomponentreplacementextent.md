---
description: El parámetro PageBlackGenerationProcessingGrayComponentReplacementExtent describe la extensión más allá de los neutros en los colores tic que se aplican a GCR.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3bd5e4fdbafba97884a7aed608b23e4c26ce1c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408508"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="e1ae9-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="e1ae9-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="e1ae9-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e1ae9-104">This topic is not current.</span></span> <span data-ttu-id="e1ae9-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e1ae9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e1ae9-106">Describe la extensión más allá de los neutros (en colores méticos) que se aplica GCR.</span><span class="sxs-lookup"><span data-stu-id="e1ae9-106">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="e1ae9-107">0 % = Reemplazo uniforme de componentes, 100 % = Reemplazo de componente gris.</span><span class="sxs-lookup"><span data-stu-id="e1ae9-107">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="e1ae9-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e1ae9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e1ae9-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e1ae9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e1ae9-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e1ae9-110">Element Information</span></span>



| <span data-ttu-id="e1ae9-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1ae9-111">Name</span></span> | <span data-ttu-id="e1ae9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae9-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="e1ae9-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e1ae9-113">Element Type</span></span> <br/>   | <span data-ttu-id="e1ae9-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e1ae9-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="e1ae9-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e1ae9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e1ae9-116">Página</span><span class="sxs-lookup"><span data-stu-id="e1ae9-116">Page</span></span><br/>                                            |
| <span data-ttu-id="e1ae9-117">Notas</span><span class="sxs-lookup"><span data-stu-id="e1ae9-117">Notes</span></span> <br/>          | <span data-ttu-id="e1ae9-118">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="e1ae9-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e1ae9-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e1ae9-119">Structure Content</span></span>

<span data-ttu-id="e1ae9-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e1ae9-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="e1ae9-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="e1ae9-121">Structure Properties</span></span>

<span data-ttu-id="e1ae9-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e1ae9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e1ae9-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e1ae9-123">Property</span></span>                | <span data-ttu-id="e1ae9-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e1ae9-124">xsi:type</span></span>           | <span data-ttu-id="e1ae9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae9-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e1ae9-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e1ae9-126">DataType</span></span><br/>     | <span data-ttu-id="e1ae9-127">string</span><span class="sxs-lookup"><span data-stu-id="e1ae9-127">string</span></span><br/>  | <span data-ttu-id="e1ae9-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e1ae9-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="e1ae9-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e1ae9-129">DefaultValue</span></span><br/> | <span data-ttu-id="e1ae9-130">string</span><span class="sxs-lookup"><span data-stu-id="e1ae9-130">string</span></span><br/>  | <span data-ttu-id="e1ae9-131">no definido</span><span class="sxs-lookup"><span data-stu-id="e1ae9-131">undefined</span></span><br/>       |
| <span data-ttu-id="e1ae9-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e1ae9-132">MaxValue</span></span><br/>     | <span data-ttu-id="e1ae9-133">integer</span><span class="sxs-lookup"><span data-stu-id="e1ae9-133">integer</span></span><br/> | <span data-ttu-id="e1ae9-134">100</span><span class="sxs-lookup"><span data-stu-id="e1ae9-134">100</span></span><br/>             |
| <span data-ttu-id="e1ae9-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="e1ae9-135">MinValue</span></span><br/>     | <span data-ttu-id="e1ae9-136">integer</span><span class="sxs-lookup"><span data-stu-id="e1ae9-136">integer</span></span><br/> | <span data-ttu-id="e1ae9-137">0</span><span class="sxs-lookup"><span data-stu-id="e1ae9-137">0</span></span><br/>               |
| <span data-ttu-id="e1ae9-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="e1ae9-138">Multiple</span></span><br/>     | <span data-ttu-id="e1ae9-139">integer</span><span class="sxs-lookup"><span data-stu-id="e1ae9-139">integer</span></span><br/> | <span data-ttu-id="e1ae9-140">1</span><span class="sxs-lookup"><span data-stu-id="e1ae9-140">1</span></span><br/>               |
| <span data-ttu-id="e1ae9-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="e1ae9-141">Mandatory</span></span><br/>    | <span data-ttu-id="e1ae9-142">string</span><span class="sxs-lookup"><span data-stu-id="e1ae9-142">string</span></span><br/>  | <span data-ttu-id="e1ae9-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e1ae9-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e1ae9-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="e1ae9-144">UnitType</span></span><br/>     | <span data-ttu-id="e1ae9-145">string</span><span class="sxs-lookup"><span data-stu-id="e1ae9-145">string</span></span><br/>  | <span data-ttu-id="e1ae9-146">percent</span><span class="sxs-lookup"><span data-stu-id="e1ae9-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e1ae9-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1ae9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1ae9-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e1ae9-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




