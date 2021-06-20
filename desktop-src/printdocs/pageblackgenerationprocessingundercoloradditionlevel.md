---
description: Obtenga información sobre el elemento PageBlackGenerationProcessingUnderColorAdditionLevel, que describe la cantidad de entrada manuscrita que se va a agregar a las áreas con BlackInkLimit.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b496fbe890f53d1da8d1054cc5a19fe6318811
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408418"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="dd201-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="dd201-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="dd201-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="dd201-104">This topic is not current.</span></span> <span data-ttu-id="dd201-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dd201-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dd201-106">Describe la cantidad de lápiz tótic (en proporción de componentes grises) que se va a agregar a las áreas donde GCR/UCR ha generado "BlackInkLimit" (o IZOStart, si se especifica) en las áreas neutras oscuras y casi neutras.</span><span class="sxs-lookup"><span data-stu-id="dd201-106">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="dd201-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dd201-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dd201-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dd201-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dd201-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dd201-109">Element Information</span></span>



| <span data-ttu-id="dd201-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd201-110">Name</span></span> | <span data-ttu-id="dd201-111">Valor</span><span class="sxs-lookup"><span data-stu-id="dd201-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="dd201-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dd201-112">Element Type</span></span> <br/>   | <span data-ttu-id="dd201-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dd201-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="dd201-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="dd201-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dd201-115">Página</span><span class="sxs-lookup"><span data-stu-id="dd201-115">Page</span></span><br/>                                            |
| <span data-ttu-id="dd201-116">Notas</span><span class="sxs-lookup"><span data-stu-id="dd201-116">Notes</span></span> <br/>          | <span data-ttu-id="dd201-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="dd201-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dd201-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dd201-118">Structure Content</span></span>

<span data-ttu-id="dd201-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="dd201-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="dd201-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="dd201-120">Structure Properties</span></span>

<span data-ttu-id="dd201-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="dd201-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dd201-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dd201-122">Property</span></span>                | <span data-ttu-id="dd201-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dd201-123">xsi:type</span></span>           | <span data-ttu-id="dd201-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dd201-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dd201-125">DataType</span><span class="sxs-lookup"><span data-stu-id="dd201-125">DataType</span></span><br/>     | <span data-ttu-id="dd201-126">string</span><span class="sxs-lookup"><span data-stu-id="dd201-126">string</span></span><br/>  | <span data-ttu-id="dd201-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dd201-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="dd201-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dd201-128">DefaultValue</span></span><br/> | <span data-ttu-id="dd201-129">string</span><span class="sxs-lookup"><span data-stu-id="dd201-129">string</span></span><br/>  | <span data-ttu-id="dd201-130">no definido</span><span class="sxs-lookup"><span data-stu-id="dd201-130">undefined</span></span><br/>       |
| <span data-ttu-id="dd201-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dd201-131">MaxValue</span></span><br/>     | <span data-ttu-id="dd201-132">integer</span><span class="sxs-lookup"><span data-stu-id="dd201-132">integer</span></span><br/> | <span data-ttu-id="dd201-133">100</span><span class="sxs-lookup"><span data-stu-id="dd201-133">100</span></span><br/>             |
| <span data-ttu-id="dd201-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="dd201-134">MinValue</span></span><br/>     | <span data-ttu-id="dd201-135">integer</span><span class="sxs-lookup"><span data-stu-id="dd201-135">integer</span></span><br/> | <span data-ttu-id="dd201-136">0</span><span class="sxs-lookup"><span data-stu-id="dd201-136">0</span></span><br/>               |
| <span data-ttu-id="dd201-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="dd201-137">Multiple</span></span><br/>     | <span data-ttu-id="dd201-138">integer</span><span class="sxs-lookup"><span data-stu-id="dd201-138">integer</span></span><br/> | <span data-ttu-id="dd201-139">1</span><span class="sxs-lookup"><span data-stu-id="dd201-139">1</span></span><br/>               |
| <span data-ttu-id="dd201-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="dd201-140">Mandatory</span></span><br/>    | <span data-ttu-id="dd201-141">string</span><span class="sxs-lookup"><span data-stu-id="dd201-141">string</span></span><br/>  | <span data-ttu-id="dd201-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="dd201-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dd201-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="dd201-143">UnitType</span></span><br/>     | <span data-ttu-id="dd201-144">string</span><span class="sxs-lookup"><span data-stu-id="dd201-144">string</span></span><br/>  | <span data-ttu-id="dd201-145">percent</span><span class="sxs-lookup"><span data-stu-id="dd201-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dd201-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd201-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd201-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="dd201-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




