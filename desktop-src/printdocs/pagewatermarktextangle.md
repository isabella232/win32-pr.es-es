---
description: Obtenga más información sobre el parámetro PageWatermarkTextAngle. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dce37512314e1eaac0cbbe3b5b4b817cb2ee455
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395980"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="e9868-105">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="e9868-105">PageWatermarkTextAngle</span></span>

<span data-ttu-id="e9868-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e9868-106">This topic is not current.</span></span> <span data-ttu-id="e9868-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e9868-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e9868-108">Especifica el ángulo del texto de la marca de agua en relación con la dirección PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="e9868-108">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="e9868-109">El ángulo se mide en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="e9868-109">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="e9868-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e9868-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e9868-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e9868-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e9868-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e9868-112">Element Information</span></span>



| <span data-ttu-id="e9868-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9868-113">Name</span></span> | <span data-ttu-id="e9868-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e9868-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="e9868-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e9868-115">Element Type</span></span> <br/>   | <span data-ttu-id="e9868-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e9868-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="e9868-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e9868-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e9868-118">Página</span><span class="sxs-lookup"><span data-stu-id="e9868-118">Page</span></span><br/>                            |
| <span data-ttu-id="e9868-119">Notas</span><span class="sxs-lookup"><span data-stu-id="e9868-119">Notes</span></span> <br/>          | <span data-ttu-id="e9868-120">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="e9868-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e9868-121">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e9868-121">Structure Content</span></span>

<span data-ttu-id="e9868-122">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e9868-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
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
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="e9868-123">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="e9868-123">Structure Properties</span></span>

<span data-ttu-id="e9868-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e9868-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e9868-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9868-125">Property</span></span>                | <span data-ttu-id="e9868-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e9868-126">xsi:type</span></span>           | <span data-ttu-id="e9868-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e9868-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e9868-128">DataType</span><span class="sxs-lookup"><span data-stu-id="e9868-128">DataType</span></span><br/>     | <span data-ttu-id="e9868-129">string</span><span class="sxs-lookup"><span data-stu-id="e9868-129">string</span></span><br/>  | <span data-ttu-id="e9868-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e9868-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="e9868-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e9868-131">DefaultValue</span></span><br/> | <span data-ttu-id="e9868-132">integer</span><span class="sxs-lookup"><span data-stu-id="e9868-132">integer</span></span><br/> | <span data-ttu-id="e9868-133">0</span><span class="sxs-lookup"><span data-stu-id="e9868-133">0</span></span><br/>               |
| <span data-ttu-id="e9868-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e9868-134">MaxValue</span></span><br/>     | <span data-ttu-id="e9868-135">integer</span><span class="sxs-lookup"><span data-stu-id="e9868-135">integer</span></span><br/> | <span data-ttu-id="e9868-136">359</span><span class="sxs-lookup"><span data-stu-id="e9868-136">359</span></span><br/>             |
| <span data-ttu-id="e9868-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="e9868-137">MinValue</span></span><br/>     | <span data-ttu-id="e9868-138">integer</span><span class="sxs-lookup"><span data-stu-id="e9868-138">integer</span></span><br/> | <span data-ttu-id="e9868-139">0</span><span class="sxs-lookup"><span data-stu-id="e9868-139">0</span></span><br/>               |
| <span data-ttu-id="e9868-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="e9868-140">Multiple</span></span><br/>     | <span data-ttu-id="e9868-141">integer</span><span class="sxs-lookup"><span data-stu-id="e9868-141">integer</span></span><br/> | <span data-ttu-id="e9868-142">1</span><span class="sxs-lookup"><span data-stu-id="e9868-142">1</span></span><br/>               |
| <span data-ttu-id="e9868-143">Mandatory</span><span class="sxs-lookup"><span data-stu-id="e9868-143">Mandatory</span></span><br/>    | <span data-ttu-id="e9868-144">string</span><span class="sxs-lookup"><span data-stu-id="e9868-144">string</span></span><br/>  | <span data-ttu-id="e9868-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e9868-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e9868-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="e9868-146">UnitType</span></span><br/>     | <span data-ttu-id="e9868-147">string</span><span class="sxs-lookup"><span data-stu-id="e9868-147">string</span></span><br/>  | <span data-ttu-id="e9868-148">grados</span><span class="sxs-lookup"><span data-stu-id="e9868-148">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e9868-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9868-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9868-150">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e9868-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




