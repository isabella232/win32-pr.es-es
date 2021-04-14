---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a475f7fa68cd961d9d7a7f42e40fc9ea80a72a4e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424139"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="ef2cd-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="ef2cd-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="ef2cd-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="ef2cd-105">This topic is not current.</span></span> <span data-ttu-id="ef2cd-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ef2cd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ef2cd-107">Especifica el desplazamiento de escala en la dirección de ImageableSizeHeight para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="ef2cd-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="ef2cd-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ef2cd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ef2cd-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ef2cd-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ef2cd-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ef2cd-110">Element Information</span></span>



| <span data-ttu-id="ef2cd-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef2cd-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef2cd-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ef2cd-112">Element Type</span></span> <br/>   | <span data-ttu-id="ef2cd-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ef2cd-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="ef2cd-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ef2cd-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ef2cd-115">Página</span><span class="sxs-lookup"><span data-stu-id="ef2cd-115">Page</span></span><br/>                                         |
| <span data-ttu-id="ef2cd-116">Notas</span><span class="sxs-lookup"><span data-stu-id="ef2cd-116">Notes</span></span> <br/>          | <span data-ttu-id="ef2cd-117">Vinculado a elemento PageScaling, opción personalizada</span><span class="sxs-lookup"><span data-stu-id="ef2cd-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ef2cd-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ef2cd-118">Structure Content</span></span>

<span data-ttu-id="ef2cd-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="ef2cd-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ef2cd-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="ef2cd-120">Structure Properties</span></span>

<span data-ttu-id="ef2cd-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ef2cd-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ef2cd-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef2cd-122">Property</span></span>                | <span data-ttu-id="ef2cd-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ef2cd-123">xsi:type</span></span>           | <span data-ttu-id="ef2cd-124">Value</span><span class="sxs-lookup"><span data-stu-id="ef2cd-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ef2cd-125">DataType</span><span class="sxs-lookup"><span data-stu-id="ef2cd-125">DataType</span></span><br/>     | <span data-ttu-id="ef2cd-126">string</span><span class="sxs-lookup"><span data-stu-id="ef2cd-126">string</span></span><br/>  | <span data-ttu-id="ef2cd-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ef2cd-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="ef2cd-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ef2cd-128">DefaultValue</span></span><br/> | <span data-ttu-id="ef2cd-129">integer</span><span class="sxs-lookup"><span data-stu-id="ef2cd-129">integer</span></span><br/> | <span data-ttu-id="ef2cd-130">no definido</span><span class="sxs-lookup"><span data-stu-id="ef2cd-130">undefined</span></span><br/>       |
| <span data-ttu-id="ef2cd-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ef2cd-131">MaxValue</span></span><br/>     | <span data-ttu-id="ef2cd-132">integer</span><span class="sxs-lookup"><span data-stu-id="ef2cd-132">integer</span></span><br/> | <span data-ttu-id="ef2cd-133">no definido</span><span class="sxs-lookup"><span data-stu-id="ef2cd-133">undefined</span></span><br/>       |
| <span data-ttu-id="ef2cd-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="ef2cd-134">MinValue</span></span><br/>     | <span data-ttu-id="ef2cd-135">integer</span><span class="sxs-lookup"><span data-stu-id="ef2cd-135">integer</span></span><br/> | <span data-ttu-id="ef2cd-136">no definido</span><span class="sxs-lookup"><span data-stu-id="ef2cd-136">undefined</span></span><br/>       |
| <span data-ttu-id="ef2cd-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="ef2cd-137">Mandatory</span></span><br/>    | <span data-ttu-id="ef2cd-138">string</span><span class="sxs-lookup"><span data-stu-id="ef2cd-138">string</span></span><br/>  | <span data-ttu-id="ef2cd-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="ef2cd-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ef2cd-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="ef2cd-140">Multiple</span></span><br/>     | <span data-ttu-id="ef2cd-141">integer</span><span class="sxs-lookup"><span data-stu-id="ef2cd-141">integer</span></span><br/> | <span data-ttu-id="ef2cd-142">1</span><span class="sxs-lookup"><span data-stu-id="ef2cd-142">1</span></span><br/>               |
| <span data-ttu-id="ef2cd-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="ef2cd-143">UnitType</span></span><br/>     | <span data-ttu-id="ef2cd-144">string</span><span class="sxs-lookup"><span data-stu-id="ef2cd-144">string</span></span><br/>  | <span data-ttu-id="ef2cd-145">microns</span><span class="sxs-lookup"><span data-stu-id="ef2cd-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ef2cd-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef2cd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef2cd-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ef2cd-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




