---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6780dd5cc3b90a4f15cb6ada66ab82c4269acd82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914266"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="a0714-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="a0714-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="a0714-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="a0714-105">This topic is not current.</span></span> <span data-ttu-id="a0714-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a0714-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a0714-107">Especifica el origen de una marca de agua en relación con el origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a0714-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="a0714-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a0714-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a0714-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="a0714-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a0714-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a0714-110">Element Information</span></span>



| <span data-ttu-id="a0714-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0714-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="a0714-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a0714-112">Element Type</span></span> <br/>   | <span data-ttu-id="a0714-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a0714-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="a0714-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="a0714-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a0714-115">Página</span><span class="sxs-lookup"><span data-stu-id="a0714-115">Page</span></span><br/>                            |
| <span data-ttu-id="a0714-116">Notas</span><span class="sxs-lookup"><span data-stu-id="a0714-116">Notes</span></span> <br/>          | <span data-ttu-id="a0714-117">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="a0714-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a0714-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="a0714-118">Structure Content</span></span>

<span data-ttu-id="a0714-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="a0714-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="a0714-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="a0714-120">Structure Properties</span></span>

<span data-ttu-id="a0714-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="a0714-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a0714-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0714-122">Property</span></span>                | <span data-ttu-id="a0714-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a0714-123">xsi:type</span></span>           | <span data-ttu-id="a0714-124">Value</span><span class="sxs-lookup"><span data-stu-id="a0714-124">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="a0714-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a0714-125">DataType</span></span><br/>     | <span data-ttu-id="a0714-126">string</span><span class="sxs-lookup"><span data-stu-id="a0714-126">string</span></span><br/>  | <span data-ttu-id="a0714-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a0714-127">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="a0714-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a0714-128">DefaultValue</span></span><br/> | <span data-ttu-id="a0714-129">integer</span><span class="sxs-lookup"><span data-stu-id="a0714-129">integer</span></span><br/> | <span data-ttu-id="a0714-130">no definido</span><span class="sxs-lookup"><span data-stu-id="a0714-130">undefined</span></span><br/>                                                   |
| <span data-ttu-id="a0714-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a0714-131">MaxValue</span></span><br/>     | <span data-ttu-id="a0714-132">integer</span><span class="sxs-lookup"><span data-stu-id="a0714-132">integer</span></span><br/> | <span data-ttu-id="a0714-133">Menor o igual que el valor de PageImageableSize-ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="a0714-133">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="a0714-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="a0714-134">MinValue</span></span><br/>     | <span data-ttu-id="a0714-135">integer</span><span class="sxs-lookup"><span data-stu-id="a0714-135">integer</span></span><br/> | <span data-ttu-id="a0714-136">0</span><span class="sxs-lookup"><span data-stu-id="a0714-136">0</span></span><br/>                                                           |
| <span data-ttu-id="a0714-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="a0714-137">Multiple</span></span><br/>     | <span data-ttu-id="a0714-138">integer</span><span class="sxs-lookup"><span data-stu-id="a0714-138">integer</span></span><br/> | <span data-ttu-id="a0714-139">1</span><span class="sxs-lookup"><span data-stu-id="a0714-139">1</span></span><br/>                                                           |
| <span data-ttu-id="a0714-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="a0714-140">Mandatory</span></span><br/>    | <span data-ttu-id="a0714-141">string</span><span class="sxs-lookup"><span data-stu-id="a0714-141">string</span></span><br/>  | <span data-ttu-id="a0714-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="a0714-142">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="a0714-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="a0714-143">UnitType</span></span><br/>     | <span data-ttu-id="a0714-144">string</span><span class="sxs-lookup"><span data-stu-id="a0714-144">string</span></span><br/>  | <span data-ttu-id="a0714-145">microns</span><span class="sxs-lookup"><span data-stu-id="a0714-145">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="a0714-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0714-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0714-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="a0714-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




