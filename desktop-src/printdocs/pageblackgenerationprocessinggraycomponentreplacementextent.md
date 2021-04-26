---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9a790d66d1f7806a7ef86ee4a85f62225aa836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997712"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="f2155-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="f2155-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="f2155-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="f2155-105">This topic is not current.</span></span> <span data-ttu-id="f2155-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f2155-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f2155-107">Describe la extensión más allá de los neutros (en colores méticos) que se aplica GCR.</span><span class="sxs-lookup"><span data-stu-id="f2155-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="f2155-108">0 % = Reemplazo uniforme de componentes, 100 % = Reemplazo de componente gris.</span><span class="sxs-lookup"><span data-stu-id="f2155-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="f2155-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f2155-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f2155-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="f2155-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f2155-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f2155-111">Element Information</span></span>



| <span data-ttu-id="f2155-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="f2155-112">Name</span></span> | <span data-ttu-id="f2155-113">Value</span><span class="sxs-lookup"><span data-stu-id="f2155-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="f2155-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f2155-114">Element Type</span></span> <br/>   | <span data-ttu-id="f2155-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f2155-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="f2155-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="f2155-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f2155-117">Página</span><span class="sxs-lookup"><span data-stu-id="f2155-117">Page</span></span><br/>                                            |
| <span data-ttu-id="f2155-118">Notas</span><span class="sxs-lookup"><span data-stu-id="f2155-118">Notes</span></span> <br/>          | <span data-ttu-id="f2155-119">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="f2155-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f2155-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="f2155-120">Structure Content</span></span>

<span data-ttu-id="f2155-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="f2155-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="f2155-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="f2155-122">Structure Properties</span></span>

<span data-ttu-id="f2155-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="f2155-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f2155-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f2155-124">Property</span></span>                | <span data-ttu-id="f2155-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f2155-125">xsi:type</span></span>           | <span data-ttu-id="f2155-126">Value</span><span class="sxs-lookup"><span data-stu-id="f2155-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f2155-127">DataType</span><span class="sxs-lookup"><span data-stu-id="f2155-127">DataType</span></span><br/>     | <span data-ttu-id="f2155-128">string</span><span class="sxs-lookup"><span data-stu-id="f2155-128">string</span></span><br/>  | <span data-ttu-id="f2155-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f2155-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="f2155-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f2155-130">DefaultValue</span></span><br/> | <span data-ttu-id="f2155-131">string</span><span class="sxs-lookup"><span data-stu-id="f2155-131">string</span></span><br/>  | <span data-ttu-id="f2155-132">no definido</span><span class="sxs-lookup"><span data-stu-id="f2155-132">undefined</span></span><br/>       |
| <span data-ttu-id="f2155-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f2155-133">MaxValue</span></span><br/>     | <span data-ttu-id="f2155-134">integer</span><span class="sxs-lookup"><span data-stu-id="f2155-134">integer</span></span><br/> | <span data-ttu-id="f2155-135">100</span><span class="sxs-lookup"><span data-stu-id="f2155-135">100</span></span><br/>             |
| <span data-ttu-id="f2155-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="f2155-136">MinValue</span></span><br/>     | <span data-ttu-id="f2155-137">integer</span><span class="sxs-lookup"><span data-stu-id="f2155-137">integer</span></span><br/> | <span data-ttu-id="f2155-138">0</span><span class="sxs-lookup"><span data-stu-id="f2155-138">0</span></span><br/>               |
| <span data-ttu-id="f2155-139">Múltiple</span><span class="sxs-lookup"><span data-stu-id="f2155-139">Multiple</span></span><br/>     | <span data-ttu-id="f2155-140">integer</span><span class="sxs-lookup"><span data-stu-id="f2155-140">integer</span></span><br/> | <span data-ttu-id="f2155-141">1</span><span class="sxs-lookup"><span data-stu-id="f2155-141">1</span></span><br/>               |
| <span data-ttu-id="f2155-142">Mandatory</span><span class="sxs-lookup"><span data-stu-id="f2155-142">Mandatory</span></span><br/>    | <span data-ttu-id="f2155-143">string</span><span class="sxs-lookup"><span data-stu-id="f2155-143">string</span></span><br/>  | <span data-ttu-id="f2155-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="f2155-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f2155-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="f2155-145">UnitType</span></span><br/>     | <span data-ttu-id="f2155-146">string</span><span class="sxs-lookup"><span data-stu-id="f2155-146">string</span></span><br/>  | <span data-ttu-id="f2155-147">percent</span><span class="sxs-lookup"><span data-stu-id="f2155-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f2155-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2155-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2155-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="f2155-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




