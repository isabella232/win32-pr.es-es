---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7918f1a466621377e57190e0b967980fec1a07e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698025"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="2012f-104">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="2012f-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="2012f-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="2012f-105">This topic is not current.</span></span> <span data-ttu-id="2012f-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2012f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2012f-107">Especifica el factor de escala en la dirección de ImageableSizeWidth para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="2012f-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="2012f-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2012f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2012f-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2012f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2012f-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2012f-110">Element Information</span></span>



| <span data-ttu-id="2012f-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="2012f-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="2012f-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2012f-112">Element Type</span></span> <br/>   | <span data-ttu-id="2012f-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2012f-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="2012f-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2012f-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2012f-115">Página</span><span class="sxs-lookup"><span data-stu-id="2012f-115">Page</span></span><br/>                                         |
| <span data-ttu-id="2012f-116">Notas</span><span class="sxs-lookup"><span data-stu-id="2012f-116">Notes</span></span> <br/>          | <span data-ttu-id="2012f-117">Vinculado a elemento PageScaling, opción personalizada</span><span class="sxs-lookup"><span data-stu-id="2012f-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2012f-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2012f-118">Structure Content</span></span>

<span data-ttu-id="2012f-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2012f-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="2012f-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="2012f-120">Structure Properties</span></span>

<span data-ttu-id="2012f-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2012f-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2012f-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2012f-122">Property</span></span>                | <span data-ttu-id="2012f-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2012f-123">xsi:type</span></span>           | <span data-ttu-id="2012f-124">Value</span><span class="sxs-lookup"><span data-stu-id="2012f-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2012f-125">DataType</span><span class="sxs-lookup"><span data-stu-id="2012f-125">DataType</span></span><br/>     | <span data-ttu-id="2012f-126">String</span><span class="sxs-lookup"><span data-stu-id="2012f-126">String</span></span><br/>  | <span data-ttu-id="2012f-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2012f-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="2012f-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2012f-128">DefaultValue</span></span><br/> | <span data-ttu-id="2012f-129">Entero</span><span class="sxs-lookup"><span data-stu-id="2012f-129">Integer</span></span><br/> | <span data-ttu-id="2012f-130">no definido</span><span class="sxs-lookup"><span data-stu-id="2012f-130">undefined</span></span><br/>       |
| <span data-ttu-id="2012f-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2012f-131">MaxValue</span></span><br/>     | <span data-ttu-id="2012f-132">Entero</span><span class="sxs-lookup"><span data-stu-id="2012f-132">Integer</span></span><br/> | <span data-ttu-id="2012f-133">no definido</span><span class="sxs-lookup"><span data-stu-id="2012f-133">undefined</span></span><br/>       |
| <span data-ttu-id="2012f-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="2012f-134">MinValue</span></span><br/>     | <span data-ttu-id="2012f-135">Entero</span><span class="sxs-lookup"><span data-stu-id="2012f-135">Integer</span></span><br/> | <span data-ttu-id="2012f-136">1</span><span class="sxs-lookup"><span data-stu-id="2012f-136">1</span></span><br/>               |
| <span data-ttu-id="2012f-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="2012f-137">Mandatory</span></span><br/>    | <span data-ttu-id="2012f-138">String</span><span class="sxs-lookup"><span data-stu-id="2012f-138">String</span></span><br/>  | <span data-ttu-id="2012f-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="2012f-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2012f-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="2012f-140">Multiple</span></span><br/>     | <span data-ttu-id="2012f-141">Entero</span><span class="sxs-lookup"><span data-stu-id="2012f-141">Integer</span></span><br/> | <span data-ttu-id="2012f-142">1</span><span class="sxs-lookup"><span data-stu-id="2012f-142">1</span></span><br/>               |
| <span data-ttu-id="2012f-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="2012f-143">UnitType</span></span><br/>     | <span data-ttu-id="2012f-144">String</span><span class="sxs-lookup"><span data-stu-id="2012f-144">String</span></span><br/>  | <span data-ttu-id="2012f-145">microns</span><span class="sxs-lookup"><span data-stu-id="2012f-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="2012f-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2012f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2012f-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2012f-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




