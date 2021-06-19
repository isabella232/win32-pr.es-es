---
description: Obtenga información sobre el parámetro PageWatermarkOriginWidth. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe6457496972231877af2a51e03bc5109083d0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396010"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="bdc40-105">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="bdc40-105">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="bdc40-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="bdc40-106">This topic is not current.</span></span> <span data-ttu-id="bdc40-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bdc40-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bdc40-108">Especifica el origen de una marca de agua relativa al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="bdc40-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="bdc40-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bdc40-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bdc40-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bdc40-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bdc40-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bdc40-111">Element Information</span></span>



| <span data-ttu-id="bdc40-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="bdc40-112">Name</span></span> | <span data-ttu-id="bdc40-113">Valor</span><span class="sxs-lookup"><span data-stu-id="bdc40-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="bdc40-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bdc40-114">Element Type</span></span> <br/>   | <span data-ttu-id="bdc40-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bdc40-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="bdc40-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="bdc40-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bdc40-117">Página</span><span class="sxs-lookup"><span data-stu-id="bdc40-117">Page</span></span><br/>                            |
| <span data-ttu-id="bdc40-118">Notas</span><span class="sxs-lookup"><span data-stu-id="bdc40-118">Notes</span></span> <br/>          | <span data-ttu-id="bdc40-119">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="bdc40-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bdc40-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bdc40-120">Structure Content</span></span>

<span data-ttu-id="bdc40-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="bdc40-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="bdc40-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="bdc40-122">Structure Properties</span></span>

<span data-ttu-id="bdc40-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="bdc40-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bdc40-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bdc40-124">Property</span></span>                | <span data-ttu-id="bdc40-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bdc40-125">xsi:type</span></span>           | <span data-ttu-id="bdc40-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bdc40-126">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bdc40-127">DataType</span><span class="sxs-lookup"><span data-stu-id="bdc40-127">DataType</span></span><br/>     | <span data-ttu-id="bdc40-128">string</span><span class="sxs-lookup"><span data-stu-id="bdc40-128">string</span></span><br/>  | <span data-ttu-id="bdc40-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bdc40-129">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="bdc40-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bdc40-130">DefaultValue</span></span><br/> | <span data-ttu-id="bdc40-131">integer</span><span class="sxs-lookup"><span data-stu-id="bdc40-131">integer</span></span><br/> | <span data-ttu-id="bdc40-132">no definido</span><span class="sxs-lookup"><span data-stu-id="bdc40-132">undefined</span></span><br/>                                                   |
| <span data-ttu-id="bdc40-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="bdc40-133">MaxValue</span></span><br/>     | <span data-ttu-id="bdc40-134">integer</span><span class="sxs-lookup"><span data-stu-id="bdc40-134">integer</span></span><br/> | <span data-ttu-id="bdc40-135">Valor de PageImageableSize: ExtentWidth menor o igual que</span><span class="sxs-lookup"><span data-stu-id="bdc40-135">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="bdc40-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="bdc40-136">MinValue</span></span><br/>     | <span data-ttu-id="bdc40-137">integer</span><span class="sxs-lookup"><span data-stu-id="bdc40-137">integer</span></span><br/> | <span data-ttu-id="bdc40-138">0</span><span class="sxs-lookup"><span data-stu-id="bdc40-138">0</span></span><br/>                                                           |
| <span data-ttu-id="bdc40-139">Múltiple</span><span class="sxs-lookup"><span data-stu-id="bdc40-139">Multiple</span></span><br/>     | <span data-ttu-id="bdc40-140">integer</span><span class="sxs-lookup"><span data-stu-id="bdc40-140">integer</span></span><br/> | <span data-ttu-id="bdc40-141">1</span><span class="sxs-lookup"><span data-stu-id="bdc40-141">1</span></span><br/>                                                           |
| <span data-ttu-id="bdc40-142">Mandatory</span><span class="sxs-lookup"><span data-stu-id="bdc40-142">Mandatory</span></span><br/>    | <span data-ttu-id="bdc40-143">string</span><span class="sxs-lookup"><span data-stu-id="bdc40-143">string</span></span><br/>  | <span data-ttu-id="bdc40-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="bdc40-144">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="bdc40-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="bdc40-145">UnitType</span></span><br/>     | <span data-ttu-id="bdc40-146">string</span><span class="sxs-lookup"><span data-stu-id="bdc40-146">string</span></span><br/>  | <span data-ttu-id="bdc40-147">Micras</span><span class="sxs-lookup"><span data-stu-id="bdc40-147">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="bdc40-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdc40-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc40-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="bdc40-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




