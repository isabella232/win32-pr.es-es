---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fb6866dae4eb4a39de5c2b3b5d678a7388d703
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279885"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="20237-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="20237-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="20237-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="20237-105">This topic is not current.</span></span> <span data-ttu-id="20237-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="20237-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="20237-107">Describe la cantidad de tinta cromática (en relación con el componente gris) que se va a agregar a las áreas en las que GCR/UCR ha generado "BlackInkLimit" (o UCAStart, si se ha especificado) en las áreas neutras oscuras y casi neutras.</span><span class="sxs-lookup"><span data-stu-id="20237-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="20237-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="20237-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="20237-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="20237-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="20237-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="20237-110">Element Information</span></span>



| <span data-ttu-id="20237-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="20237-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="20237-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="20237-112">Element Type</span></span> <br/>   | <span data-ttu-id="20237-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="20237-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="20237-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="20237-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="20237-115">Página</span><span class="sxs-lookup"><span data-stu-id="20237-115">Page</span></span><br/>                                            |
| <span data-ttu-id="20237-116">Notas</span><span class="sxs-lookup"><span data-stu-id="20237-116">Notes</span></span> <br/>          | <span data-ttu-id="20237-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="20237-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="20237-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="20237-118">Structure Content</span></span>

<span data-ttu-id="20237-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="20237-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="20237-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="20237-120">Structure Properties</span></span>

<span data-ttu-id="20237-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="20237-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="20237-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20237-122">Property</span></span>                | <span data-ttu-id="20237-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="20237-123">xsi:type</span></span>           | <span data-ttu-id="20237-124">Value</span><span class="sxs-lookup"><span data-stu-id="20237-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="20237-125">DataType</span><span class="sxs-lookup"><span data-stu-id="20237-125">DataType</span></span><br/>     | <span data-ttu-id="20237-126">string</span><span class="sxs-lookup"><span data-stu-id="20237-126">string</span></span><br/>  | <span data-ttu-id="20237-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="20237-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="20237-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="20237-128">DefaultValue</span></span><br/> | <span data-ttu-id="20237-129">string</span><span class="sxs-lookup"><span data-stu-id="20237-129">string</span></span><br/>  | <span data-ttu-id="20237-130">no definido</span><span class="sxs-lookup"><span data-stu-id="20237-130">undefined</span></span><br/>       |
| <span data-ttu-id="20237-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="20237-131">MaxValue</span></span><br/>     | <span data-ttu-id="20237-132">integer</span><span class="sxs-lookup"><span data-stu-id="20237-132">integer</span></span><br/> | <span data-ttu-id="20237-133">100</span><span class="sxs-lookup"><span data-stu-id="20237-133">100</span></span><br/>             |
| <span data-ttu-id="20237-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="20237-134">MinValue</span></span><br/>     | <span data-ttu-id="20237-135">integer</span><span class="sxs-lookup"><span data-stu-id="20237-135">integer</span></span><br/> | <span data-ttu-id="20237-136">0</span><span class="sxs-lookup"><span data-stu-id="20237-136">0</span></span><br/>               |
| <span data-ttu-id="20237-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="20237-137">Multiple</span></span><br/>     | <span data-ttu-id="20237-138">integer</span><span class="sxs-lookup"><span data-stu-id="20237-138">integer</span></span><br/> | <span data-ttu-id="20237-139">1</span><span class="sxs-lookup"><span data-stu-id="20237-139">1</span></span><br/>               |
| <span data-ttu-id="20237-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="20237-140">Mandatory</span></span><br/>    | <span data-ttu-id="20237-141">string</span><span class="sxs-lookup"><span data-stu-id="20237-141">string</span></span><br/>  | <span data-ttu-id="20237-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="20237-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="20237-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="20237-143">UnitType</span></span><br/>     | <span data-ttu-id="20237-144">string</span><span class="sxs-lookup"><span data-stu-id="20237-144">string</span></span><br/>  | <span data-ttu-id="20237-145">percent</span><span class="sxs-lookup"><span data-stu-id="20237-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="20237-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20237-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20237-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="20237-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




