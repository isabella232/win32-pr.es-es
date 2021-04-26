---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04615b85939d483f6bd2e720afa65a88d44c1caf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998382"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="6dca3-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="6dca3-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="6dca3-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="6dca3-105">This topic is not current.</span></span> <span data-ttu-id="6dca3-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6dca3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6dca3-107">Especifica el ancho del medianía de enlace.</span><span class="sxs-lookup"><span data-stu-id="6dca3-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="6dca3-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6dca3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6dca3-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="6dca3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6dca3-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6dca3-110">Element Information</span></span>



| <span data-ttu-id="6dca3-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="6dca3-111">Name</span></span> | <span data-ttu-id="6dca3-112">Value</span><span class="sxs-lookup"><span data-stu-id="6dca3-112">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="6dca3-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6dca3-113">Element Type</span></span> <br/>   | <span data-ttu-id="6dca3-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6dca3-114">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="6dca3-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="6dca3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6dca3-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="6dca3-116">Job</span></span> <br/>                         |
| <span data-ttu-id="6dca3-117">Notas</span><span class="sxs-lookup"><span data-stu-id="6dca3-117">Notes</span></span> <br/>          | <span data-ttu-id="6dca3-118">Vinculado al elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="6dca3-118">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6dca3-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="6dca3-119">Structure Content</span></span>

<span data-ttu-id="6dca3-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="6dca3-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="6dca3-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="6dca3-121">Structure Properties</span></span>

<span data-ttu-id="6dca3-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="6dca3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6dca3-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6dca3-123">Property</span></span>                | <span data-ttu-id="6dca3-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6dca3-124">xsi:type</span></span>           | <span data-ttu-id="6dca3-125">Value</span><span class="sxs-lookup"><span data-stu-id="6dca3-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6dca3-126">DataType</span><span class="sxs-lookup"><span data-stu-id="6dca3-126">DataType</span></span><br/>     | <span data-ttu-id="6dca3-127">string</span><span class="sxs-lookup"><span data-stu-id="6dca3-127">string</span></span><br/>  | <span data-ttu-id="6dca3-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6dca3-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="6dca3-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6dca3-129">DefaultValue</span></span><br/> | <span data-ttu-id="6dca3-130">integer</span><span class="sxs-lookup"><span data-stu-id="6dca3-130">integer</span></span><br/> | <span data-ttu-id="6dca3-131">no definido</span><span class="sxs-lookup"><span data-stu-id="6dca3-131">undefined</span></span><br/>       |
| <span data-ttu-id="6dca3-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6dca3-132">MaxValue</span></span><br/>     | <span data-ttu-id="6dca3-133">integer</span><span class="sxs-lookup"><span data-stu-id="6dca3-133">integer</span></span><br/> | <span data-ttu-id="6dca3-134">no definido</span><span class="sxs-lookup"><span data-stu-id="6dca3-134">undefined</span></span><br/>       |
| <span data-ttu-id="6dca3-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="6dca3-135">MinValue</span></span><br/>     | <span data-ttu-id="6dca3-136">integer</span><span class="sxs-lookup"><span data-stu-id="6dca3-136">integer</span></span><br/> | <span data-ttu-id="6dca3-137">no definido</span><span class="sxs-lookup"><span data-stu-id="6dca3-137">undefined</span></span><br/>       |
| <span data-ttu-id="6dca3-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="6dca3-138">Mandatory</span></span><br/>    | <span data-ttu-id="6dca3-139">String</span><span class="sxs-lookup"><span data-stu-id="6dca3-139">String</span></span><br/>  | <span data-ttu-id="6dca3-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="6dca3-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6dca3-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="6dca3-141">Multiple</span></span><br/>     | <span data-ttu-id="6dca3-142">integer</span><span class="sxs-lookup"><span data-stu-id="6dca3-142">integer</span></span><br/> | <span data-ttu-id="6dca3-143">1</span><span class="sxs-lookup"><span data-stu-id="6dca3-143">1</span></span><br/>               |
| <span data-ttu-id="6dca3-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="6dca3-144">UnitType</span></span><br/>     | <span data-ttu-id="6dca3-145">string</span><span class="sxs-lookup"><span data-stu-id="6dca3-145">string</span></span><br/>  | <span data-ttu-id="6dca3-146">Micras</span><span class="sxs-lookup"><span data-stu-id="6dca3-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6dca3-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6dca3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dca3-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="6dca3-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




