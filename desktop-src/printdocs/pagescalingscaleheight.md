---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3f91f6b188dadbd86a18152be5228b62d21ab4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707621"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="2c890-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="2c890-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="2c890-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="2c890-105">This topic is not current.</span></span> <span data-ttu-id="2c890-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2c890-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c890-107">Especifica el factor de escala en la dirección de ImageableSizeHeight para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="2c890-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="2c890-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2c890-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2c890-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2c890-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2c890-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2c890-110">Element Information</span></span>



| <span data-ttu-id="2c890-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c890-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="2c890-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2c890-112">Element Type</span></span> <br/>   | <span data-ttu-id="2c890-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2c890-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="2c890-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2c890-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2c890-115">Página</span><span class="sxs-lookup"><span data-stu-id="2c890-115">Page</span></span><br/>                                         |
| <span data-ttu-id="2c890-116">Notas</span><span class="sxs-lookup"><span data-stu-id="2c890-116">Notes</span></span> <br/>          | <span data-ttu-id="2c890-117">Vinculado a elemento PageScaling, opción personalizada</span><span class="sxs-lookup"><span data-stu-id="2c890-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2c890-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2c890-118">Structure Content</span></span>

<span data-ttu-id="2c890-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2c890-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleHeight">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="2c890-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="2c890-120">Structure Properties</span></span>

<span data-ttu-id="2c890-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2c890-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2c890-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c890-122">Property</span></span>                | <span data-ttu-id="2c890-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2c890-123">xsi:type</span></span>           | <span data-ttu-id="2c890-124">Value</span><span class="sxs-lookup"><span data-stu-id="2c890-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2c890-125">DataType</span><span class="sxs-lookup"><span data-stu-id="2c890-125">DataType</span></span><br/>     | <span data-ttu-id="2c890-126">String</span><span class="sxs-lookup"><span data-stu-id="2c890-126">String</span></span><br/>  | <span data-ttu-id="2c890-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2c890-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="2c890-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2c890-128">DefaultValue</span></span><br/> | <span data-ttu-id="2c890-129">Entero</span><span class="sxs-lookup"><span data-stu-id="2c890-129">Integer</span></span><br/> | <span data-ttu-id="2c890-130">no definido</span><span class="sxs-lookup"><span data-stu-id="2c890-130">undefined</span></span><br/>       |
| <span data-ttu-id="2c890-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2c890-131">MaxValue</span></span><br/>     | <span data-ttu-id="2c890-132">Entero</span><span class="sxs-lookup"><span data-stu-id="2c890-132">Integer</span></span><br/> | <span data-ttu-id="2c890-133">no definido</span><span class="sxs-lookup"><span data-stu-id="2c890-133">undefined</span></span><br/>       |
| <span data-ttu-id="2c890-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="2c890-134">MinValue</span></span><br/>     | <span data-ttu-id="2c890-135">Entero</span><span class="sxs-lookup"><span data-stu-id="2c890-135">Integer</span></span><br/> | <span data-ttu-id="2c890-136">1</span><span class="sxs-lookup"><span data-stu-id="2c890-136">1</span></span><br/>               |
| <span data-ttu-id="2c890-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="2c890-137">Mandatory</span></span><br/>    | <span data-ttu-id="2c890-138">String</span><span class="sxs-lookup"><span data-stu-id="2c890-138">String</span></span><br/>  | <span data-ttu-id="2c890-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="2c890-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2c890-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="2c890-140">Multiple</span></span><br/>     | <span data-ttu-id="2c890-141">Entero</span><span class="sxs-lookup"><span data-stu-id="2c890-141">Integer</span></span><br/> | <span data-ttu-id="2c890-142">1</span><span class="sxs-lookup"><span data-stu-id="2c890-142">1</span></span><br/>               |
| <span data-ttu-id="2c890-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="2c890-143">UnitType</span></span><br/>     | <span data-ttu-id="2c890-144">String</span><span class="sxs-lookup"><span data-stu-id="2c890-144">String</span></span><br/>  | <span data-ttu-id="2c890-145">percent</span><span class="sxs-lookup"><span data-stu-id="2c890-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="2c890-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c890-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c890-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2c890-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




