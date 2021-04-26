---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b558a044716c5c13ae012665193f958f8ce6aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997902"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="caa75-104">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="caa75-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="caa75-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="caa75-105">This topic is not current.</span></span> <span data-ttu-id="caa75-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="caa75-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="caa75-107">Especifica el origen de una hoja de cobertura frontal personalizada.</span><span class="sxs-lookup"><span data-stu-id="caa75-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="caa75-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="caa75-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="caa75-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="caa75-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="caa75-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="caa75-110">Element Information</span></span>



| <span data-ttu-id="caa75-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="caa75-111">Name</span></span> | <span data-ttu-id="caa75-112">Value</span><span class="sxs-lookup"><span data-stu-id="caa75-112">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="caa75-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="caa75-113">Element Type</span></span> <br/>   | <span data-ttu-id="caa75-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="caa75-114">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="caa75-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="caa75-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="caa75-116">Documento</span><span class="sxs-lookup"><span data-stu-id="caa75-116">Document</span></span><br/>                             |
| <span data-ttu-id="caa75-117">Notas</span><span class="sxs-lookup"><span data-stu-id="caa75-117">Notes</span></span> <br/>          | <span data-ttu-id="caa75-118">Vinculado al elemento DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="caa75-118">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="caa75-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="caa75-119">Structure Content</span></span>

<span data-ttu-id="caa75-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="caa75-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverFrontSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="caa75-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="caa75-121">Structure Properties</span></span>

<span data-ttu-id="caa75-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="caa75-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="caa75-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="caa75-123">Property</span></span>                | <span data-ttu-id="caa75-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="caa75-124">xsi:type</span></span>           | <span data-ttu-id="caa75-125">Value</span><span class="sxs-lookup"><span data-stu-id="caa75-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="caa75-126">DataType</span><span class="sxs-lookup"><span data-stu-id="caa75-126">DataType</span></span><br/>     | <span data-ttu-id="caa75-127">string</span><span class="sxs-lookup"><span data-stu-id="caa75-127">string</span></span><br/>  | <span data-ttu-id="caa75-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="caa75-128">xs:string</span></span><br/>       |
| <span data-ttu-id="caa75-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="caa75-129">DefaultValue</span></span><br/> | <span data-ttu-id="caa75-130">string</span><span class="sxs-lookup"><span data-stu-id="caa75-130">string</span></span><br/>  | <span data-ttu-id="caa75-131">no definido</span><span class="sxs-lookup"><span data-stu-id="caa75-131">undefined</span></span><br/>       |
| <span data-ttu-id="caa75-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="caa75-132">MaxLength</span></span><br/>    | <span data-ttu-id="caa75-133">integer</span><span class="sxs-lookup"><span data-stu-id="caa75-133">integer</span></span><br/> | <span data-ttu-id="caa75-134">no definido</span><span class="sxs-lookup"><span data-stu-id="caa75-134">undefined</span></span><br/>       |
| <span data-ttu-id="caa75-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="caa75-135">MinLength</span></span><br/>    | <span data-ttu-id="caa75-136">integer</span><span class="sxs-lookup"><span data-stu-id="caa75-136">integer</span></span><br/> | <span data-ttu-id="caa75-137">1</span><span class="sxs-lookup"><span data-stu-id="caa75-137">1</span></span><br/>               |
| <span data-ttu-id="caa75-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="caa75-138">Mandatory</span></span><br/>    | <span data-ttu-id="caa75-139">string</span><span class="sxs-lookup"><span data-stu-id="caa75-139">string</span></span><br/>  | <span data-ttu-id="caa75-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="caa75-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="caa75-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="caa75-141">UnitType</span></span><br/>     | <span data-ttu-id="caa75-142">string</span><span class="sxs-lookup"><span data-stu-id="caa75-142">string</span></span><br/>  | <span data-ttu-id="caa75-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="caa75-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="caa75-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="caa75-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caa75-145">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="caa75-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




