---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993882"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="ae36a-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="ae36a-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="ae36a-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ae36a-105">This topic is not current.</span></span> <span data-ttu-id="ae36a-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ae36a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ae36a-107">Especifica la suma máxima permitida de la cobertura de lápiz de cuatro en cualquier lugar de una imagen.</span><span class="sxs-lookup"><span data-stu-id="ae36a-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="ae36a-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ae36a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ae36a-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ae36a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ae36a-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ae36a-110">Element Information</span></span>



| <span data-ttu-id="ae36a-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae36a-111">Name</span></span> | <span data-ttu-id="ae36a-112">Value</span><span class="sxs-lookup"><span data-stu-id="ae36a-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="ae36a-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ae36a-113">Element Type</span></span> <br/>   | <span data-ttu-id="ae36a-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ae36a-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="ae36a-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ae36a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ae36a-116">Página</span><span class="sxs-lookup"><span data-stu-id="ae36a-116">Page</span></span><br/>                                            |
| <span data-ttu-id="ae36a-117">Notas</span><span class="sxs-lookup"><span data-stu-id="ae36a-117">Notes</span></span> <br/>          | <span data-ttu-id="ae36a-118">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="ae36a-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ae36a-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ae36a-119">Structure Content</span></span>

<span data-ttu-id="ae36a-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="ae36a-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="ae36a-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="ae36a-121">Structure Properties</span></span>

<span data-ttu-id="ae36a-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ae36a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ae36a-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae36a-123">Property</span></span>                | <span data-ttu-id="ae36a-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ae36a-124">xsi:type</span></span>           | <span data-ttu-id="ae36a-125">Value</span><span class="sxs-lookup"><span data-stu-id="ae36a-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ae36a-126">DataType</span><span class="sxs-lookup"><span data-stu-id="ae36a-126">DataType</span></span><br/>     | <span data-ttu-id="ae36a-127">string</span><span class="sxs-lookup"><span data-stu-id="ae36a-127">string</span></span><br/>  | <span data-ttu-id="ae36a-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ae36a-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="ae36a-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ae36a-129">DefaultValue</span></span><br/> | <span data-ttu-id="ae36a-130">string</span><span class="sxs-lookup"><span data-stu-id="ae36a-130">string</span></span><br/>  | <span data-ttu-id="ae36a-131">no definido</span><span class="sxs-lookup"><span data-stu-id="ae36a-131">undefined</span></span><br/>       |
| <span data-ttu-id="ae36a-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ae36a-132">MaxValue</span></span><br/>     | <span data-ttu-id="ae36a-133">integer</span><span class="sxs-lookup"><span data-stu-id="ae36a-133">integer</span></span><br/> | <span data-ttu-id="ae36a-134">400</span><span class="sxs-lookup"><span data-stu-id="ae36a-134">400</span></span><br/>             |
| <span data-ttu-id="ae36a-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="ae36a-135">MinValue</span></span><br/>     | <span data-ttu-id="ae36a-136">integer</span><span class="sxs-lookup"><span data-stu-id="ae36a-136">integer</span></span><br/> | <span data-ttu-id="ae36a-137">200</span><span class="sxs-lookup"><span data-stu-id="ae36a-137">200</span></span><br/>             |
| <span data-ttu-id="ae36a-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="ae36a-138">Multiple</span></span><br/>     | <span data-ttu-id="ae36a-139">integer</span><span class="sxs-lookup"><span data-stu-id="ae36a-139">integer</span></span><br/> | <span data-ttu-id="ae36a-140">1</span><span class="sxs-lookup"><span data-stu-id="ae36a-140">1</span></span><br/>               |
| <span data-ttu-id="ae36a-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="ae36a-141">Mandatory</span></span><br/>    | <span data-ttu-id="ae36a-142">string</span><span class="sxs-lookup"><span data-stu-id="ae36a-142">string</span></span><br/>  | <span data-ttu-id="ae36a-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="ae36a-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ae36a-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="ae36a-144">UnitType</span></span><br/>     | <span data-ttu-id="ae36a-145">string</span><span class="sxs-lookup"><span data-stu-id="ae36a-145">string</span></span><br/>  | <span data-ttu-id="ae36a-146">percent</span><span class="sxs-lookup"><span data-stu-id="ae36a-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ae36a-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae36a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae36a-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ae36a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




