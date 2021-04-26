---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 595bc3e4514b1a2e8a4d302005b97e2625a560e2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999192"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="87980-104">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="87980-104">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="87980-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="87980-105">This topic is not current.</span></span> <span data-ttu-id="87980-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="87980-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87980-107">Describe el nivel de sombra por debajo del cual se aplicará MICO.</span><span class="sxs-lookup"><span data-stu-id="87980-107">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="87980-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="87980-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87980-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="87980-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="87980-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="87980-110">Element Information</span></span>



| <span data-ttu-id="87980-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="87980-111">Name</span></span> | <span data-ttu-id="87980-112">Value</span><span class="sxs-lookup"><span data-stu-id="87980-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="87980-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="87980-113">Element Type</span></span> <br/>   | <span data-ttu-id="87980-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="87980-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="87980-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="87980-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87980-116">Página</span><span class="sxs-lookup"><span data-stu-id="87980-116">Page</span></span><br/>                                            |
| <span data-ttu-id="87980-117">Notas</span><span class="sxs-lookup"><span data-stu-id="87980-117">Notes</span></span> <br/>          | <span data-ttu-id="87980-118">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="87980-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="87980-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="87980-119">Structure Content</span></span>

<span data-ttu-id="87980-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="87980-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="87980-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="87980-121">Structure Properties</span></span>

<span data-ttu-id="87980-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="87980-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87980-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87980-123">Property</span></span>                | <span data-ttu-id="87980-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="87980-124">xsi:type</span></span>           | <span data-ttu-id="87980-125">Value</span><span class="sxs-lookup"><span data-stu-id="87980-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="87980-126">DataType</span><span class="sxs-lookup"><span data-stu-id="87980-126">DataType</span></span><br/>     | <span data-ttu-id="87980-127">string</span><span class="sxs-lookup"><span data-stu-id="87980-127">string</span></span><br/>  | <span data-ttu-id="87980-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="87980-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="87980-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="87980-129">DefaultValue</span></span><br/> | <span data-ttu-id="87980-130">string</span><span class="sxs-lookup"><span data-stu-id="87980-130">string</span></span><br/>  | <span data-ttu-id="87980-131">no definido</span><span class="sxs-lookup"><span data-stu-id="87980-131">undefined</span></span><br/>       |
| <span data-ttu-id="87980-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="87980-132">MaxValue</span></span><br/>     | <span data-ttu-id="87980-133">integer</span><span class="sxs-lookup"><span data-stu-id="87980-133">integer</span></span><br/> | <span data-ttu-id="87980-134">100</span><span class="sxs-lookup"><span data-stu-id="87980-134">100</span></span><br/>             |
| <span data-ttu-id="87980-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="87980-135">MinValue</span></span><br/>     | <span data-ttu-id="87980-136">integer</span><span class="sxs-lookup"><span data-stu-id="87980-136">integer</span></span><br/> | <span data-ttu-id="87980-137">0</span><span class="sxs-lookup"><span data-stu-id="87980-137">0</span></span><br/>               |
| <span data-ttu-id="87980-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="87980-138">Multiple</span></span><br/>     | <span data-ttu-id="87980-139">integer</span><span class="sxs-lookup"><span data-stu-id="87980-139">integer</span></span><br/> | <span data-ttu-id="87980-140">1</span><span class="sxs-lookup"><span data-stu-id="87980-140">1</span></span><br/>               |
| <span data-ttu-id="87980-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="87980-141">Mandatory</span></span><br/>    | <span data-ttu-id="87980-142">string</span><span class="sxs-lookup"><span data-stu-id="87980-142">string</span></span><br/>  | <span data-ttu-id="87980-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="87980-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="87980-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="87980-144">UnitType</span></span><br/>     | <span data-ttu-id="87980-145">string</span><span class="sxs-lookup"><span data-stu-id="87980-145">string</span></span><br/>  | <span data-ttu-id="87980-146">percent</span><span class="sxs-lookup"><span data-stu-id="87980-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="87980-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87980-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87980-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="87980-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




