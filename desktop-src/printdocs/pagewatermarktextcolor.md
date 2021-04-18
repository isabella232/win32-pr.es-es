---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77e76dd1b304a46b2760565a09fe0134d3f0b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104547462"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="3e8db-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="3e8db-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="3e8db-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="3e8db-105">This topic is not current.</span></span> <span data-ttu-id="3e8db-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3e8db-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3e8db-107">Define el color sRGB del texto de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="3e8db-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="3e8db-108">El formato es ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="3e8db-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="3e8db-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3e8db-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3e8db-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="3e8db-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3e8db-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3e8db-111">Element Information</span></span>



| <span data-ttu-id="3e8db-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="3e8db-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="3e8db-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3e8db-113">Element Type</span></span> <br/>   | <span data-ttu-id="3e8db-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3e8db-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="3e8db-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="3e8db-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3e8db-116">Página</span><span class="sxs-lookup"><span data-stu-id="3e8db-116">Page</span></span><br/>                            |
| <span data-ttu-id="3e8db-117">Notas</span><span class="sxs-lookup"><span data-stu-id="3e8db-117">Notes</span></span> <br/>          | <span data-ttu-id="3e8db-118">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="3e8db-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3e8db-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="3e8db-119">Structure Content</span></span>

<span data-ttu-id="3e8db-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e8db-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3e8db-121">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="3e8db-121">Structure Properties</span></span>

<span data-ttu-id="3e8db-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="3e8db-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3e8db-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3e8db-123">Property</span></span>                | <span data-ttu-id="3e8db-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3e8db-124">xsi:type</span></span>           | <span data-ttu-id="3e8db-125">Value</span><span class="sxs-lookup"><span data-stu-id="3e8db-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3e8db-126">DataType</span><span class="sxs-lookup"><span data-stu-id="3e8db-126">DataType</span></span><br/>     | <span data-ttu-id="3e8db-127">string</span><span class="sxs-lookup"><span data-stu-id="3e8db-127">string</span></span><br/>  | <span data-ttu-id="3e8db-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="3e8db-128">xs:string</span></span><br/>       |
| <span data-ttu-id="3e8db-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3e8db-129">DefaultValue</span></span><br/> | <span data-ttu-id="3e8db-130">integer</span><span class="sxs-lookup"><span data-stu-id="3e8db-130">integer</span></span><br/> | <span data-ttu-id="3e8db-131">no definido</span><span class="sxs-lookup"><span data-stu-id="3e8db-131">undefined</span></span><br/>       |
| <span data-ttu-id="3e8db-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3e8db-132">MaxValue</span></span><br/>     | <span data-ttu-id="3e8db-133">integer</span><span class="sxs-lookup"><span data-stu-id="3e8db-133">integer</span></span><br/> | <span data-ttu-id="3e8db-134">no definido</span><span class="sxs-lookup"><span data-stu-id="3e8db-134">undefined</span></span><br/>       |
| <span data-ttu-id="3e8db-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="3e8db-135">MinValue</span></span><br/>     | <span data-ttu-id="3e8db-136">integer</span><span class="sxs-lookup"><span data-stu-id="3e8db-136">integer</span></span><br/> | <span data-ttu-id="3e8db-137">no definido</span><span class="sxs-lookup"><span data-stu-id="3e8db-137">undefined</span></span><br/>       |
| <span data-ttu-id="3e8db-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="3e8db-138">Mandatory</span></span><br/>    | <span data-ttu-id="3e8db-139">string</span><span class="sxs-lookup"><span data-stu-id="3e8db-139">string</span></span><br/>  | <span data-ttu-id="3e8db-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="3e8db-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3e8db-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="3e8db-141">UnitType</span></span><br/>     | <span data-ttu-id="3e8db-142">string</span><span class="sxs-lookup"><span data-stu-id="3e8db-142">string</span></span><br/>  | <span data-ttu-id="3e8db-143">sRGB</span><span class="sxs-lookup"><span data-stu-id="3e8db-143">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="3e8db-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e8db-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e8db-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="3e8db-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




