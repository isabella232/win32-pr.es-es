---
description: Obtenga información sobre el parámetro PageWatermarkTransparency. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394790"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="53dcc-105">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="53dcc-105">PageWatermarkTransparency</span></span>

<span data-ttu-id="53dcc-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="53dcc-106">This topic is not current.</span></span> <span data-ttu-id="53dcc-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="53dcc-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="53dcc-108">Especifica la transparencia de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="53dcc-108">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="53dcc-109">Totalmente opaco tendría un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="53dcc-109">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="53dcc-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="53dcc-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="53dcc-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="53dcc-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="53dcc-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="53dcc-112">Element Information</span></span>



| <span data-ttu-id="53dcc-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="53dcc-113">Name</span></span> | <span data-ttu-id="53dcc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="53dcc-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="53dcc-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="53dcc-115">Element Type</span></span> <br/>   | <span data-ttu-id="53dcc-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="53dcc-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="53dcc-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="53dcc-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="53dcc-118">Página</span><span class="sxs-lookup"><span data-stu-id="53dcc-118">Page</span></span><br/>                            |
| <span data-ttu-id="53dcc-119">Notas</span><span class="sxs-lookup"><span data-stu-id="53dcc-119">Notes</span></span> <br/>          | <span data-ttu-id="53dcc-120">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="53dcc-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="53dcc-121">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="53dcc-121">Structure Content</span></span>

<span data-ttu-id="53dcc-122">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="53dcc-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="53dcc-123">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="53dcc-123">Structure Properties</span></span>

<span data-ttu-id="53dcc-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="53dcc-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="53dcc-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53dcc-125">Property</span></span>                | <span data-ttu-id="53dcc-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="53dcc-126">xsi:type</span></span>           | <span data-ttu-id="53dcc-127">Valor</span><span class="sxs-lookup"><span data-stu-id="53dcc-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="53dcc-128">DataType</span><span class="sxs-lookup"><span data-stu-id="53dcc-128">DataType</span></span><br/>     | <span data-ttu-id="53dcc-129">string</span><span class="sxs-lookup"><span data-stu-id="53dcc-129">string</span></span><br/>  | <span data-ttu-id="53dcc-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="53dcc-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="53dcc-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="53dcc-131">DefaultValue</span></span><br/> | <span data-ttu-id="53dcc-132">integer</span><span class="sxs-lookup"><span data-stu-id="53dcc-132">integer</span></span><br/> | <span data-ttu-id="53dcc-133">0</span><span class="sxs-lookup"><span data-stu-id="53dcc-133">0</span></span><br/>               |
| <span data-ttu-id="53dcc-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="53dcc-134">MaxValue</span></span><br/>     | <span data-ttu-id="53dcc-135">integer</span><span class="sxs-lookup"><span data-stu-id="53dcc-135">integer</span></span><br/> | <span data-ttu-id="53dcc-136">100</span><span class="sxs-lookup"><span data-stu-id="53dcc-136">100</span></span><br/>             |
| <span data-ttu-id="53dcc-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="53dcc-137">MinValue</span></span><br/>     | <span data-ttu-id="53dcc-138">integer</span><span class="sxs-lookup"><span data-stu-id="53dcc-138">integer</span></span><br/> | <span data-ttu-id="53dcc-139">0</span><span class="sxs-lookup"><span data-stu-id="53dcc-139">0</span></span><br/>               |
| <span data-ttu-id="53dcc-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="53dcc-140">Multiple</span></span><br/>     | <span data-ttu-id="53dcc-141">integer</span><span class="sxs-lookup"><span data-stu-id="53dcc-141">integer</span></span><br/> | <span data-ttu-id="53dcc-142">1</span><span class="sxs-lookup"><span data-stu-id="53dcc-142">1</span></span><br/>               |
| <span data-ttu-id="53dcc-143">Mandatory</span><span class="sxs-lookup"><span data-stu-id="53dcc-143">Mandatory</span></span><br/>    | <span data-ttu-id="53dcc-144">string</span><span class="sxs-lookup"><span data-stu-id="53dcc-144">string</span></span><br/>  | <span data-ttu-id="53dcc-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="53dcc-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="53dcc-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="53dcc-146">UnitType</span></span><br/>     | <span data-ttu-id="53dcc-147">string</span><span class="sxs-lookup"><span data-stu-id="53dcc-147">string</span></span><br/>  | <span data-ttu-id="53dcc-148">percent</span><span class="sxs-lookup"><span data-stu-id="53dcc-148">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="53dcc-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53dcc-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53dcc-150">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="53dcc-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




