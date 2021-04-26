---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996892"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="27788-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="27788-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="27788-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="27788-105">This topic is not current.</span></span> <span data-ttu-id="27788-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="27788-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27788-107">Define el color de sRGB para el texto de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="27788-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="27788-108">El formato es ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="27788-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="27788-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="27788-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27788-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="27788-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="27788-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="27788-111">Element Information</span></span>



| <span data-ttu-id="27788-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="27788-112">Name</span></span> | <span data-ttu-id="27788-113">Value</span><span class="sxs-lookup"><span data-stu-id="27788-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="27788-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="27788-114">Element Type</span></span> <br/>   | <span data-ttu-id="27788-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="27788-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="27788-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="27788-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27788-117">Página</span><span class="sxs-lookup"><span data-stu-id="27788-117">Page</span></span><br/>                            |
| <span data-ttu-id="27788-118">Notas</span><span class="sxs-lookup"><span data-stu-id="27788-118">Notes</span></span> <br/>          | <span data-ttu-id="27788-119">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="27788-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="27788-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="27788-120">Structure Content</span></span>

<span data-ttu-id="27788-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="27788-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="27788-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="27788-122">Structure Properties</span></span>

<span data-ttu-id="27788-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="27788-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27788-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27788-124">Property</span></span>                | <span data-ttu-id="27788-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="27788-125">xsi:type</span></span>           | <span data-ttu-id="27788-126">Value</span><span class="sxs-lookup"><span data-stu-id="27788-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="27788-127">DataType</span><span class="sxs-lookup"><span data-stu-id="27788-127">DataType</span></span><br/>     | <span data-ttu-id="27788-128">string</span><span class="sxs-lookup"><span data-stu-id="27788-128">string</span></span><br/>  | <span data-ttu-id="27788-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="27788-129">xs:string</span></span><br/>       |
| <span data-ttu-id="27788-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="27788-130">DefaultValue</span></span><br/> | <span data-ttu-id="27788-131">integer</span><span class="sxs-lookup"><span data-stu-id="27788-131">integer</span></span><br/> | <span data-ttu-id="27788-132">no definido</span><span class="sxs-lookup"><span data-stu-id="27788-132">undefined</span></span><br/>       |
| <span data-ttu-id="27788-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="27788-133">MaxValue</span></span><br/>     | <span data-ttu-id="27788-134">integer</span><span class="sxs-lookup"><span data-stu-id="27788-134">integer</span></span><br/> | <span data-ttu-id="27788-135">no definido</span><span class="sxs-lookup"><span data-stu-id="27788-135">undefined</span></span><br/>       |
| <span data-ttu-id="27788-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="27788-136">MinValue</span></span><br/>     | <span data-ttu-id="27788-137">integer</span><span class="sxs-lookup"><span data-stu-id="27788-137">integer</span></span><br/> | <span data-ttu-id="27788-138">no definido</span><span class="sxs-lookup"><span data-stu-id="27788-138">undefined</span></span><br/>       |
| <span data-ttu-id="27788-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="27788-139">Mandatory</span></span><br/>    | <span data-ttu-id="27788-140">string</span><span class="sxs-lookup"><span data-stu-id="27788-140">string</span></span><br/>  | <span data-ttu-id="27788-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="27788-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="27788-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="27788-142">UnitType</span></span><br/>     | <span data-ttu-id="27788-143">string</span><span class="sxs-lookup"><span data-stu-id="27788-143">string</span></span><br/>  | <span data-ttu-id="27788-144">sRGB</span><span class="sxs-lookup"><span data-stu-id="27788-144">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="27788-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27788-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27788-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="27788-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




