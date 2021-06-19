---
description: Obtenga información sobre el parámetro PageWatermarkTextFontSize. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb28044ca676dedfb136cb58190db90a06fd624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396000"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="e0a4e-105">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="e0a4e-105">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="e0a4e-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e0a4e-106">This topic is not current.</span></span> <span data-ttu-id="e0a4e-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e0a4e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e0a4e-108">Define los tamaños de fuente disponibles para el texto de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="e0a4e-108">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="e0a4e-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e0a4e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e0a4e-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e0a4e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e0a4e-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e0a4e-111">Element Information</span></span>



| <span data-ttu-id="e0a4e-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0a4e-112">Name</span></span> | <span data-ttu-id="e0a4e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e0a4e-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="e0a4e-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e0a4e-114">Element Type</span></span> <br/>   | <span data-ttu-id="e0a4e-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e0a4e-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="e0a4e-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e0a4e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e0a4e-117">Página</span><span class="sxs-lookup"><span data-stu-id="e0a4e-117">Page</span></span><br/>                            |
| <span data-ttu-id="e0a4e-118">Notas</span><span class="sxs-lookup"><span data-stu-id="e0a4e-118">Notes</span></span> <br/>          | <span data-ttu-id="e0a4e-119">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="e0a4e-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e0a4e-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e0a4e-120">Structure Content</span></span>

<span data-ttu-id="e0a4e-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e0a4e-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e0a4e-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="e0a4e-122">Structure Properties</span></span>

<span data-ttu-id="e0a4e-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e0a4e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e0a4e-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0a4e-124">Property</span></span>                | <span data-ttu-id="e0a4e-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e0a4e-125">xsi:type</span></span>           | <span data-ttu-id="e0a4e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e0a4e-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e0a4e-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e0a4e-127">DataType</span></span><br/>     | <span data-ttu-id="e0a4e-128">string</span><span class="sxs-lookup"><span data-stu-id="e0a4e-128">string</span></span><br/>  | <span data-ttu-id="e0a4e-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e0a4e-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="e0a4e-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e0a4e-130">DefaultValue</span></span><br/> | <span data-ttu-id="e0a4e-131">integer</span><span class="sxs-lookup"><span data-stu-id="e0a4e-131">integer</span></span><br/> | <span data-ttu-id="e0a4e-132">no definido</span><span class="sxs-lookup"><span data-stu-id="e0a4e-132">undefined</span></span><br/>       |
| <span data-ttu-id="e0a4e-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e0a4e-133">MaxValue</span></span><br/>     | <span data-ttu-id="e0a4e-134">integer</span><span class="sxs-lookup"><span data-stu-id="e0a4e-134">integer</span></span><br/> | <span data-ttu-id="e0a4e-135">no definido</span><span class="sxs-lookup"><span data-stu-id="e0a4e-135">undefined</span></span><br/>       |
| <span data-ttu-id="e0a4e-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="e0a4e-136">MinValue</span></span><br/>     | <span data-ttu-id="e0a4e-137">integer</span><span class="sxs-lookup"><span data-stu-id="e0a4e-137">integer</span></span><br/> | <span data-ttu-id="e0a4e-138">no definido</span><span class="sxs-lookup"><span data-stu-id="e0a4e-138">undefined</span></span><br/>       |
| <span data-ttu-id="e0a4e-139">Múltiple</span><span class="sxs-lookup"><span data-stu-id="e0a4e-139">Multiple</span></span><br/>     | <span data-ttu-id="e0a4e-140">integer</span><span class="sxs-lookup"><span data-stu-id="e0a4e-140">integer</span></span><br/> | <span data-ttu-id="e0a4e-141">no definido</span><span class="sxs-lookup"><span data-stu-id="e0a4e-141">undefined</span></span><br/>       |
| <span data-ttu-id="e0a4e-142">Mandatory</span><span class="sxs-lookup"><span data-stu-id="e0a4e-142">Mandatory</span></span><br/>    | <span data-ttu-id="e0a4e-143">string</span><span class="sxs-lookup"><span data-stu-id="e0a4e-143">string</span></span><br/>  | <span data-ttu-id="e0a4e-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e0a4e-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e0a4e-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="e0a4e-145">UnitType</span></span><br/>     | <span data-ttu-id="e0a4e-146">string</span><span class="sxs-lookup"><span data-stu-id="e0a4e-146">string</span></span><br/>  | <span data-ttu-id="e0a4e-147">puntos</span><span class="sxs-lookup"><span data-stu-id="e0a4e-147">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="e0a4e-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0a4e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0a4e-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e0a4e-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




