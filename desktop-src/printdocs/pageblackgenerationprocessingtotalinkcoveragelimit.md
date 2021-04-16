---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07566926c2115855ea7321af90e7d1caebcd0a82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105670109"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="8d22a-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="8d22a-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="8d22a-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="8d22a-105">This topic is not current.</span></span> <span data-ttu-id="8d22a-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8d22a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8d22a-107">Especifica la suma máxima permitida de las cuatro coberturas de tinta en cualquier parte de una imagen.</span><span class="sxs-lookup"><span data-stu-id="8d22a-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="8d22a-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8d22a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8d22a-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="8d22a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8d22a-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8d22a-110">Element Information</span></span>



| <span data-ttu-id="8d22a-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="8d22a-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="8d22a-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8d22a-112">Element Type</span></span> <br/>   | <span data-ttu-id="8d22a-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8d22a-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="8d22a-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="8d22a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8d22a-115">Página</span><span class="sxs-lookup"><span data-stu-id="8d22a-115">Page</span></span><br/>                                            |
| <span data-ttu-id="8d22a-116">Notas</span><span class="sxs-lookup"><span data-stu-id="8d22a-116">Notes</span></span> <br/>          | <span data-ttu-id="8d22a-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="8d22a-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8d22a-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="8d22a-118">Structure Content</span></span>

<span data-ttu-id="8d22a-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="8d22a-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8d22a-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="8d22a-120">Structure Properties</span></span>

<span data-ttu-id="8d22a-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="8d22a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8d22a-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d22a-122">Property</span></span>                | <span data-ttu-id="8d22a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8d22a-123">xsi:type</span></span>           | <span data-ttu-id="8d22a-124">Value</span><span class="sxs-lookup"><span data-stu-id="8d22a-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8d22a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="8d22a-125">DataType</span></span><br/>     | <span data-ttu-id="8d22a-126">string</span><span class="sxs-lookup"><span data-stu-id="8d22a-126">string</span></span><br/>  | <span data-ttu-id="8d22a-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8d22a-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="8d22a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8d22a-128">DefaultValue</span></span><br/> | <span data-ttu-id="8d22a-129">string</span><span class="sxs-lookup"><span data-stu-id="8d22a-129">string</span></span><br/>  | <span data-ttu-id="8d22a-130">no definido</span><span class="sxs-lookup"><span data-stu-id="8d22a-130">undefined</span></span><br/>       |
| <span data-ttu-id="8d22a-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8d22a-131">MaxValue</span></span><br/>     | <span data-ttu-id="8d22a-132">integer</span><span class="sxs-lookup"><span data-stu-id="8d22a-132">integer</span></span><br/> | <span data-ttu-id="8d22a-133">400</span><span class="sxs-lookup"><span data-stu-id="8d22a-133">400</span></span><br/>             |
| <span data-ttu-id="8d22a-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="8d22a-134">MinValue</span></span><br/>     | <span data-ttu-id="8d22a-135">integer</span><span class="sxs-lookup"><span data-stu-id="8d22a-135">integer</span></span><br/> | <span data-ttu-id="8d22a-136">200</span><span class="sxs-lookup"><span data-stu-id="8d22a-136">200</span></span><br/>             |
| <span data-ttu-id="8d22a-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="8d22a-137">Multiple</span></span><br/>     | <span data-ttu-id="8d22a-138">integer</span><span class="sxs-lookup"><span data-stu-id="8d22a-138">integer</span></span><br/> | <span data-ttu-id="8d22a-139">1</span><span class="sxs-lookup"><span data-stu-id="8d22a-139">1</span></span><br/>               |
| <span data-ttu-id="8d22a-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="8d22a-140">Mandatory</span></span><br/>    | <span data-ttu-id="8d22a-141">string</span><span class="sxs-lookup"><span data-stu-id="8d22a-141">string</span></span><br/>  | <span data-ttu-id="8d22a-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="8d22a-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8d22a-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="8d22a-143">UnitType</span></span><br/>     | <span data-ttu-id="8d22a-144">string</span><span class="sxs-lookup"><span data-stu-id="8d22a-144">string</span></span><br/>  | <span data-ttu-id="8d22a-145">percent</span><span class="sxs-lookup"><span data-stu-id="8d22a-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8d22a-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d22a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d22a-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8d22a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




