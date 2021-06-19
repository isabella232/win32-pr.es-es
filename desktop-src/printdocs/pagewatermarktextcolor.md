---
description: Obtenga información sobre el parámetro PageWatermarkTextColor. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7cb7b893ec9a2ecf774173cf2a9f2410549087
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396020"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="7f020-105">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="7f020-105">PageWatermarkTextColor</span></span>

<span data-ttu-id="7f020-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="7f020-106">This topic is not current.</span></span> <span data-ttu-id="7f020-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7f020-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7f020-108">Define el color de sRGB para el texto de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="7f020-108">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="7f020-109">El formato es ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="7f020-109">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="7f020-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7f020-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7f020-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7f020-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7f020-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7f020-112">Element Information</span></span>



| <span data-ttu-id="7f020-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="7f020-113">Name</span></span> | <span data-ttu-id="7f020-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7f020-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="7f020-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7f020-115">Element Type</span></span> <br/>   | <span data-ttu-id="7f020-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7f020-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="7f020-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="7f020-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7f020-118">Página</span><span class="sxs-lookup"><span data-stu-id="7f020-118">Page</span></span><br/>                            |
| <span data-ttu-id="7f020-119">Notas</span><span class="sxs-lookup"><span data-stu-id="7f020-119">Notes</span></span> <br/>          | <span data-ttu-id="7f020-120">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="7f020-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7f020-121">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7f020-121">Structure Content</span></span>

<span data-ttu-id="7f020-122">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="7f020-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7f020-123">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="7f020-123">Structure Properties</span></span>

<span data-ttu-id="7f020-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="7f020-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7f020-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7f020-125">Property</span></span>                | <span data-ttu-id="7f020-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7f020-126">xsi:type</span></span>           | <span data-ttu-id="7f020-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7f020-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7f020-128">DataType</span><span class="sxs-lookup"><span data-stu-id="7f020-128">DataType</span></span><br/>     | <span data-ttu-id="7f020-129">string</span><span class="sxs-lookup"><span data-stu-id="7f020-129">string</span></span><br/>  | <span data-ttu-id="7f020-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="7f020-130">xs:string</span></span><br/>       |
| <span data-ttu-id="7f020-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7f020-131">DefaultValue</span></span><br/> | <span data-ttu-id="7f020-132">integer</span><span class="sxs-lookup"><span data-stu-id="7f020-132">integer</span></span><br/> | <span data-ttu-id="7f020-133">no definido</span><span class="sxs-lookup"><span data-stu-id="7f020-133">undefined</span></span><br/>       |
| <span data-ttu-id="7f020-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7f020-134">MaxValue</span></span><br/>     | <span data-ttu-id="7f020-135">integer</span><span class="sxs-lookup"><span data-stu-id="7f020-135">integer</span></span><br/> | <span data-ttu-id="7f020-136">no definido</span><span class="sxs-lookup"><span data-stu-id="7f020-136">undefined</span></span><br/>       |
| <span data-ttu-id="7f020-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="7f020-137">MinValue</span></span><br/>     | <span data-ttu-id="7f020-138">integer</span><span class="sxs-lookup"><span data-stu-id="7f020-138">integer</span></span><br/> | <span data-ttu-id="7f020-139">no definido</span><span class="sxs-lookup"><span data-stu-id="7f020-139">undefined</span></span><br/>       |
| <span data-ttu-id="7f020-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="7f020-140">Mandatory</span></span><br/>    | <span data-ttu-id="7f020-141">string</span><span class="sxs-lookup"><span data-stu-id="7f020-141">string</span></span><br/>  | <span data-ttu-id="7f020-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7f020-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7f020-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="7f020-143">UnitType</span></span><br/>     | <span data-ttu-id="7f020-144">string</span><span class="sxs-lookup"><span data-stu-id="7f020-144">string</span></span><br/>  | <span data-ttu-id="7f020-145">sRGB</span><span class="sxs-lookup"><span data-stu-id="7f020-145">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="7f020-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f020-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f020-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="7f020-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




