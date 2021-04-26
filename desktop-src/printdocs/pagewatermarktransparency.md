---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d46a03cfb1b2129f4c89a6ea7c751e23cd565e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996882"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="18ae4-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="18ae4-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="18ae4-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="18ae4-105">This topic is not current.</span></span> <span data-ttu-id="18ae4-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="18ae4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="18ae4-107">Especifica la transparencia de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="18ae4-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="18ae4-108">Totalmente opaco tendría un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="18ae4-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="18ae4-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="18ae4-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="18ae4-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="18ae4-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="18ae4-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="18ae4-111">Element Information</span></span>



| <span data-ttu-id="18ae4-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="18ae4-112">Name</span></span> | <span data-ttu-id="18ae4-113">Value</span><span class="sxs-lookup"><span data-stu-id="18ae4-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="18ae4-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="18ae4-114">Element Type</span></span> <br/>   | <span data-ttu-id="18ae4-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="18ae4-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="18ae4-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="18ae4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="18ae4-117">Página</span><span class="sxs-lookup"><span data-stu-id="18ae4-117">Page</span></span><br/>                            |
| <span data-ttu-id="18ae4-118">Notas</span><span class="sxs-lookup"><span data-stu-id="18ae4-118">Notes</span></span> <br/>          | <span data-ttu-id="18ae4-119">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="18ae4-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="18ae4-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="18ae4-120">Structure Content</span></span>

<span data-ttu-id="18ae4-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="18ae4-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="18ae4-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="18ae4-122">Structure Properties</span></span>

<span data-ttu-id="18ae4-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="18ae4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="18ae4-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18ae4-124">Property</span></span>                | <span data-ttu-id="18ae4-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="18ae4-125">xsi:type</span></span>           | <span data-ttu-id="18ae4-126">Value</span><span class="sxs-lookup"><span data-stu-id="18ae4-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="18ae4-127">DataType</span><span class="sxs-lookup"><span data-stu-id="18ae4-127">DataType</span></span><br/>     | <span data-ttu-id="18ae4-128">string</span><span class="sxs-lookup"><span data-stu-id="18ae4-128">string</span></span><br/>  | <span data-ttu-id="18ae4-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="18ae4-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="18ae4-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="18ae4-130">DefaultValue</span></span><br/> | <span data-ttu-id="18ae4-131">integer</span><span class="sxs-lookup"><span data-stu-id="18ae4-131">integer</span></span><br/> | <span data-ttu-id="18ae4-132">0</span><span class="sxs-lookup"><span data-stu-id="18ae4-132">0</span></span><br/>               |
| <span data-ttu-id="18ae4-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="18ae4-133">MaxValue</span></span><br/>     | <span data-ttu-id="18ae4-134">integer</span><span class="sxs-lookup"><span data-stu-id="18ae4-134">integer</span></span><br/> | <span data-ttu-id="18ae4-135">100</span><span class="sxs-lookup"><span data-stu-id="18ae4-135">100</span></span><br/>             |
| <span data-ttu-id="18ae4-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="18ae4-136">MinValue</span></span><br/>     | <span data-ttu-id="18ae4-137">integer</span><span class="sxs-lookup"><span data-stu-id="18ae4-137">integer</span></span><br/> | <span data-ttu-id="18ae4-138">0</span><span class="sxs-lookup"><span data-stu-id="18ae4-138">0</span></span><br/>               |
| <span data-ttu-id="18ae4-139">Múltiple</span><span class="sxs-lookup"><span data-stu-id="18ae4-139">Multiple</span></span><br/>     | <span data-ttu-id="18ae4-140">integer</span><span class="sxs-lookup"><span data-stu-id="18ae4-140">integer</span></span><br/> | <span data-ttu-id="18ae4-141">1</span><span class="sxs-lookup"><span data-stu-id="18ae4-141">1</span></span><br/>               |
| <span data-ttu-id="18ae4-142">Mandatory</span><span class="sxs-lookup"><span data-stu-id="18ae4-142">Mandatory</span></span><br/>    | <span data-ttu-id="18ae4-143">string</span><span class="sxs-lookup"><span data-stu-id="18ae4-143">string</span></span><br/>  | <span data-ttu-id="18ae4-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="18ae4-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="18ae4-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="18ae4-145">UnitType</span></span><br/>     | <span data-ttu-id="18ae4-146">string</span><span class="sxs-lookup"><span data-stu-id="18ae4-146">string</span></span><br/>  | <span data-ttu-id="18ae4-147">percent</span><span class="sxs-lookup"><span data-stu-id="18ae4-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="18ae4-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18ae4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18ae4-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="18ae4-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




