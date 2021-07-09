---
description: Obtenga información sobre el parámetro PageScalingScaleHeight. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51bdb5577b5e3863cfadab1fa9eb74ff40d54da
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548843"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="5abf8-105">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="5abf8-105">PageScalingScaleHeight</span></span>

<span data-ttu-id="5abf8-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5abf8-106">This topic is not current.</span></span> <span data-ttu-id="5abf8-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5abf8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5abf8-108">Especifica el factor de escalado en la dirección ImageableSizeHeight para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="5abf8-108">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="5abf8-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5abf8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5abf8-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5abf8-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5abf8-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5abf8-111">Element Information</span></span>



| <span data-ttu-id="5abf8-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="5abf8-112">Name</span></span> | <span data-ttu-id="5abf8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5abf8-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="5abf8-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5abf8-114">Element Type</span></span> <br/>   | <span data-ttu-id="5abf8-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5abf8-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="5abf8-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5abf8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5abf8-117">Página</span><span class="sxs-lookup"><span data-stu-id="5abf8-117">Page</span></span><br/>                                         |
| <span data-ttu-id="5abf8-118">Notas</span><span class="sxs-lookup"><span data-stu-id="5abf8-118">Notes</span></span> <br/>          | <span data-ttu-id="5abf8-119">Vinculado al elemento PageScaling, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="5abf8-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5abf8-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5abf8-120">Structure Content</span></span>

<span data-ttu-id="5abf8-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5abf8-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5abf8-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="5abf8-122">Structure Properties</span></span>

<span data-ttu-id="5abf8-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5abf8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5abf8-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5abf8-124">Property</span></span>                | <span data-ttu-id="5abf8-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5abf8-125">xsi:type</span></span>           | <span data-ttu-id="5abf8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5abf8-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5abf8-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5abf8-127">DataType</span></span><br/>     | <span data-ttu-id="5abf8-128">String</span><span class="sxs-lookup"><span data-stu-id="5abf8-128">String</span></span><br/>  | <span data-ttu-id="5abf8-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5abf8-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="5abf8-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5abf8-130">DefaultValue</span></span><br/> | <span data-ttu-id="5abf8-131">Entero</span><span class="sxs-lookup"><span data-stu-id="5abf8-131">Integer</span></span><br/> | <span data-ttu-id="5abf8-132">no definido</span><span class="sxs-lookup"><span data-stu-id="5abf8-132">undefined</span></span><br/>       |
| <span data-ttu-id="5abf8-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5abf8-133">MaxValue</span></span><br/>     | <span data-ttu-id="5abf8-134">Entero</span><span class="sxs-lookup"><span data-stu-id="5abf8-134">Integer</span></span><br/> | <span data-ttu-id="5abf8-135">no definido</span><span class="sxs-lookup"><span data-stu-id="5abf8-135">undefined</span></span><br/>       |
| <span data-ttu-id="5abf8-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="5abf8-136">MinValue</span></span><br/>     | <span data-ttu-id="5abf8-137">Entero</span><span class="sxs-lookup"><span data-stu-id="5abf8-137">Integer</span></span><br/> | <span data-ttu-id="5abf8-138">1</span><span class="sxs-lookup"><span data-stu-id="5abf8-138">1</span></span><br/>               |
| <span data-ttu-id="5abf8-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5abf8-139">Mandatory</span></span><br/>    | <span data-ttu-id="5abf8-140">String</span><span class="sxs-lookup"><span data-stu-id="5abf8-140">String</span></span><br/>  | <span data-ttu-id="5abf8-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5abf8-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5abf8-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="5abf8-142">Multiple</span></span><br/>     | <span data-ttu-id="5abf8-143">Entero</span><span class="sxs-lookup"><span data-stu-id="5abf8-143">Integer</span></span><br/> | <span data-ttu-id="5abf8-144">1</span><span class="sxs-lookup"><span data-stu-id="5abf8-144">1</span></span><br/>               |
| <span data-ttu-id="5abf8-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="5abf8-145">UnitType</span></span><br/>     | <span data-ttu-id="5abf8-146">String</span><span class="sxs-lookup"><span data-stu-id="5abf8-146">String</span></span><br/>  | <span data-ttu-id="5abf8-147">percent</span><span class="sxs-lookup"><span data-stu-id="5abf8-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5abf8-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5abf8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5abf8-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5abf8-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




