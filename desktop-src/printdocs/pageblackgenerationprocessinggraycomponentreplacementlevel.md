---
description: Obtenga información sobre el elemento PageBlackGenerationProcessingGrayComponentReplacementLevel, que especifica el porcentaje de reemplazo de componentes grises.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8499c8521b974d01657c171a99e86e738c82b4e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408488"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="67f8a-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="67f8a-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="67f8a-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="67f8a-104">This topic is not current.</span></span> <span data-ttu-id="67f8a-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="67f8a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="67f8a-106">Especifica el porcentaje de reemplazo de componentes grises que se realizará.</span><span class="sxs-lookup"><span data-stu-id="67f8a-106">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="67f8a-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="67f8a-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="67f8a-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="67f8a-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="67f8a-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="67f8a-109">Element Information</span></span>



| <span data-ttu-id="67f8a-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="67f8a-110">Name</span></span> | <span data-ttu-id="67f8a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="67f8a-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="67f8a-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="67f8a-112">Element Type</span></span> <br/>   | <span data-ttu-id="67f8a-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="67f8a-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="67f8a-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="67f8a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="67f8a-115">Página</span><span class="sxs-lookup"><span data-stu-id="67f8a-115">Page</span></span><br/>                                            |
| <span data-ttu-id="67f8a-116">Notas</span><span class="sxs-lookup"><span data-stu-id="67f8a-116">Notes</span></span> <br/>          | <span data-ttu-id="67f8a-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="67f8a-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="67f8a-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="67f8a-118">Structure Content</span></span>

<span data-ttu-id="67f8a-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="67f8a-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="67f8a-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="67f8a-120">Structure Properties</span></span>

<span data-ttu-id="67f8a-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="67f8a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="67f8a-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67f8a-122">Property</span></span>                | <span data-ttu-id="67f8a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="67f8a-123">xsi:type</span></span>           | <span data-ttu-id="67f8a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="67f8a-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="67f8a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="67f8a-125">DataType</span></span><br/>     | <span data-ttu-id="67f8a-126">string</span><span class="sxs-lookup"><span data-stu-id="67f8a-126">string</span></span><br/>  | <span data-ttu-id="67f8a-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="67f8a-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="67f8a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="67f8a-128">DefaultValue</span></span><br/> | <span data-ttu-id="67f8a-129">string</span><span class="sxs-lookup"><span data-stu-id="67f8a-129">string</span></span><br/>  | <span data-ttu-id="67f8a-130">no definido</span><span class="sxs-lookup"><span data-stu-id="67f8a-130">undefined</span></span><br/>       |
| <span data-ttu-id="67f8a-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="67f8a-131">MaxValue</span></span><br/>     | <span data-ttu-id="67f8a-132">integer</span><span class="sxs-lookup"><span data-stu-id="67f8a-132">integer</span></span><br/> | <span data-ttu-id="67f8a-133">100</span><span class="sxs-lookup"><span data-stu-id="67f8a-133">100</span></span><br/>             |
| <span data-ttu-id="67f8a-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="67f8a-134">MinValue</span></span><br/>     | <span data-ttu-id="67f8a-135">integer</span><span class="sxs-lookup"><span data-stu-id="67f8a-135">integer</span></span><br/> | <span data-ttu-id="67f8a-136">0</span><span class="sxs-lookup"><span data-stu-id="67f8a-136">0</span></span><br/>               |
| <span data-ttu-id="67f8a-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="67f8a-137">Multiple</span></span><br/>     | <span data-ttu-id="67f8a-138">integer</span><span class="sxs-lookup"><span data-stu-id="67f8a-138">integer</span></span><br/> | <span data-ttu-id="67f8a-139">1</span><span class="sxs-lookup"><span data-stu-id="67f8a-139">1</span></span><br/>               |
| <span data-ttu-id="67f8a-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="67f8a-140">Mandatory</span></span><br/>    | <span data-ttu-id="67f8a-141">string</span><span class="sxs-lookup"><span data-stu-id="67f8a-141">string</span></span><br/>  | <span data-ttu-id="67f8a-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="67f8a-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="67f8a-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="67f8a-143">UnitType</span></span><br/>     | <span data-ttu-id="67f8a-144">string</span><span class="sxs-lookup"><span data-stu-id="67f8a-144">string</span></span><br/>  | <span data-ttu-id="67f8a-145">percent</span><span class="sxs-lookup"><span data-stu-id="67f8a-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="67f8a-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67f8a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67f8a-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="67f8a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




