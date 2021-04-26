---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90736f8cac9c919f9d640ffc01311024ef79bc3a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994501"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="76872-104">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="76872-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="76872-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="76872-105">This topic is not current.</span></span> <span data-ttu-id="76872-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="76872-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="76872-107">Especifica el origen de una marca de agua con respecto al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="76872-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="76872-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="76872-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="76872-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="76872-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="76872-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="76872-110">Element Information</span></span>



| <span data-ttu-id="76872-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="76872-111">Name</span></span> | <span data-ttu-id="76872-112">Value</span><span class="sxs-lookup"><span data-stu-id="76872-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="76872-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="76872-113">Element Type</span></span> <br/>   | <span data-ttu-id="76872-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="76872-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="76872-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="76872-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="76872-116">Página</span><span class="sxs-lookup"><span data-stu-id="76872-116">Page</span></span><br/>                            |
| <span data-ttu-id="76872-117">Notas</span><span class="sxs-lookup"><span data-stu-id="76872-117">Notes</span></span> <br/>          | <span data-ttu-id="76872-118">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="76872-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="76872-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="76872-119">Structure Content</span></span>

<span data-ttu-id="76872-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="76872-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="76872-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="76872-121">Structure Properties</span></span>

<span data-ttu-id="76872-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="76872-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="76872-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="76872-123">Property</span></span>                | <span data-ttu-id="76872-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="76872-124">xsi:type</span></span>           | <span data-ttu-id="76872-125">Value</span><span class="sxs-lookup"><span data-stu-id="76872-125">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="76872-126">DataType</span><span class="sxs-lookup"><span data-stu-id="76872-126">DataType</span></span><br/>     | <span data-ttu-id="76872-127">string</span><span class="sxs-lookup"><span data-stu-id="76872-127">string</span></span><br/>  | <span data-ttu-id="76872-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="76872-128">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="76872-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="76872-129">DefaultValue</span></span><br/> | <span data-ttu-id="76872-130">integer</span><span class="sxs-lookup"><span data-stu-id="76872-130">integer</span></span><br/> | <span data-ttu-id="76872-131">no definido</span><span class="sxs-lookup"><span data-stu-id="76872-131">undefined</span></span><br/>                                                    |
| <span data-ttu-id="76872-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="76872-132">MaxValue</span></span><br/>     | <span data-ttu-id="76872-133">integer</span><span class="sxs-lookup"><span data-stu-id="76872-133">integer</span></span><br/> | <span data-ttu-id="76872-134">Valor de ExtentHeight menor o igual que PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="76872-134">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="76872-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="76872-135">MinValue</span></span><br/>     | <span data-ttu-id="76872-136">integer</span><span class="sxs-lookup"><span data-stu-id="76872-136">integer</span></span><br/> | <span data-ttu-id="76872-137">0</span><span class="sxs-lookup"><span data-stu-id="76872-137">0</span></span><br/>                                                            |
| <span data-ttu-id="76872-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="76872-138">Multiple</span></span><br/>     | <span data-ttu-id="76872-139">integer</span><span class="sxs-lookup"><span data-stu-id="76872-139">integer</span></span><br/> | <span data-ttu-id="76872-140">1</span><span class="sxs-lookup"><span data-stu-id="76872-140">1</span></span><br/>                                                            |
| <span data-ttu-id="76872-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="76872-141">Mandatory</span></span><br/>    | <span data-ttu-id="76872-142">string</span><span class="sxs-lookup"><span data-stu-id="76872-142">string</span></span><br/>  | <span data-ttu-id="76872-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="76872-143">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="76872-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="76872-144">UnitType</span></span><br/>     | <span data-ttu-id="76872-145">string</span><span class="sxs-lookup"><span data-stu-id="76872-145">string</span></span><br/>  | <span data-ttu-id="76872-146">Micras</span><span class="sxs-lookup"><span data-stu-id="76872-146">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="76872-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76872-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76872-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="76872-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




