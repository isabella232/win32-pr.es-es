---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78cf29952258a7c6c3489d40291ba8cd4b756c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996072"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="37edc-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="37edc-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="37edc-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="37edc-105">This topic is not current.</span></span> <span data-ttu-id="37edc-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="37edc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="37edc-107">Especifica el origen de una marca de agua relativa al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="37edc-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="37edc-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="37edc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="37edc-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="37edc-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="37edc-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="37edc-110">Element Information</span></span>



| <span data-ttu-id="37edc-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="37edc-111">Name</span></span> | <span data-ttu-id="37edc-112">Value</span><span class="sxs-lookup"><span data-stu-id="37edc-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="37edc-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="37edc-113">Element Type</span></span> <br/>   | <span data-ttu-id="37edc-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="37edc-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="37edc-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="37edc-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="37edc-116">Página</span><span class="sxs-lookup"><span data-stu-id="37edc-116">Page</span></span><br/>                            |
| <span data-ttu-id="37edc-117">Notas</span><span class="sxs-lookup"><span data-stu-id="37edc-117">Notes</span></span> <br/>          | <span data-ttu-id="37edc-118">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="37edc-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="37edc-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="37edc-119">Structure Content</span></span>

<span data-ttu-id="37edc-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="37edc-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="37edc-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="37edc-121">Structure Properties</span></span>

<span data-ttu-id="37edc-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="37edc-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="37edc-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37edc-123">Property</span></span>                | <span data-ttu-id="37edc-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="37edc-124">xsi:type</span></span>           | <span data-ttu-id="37edc-125">Value</span><span class="sxs-lookup"><span data-stu-id="37edc-125">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="37edc-126">DataType</span><span class="sxs-lookup"><span data-stu-id="37edc-126">DataType</span></span><br/>     | <span data-ttu-id="37edc-127">string</span><span class="sxs-lookup"><span data-stu-id="37edc-127">string</span></span><br/>  | <span data-ttu-id="37edc-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="37edc-128">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="37edc-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="37edc-129">DefaultValue</span></span><br/> | <span data-ttu-id="37edc-130">integer</span><span class="sxs-lookup"><span data-stu-id="37edc-130">integer</span></span><br/> | <span data-ttu-id="37edc-131">no definido</span><span class="sxs-lookup"><span data-stu-id="37edc-131">undefined</span></span><br/>                                                   |
| <span data-ttu-id="37edc-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="37edc-132">MaxValue</span></span><br/>     | <span data-ttu-id="37edc-133">integer</span><span class="sxs-lookup"><span data-stu-id="37edc-133">integer</span></span><br/> | <span data-ttu-id="37edc-134">Valor de PageImageableSize: ExtentWidth menor o igual que</span><span class="sxs-lookup"><span data-stu-id="37edc-134">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="37edc-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="37edc-135">MinValue</span></span><br/>     | <span data-ttu-id="37edc-136">integer</span><span class="sxs-lookup"><span data-stu-id="37edc-136">integer</span></span><br/> | <span data-ttu-id="37edc-137">0</span><span class="sxs-lookup"><span data-stu-id="37edc-137">0</span></span><br/>                                                           |
| <span data-ttu-id="37edc-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="37edc-138">Multiple</span></span><br/>     | <span data-ttu-id="37edc-139">integer</span><span class="sxs-lookup"><span data-stu-id="37edc-139">integer</span></span><br/> | <span data-ttu-id="37edc-140">1</span><span class="sxs-lookup"><span data-stu-id="37edc-140">1</span></span><br/>                                                           |
| <span data-ttu-id="37edc-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="37edc-141">Mandatory</span></span><br/>    | <span data-ttu-id="37edc-142">string</span><span class="sxs-lookup"><span data-stu-id="37edc-142">string</span></span><br/>  | <span data-ttu-id="37edc-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="37edc-143">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="37edc-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="37edc-144">UnitType</span></span><br/>     | <span data-ttu-id="37edc-145">string</span><span class="sxs-lookup"><span data-stu-id="37edc-145">string</span></span><br/>  | <span data-ttu-id="37edc-146">Micras</span><span class="sxs-lookup"><span data-stu-id="37edc-146">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="37edc-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37edc-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37edc-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="37edc-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




