---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246f77c5878b74e1b149c6d4020230030fb3c5b0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707609"
---
# <a name="pagescalingscale"></a><span data-ttu-id="b6209-104">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="b6209-104">PageScalingScale</span></span>

<span data-ttu-id="b6209-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="b6209-105">This topic is not current.</span></span> <span data-ttu-id="b6209-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b6209-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b6209-107">Especifica el factor de escala para el ajuste de escala del cuadrado personalizado.</span><span class="sxs-lookup"><span data-stu-id="b6209-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="b6209-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b6209-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b6209-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="b6209-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b6209-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b6209-110">Element Information</span></span>



| <span data-ttu-id="b6209-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6209-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="b6209-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b6209-112">Element Type</span></span> <br/>   | <span data-ttu-id="b6209-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b6209-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="b6209-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="b6209-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b6209-115">Página</span><span class="sxs-lookup"><span data-stu-id="b6209-115">Page</span></span><br/>                                         |
| <span data-ttu-id="b6209-116">Notas</span><span class="sxs-lookup"><span data-stu-id="b6209-116">Notes</span></span> <br/>          | <span data-ttu-id="b6209-117">Vinculado a elemento PageScaling, opción personalizada</span><span class="sxs-lookup"><span data-stu-id="b6209-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b6209-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="b6209-118">Structure Content</span></span>

<span data-ttu-id="b6209-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="b6209-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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

## <a name="structure-properties"></a><span data-ttu-id="b6209-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="b6209-120">Structure Properties</span></span>

<span data-ttu-id="b6209-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="b6209-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b6209-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6209-122">Property</span></span>                | <span data-ttu-id="b6209-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b6209-123">xsi:type</span></span>           | <span data-ttu-id="b6209-124">Value</span><span class="sxs-lookup"><span data-stu-id="b6209-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b6209-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b6209-125">DataType</span></span><br/>     | <span data-ttu-id="b6209-126">string</span><span class="sxs-lookup"><span data-stu-id="b6209-126">string</span></span><br/>  | <span data-ttu-id="b6209-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b6209-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="b6209-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b6209-128">DefaultValue</span></span><br/> | <span data-ttu-id="b6209-129">integer</span><span class="sxs-lookup"><span data-stu-id="b6209-129">integer</span></span><br/> | <span data-ttu-id="b6209-130">no definido</span><span class="sxs-lookup"><span data-stu-id="b6209-130">undefined</span></span><br/>       |
| <span data-ttu-id="b6209-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b6209-131">MaxValue</span></span><br/>     | <span data-ttu-id="b6209-132">integer</span><span class="sxs-lookup"><span data-stu-id="b6209-132">integer</span></span><br/> | <span data-ttu-id="b6209-133">no definido</span><span class="sxs-lookup"><span data-stu-id="b6209-133">undefined</span></span><br/>       |
| <span data-ttu-id="b6209-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b6209-134">MinValue</span></span><br/>     | <span data-ttu-id="b6209-135">integer</span><span class="sxs-lookup"><span data-stu-id="b6209-135">integer</span></span><br/> | <span data-ttu-id="b6209-136">1</span><span class="sxs-lookup"><span data-stu-id="b6209-136">1</span></span><br/>               |
| <span data-ttu-id="b6209-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="b6209-137">Mandatory</span></span><br/>    | <span data-ttu-id="b6209-138">string</span><span class="sxs-lookup"><span data-stu-id="b6209-138">string</span></span><br/>  | <span data-ttu-id="b6209-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="b6209-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b6209-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="b6209-140">Multiple</span></span><br/>     | <span data-ttu-id="b6209-141">integer</span><span class="sxs-lookup"><span data-stu-id="b6209-141">integer</span></span><br/> | <span data-ttu-id="b6209-142">1</span><span class="sxs-lookup"><span data-stu-id="b6209-142">1</span></span><br/>               |
| <span data-ttu-id="b6209-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="b6209-143">UnitType</span></span><br/>     | <span data-ttu-id="b6209-144">string</span><span class="sxs-lookup"><span data-stu-id="b6209-144">string</span></span><br/>  | <span data-ttu-id="b6209-145">percent</span><span class="sxs-lookup"><span data-stu-id="b6209-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b6209-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6209-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6209-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b6209-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




