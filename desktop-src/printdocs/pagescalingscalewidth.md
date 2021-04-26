---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ef53d9fe2906ae04cd1e7e3ea1513a631bc162
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997462"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="b9a79-104">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="b9a79-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="b9a79-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="b9a79-105">This topic is not current.</span></span> <span data-ttu-id="b9a79-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b9a79-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b9a79-107">Especifica el factor de escalado en la dirección ImageableSizeWidth para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="b9a79-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="b9a79-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b9a79-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b9a79-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="b9a79-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b9a79-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b9a79-110">Element Information</span></span>



| <span data-ttu-id="b9a79-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="b9a79-111">Name</span></span> | <span data-ttu-id="b9a79-112">Value</span><span class="sxs-lookup"><span data-stu-id="b9a79-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="b9a79-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b9a79-113">Element Type</span></span> <br/>   | <span data-ttu-id="b9a79-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b9a79-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="b9a79-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="b9a79-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b9a79-116">Página</span><span class="sxs-lookup"><span data-stu-id="b9a79-116">Page</span></span><br/>                                         |
| <span data-ttu-id="b9a79-117">Notas</span><span class="sxs-lookup"><span data-stu-id="b9a79-117">Notes</span></span> <br/>          | <span data-ttu-id="b9a79-118">Vinculado al elemento PageScaling, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="b9a79-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b9a79-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="b9a79-119">Structure Content</span></span>

<span data-ttu-id="b9a79-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="b9a79-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b9a79-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="b9a79-121">Structure Properties</span></span>

<span data-ttu-id="b9a79-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="b9a79-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b9a79-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9a79-123">Property</span></span>                | <span data-ttu-id="b9a79-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b9a79-124">xsi:type</span></span>           | <span data-ttu-id="b9a79-125">Value</span><span class="sxs-lookup"><span data-stu-id="b9a79-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b9a79-126">DataType</span><span class="sxs-lookup"><span data-stu-id="b9a79-126">DataType</span></span><br/>     | <span data-ttu-id="b9a79-127">String</span><span class="sxs-lookup"><span data-stu-id="b9a79-127">String</span></span><br/>  | <span data-ttu-id="b9a79-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b9a79-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="b9a79-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b9a79-129">DefaultValue</span></span><br/> | <span data-ttu-id="b9a79-130">Entero</span><span class="sxs-lookup"><span data-stu-id="b9a79-130">Integer</span></span><br/> | <span data-ttu-id="b9a79-131">no definido</span><span class="sxs-lookup"><span data-stu-id="b9a79-131">undefined</span></span><br/>       |
| <span data-ttu-id="b9a79-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b9a79-132">MaxValue</span></span><br/>     | <span data-ttu-id="b9a79-133">Entero</span><span class="sxs-lookup"><span data-stu-id="b9a79-133">Integer</span></span><br/> | <span data-ttu-id="b9a79-134">no definido</span><span class="sxs-lookup"><span data-stu-id="b9a79-134">undefined</span></span><br/>       |
| <span data-ttu-id="b9a79-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="b9a79-135">MinValue</span></span><br/>     | <span data-ttu-id="b9a79-136">Entero</span><span class="sxs-lookup"><span data-stu-id="b9a79-136">Integer</span></span><br/> | <span data-ttu-id="b9a79-137">1</span><span class="sxs-lookup"><span data-stu-id="b9a79-137">1</span></span><br/>               |
| <span data-ttu-id="b9a79-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="b9a79-138">Mandatory</span></span><br/>    | <span data-ttu-id="b9a79-139">String</span><span class="sxs-lookup"><span data-stu-id="b9a79-139">String</span></span><br/>  | <span data-ttu-id="b9a79-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="b9a79-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b9a79-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="b9a79-141">Multiple</span></span><br/>     | <span data-ttu-id="b9a79-142">Entero</span><span class="sxs-lookup"><span data-stu-id="b9a79-142">Integer</span></span><br/> | <span data-ttu-id="b9a79-143">1</span><span class="sxs-lookup"><span data-stu-id="b9a79-143">1</span></span><br/>               |
| <span data-ttu-id="b9a79-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="b9a79-144">UnitType</span></span><br/>     | <span data-ttu-id="b9a79-145">String</span><span class="sxs-lookup"><span data-stu-id="b9a79-145">String</span></span><br/>  | <span data-ttu-id="b9a79-146">Micras</span><span class="sxs-lookup"><span data-stu-id="b9a79-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b9a79-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9a79-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9a79-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b9a79-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




