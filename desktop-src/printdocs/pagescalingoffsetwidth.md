---
description: Obtenga información sobre el parámetro PageScalingOffsetWidth. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63152e6a3d9f8ea47bac3b5a0efe559e71e0cb35
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548853"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="dbaad-105">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="dbaad-105">PageScalingOffsetWidth</span></span>

<span data-ttu-id="dbaad-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="dbaad-106">This topic is not current.</span></span> <span data-ttu-id="dbaad-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dbaad-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dbaad-108">Especifica el desplazamiento de escala en la dirección ImageableSizeWidth para el escalado personalizado.</span><span class="sxs-lookup"><span data-stu-id="dbaad-108">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="dbaad-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dbaad-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dbaad-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dbaad-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dbaad-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dbaad-111">Element Information</span></span>



| <span data-ttu-id="dbaad-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="dbaad-112">Name</span></span> | <span data-ttu-id="dbaad-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dbaad-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="dbaad-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dbaad-114">Element Type</span></span> <br/>   | <span data-ttu-id="dbaad-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dbaad-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="dbaad-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="dbaad-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dbaad-117">Página</span><span class="sxs-lookup"><span data-stu-id="dbaad-117">Page</span></span><br/>                                         |
| <span data-ttu-id="dbaad-118">Notas</span><span class="sxs-lookup"><span data-stu-id="dbaad-118">Notes</span></span> <br/>          | <span data-ttu-id="dbaad-119">Vinculado al elemento PageScaling, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="dbaad-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dbaad-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dbaad-120">Structure Content</span></span>

<span data-ttu-id="dbaad-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="dbaad-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="dbaad-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="dbaad-122">Structure Properties</span></span>

<span data-ttu-id="dbaad-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="dbaad-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dbaad-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbaad-124">Property</span></span>                | <span data-ttu-id="dbaad-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dbaad-125">xsi:type</span></span>           | <span data-ttu-id="dbaad-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dbaad-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dbaad-127">DataType</span><span class="sxs-lookup"><span data-stu-id="dbaad-127">DataType</span></span><br/>     | <span data-ttu-id="dbaad-128">string</span><span class="sxs-lookup"><span data-stu-id="dbaad-128">string</span></span><br/>  | <span data-ttu-id="dbaad-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dbaad-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="dbaad-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dbaad-130">DefaultValue</span></span><br/> | <span data-ttu-id="dbaad-131">integer</span><span class="sxs-lookup"><span data-stu-id="dbaad-131">integer</span></span><br/> | <span data-ttu-id="dbaad-132">no definido</span><span class="sxs-lookup"><span data-stu-id="dbaad-132">undefined</span></span><br/>       |
| <span data-ttu-id="dbaad-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dbaad-133">MaxValue</span></span><br/>     | <span data-ttu-id="dbaad-134">integer</span><span class="sxs-lookup"><span data-stu-id="dbaad-134">integer</span></span><br/> | <span data-ttu-id="dbaad-135">no definido</span><span class="sxs-lookup"><span data-stu-id="dbaad-135">undefined</span></span><br/>       |
| <span data-ttu-id="dbaad-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="dbaad-136">MinValue</span></span><br/>     | <span data-ttu-id="dbaad-137">integer</span><span class="sxs-lookup"><span data-stu-id="dbaad-137">integer</span></span><br/> | <span data-ttu-id="dbaad-138">no definido</span><span class="sxs-lookup"><span data-stu-id="dbaad-138">undefined</span></span><br/>       |
| <span data-ttu-id="dbaad-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="dbaad-139">Mandatory</span></span><br/>    | <span data-ttu-id="dbaad-140">string</span><span class="sxs-lookup"><span data-stu-id="dbaad-140">string</span></span><br/>  | <span data-ttu-id="dbaad-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="dbaad-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dbaad-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="dbaad-142">Multiple</span></span><br/>     | <span data-ttu-id="dbaad-143">integer</span><span class="sxs-lookup"><span data-stu-id="dbaad-143">integer</span></span><br/> | <span data-ttu-id="dbaad-144">1</span><span class="sxs-lookup"><span data-stu-id="dbaad-144">1</span></span><br/>               |
| <span data-ttu-id="dbaad-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="dbaad-145">UnitType</span></span><br/>     | <span data-ttu-id="dbaad-146">string</span><span class="sxs-lookup"><span data-stu-id="dbaad-146">string</span></span><br/>  | <span data-ttu-id="dbaad-147">Micras</span><span class="sxs-lookup"><span data-stu-id="dbaad-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dbaad-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbaad-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbaad-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="dbaad-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




