---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914274"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="5ae94-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="5ae94-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="5ae94-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="5ae94-105">This topic is not current.</span></span> <span data-ttu-id="5ae94-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5ae94-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5ae94-107">Describe la extensión más allá de las neutras (en colores cromáticos) que GCR aplica.</span><span class="sxs-lookup"><span data-stu-id="5ae94-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="5ae94-108">0% = reemplazo uniforme de componentes, 100% = reemplazo del componente gris.</span><span class="sxs-lookup"><span data-stu-id="5ae94-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="5ae94-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5ae94-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5ae94-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5ae94-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5ae94-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5ae94-111">Element Information</span></span>



| <span data-ttu-id="5ae94-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ae94-112">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="5ae94-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5ae94-113">Element Type</span></span> <br/>   | <span data-ttu-id="5ae94-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5ae94-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="5ae94-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5ae94-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5ae94-116">Página</span><span class="sxs-lookup"><span data-stu-id="5ae94-116">Page</span></span><br/>                                            |
| <span data-ttu-id="5ae94-117">Notas</span><span class="sxs-lookup"><span data-stu-id="5ae94-117">Notes</span></span> <br/>          | <span data-ttu-id="5ae94-118">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="5ae94-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5ae94-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5ae94-119">Structure Content</span></span>

<span data-ttu-id="5ae94-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5ae94-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5ae94-121">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="5ae94-121">Structure Properties</span></span>

<span data-ttu-id="5ae94-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5ae94-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5ae94-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ae94-123">Property</span></span>                | <span data-ttu-id="5ae94-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5ae94-124">xsi:type</span></span>           | <span data-ttu-id="5ae94-125">Value</span><span class="sxs-lookup"><span data-stu-id="5ae94-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5ae94-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5ae94-126">DataType</span></span><br/>     | <span data-ttu-id="5ae94-127">string</span><span class="sxs-lookup"><span data-stu-id="5ae94-127">string</span></span><br/>  | <span data-ttu-id="5ae94-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5ae94-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5ae94-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5ae94-129">DefaultValue</span></span><br/> | <span data-ttu-id="5ae94-130">string</span><span class="sxs-lookup"><span data-stu-id="5ae94-130">string</span></span><br/>  | <span data-ttu-id="5ae94-131">no definido</span><span class="sxs-lookup"><span data-stu-id="5ae94-131">undefined</span></span><br/>       |
| <span data-ttu-id="5ae94-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5ae94-132">MaxValue</span></span><br/>     | <span data-ttu-id="5ae94-133">integer</span><span class="sxs-lookup"><span data-stu-id="5ae94-133">integer</span></span><br/> | <span data-ttu-id="5ae94-134">100</span><span class="sxs-lookup"><span data-stu-id="5ae94-134">100</span></span><br/>             |
| <span data-ttu-id="5ae94-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="5ae94-135">MinValue</span></span><br/>     | <span data-ttu-id="5ae94-136">integer</span><span class="sxs-lookup"><span data-stu-id="5ae94-136">integer</span></span><br/> | <span data-ttu-id="5ae94-137">0</span><span class="sxs-lookup"><span data-stu-id="5ae94-137">0</span></span><br/>               |
| <span data-ttu-id="5ae94-138">Múltiple</span><span class="sxs-lookup"><span data-stu-id="5ae94-138">Multiple</span></span><br/>     | <span data-ttu-id="5ae94-139">integer</span><span class="sxs-lookup"><span data-stu-id="5ae94-139">integer</span></span><br/> | <span data-ttu-id="5ae94-140">1</span><span class="sxs-lookup"><span data-stu-id="5ae94-140">1</span></span><br/>               |
| <span data-ttu-id="5ae94-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5ae94-141">Mandatory</span></span><br/>    | <span data-ttu-id="5ae94-142">string</span><span class="sxs-lookup"><span data-stu-id="5ae94-142">string</span></span><br/>  | <span data-ttu-id="5ae94-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="5ae94-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5ae94-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="5ae94-144">UnitType</span></span><br/>     | <span data-ttu-id="5ae94-145">string</span><span class="sxs-lookup"><span data-stu-id="5ae94-145">string</span></span><br/>  | <span data-ttu-id="5ae94-146">percent</span><span class="sxs-lookup"><span data-stu-id="5ae94-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5ae94-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ae94-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae94-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5ae94-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




