---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e96382656b1092a0dbc71352e788208f70b34
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717415"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="427b9-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="427b9-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="427b9-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="427b9-105">This topic is not current.</span></span> <span data-ttu-id="427b9-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="427b9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="427b9-107">Especifica la transparencia de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="427b9-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="427b9-108">Totalmente opaca tendría un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="427b9-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="427b9-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="427b9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="427b9-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="427b9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="427b9-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="427b9-111">Element Information</span></span>



| <span data-ttu-id="427b9-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="427b9-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="427b9-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="427b9-113">Element Type</span></span> <br/>   | <span data-ttu-id="427b9-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="427b9-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="427b9-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="427b9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="427b9-116">Página</span><span class="sxs-lookup"><span data-stu-id="427b9-116">Page</span></span><br/>                            |
| <span data-ttu-id="427b9-117">Notas</span><span class="sxs-lookup"><span data-stu-id="427b9-117">Notes</span></span> <br/>          | <span data-ttu-id="427b9-118">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="427b9-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="427b9-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="427b9-119">Structure Content</span></span>

<span data-ttu-id="427b9-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="427b9-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="427b9-121">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="427b9-121">Structure Properties</span></span>

<span data-ttu-id="427b9-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="427b9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="427b9-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="427b9-123">Property</span></span>                | <span data-ttu-id="427b9-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="427b9-124">xsi:type</span></span>           | <span data-ttu-id="427b9-125">Value</span><span class="sxs-lookup"><span data-stu-id="427b9-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="427b9-126">DataType</span><span class="sxs-lookup"><span data-stu-id="427b9-126">DataType</span></span><br/>     | <span data-ttu-id="427b9-127">string</span><span class="sxs-lookup"><span data-stu-id="427b9-127">string</span></span><br/>  | <span data-ttu-id="427b9-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="427b9-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="427b9-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="427b9-129">DefaultValue</span></span><br/> | <span data-ttu-id="427b9-130">integer</span><span class="sxs-lookup"><span data-stu-id="427b9-130">integer</span></span><br/> | <span data-ttu-id="427b9-131">0</span><span class="sxs-lookup"><span data-stu-id="427b9-131">0</span></span><br/>               |
| <span data-ttu-id="427b9-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="427b9-132">MaxValue</span></span><br/>     | <span data-ttu-id="427b9-133">integer</span><span class="sxs-lookup"><span data-stu-id="427b9-133">integer</span></span><br/> | <span data-ttu-id="427b9-134">100</span><span class="sxs-lookup"><span data-stu-id="427b9-134">100</span></span><br/>             |
| <span data-ttu-id="427b9-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="427b9-135">MinValue</span></span><br/>     | <span data-ttu-id="427b9-136">integer</span><span class="sxs-lookup"><span data-stu-id="427b9-136">integer</span></span><br/> | <span data-ttu-id="427b9-137">0</span><span class="sxs-lookup"><span data-stu-id="427b9-137">0</span></span><br/>               |
| <span data-ttu-id="427b9-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="427b9-138">Multiple</span></span><br/>     | <span data-ttu-id="427b9-139">integer</span><span class="sxs-lookup"><span data-stu-id="427b9-139">integer</span></span><br/> | <span data-ttu-id="427b9-140">1</span><span class="sxs-lookup"><span data-stu-id="427b9-140">1</span></span><br/>               |
| <span data-ttu-id="427b9-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="427b9-141">Mandatory</span></span><br/>    | <span data-ttu-id="427b9-142">string</span><span class="sxs-lookup"><span data-stu-id="427b9-142">string</span></span><br/>  | <span data-ttu-id="427b9-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="427b9-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="427b9-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="427b9-144">UnitType</span></span><br/>     | <span data-ttu-id="427b9-145">string</span><span class="sxs-lookup"><span data-stu-id="427b9-145">string</span></span><br/>  | <span data-ttu-id="427b9-146">percent</span><span class="sxs-lookup"><span data-stu-id="427b9-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="427b9-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="427b9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="427b9-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="427b9-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




