---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d44dbc63632479c66686cea50b781abf715c76
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424155"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="296ff-104">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="296ff-104">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="296ff-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="296ff-105">This topic is not current.</span></span> <span data-ttu-id="296ff-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="296ff-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="296ff-107">Describe el nivel de sombra por debajo del cual se aplicará UCA.</span><span class="sxs-lookup"><span data-stu-id="296ff-107">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="296ff-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="296ff-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="296ff-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="296ff-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="296ff-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="296ff-110">Element Information</span></span>



| <span data-ttu-id="296ff-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="296ff-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="296ff-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="296ff-112">Element Type</span></span> <br/>   | <span data-ttu-id="296ff-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="296ff-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="296ff-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="296ff-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="296ff-115">Página</span><span class="sxs-lookup"><span data-stu-id="296ff-115">Page</span></span><br/>                                            |
| <span data-ttu-id="296ff-116">Notas</span><span class="sxs-lookup"><span data-stu-id="296ff-116">Notes</span></span> <br/>          | <span data-ttu-id="296ff-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="296ff-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="296ff-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="296ff-118">Structure Content</span></span>

<span data-ttu-id="296ff-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="296ff-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="296ff-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="296ff-120">Structure Properties</span></span>

<span data-ttu-id="296ff-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="296ff-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="296ff-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="296ff-122">Property</span></span>                | <span data-ttu-id="296ff-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="296ff-123">xsi:type</span></span>           | <span data-ttu-id="296ff-124">Value</span><span class="sxs-lookup"><span data-stu-id="296ff-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="296ff-125">DataType</span><span class="sxs-lookup"><span data-stu-id="296ff-125">DataType</span></span><br/>     | <span data-ttu-id="296ff-126">string</span><span class="sxs-lookup"><span data-stu-id="296ff-126">string</span></span><br/>  | <span data-ttu-id="296ff-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="296ff-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="296ff-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="296ff-128">DefaultValue</span></span><br/> | <span data-ttu-id="296ff-129">string</span><span class="sxs-lookup"><span data-stu-id="296ff-129">string</span></span><br/>  | <span data-ttu-id="296ff-130">no definido</span><span class="sxs-lookup"><span data-stu-id="296ff-130">undefined</span></span><br/>       |
| <span data-ttu-id="296ff-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="296ff-131">MaxValue</span></span><br/>     | <span data-ttu-id="296ff-132">integer</span><span class="sxs-lookup"><span data-stu-id="296ff-132">integer</span></span><br/> | <span data-ttu-id="296ff-133">100</span><span class="sxs-lookup"><span data-stu-id="296ff-133">100</span></span><br/>             |
| <span data-ttu-id="296ff-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="296ff-134">MinValue</span></span><br/>     | <span data-ttu-id="296ff-135">integer</span><span class="sxs-lookup"><span data-stu-id="296ff-135">integer</span></span><br/> | <span data-ttu-id="296ff-136">0</span><span class="sxs-lookup"><span data-stu-id="296ff-136">0</span></span><br/>               |
| <span data-ttu-id="296ff-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="296ff-137">Multiple</span></span><br/>     | <span data-ttu-id="296ff-138">integer</span><span class="sxs-lookup"><span data-stu-id="296ff-138">integer</span></span><br/> | <span data-ttu-id="296ff-139">1</span><span class="sxs-lookup"><span data-stu-id="296ff-139">1</span></span><br/>               |
| <span data-ttu-id="296ff-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="296ff-140">Mandatory</span></span><br/>    | <span data-ttu-id="296ff-141">string</span><span class="sxs-lookup"><span data-stu-id="296ff-141">string</span></span><br/>  | <span data-ttu-id="296ff-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="296ff-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="296ff-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="296ff-143">UnitType</span></span><br/>     | <span data-ttu-id="296ff-144">string</span><span class="sxs-lookup"><span data-stu-id="296ff-144">string</span></span><br/>  | <span data-ttu-id="296ff-145">percent</span><span class="sxs-lookup"><span data-stu-id="296ff-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="296ff-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="296ff-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="296ff-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="296ff-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




