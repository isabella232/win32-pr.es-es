---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a91178f1506196ab505a90de8bf3a3163fa8a3c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993743"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="4a90d-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="4a90d-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="4a90d-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4a90d-105">This topic is not current.</span></span> <span data-ttu-id="4a90d-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4a90d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4a90d-107">Especifica el desplazamiento de escala en la dirección ImageableSizeHeight para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="4a90d-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="4a90d-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4a90d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4a90d-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4a90d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4a90d-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4a90d-110">Element Information</span></span>



| <span data-ttu-id="4a90d-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a90d-111">Name</span></span> | <span data-ttu-id="4a90d-112">Value</span><span class="sxs-lookup"><span data-stu-id="4a90d-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="4a90d-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4a90d-113">Element Type</span></span> <br/>   | <span data-ttu-id="4a90d-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4a90d-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="4a90d-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="4a90d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4a90d-116">Página</span><span class="sxs-lookup"><span data-stu-id="4a90d-116">Page</span></span><br/>                                         |
| <span data-ttu-id="4a90d-117">Notas</span><span class="sxs-lookup"><span data-stu-id="4a90d-117">Notes</span></span> <br/>          | <span data-ttu-id="4a90d-118">Vinculado al elemento PageScaling, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="4a90d-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4a90d-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4a90d-119">Structure Content</span></span>

<span data-ttu-id="4a90d-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="4a90d-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="4a90d-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="4a90d-121">Structure Properties</span></span>

<span data-ttu-id="4a90d-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="4a90d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4a90d-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a90d-123">Property</span></span>                | <span data-ttu-id="4a90d-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4a90d-124">xsi:type</span></span>           | <span data-ttu-id="4a90d-125">Value</span><span class="sxs-lookup"><span data-stu-id="4a90d-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4a90d-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4a90d-126">DataType</span></span><br/>     | <span data-ttu-id="4a90d-127">string</span><span class="sxs-lookup"><span data-stu-id="4a90d-127">string</span></span><br/>  | <span data-ttu-id="4a90d-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4a90d-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="4a90d-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4a90d-129">DefaultValue</span></span><br/> | <span data-ttu-id="4a90d-130">integer</span><span class="sxs-lookup"><span data-stu-id="4a90d-130">integer</span></span><br/> | <span data-ttu-id="4a90d-131">no definido</span><span class="sxs-lookup"><span data-stu-id="4a90d-131">undefined</span></span><br/>       |
| <span data-ttu-id="4a90d-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4a90d-132">MaxValue</span></span><br/>     | <span data-ttu-id="4a90d-133">integer</span><span class="sxs-lookup"><span data-stu-id="4a90d-133">integer</span></span><br/> | <span data-ttu-id="4a90d-134">no definido</span><span class="sxs-lookup"><span data-stu-id="4a90d-134">undefined</span></span><br/>       |
| <span data-ttu-id="4a90d-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="4a90d-135">MinValue</span></span><br/>     | <span data-ttu-id="4a90d-136">integer</span><span class="sxs-lookup"><span data-stu-id="4a90d-136">integer</span></span><br/> | <span data-ttu-id="4a90d-137">no definido</span><span class="sxs-lookup"><span data-stu-id="4a90d-137">undefined</span></span><br/>       |
| <span data-ttu-id="4a90d-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="4a90d-138">Mandatory</span></span><br/>    | <span data-ttu-id="4a90d-139">string</span><span class="sxs-lookup"><span data-stu-id="4a90d-139">string</span></span><br/>  | <span data-ttu-id="4a90d-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4a90d-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4a90d-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="4a90d-141">Multiple</span></span><br/>     | <span data-ttu-id="4a90d-142">integer</span><span class="sxs-lookup"><span data-stu-id="4a90d-142">integer</span></span><br/> | <span data-ttu-id="4a90d-143">1</span><span class="sxs-lookup"><span data-stu-id="4a90d-143">1</span></span><br/>               |
| <span data-ttu-id="4a90d-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="4a90d-144">UnitType</span></span><br/>     | <span data-ttu-id="4a90d-145">string</span><span class="sxs-lookup"><span data-stu-id="4a90d-145">string</span></span><br/>  | <span data-ttu-id="4a90d-146">Micras</span><span class="sxs-lookup"><span data-stu-id="4a90d-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4a90d-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a90d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a90d-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4a90d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




