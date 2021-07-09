---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Revise el parámetro PageBlackGenerationProcessingUnderColorAdditionStart. Este tema no es actual. Para obtener información actual, vea Especificación del esquema de impresión.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbd970f30a7d573b7c803ea447e4ac3e94ca2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549353"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="49920-105">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="49920-105">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="49920-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="49920-106">This topic is not current.</span></span> <span data-ttu-id="49920-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="49920-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="49920-108">Describe el nivel de sombra por debajo del que se aplicará SHADOW.</span><span class="sxs-lookup"><span data-stu-id="49920-108">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="49920-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="49920-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="49920-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="49920-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="49920-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="49920-111">Element Information</span></span>



| <span data-ttu-id="49920-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="49920-112">Name</span></span> | <span data-ttu-id="49920-113">Valor</span><span class="sxs-lookup"><span data-stu-id="49920-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="49920-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="49920-114">Element Type</span></span> <br/>   | <span data-ttu-id="49920-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="49920-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="49920-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="49920-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="49920-117">Página</span><span class="sxs-lookup"><span data-stu-id="49920-117">Page</span></span><br/>                                            |
| <span data-ttu-id="49920-118">Notas</span><span class="sxs-lookup"><span data-stu-id="49920-118">Notes</span></span> <br/>          | <span data-ttu-id="49920-119">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="49920-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="49920-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="49920-120">Structure Content</span></span>

<span data-ttu-id="49920-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="49920-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
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

## <a name="structure-properties"></a><span data-ttu-id="49920-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="49920-122">Structure Properties</span></span>

<span data-ttu-id="49920-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="49920-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="49920-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="49920-124">Property</span></span>                | <span data-ttu-id="49920-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="49920-125">xsi:type</span></span>           | <span data-ttu-id="49920-126">Valor</span><span class="sxs-lookup"><span data-stu-id="49920-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="49920-127">DataType</span><span class="sxs-lookup"><span data-stu-id="49920-127">DataType</span></span><br/>     | <span data-ttu-id="49920-128">string</span><span class="sxs-lookup"><span data-stu-id="49920-128">string</span></span><br/>  | <span data-ttu-id="49920-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="49920-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="49920-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="49920-130">DefaultValue</span></span><br/> | <span data-ttu-id="49920-131">string</span><span class="sxs-lookup"><span data-stu-id="49920-131">string</span></span><br/>  | <span data-ttu-id="49920-132">no definido</span><span class="sxs-lookup"><span data-stu-id="49920-132">undefined</span></span><br/>       |
| <span data-ttu-id="49920-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="49920-133">MaxValue</span></span><br/>     | <span data-ttu-id="49920-134">integer</span><span class="sxs-lookup"><span data-stu-id="49920-134">integer</span></span><br/> | <span data-ttu-id="49920-135">100</span><span class="sxs-lookup"><span data-stu-id="49920-135">100</span></span><br/>             |
| <span data-ttu-id="49920-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="49920-136">MinValue</span></span><br/>     | <span data-ttu-id="49920-137">integer</span><span class="sxs-lookup"><span data-stu-id="49920-137">integer</span></span><br/> | <span data-ttu-id="49920-138">0</span><span class="sxs-lookup"><span data-stu-id="49920-138">0</span></span><br/>               |
| <span data-ttu-id="49920-139">Múltiple</span><span class="sxs-lookup"><span data-stu-id="49920-139">Multiple</span></span><br/>     | <span data-ttu-id="49920-140">integer</span><span class="sxs-lookup"><span data-stu-id="49920-140">integer</span></span><br/> | <span data-ttu-id="49920-141">1</span><span class="sxs-lookup"><span data-stu-id="49920-141">1</span></span><br/>               |
| <span data-ttu-id="49920-142">Mandatory</span><span class="sxs-lookup"><span data-stu-id="49920-142">Mandatory</span></span><br/>    | <span data-ttu-id="49920-143">string</span><span class="sxs-lookup"><span data-stu-id="49920-143">string</span></span><br/>  | <span data-ttu-id="49920-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="49920-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="49920-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="49920-145">UnitType</span></span><br/>     | <span data-ttu-id="49920-146">string</span><span class="sxs-lookup"><span data-stu-id="49920-146">string</span></span><br/>  | <span data-ttu-id="49920-147">percent</span><span class="sxs-lookup"><span data-stu-id="49920-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="49920-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49920-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49920-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="49920-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




