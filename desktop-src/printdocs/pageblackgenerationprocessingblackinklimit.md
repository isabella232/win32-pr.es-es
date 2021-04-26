---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3052d8cec8fd46c2f7607e6366aa6868cccbdbda
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996192"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="5f4b7-104">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="5f4b7-104">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="5f4b7-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5f4b7-105">This topic is not current.</span></span> <span data-ttu-id="5f4b7-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5f4b7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5f4b7-107">El contenido de la aplicación etiquetado con el color con nombre especificado DEBE aparecer en todas las separaciones de colores.</span><span class="sxs-lookup"><span data-stu-id="5f4b7-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="5f4b7-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5f4b7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5f4b7-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5f4b7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5f4b7-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5f4b7-110">Element Information</span></span>



| <span data-ttu-id="5f4b7-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f4b7-111">Name</span></span> | <span data-ttu-id="5f4b7-112">Value</span><span class="sxs-lookup"><span data-stu-id="5f4b7-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="5f4b7-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5f4b7-113">Element Type</span></span> <br/>   | <span data-ttu-id="5f4b7-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5f4b7-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="5f4b7-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5f4b7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5f4b7-116">Página</span><span class="sxs-lookup"><span data-stu-id="5f4b7-116">Page</span></span><br/>                                            |
| <span data-ttu-id="5f4b7-117">Notas</span><span class="sxs-lookup"><span data-stu-id="5f4b7-117">Notes</span></span> <br/>          | <span data-ttu-id="5f4b7-118">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="5f4b7-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5f4b7-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5f4b7-119">Structure Content</span></span>

<span data-ttu-id="5f4b7-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5f4b7-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="5f4b7-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="5f4b7-121">Structure Properties</span></span>

<span data-ttu-id="5f4b7-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5f4b7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5f4b7-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f4b7-123">Property</span></span>                | <span data-ttu-id="5f4b7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5f4b7-124">xsi:type</span></span>           | <span data-ttu-id="5f4b7-125">Value</span><span class="sxs-lookup"><span data-stu-id="5f4b7-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5f4b7-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5f4b7-126">DataType</span></span><br/>     | <span data-ttu-id="5f4b7-127">string</span><span class="sxs-lookup"><span data-stu-id="5f4b7-127">string</span></span><br/>  | <span data-ttu-id="5f4b7-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f4b7-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5f4b7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5f4b7-129">DefaultValue</span></span><br/> | <span data-ttu-id="5f4b7-130">string</span><span class="sxs-lookup"><span data-stu-id="5f4b7-130">string</span></span><br/>  | <span data-ttu-id="5f4b7-131">no definido</span><span class="sxs-lookup"><span data-stu-id="5f4b7-131">undefined</span></span><br/>       |
| <span data-ttu-id="5f4b7-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5f4b7-132">MaxValue</span></span><br/>     | <span data-ttu-id="5f4b7-133">integer</span><span class="sxs-lookup"><span data-stu-id="5f4b7-133">integer</span></span><br/> | <span data-ttu-id="5f4b7-134">100</span><span class="sxs-lookup"><span data-stu-id="5f4b7-134">100</span></span><br/>             |
| <span data-ttu-id="5f4b7-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="5f4b7-135">MinValue</span></span><br/>     | <span data-ttu-id="5f4b7-136">integer</span><span class="sxs-lookup"><span data-stu-id="5f4b7-136">integer</span></span><br/> | <span data-ttu-id="5f4b7-137">0</span><span class="sxs-lookup"><span data-stu-id="5f4b7-137">0</span></span><br/>               |
| <span data-ttu-id="5f4b7-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="5f4b7-138">Multiple</span></span><br/>     | <span data-ttu-id="5f4b7-139">integer</span><span class="sxs-lookup"><span data-stu-id="5f4b7-139">integer</span></span><br/> | <span data-ttu-id="5f4b7-140">1</span><span class="sxs-lookup"><span data-stu-id="5f4b7-140">1</span></span><br/>               |
| <span data-ttu-id="5f4b7-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5f4b7-141">Mandatory</span></span><br/>    | <span data-ttu-id="5f4b7-142">string</span><span class="sxs-lookup"><span data-stu-id="5f4b7-142">string</span></span><br/>  | <span data-ttu-id="5f4b7-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5f4b7-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5f4b7-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="5f4b7-144">UnitType</span></span><br/>     | <span data-ttu-id="5f4b7-145">string</span><span class="sxs-lookup"><span data-stu-id="5f4b7-145">string</span></span><br/>  | <span data-ttu-id="5f4b7-146">percent</span><span class="sxs-lookup"><span data-stu-id="5f4b7-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5f4b7-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f4b7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f4b7-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5f4b7-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




