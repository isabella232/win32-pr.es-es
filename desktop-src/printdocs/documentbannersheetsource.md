---
description: Obtenga información sobre el elemento DocumentBannerSheetSource, que especifica el origen de una hoja de banner personalizada.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33aa949982e98781c42cbf6aa770dbd4e3d1707
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409478"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="2080c-103">DocumentBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="2080c-103">DocumentBannerSheetSource</span></span>

<span data-ttu-id="2080c-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="2080c-104">This topic is not current.</span></span> <span data-ttu-id="2080c-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2080c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2080c-106">Especifica el origen de una hoja de banner personalizada.</span><span class="sxs-lookup"><span data-stu-id="2080c-106">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="2080c-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2080c-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2080c-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2080c-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2080c-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2080c-109">Element Information</span></span>



| <span data-ttu-id="2080c-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="2080c-110">Name</span></span> | <span data-ttu-id="2080c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="2080c-111">Value</span></span> |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="2080c-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2080c-112">Element Type</span></span> <br/>   | <span data-ttu-id="2080c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2080c-113">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="2080c-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2080c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2080c-115">Documento</span><span class="sxs-lookup"><span data-stu-id="2080c-115">Document</span></span><br/>                              |
| <span data-ttu-id="2080c-116">Notas</span><span class="sxs-lookup"><span data-stu-id="2080c-116">Notes</span></span> <br/>          | <span data-ttu-id="2080c-117">Vinculado al elemento DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="2080c-117">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2080c-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2080c-118">Structure Content</span></span>

<span data-ttu-id="2080c-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2080c-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBannerSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="2080c-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="2080c-120">Structure Properties</span></span>

<span data-ttu-id="2080c-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2080c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2080c-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2080c-122">Property</span></span>                | <span data-ttu-id="2080c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2080c-123">xsi:type</span></span>           | <span data-ttu-id="2080c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2080c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2080c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="2080c-125">DataType</span></span><br/>     | <span data-ttu-id="2080c-126">string</span><span class="sxs-lookup"><span data-stu-id="2080c-126">string</span></span><br/>  | <span data-ttu-id="2080c-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="2080c-127">xs:string</span></span><br/>       |
| <span data-ttu-id="2080c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2080c-128">DefaultValue</span></span><br/> | <span data-ttu-id="2080c-129">string</span><span class="sxs-lookup"><span data-stu-id="2080c-129">string</span></span><br/>  | <span data-ttu-id="2080c-130">no definido</span><span class="sxs-lookup"><span data-stu-id="2080c-130">undefined</span></span><br/>       |
| <span data-ttu-id="2080c-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="2080c-131">MaxLength</span></span><br/>    | <span data-ttu-id="2080c-132">integer</span><span class="sxs-lookup"><span data-stu-id="2080c-132">integer</span></span><br/> | <span data-ttu-id="2080c-133">no definido</span><span class="sxs-lookup"><span data-stu-id="2080c-133">undefined</span></span><br/>       |
| <span data-ttu-id="2080c-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="2080c-134">MinLength</span></span><br/>    | <span data-ttu-id="2080c-135">integer</span><span class="sxs-lookup"><span data-stu-id="2080c-135">integer</span></span><br/> | <span data-ttu-id="2080c-136">1</span><span class="sxs-lookup"><span data-stu-id="2080c-136">1</span></span><br/>               |
| <span data-ttu-id="2080c-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="2080c-137">Mandatory</span></span><br/>    | <span data-ttu-id="2080c-138">string</span><span class="sxs-lookup"><span data-stu-id="2080c-138">string</span></span><br/>  | <span data-ttu-id="2080c-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="2080c-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2080c-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="2080c-140">UnitType</span></span><br/>     | <span data-ttu-id="2080c-141">string</span><span class="sxs-lookup"><span data-stu-id="2080c-141">string</span></span><br/>  | <span data-ttu-id="2080c-142">caracteres</span><span class="sxs-lookup"><span data-stu-id="2080c-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="2080c-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2080c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2080c-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2080c-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




