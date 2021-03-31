---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678630b7b7f6650a1317efef95c30effc71c6082
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083606"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="655ef-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="655ef-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="655ef-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="655ef-105">This topic is not current.</span></span> <span data-ttu-id="655ef-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="655ef-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="655ef-107">Define los tamaños de fuente disponibles para el texto de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="655ef-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="655ef-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="655ef-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="655ef-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="655ef-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="655ef-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="655ef-110">Element Information</span></span>



| <span data-ttu-id="655ef-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="655ef-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="655ef-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="655ef-112">Element Type</span></span> <br/>   | <span data-ttu-id="655ef-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="655ef-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="655ef-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="655ef-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="655ef-115">Página</span><span class="sxs-lookup"><span data-stu-id="655ef-115">Page</span></span><br/>                            |
| <span data-ttu-id="655ef-116">Notas</span><span class="sxs-lookup"><span data-stu-id="655ef-116">Notes</span></span> <br/>          | <span data-ttu-id="655ef-117">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="655ef-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="655ef-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="655ef-118">Structure Content</span></span>

<span data-ttu-id="655ef-119">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="655ef-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextFontSize">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">points</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="655ef-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="655ef-120">Structure Properties</span></span>

<span data-ttu-id="655ef-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="655ef-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="655ef-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="655ef-122">Property</span></span>                | <span data-ttu-id="655ef-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="655ef-123">xsi:type</span></span>           | <span data-ttu-id="655ef-124">Value</span><span class="sxs-lookup"><span data-stu-id="655ef-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="655ef-125">DataType</span><span class="sxs-lookup"><span data-stu-id="655ef-125">DataType</span></span><br/>     | <span data-ttu-id="655ef-126">string</span><span class="sxs-lookup"><span data-stu-id="655ef-126">string</span></span><br/>  | <span data-ttu-id="655ef-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="655ef-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="655ef-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="655ef-128">DefaultValue</span></span><br/> | <span data-ttu-id="655ef-129">integer</span><span class="sxs-lookup"><span data-stu-id="655ef-129">integer</span></span><br/> | <span data-ttu-id="655ef-130">no definido</span><span class="sxs-lookup"><span data-stu-id="655ef-130">undefined</span></span><br/>       |
| <span data-ttu-id="655ef-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="655ef-131">MaxValue</span></span><br/>     | <span data-ttu-id="655ef-132">integer</span><span class="sxs-lookup"><span data-stu-id="655ef-132">integer</span></span><br/> | <span data-ttu-id="655ef-133">no definido</span><span class="sxs-lookup"><span data-stu-id="655ef-133">undefined</span></span><br/>       |
| <span data-ttu-id="655ef-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="655ef-134">MinValue</span></span><br/>     | <span data-ttu-id="655ef-135">integer</span><span class="sxs-lookup"><span data-stu-id="655ef-135">integer</span></span><br/> | <span data-ttu-id="655ef-136">no definido</span><span class="sxs-lookup"><span data-stu-id="655ef-136">undefined</span></span><br/>       |
| <span data-ttu-id="655ef-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="655ef-137">Multiple</span></span><br/>     | <span data-ttu-id="655ef-138">integer</span><span class="sxs-lookup"><span data-stu-id="655ef-138">integer</span></span><br/> | <span data-ttu-id="655ef-139">no definido</span><span class="sxs-lookup"><span data-stu-id="655ef-139">undefined</span></span><br/>       |
| <span data-ttu-id="655ef-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="655ef-140">Mandatory</span></span><br/>    | <span data-ttu-id="655ef-141">string</span><span class="sxs-lookup"><span data-stu-id="655ef-141">string</span></span><br/>  | <span data-ttu-id="655ef-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="655ef-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="655ef-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="655ef-143">UnitType</span></span><br/>     | <span data-ttu-id="655ef-144">string</span><span class="sxs-lookup"><span data-stu-id="655ef-144">string</span></span><br/>  | <span data-ttu-id="655ef-145">puntos</span><span class="sxs-lookup"><span data-stu-id="655ef-145">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="655ef-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="655ef-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="655ef-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="655ef-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




