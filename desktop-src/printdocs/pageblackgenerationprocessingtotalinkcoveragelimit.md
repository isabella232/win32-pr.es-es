---
description: Obtenga información sobre el elemento PageBlackGenerationProcessingTotalInkCoverageLimit, que especifica la suma máxima permitida de la cobertura de lápiz de cuatro en cualquier lugar de una imagen.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408448"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="1794c-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="1794c-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="1794c-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1794c-104">This topic is not current.</span></span> <span data-ttu-id="1794c-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1794c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1794c-106">Especifica la suma máxima permitida de la cobertura de lápiz de cuatro en cualquier lugar de una imagen.</span><span class="sxs-lookup"><span data-stu-id="1794c-106">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="1794c-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1794c-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1794c-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="1794c-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1794c-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1794c-109">Element Information</span></span>



| <span data-ttu-id="1794c-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="1794c-110">Name</span></span> | <span data-ttu-id="1794c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1794c-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1794c-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1794c-112">Element Type</span></span> <br/>   | <span data-ttu-id="1794c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1794c-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1794c-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1794c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1794c-115">Página</span><span class="sxs-lookup"><span data-stu-id="1794c-115">Page</span></span><br/>                                            |
| <span data-ttu-id="1794c-116">Notas</span><span class="sxs-lookup"><span data-stu-id="1794c-116">Notes</span></span> <br/>          | <span data-ttu-id="1794c-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="1794c-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1794c-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="1794c-118">Structure Content</span></span>

<span data-ttu-id="1794c-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="1794c-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1794c-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="1794c-120">Structure Properties</span></span>

<span data-ttu-id="1794c-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1794c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1794c-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1794c-122">Property</span></span>                | <span data-ttu-id="1794c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1794c-123">xsi:type</span></span>           | <span data-ttu-id="1794c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1794c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1794c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="1794c-125">DataType</span></span><br/>     | <span data-ttu-id="1794c-126">string</span><span class="sxs-lookup"><span data-stu-id="1794c-126">string</span></span><br/>  | <span data-ttu-id="1794c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1794c-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="1794c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1794c-128">DefaultValue</span></span><br/> | <span data-ttu-id="1794c-129">string</span><span class="sxs-lookup"><span data-stu-id="1794c-129">string</span></span><br/>  | <span data-ttu-id="1794c-130">no definido</span><span class="sxs-lookup"><span data-stu-id="1794c-130">undefined</span></span><br/>       |
| <span data-ttu-id="1794c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1794c-131">MaxValue</span></span><br/>     | <span data-ttu-id="1794c-132">integer</span><span class="sxs-lookup"><span data-stu-id="1794c-132">integer</span></span><br/> | <span data-ttu-id="1794c-133">400</span><span class="sxs-lookup"><span data-stu-id="1794c-133">400</span></span><br/>             |
| <span data-ttu-id="1794c-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="1794c-134">MinValue</span></span><br/>     | <span data-ttu-id="1794c-135">integer</span><span class="sxs-lookup"><span data-stu-id="1794c-135">integer</span></span><br/> | <span data-ttu-id="1794c-136">200</span><span class="sxs-lookup"><span data-stu-id="1794c-136">200</span></span><br/>             |
| <span data-ttu-id="1794c-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="1794c-137">Multiple</span></span><br/>     | <span data-ttu-id="1794c-138">integer</span><span class="sxs-lookup"><span data-stu-id="1794c-138">integer</span></span><br/> | <span data-ttu-id="1794c-139">1</span><span class="sxs-lookup"><span data-stu-id="1794c-139">1</span></span><br/>               |
| <span data-ttu-id="1794c-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="1794c-140">Mandatory</span></span><br/>    | <span data-ttu-id="1794c-141">string</span><span class="sxs-lookup"><span data-stu-id="1794c-141">string</span></span><br/>  | <span data-ttu-id="1794c-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="1794c-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1794c-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="1794c-143">UnitType</span></span><br/>     | <span data-ttu-id="1794c-144">string</span><span class="sxs-lookup"><span data-stu-id="1794c-144">string</span></span><br/>  | <span data-ttu-id="1794c-145">percent</span><span class="sxs-lookup"><span data-stu-id="1794c-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1794c-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1794c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1794c-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1794c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




