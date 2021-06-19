---
description: Obtenga información sobre el parámetro PageWatermarkOriginHeight. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59e9336088d44cef1941df03319519ae69af1c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395990"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="7abe0-105">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="7abe0-105">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="7abe0-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="7abe0-106">This topic is not current.</span></span> <span data-ttu-id="7abe0-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7abe0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7abe0-108">Especifica el origen de una marca de agua relativa al origen de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="7abe0-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="7abe0-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7abe0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7abe0-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7abe0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7abe0-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7abe0-111">Element Information</span></span>



| <span data-ttu-id="7abe0-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="7abe0-112">Name</span></span> | <span data-ttu-id="7abe0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7abe0-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="7abe0-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7abe0-114">Element Type</span></span> <br/>   | <span data-ttu-id="7abe0-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7abe0-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="7abe0-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="7abe0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7abe0-117">Página</span><span class="sxs-lookup"><span data-stu-id="7abe0-117">Page</span></span><br/>                            |
| <span data-ttu-id="7abe0-118">Notas</span><span class="sxs-lookup"><span data-stu-id="7abe0-118">Notes</span></span> <br/>          | <span data-ttu-id="7abe0-119">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="7abe0-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7abe0-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7abe0-120">Structure Content</span></span>

<span data-ttu-id="7abe0-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="7abe0-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7abe0-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="7abe0-122">Structure Properties</span></span>

<span data-ttu-id="7abe0-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="7abe0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7abe0-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7abe0-124">Property</span></span>                | <span data-ttu-id="7abe0-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7abe0-125">xsi:type</span></span>           | <span data-ttu-id="7abe0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7abe0-126">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7abe0-127">DataType</span><span class="sxs-lookup"><span data-stu-id="7abe0-127">DataType</span></span><br/>     | <span data-ttu-id="7abe0-128">string</span><span class="sxs-lookup"><span data-stu-id="7abe0-128">string</span></span><br/>  | <span data-ttu-id="7abe0-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7abe0-129">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="7abe0-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7abe0-130">DefaultValue</span></span><br/> | <span data-ttu-id="7abe0-131">integer</span><span class="sxs-lookup"><span data-stu-id="7abe0-131">integer</span></span><br/> | <span data-ttu-id="7abe0-132">no definido</span><span class="sxs-lookup"><span data-stu-id="7abe0-132">undefined</span></span><br/>                                                    |
| <span data-ttu-id="7abe0-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7abe0-133">MaxValue</span></span><br/>     | <span data-ttu-id="7abe0-134">integer</span><span class="sxs-lookup"><span data-stu-id="7abe0-134">integer</span></span><br/> | <span data-ttu-id="7abe0-135">Valor de ExtentHeight menor o igual que PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="7abe0-135">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="7abe0-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="7abe0-136">MinValue</span></span><br/>     | <span data-ttu-id="7abe0-137">integer</span><span class="sxs-lookup"><span data-stu-id="7abe0-137">integer</span></span><br/> | <span data-ttu-id="7abe0-138">0</span><span class="sxs-lookup"><span data-stu-id="7abe0-138">0</span></span><br/>                                                            |
| <span data-ttu-id="7abe0-139">Múltiple</span><span class="sxs-lookup"><span data-stu-id="7abe0-139">Multiple</span></span><br/>     | <span data-ttu-id="7abe0-140">integer</span><span class="sxs-lookup"><span data-stu-id="7abe0-140">integer</span></span><br/> | <span data-ttu-id="7abe0-141">1</span><span class="sxs-lookup"><span data-stu-id="7abe0-141">1</span></span><br/>                                                            |
| <span data-ttu-id="7abe0-142">Mandatory</span><span class="sxs-lookup"><span data-stu-id="7abe0-142">Mandatory</span></span><br/>    | <span data-ttu-id="7abe0-143">string</span><span class="sxs-lookup"><span data-stu-id="7abe0-143">string</span></span><br/>  | <span data-ttu-id="7abe0-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7abe0-144">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="7abe0-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="7abe0-145">UnitType</span></span><br/>     | <span data-ttu-id="7abe0-146">string</span><span class="sxs-lookup"><span data-stu-id="7abe0-146">string</span></span><br/>  | <span data-ttu-id="7abe0-147">Micras</span><span class="sxs-lookup"><span data-stu-id="7abe0-147">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="7abe0-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7abe0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7abe0-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="7abe0-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




