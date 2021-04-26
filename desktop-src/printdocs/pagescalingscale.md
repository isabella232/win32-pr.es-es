---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974242cf43bae50a8e81b17bcdd13d653032c6a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999202"
---
# <a name="pagescalingscale"></a><span data-ttu-id="ad55b-104">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="ad55b-104">PageScalingScale</span></span>

<span data-ttu-id="ad55b-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ad55b-105">This topic is not current.</span></span> <span data-ttu-id="ad55b-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ad55b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad55b-107">Especifica el factor de escalado para el escalado cuadrado personalizado.</span><span class="sxs-lookup"><span data-stu-id="ad55b-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="ad55b-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ad55b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ad55b-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ad55b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ad55b-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ad55b-110">Element Information</span></span>



| <span data-ttu-id="ad55b-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad55b-111">Name</span></span> | <span data-ttu-id="ad55b-112">Value</span><span class="sxs-lookup"><span data-stu-id="ad55b-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="ad55b-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ad55b-113">Element Type</span></span> <br/>   | <span data-ttu-id="ad55b-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ad55b-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="ad55b-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ad55b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ad55b-116">Página</span><span class="sxs-lookup"><span data-stu-id="ad55b-116">Page</span></span><br/>                                         |
| <span data-ttu-id="ad55b-117">Notas</span><span class="sxs-lookup"><span data-stu-id="ad55b-117">Notes</span></span> <br/>          | <span data-ttu-id="ad55b-118">Vinculado al elemento PageScaling, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="ad55b-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ad55b-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ad55b-119">Structure Content</span></span>

<span data-ttu-id="ad55b-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="ad55b-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ad55b-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="ad55b-121">Structure Properties</span></span>

<span data-ttu-id="ad55b-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ad55b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ad55b-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad55b-123">Property</span></span>                | <span data-ttu-id="ad55b-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ad55b-124">xsi:type</span></span>           | <span data-ttu-id="ad55b-125">Value</span><span class="sxs-lookup"><span data-stu-id="ad55b-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ad55b-126">DataType</span><span class="sxs-lookup"><span data-stu-id="ad55b-126">DataType</span></span><br/>     | <span data-ttu-id="ad55b-127">string</span><span class="sxs-lookup"><span data-stu-id="ad55b-127">string</span></span><br/>  | <span data-ttu-id="ad55b-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ad55b-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="ad55b-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ad55b-129">DefaultValue</span></span><br/> | <span data-ttu-id="ad55b-130">integer</span><span class="sxs-lookup"><span data-stu-id="ad55b-130">integer</span></span><br/> | <span data-ttu-id="ad55b-131">no definido</span><span class="sxs-lookup"><span data-stu-id="ad55b-131">undefined</span></span><br/>       |
| <span data-ttu-id="ad55b-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ad55b-132">MaxValue</span></span><br/>     | <span data-ttu-id="ad55b-133">integer</span><span class="sxs-lookup"><span data-stu-id="ad55b-133">integer</span></span><br/> | <span data-ttu-id="ad55b-134">no definido</span><span class="sxs-lookup"><span data-stu-id="ad55b-134">undefined</span></span><br/>       |
| <span data-ttu-id="ad55b-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="ad55b-135">MinValue</span></span><br/>     | <span data-ttu-id="ad55b-136">integer</span><span class="sxs-lookup"><span data-stu-id="ad55b-136">integer</span></span><br/> | <span data-ttu-id="ad55b-137">1</span><span class="sxs-lookup"><span data-stu-id="ad55b-137">1</span></span><br/>               |
| <span data-ttu-id="ad55b-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="ad55b-138">Mandatory</span></span><br/>    | <span data-ttu-id="ad55b-139">string</span><span class="sxs-lookup"><span data-stu-id="ad55b-139">string</span></span><br/>  | <span data-ttu-id="ad55b-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="ad55b-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ad55b-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="ad55b-141">Multiple</span></span><br/>     | <span data-ttu-id="ad55b-142">integer</span><span class="sxs-lookup"><span data-stu-id="ad55b-142">integer</span></span><br/> | <span data-ttu-id="ad55b-143">1</span><span class="sxs-lookup"><span data-stu-id="ad55b-143">1</span></span><br/>               |
| <span data-ttu-id="ad55b-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="ad55b-144">UnitType</span></span><br/>     | <span data-ttu-id="ad55b-145">string</span><span class="sxs-lookup"><span data-stu-id="ad55b-145">string</span></span><br/>  | <span data-ttu-id="ad55b-146">percent</span><span class="sxs-lookup"><span data-stu-id="ad55b-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ad55b-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad55b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad55b-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ad55b-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




