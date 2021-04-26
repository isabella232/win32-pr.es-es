---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cc8c7f3c9a692ffbe180c253d448d7c4e320d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999150"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="8ef26-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="8ef26-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="8ef26-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="8ef26-105">This topic is not current.</span></span> <span data-ttu-id="8ef26-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8ef26-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8ef26-107">Define los tamaños de fuente disponibles para el texto de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="8ef26-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="8ef26-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8ef26-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8ef26-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="8ef26-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8ef26-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8ef26-110">Element Information</span></span>



| <span data-ttu-id="8ef26-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ef26-111">Name</span></span> | <span data-ttu-id="8ef26-112">Value</span><span class="sxs-lookup"><span data-stu-id="8ef26-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="8ef26-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8ef26-113">Element Type</span></span> <br/>   | <span data-ttu-id="8ef26-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8ef26-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="8ef26-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="8ef26-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8ef26-116">Página</span><span class="sxs-lookup"><span data-stu-id="8ef26-116">Page</span></span><br/>                            |
| <span data-ttu-id="8ef26-117">Notas</span><span class="sxs-lookup"><span data-stu-id="8ef26-117">Notes</span></span> <br/>          | <span data-ttu-id="8ef26-118">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="8ef26-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8ef26-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="8ef26-119">Structure Content</span></span>

<span data-ttu-id="8ef26-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8ef26-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8ef26-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="8ef26-121">Structure Properties</span></span>

<span data-ttu-id="8ef26-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="8ef26-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8ef26-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ef26-123">Property</span></span>                | <span data-ttu-id="8ef26-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8ef26-124">xsi:type</span></span>           | <span data-ttu-id="8ef26-125">Value</span><span class="sxs-lookup"><span data-stu-id="8ef26-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8ef26-126">DataType</span><span class="sxs-lookup"><span data-stu-id="8ef26-126">DataType</span></span><br/>     | <span data-ttu-id="8ef26-127">string</span><span class="sxs-lookup"><span data-stu-id="8ef26-127">string</span></span><br/>  | <span data-ttu-id="8ef26-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8ef26-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="8ef26-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8ef26-129">DefaultValue</span></span><br/> | <span data-ttu-id="8ef26-130">integer</span><span class="sxs-lookup"><span data-stu-id="8ef26-130">integer</span></span><br/> | <span data-ttu-id="8ef26-131">no definido</span><span class="sxs-lookup"><span data-stu-id="8ef26-131">undefined</span></span><br/>       |
| <span data-ttu-id="8ef26-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8ef26-132">MaxValue</span></span><br/>     | <span data-ttu-id="8ef26-133">integer</span><span class="sxs-lookup"><span data-stu-id="8ef26-133">integer</span></span><br/> | <span data-ttu-id="8ef26-134">no definido</span><span class="sxs-lookup"><span data-stu-id="8ef26-134">undefined</span></span><br/>       |
| <span data-ttu-id="8ef26-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="8ef26-135">MinValue</span></span><br/>     | <span data-ttu-id="8ef26-136">integer</span><span class="sxs-lookup"><span data-stu-id="8ef26-136">integer</span></span><br/> | <span data-ttu-id="8ef26-137">no definido</span><span class="sxs-lookup"><span data-stu-id="8ef26-137">undefined</span></span><br/>       |
| <span data-ttu-id="8ef26-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="8ef26-138">Multiple</span></span><br/>     | <span data-ttu-id="8ef26-139">integer</span><span class="sxs-lookup"><span data-stu-id="8ef26-139">integer</span></span><br/> | <span data-ttu-id="8ef26-140">no definido</span><span class="sxs-lookup"><span data-stu-id="8ef26-140">undefined</span></span><br/>       |
| <span data-ttu-id="8ef26-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="8ef26-141">Mandatory</span></span><br/>    | <span data-ttu-id="8ef26-142">string</span><span class="sxs-lookup"><span data-stu-id="8ef26-142">string</span></span><br/>  | <span data-ttu-id="8ef26-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="8ef26-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8ef26-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="8ef26-144">UnitType</span></span><br/>     | <span data-ttu-id="8ef26-145">string</span><span class="sxs-lookup"><span data-stu-id="8ef26-145">string</span></span><br/>  | <span data-ttu-id="8ef26-146">puntos</span><span class="sxs-lookup"><span data-stu-id="8ef26-146">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="8ef26-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ef26-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ef26-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8ef26-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




