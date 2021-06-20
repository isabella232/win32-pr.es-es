---
description: Obtenga información sobre el elemento PageBlackGenerationProcessingGrayComponentReplacementStart, que describe el punto donde se debe iniciar GCR.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e7e5a7e22c20b15dc373a2cce2bfe19e3417d4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408468"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="1157d-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="1157d-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="1157d-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1157d-104">This topic is not current.</span></span> <span data-ttu-id="1157d-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1157d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1157d-106">Describe el punto del intervalo de "resaltado a sombra" donde debe iniciarse GCR (sombra 100 % más oscura).</span><span class="sxs-lookup"><span data-stu-id="1157d-106">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="1157d-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1157d-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1157d-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="1157d-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1157d-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1157d-109">Element Information</span></span>



| <span data-ttu-id="1157d-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="1157d-110">Name</span></span> | <span data-ttu-id="1157d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1157d-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1157d-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1157d-112">Element Type</span></span> <br/>   | <span data-ttu-id="1157d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1157d-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1157d-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1157d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1157d-115">Página</span><span class="sxs-lookup"><span data-stu-id="1157d-115">Page</span></span><br/>                                            |
| <span data-ttu-id="1157d-116">Notas</span><span class="sxs-lookup"><span data-stu-id="1157d-116">Notes</span></span> <br/>          | <span data-ttu-id="1157d-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="1157d-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1157d-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="1157d-118">Structure Content</span></span>

<span data-ttu-id="1157d-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="1157d-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a><span data-ttu-id="1157d-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="1157d-120">Structure Properties</span></span>

<span data-ttu-id="1157d-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1157d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1157d-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1157d-122">Property</span></span>                | <span data-ttu-id="1157d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1157d-123">xsi:type</span></span>           | <span data-ttu-id="1157d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1157d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1157d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="1157d-125">DataType</span></span><br/>     | <span data-ttu-id="1157d-126">string</span><span class="sxs-lookup"><span data-stu-id="1157d-126">string</span></span><br/>  | <span data-ttu-id="1157d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1157d-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="1157d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1157d-128">DefaultValue</span></span><br/> | <span data-ttu-id="1157d-129">string</span><span class="sxs-lookup"><span data-stu-id="1157d-129">string</span></span><br/>  | <span data-ttu-id="1157d-130">no definido</span><span class="sxs-lookup"><span data-stu-id="1157d-130">undefined</span></span><br/>       |
| <span data-ttu-id="1157d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1157d-131">MaxValue</span></span><br/>     | <span data-ttu-id="1157d-132">integer</span><span class="sxs-lookup"><span data-stu-id="1157d-132">integer</span></span><br/> | <span data-ttu-id="1157d-133">100</span><span class="sxs-lookup"><span data-stu-id="1157d-133">100</span></span><br/>             |
| <span data-ttu-id="1157d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="1157d-134">MinValue</span></span><br/>     | <span data-ttu-id="1157d-135">integer</span><span class="sxs-lookup"><span data-stu-id="1157d-135">integer</span></span><br/> | <span data-ttu-id="1157d-136">0</span><span class="sxs-lookup"><span data-stu-id="1157d-136">0</span></span><br/>               |
| <span data-ttu-id="1157d-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="1157d-137">Multiple</span></span><br/>     | <span data-ttu-id="1157d-138">integer</span><span class="sxs-lookup"><span data-stu-id="1157d-138">integer</span></span><br/> | <span data-ttu-id="1157d-139">1</span><span class="sxs-lookup"><span data-stu-id="1157d-139">1</span></span><br/>               |
| <span data-ttu-id="1157d-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="1157d-140">Mandatory</span></span><br/>    | <span data-ttu-id="1157d-141">string</span><span class="sxs-lookup"><span data-stu-id="1157d-141">string</span></span><br/>  | <span data-ttu-id="1157d-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="1157d-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1157d-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="1157d-143">UnitType</span></span><br/>     | <span data-ttu-id="1157d-144">string</span><span class="sxs-lookup"><span data-stu-id="1157d-144">string</span></span><br/>  | <span data-ttu-id="1157d-145">percent</span><span class="sxs-lookup"><span data-stu-id="1157d-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1157d-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1157d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1157d-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1157d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




