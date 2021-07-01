---
description: Obtenga información sobre el parámetro PageBlackGenerationProcessingBlackInkLimit. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118430"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="58c13-105">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="58c13-105">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="58c13-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="58c13-106">This topic is not current.</span></span> <span data-ttu-id="58c13-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="58c13-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="58c13-108">El contenido de la aplicación etiquetado con el color con nombre especificado DEBE aparecer en todas las separaciones de colores.</span><span class="sxs-lookup"><span data-stu-id="58c13-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="58c13-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="58c13-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="58c13-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="58c13-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="58c13-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="58c13-111">Element Information</span></span>



| <span data-ttu-id="58c13-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="58c13-112">Name</span></span> | <span data-ttu-id="58c13-113">Valor</span><span class="sxs-lookup"><span data-stu-id="58c13-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="58c13-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="58c13-114">Element Type</span></span> <br/>   | <span data-ttu-id="58c13-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="58c13-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="58c13-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="58c13-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="58c13-117">Página</span><span class="sxs-lookup"><span data-stu-id="58c13-117">Page</span></span><br/>                                            |
| <span data-ttu-id="58c13-118">Notas</span><span class="sxs-lookup"><span data-stu-id="58c13-118">Notes</span></span> <br/>          | <span data-ttu-id="58c13-119">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="58c13-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="58c13-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="58c13-120">Structure Content</span></span>

<span data-ttu-id="58c13-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="58c13-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
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

## <a name="structure-properties"></a><span data-ttu-id="58c13-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="58c13-122">Structure Properties</span></span>

<span data-ttu-id="58c13-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="58c13-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="58c13-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="58c13-124">Property</span></span>                | <span data-ttu-id="58c13-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="58c13-125">xsi:type</span></span>           | <span data-ttu-id="58c13-126">Valor</span><span class="sxs-lookup"><span data-stu-id="58c13-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="58c13-127">DataType</span><span class="sxs-lookup"><span data-stu-id="58c13-127">DataType</span></span><br/>     | <span data-ttu-id="58c13-128">string</span><span class="sxs-lookup"><span data-stu-id="58c13-128">string</span></span><br/>  | <span data-ttu-id="58c13-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="58c13-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="58c13-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="58c13-130">DefaultValue</span></span><br/> | <span data-ttu-id="58c13-131">string</span><span class="sxs-lookup"><span data-stu-id="58c13-131">string</span></span><br/>  | <span data-ttu-id="58c13-132">no definido</span><span class="sxs-lookup"><span data-stu-id="58c13-132">undefined</span></span><br/>       |
| <span data-ttu-id="58c13-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="58c13-133">MaxValue</span></span><br/>     | <span data-ttu-id="58c13-134">integer</span><span class="sxs-lookup"><span data-stu-id="58c13-134">integer</span></span><br/> | <span data-ttu-id="58c13-135">100</span><span class="sxs-lookup"><span data-stu-id="58c13-135">100</span></span><br/>             |
| <span data-ttu-id="58c13-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="58c13-136">MinValue</span></span><br/>     | <span data-ttu-id="58c13-137">integer</span><span class="sxs-lookup"><span data-stu-id="58c13-137">integer</span></span><br/> | <span data-ttu-id="58c13-138">0</span><span class="sxs-lookup"><span data-stu-id="58c13-138">0</span></span><br/>               |
| <span data-ttu-id="58c13-139">Múltiple</span><span class="sxs-lookup"><span data-stu-id="58c13-139">Multiple</span></span><br/>     | <span data-ttu-id="58c13-140">integer</span><span class="sxs-lookup"><span data-stu-id="58c13-140">integer</span></span><br/> | <span data-ttu-id="58c13-141">1</span><span class="sxs-lookup"><span data-stu-id="58c13-141">1</span></span><br/>               |
| <span data-ttu-id="58c13-142">Mandatory</span><span class="sxs-lookup"><span data-stu-id="58c13-142">Mandatory</span></span><br/>    | <span data-ttu-id="58c13-143">string</span><span class="sxs-lookup"><span data-stu-id="58c13-143">string</span></span><br/>  | <span data-ttu-id="58c13-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="58c13-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="58c13-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="58c13-145">UnitType</span></span><br/>     | <span data-ttu-id="58c13-146">string</span><span class="sxs-lookup"><span data-stu-id="58c13-146">string</span></span><br/>  | <span data-ttu-id="58c13-147">percent</span><span class="sxs-lookup"><span data-stu-id="58c13-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="58c13-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58c13-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58c13-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="58c13-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




