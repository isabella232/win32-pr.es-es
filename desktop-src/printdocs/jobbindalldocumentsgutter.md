---
description: Obtenga información sobre el elemento JobBindAllDocumentsGutter, que especifica el ancho del medianía de enlace.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42180ff9a00d1502d844b270fe5da7324825ca3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409078"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="52f08-103">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="52f08-103">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="52f08-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="52f08-104">This topic is not current.</span></span> <span data-ttu-id="52f08-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="52f08-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="52f08-106">Especifica el ancho del medianía de enlace.</span><span class="sxs-lookup"><span data-stu-id="52f08-106">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="52f08-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="52f08-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="52f08-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="52f08-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="52f08-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="52f08-109">Element Information</span></span>



| <span data-ttu-id="52f08-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="52f08-110">Name</span></span> | <span data-ttu-id="52f08-111">Valor</span><span class="sxs-lookup"><span data-stu-id="52f08-111">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="52f08-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="52f08-112">Element Type</span></span> <br/>   | <span data-ttu-id="52f08-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="52f08-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="52f08-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="52f08-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="52f08-115">Trabajo</span><span class="sxs-lookup"><span data-stu-id="52f08-115">Job</span></span> <br/>                         |
| <span data-ttu-id="52f08-116">Notas</span><span class="sxs-lookup"><span data-stu-id="52f08-116">Notes</span></span> <br/>          | <span data-ttu-id="52f08-117">Vinculado al elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="52f08-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="52f08-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="52f08-118">Structure Content</span></span>

<span data-ttu-id="52f08-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="52f08-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="52f08-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="52f08-120">Structure Properties</span></span>

<span data-ttu-id="52f08-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="52f08-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="52f08-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52f08-122">Property</span></span>                | <span data-ttu-id="52f08-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="52f08-123">xsi:type</span></span>           | <span data-ttu-id="52f08-124">Valor</span><span class="sxs-lookup"><span data-stu-id="52f08-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="52f08-125">DataType</span><span class="sxs-lookup"><span data-stu-id="52f08-125">DataType</span></span><br/>     | <span data-ttu-id="52f08-126">string</span><span class="sxs-lookup"><span data-stu-id="52f08-126">string</span></span><br/>  | <span data-ttu-id="52f08-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="52f08-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="52f08-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="52f08-128">DefaultValue</span></span><br/> | <span data-ttu-id="52f08-129">integer</span><span class="sxs-lookup"><span data-stu-id="52f08-129">integer</span></span><br/> | <span data-ttu-id="52f08-130">no definido</span><span class="sxs-lookup"><span data-stu-id="52f08-130">undefined</span></span><br/>       |
| <span data-ttu-id="52f08-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="52f08-131">MaxValue</span></span><br/>     | <span data-ttu-id="52f08-132">integer</span><span class="sxs-lookup"><span data-stu-id="52f08-132">integer</span></span><br/> | <span data-ttu-id="52f08-133">no definido</span><span class="sxs-lookup"><span data-stu-id="52f08-133">undefined</span></span><br/>       |
| <span data-ttu-id="52f08-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="52f08-134">MinValue</span></span><br/>     | <span data-ttu-id="52f08-135">integer</span><span class="sxs-lookup"><span data-stu-id="52f08-135">integer</span></span><br/> | <span data-ttu-id="52f08-136">no definido</span><span class="sxs-lookup"><span data-stu-id="52f08-136">undefined</span></span><br/>       |
| <span data-ttu-id="52f08-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="52f08-137">Mandatory</span></span><br/>    | <span data-ttu-id="52f08-138">String</span><span class="sxs-lookup"><span data-stu-id="52f08-138">String</span></span><br/>  | <span data-ttu-id="52f08-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="52f08-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="52f08-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="52f08-140">Multiple</span></span><br/>     | <span data-ttu-id="52f08-141">integer</span><span class="sxs-lookup"><span data-stu-id="52f08-141">integer</span></span><br/> | <span data-ttu-id="52f08-142">1</span><span class="sxs-lookup"><span data-stu-id="52f08-142">1</span></span><br/>               |
| <span data-ttu-id="52f08-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="52f08-143">UnitType</span></span><br/>     | <span data-ttu-id="52f08-144">string</span><span class="sxs-lookup"><span data-stu-id="52f08-144">string</span></span><br/>  | <span data-ttu-id="52f08-145">Micras</span><span class="sxs-lookup"><span data-stu-id="52f08-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="52f08-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52f08-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f08-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="52f08-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




