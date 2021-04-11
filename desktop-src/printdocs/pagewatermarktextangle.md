---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916e409040f0c7163f1168d48581270f077aaa3a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279882"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="4b920-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="4b920-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="4b920-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="4b920-105">This topic is not current.</span></span> <span data-ttu-id="4b920-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4b920-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b920-107">Especifica el ángulo del texto de la marca de agua con respecto a la dirección PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="4b920-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="4b920-108">El ángulo se mide en la dirección en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="4b920-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="4b920-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4b920-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4b920-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4b920-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4b920-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4b920-111">Element Information</span></span>



| <span data-ttu-id="4b920-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="4b920-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="4b920-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4b920-113">Element Type</span></span> <br/>   | <span data-ttu-id="4b920-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4b920-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="4b920-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="4b920-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4b920-116">Página</span><span class="sxs-lookup"><span data-stu-id="4b920-116">Page</span></span><br/>                            |
| <span data-ttu-id="4b920-117">Notas</span><span class="sxs-lookup"><span data-stu-id="4b920-117">Notes</span></span> <br/>          | <span data-ttu-id="4b920-118">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="4b920-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4b920-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4b920-119">Structure Content</span></span>

<span data-ttu-id="4b920-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="4b920-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4b920-121">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="4b920-121">Structure Properties</span></span>

<span data-ttu-id="4b920-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="4b920-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4b920-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b920-123">Property</span></span>                | <span data-ttu-id="4b920-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4b920-124">xsi:type</span></span>           | <span data-ttu-id="4b920-125">Value</span><span class="sxs-lookup"><span data-stu-id="4b920-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4b920-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4b920-126">DataType</span></span><br/>     | <span data-ttu-id="4b920-127">string</span><span class="sxs-lookup"><span data-stu-id="4b920-127">string</span></span><br/>  | <span data-ttu-id="4b920-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4b920-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="4b920-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4b920-129">DefaultValue</span></span><br/> | <span data-ttu-id="4b920-130">integer</span><span class="sxs-lookup"><span data-stu-id="4b920-130">integer</span></span><br/> | <span data-ttu-id="4b920-131">0</span><span class="sxs-lookup"><span data-stu-id="4b920-131">0</span></span><br/>               |
| <span data-ttu-id="4b920-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4b920-132">MaxValue</span></span><br/>     | <span data-ttu-id="4b920-133">integer</span><span class="sxs-lookup"><span data-stu-id="4b920-133">integer</span></span><br/> | <span data-ttu-id="4b920-134">359</span><span class="sxs-lookup"><span data-stu-id="4b920-134">359</span></span><br/>             |
| <span data-ttu-id="4b920-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="4b920-135">MinValue</span></span><br/>     | <span data-ttu-id="4b920-136">integer</span><span class="sxs-lookup"><span data-stu-id="4b920-136">integer</span></span><br/> | <span data-ttu-id="4b920-137">0</span><span class="sxs-lookup"><span data-stu-id="4b920-137">0</span></span><br/>               |
| <span data-ttu-id="4b920-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="4b920-138">Multiple</span></span><br/>     | <span data-ttu-id="4b920-139">integer</span><span class="sxs-lookup"><span data-stu-id="4b920-139">integer</span></span><br/> | <span data-ttu-id="4b920-140">1</span><span class="sxs-lookup"><span data-stu-id="4b920-140">1</span></span><br/>               |
| <span data-ttu-id="4b920-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="4b920-141">Mandatory</span></span><br/>    | <span data-ttu-id="4b920-142">string</span><span class="sxs-lookup"><span data-stu-id="4b920-142">string</span></span><br/>  | <span data-ttu-id="4b920-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="4b920-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4b920-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="4b920-144">UnitType</span></span><br/>     | <span data-ttu-id="4b920-145">string</span><span class="sxs-lookup"><span data-stu-id="4b920-145">string</span></span><br/>  | <span data-ttu-id="4b920-146">grados</span><span class="sxs-lookup"><span data-stu-id="4b920-146">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4b920-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b920-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b920-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4b920-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




