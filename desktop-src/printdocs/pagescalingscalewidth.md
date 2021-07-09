---
description: Obtenga información sobre el parámetro PageScalingScaleWidth. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6180395eb656ee40d8558f7208fec2ad2fce8
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548803"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="d24c1-105">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="d24c1-105">PageScalingScaleWidth</span></span>

<span data-ttu-id="d24c1-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d24c1-106">This topic is not current.</span></span> <span data-ttu-id="d24c1-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d24c1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d24c1-108">Especifica el factor de escalado en la dirección ImageableSizeWidth para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="d24c1-108">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="d24c1-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d24c1-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d24c1-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="d24c1-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d24c1-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d24c1-111">Element Information</span></span>



| <span data-ttu-id="d24c1-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="d24c1-112">Name</span></span> | <span data-ttu-id="d24c1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d24c1-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="d24c1-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d24c1-114">Element Type</span></span> <br/>   | <span data-ttu-id="d24c1-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d24c1-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="d24c1-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d24c1-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d24c1-117">Página</span><span class="sxs-lookup"><span data-stu-id="d24c1-117">Page</span></span><br/>                                         |
| <span data-ttu-id="d24c1-118">Notas</span><span class="sxs-lookup"><span data-stu-id="d24c1-118">Notes</span></span> <br/>          | <span data-ttu-id="d24c1-119">Vinculado al elemento PageScaling, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="d24c1-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d24c1-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="d24c1-120">Structure Content</span></span>

<span data-ttu-id="d24c1-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="d24c1-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d24c1-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="d24c1-122">Structure Properties</span></span>

<span data-ttu-id="d24c1-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d24c1-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d24c1-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d24c1-124">Property</span></span>                | <span data-ttu-id="d24c1-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d24c1-125">xsi:type</span></span>           | <span data-ttu-id="d24c1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d24c1-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d24c1-127">DataType</span><span class="sxs-lookup"><span data-stu-id="d24c1-127">DataType</span></span><br/>     | <span data-ttu-id="d24c1-128">String</span><span class="sxs-lookup"><span data-stu-id="d24c1-128">String</span></span><br/>  | <span data-ttu-id="d24c1-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d24c1-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="d24c1-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d24c1-130">DefaultValue</span></span><br/> | <span data-ttu-id="d24c1-131">Entero</span><span class="sxs-lookup"><span data-stu-id="d24c1-131">Integer</span></span><br/> | <span data-ttu-id="d24c1-132">no definido</span><span class="sxs-lookup"><span data-stu-id="d24c1-132">undefined</span></span><br/>       |
| <span data-ttu-id="d24c1-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d24c1-133">MaxValue</span></span><br/>     | <span data-ttu-id="d24c1-134">Entero</span><span class="sxs-lookup"><span data-stu-id="d24c1-134">Integer</span></span><br/> | <span data-ttu-id="d24c1-135">no definido</span><span class="sxs-lookup"><span data-stu-id="d24c1-135">undefined</span></span><br/>       |
| <span data-ttu-id="d24c1-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="d24c1-136">MinValue</span></span><br/>     | <span data-ttu-id="d24c1-137">Entero</span><span class="sxs-lookup"><span data-stu-id="d24c1-137">Integer</span></span><br/> | <span data-ttu-id="d24c1-138">1</span><span class="sxs-lookup"><span data-stu-id="d24c1-138">1</span></span><br/>               |
| <span data-ttu-id="d24c1-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="d24c1-139">Mandatory</span></span><br/>    | <span data-ttu-id="d24c1-140">String</span><span class="sxs-lookup"><span data-stu-id="d24c1-140">String</span></span><br/>  | <span data-ttu-id="d24c1-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="d24c1-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d24c1-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="d24c1-142">Multiple</span></span><br/>     | <span data-ttu-id="d24c1-143">Entero</span><span class="sxs-lookup"><span data-stu-id="d24c1-143">Integer</span></span><br/> | <span data-ttu-id="d24c1-144">1</span><span class="sxs-lookup"><span data-stu-id="d24c1-144">1</span></span><br/>               |
| <span data-ttu-id="d24c1-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="d24c1-145">UnitType</span></span><br/>     | <span data-ttu-id="d24c1-146">String</span><span class="sxs-lookup"><span data-stu-id="d24c1-146">String</span></span><br/>  | <span data-ttu-id="d24c1-147">Micras</span><span class="sxs-lookup"><span data-stu-id="d24c1-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d24c1-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d24c1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d24c1-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d24c1-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




