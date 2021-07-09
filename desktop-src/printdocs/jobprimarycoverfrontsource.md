---
description: Obtenga información sobre el parámetro JobPrimaryCoverFrontSource. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: JobPrimaryCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4698d826e59e513d5eb171381cd1b18ea4a751
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549403"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="dceb5-105">JobPrimaryCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="dceb5-105">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="dceb5-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="dceb5-106">This topic is not current.</span></span> <span data-ttu-id="dceb5-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dceb5-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dceb5-108">Especifica el origen de una hoja principal de front-cover personalizada para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="dceb5-108">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="dceb5-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dceb5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dceb5-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dceb5-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dceb5-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dceb5-111">Element Information</span></span>



| <span data-ttu-id="dceb5-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="dceb5-112">Name</span></span> | <span data-ttu-id="dceb5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dceb5-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="dceb5-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dceb5-114">Element Type</span></span> <br/>   | <span data-ttu-id="dceb5-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dceb5-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="dceb5-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="dceb5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dceb5-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="dceb5-117">Job</span></span><br/>                             |
| <span data-ttu-id="dceb5-118">Notas</span><span class="sxs-lookup"><span data-stu-id="dceb5-118">Notes</span></span> <br/>          | <span data-ttu-id="dceb5-119">Vinculado al elemento JobCoverFront</span><span class="sxs-lookup"><span data-stu-id="dceb5-119">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dceb5-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dceb5-120">Structure Content</span></span>

<span data-ttu-id="dceb5-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="dceb5-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverFrontSource">
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

## <a name="structure-properties"></a><span data-ttu-id="dceb5-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="dceb5-122">Structure Properties</span></span>

<span data-ttu-id="dceb5-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="dceb5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dceb5-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dceb5-124">Property</span></span>                | <span data-ttu-id="dceb5-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dceb5-125">xsi:type</span></span>           | <span data-ttu-id="dceb5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dceb5-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dceb5-127">DataType</span><span class="sxs-lookup"><span data-stu-id="dceb5-127">DataType</span></span><br/>     | <span data-ttu-id="dceb5-128">string</span><span class="sxs-lookup"><span data-stu-id="dceb5-128">string</span></span><br/>  | <span data-ttu-id="dceb5-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="dceb5-129">xs:string</span></span><br/>       |
| <span data-ttu-id="dceb5-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dceb5-130">DefaultValue</span></span><br/> | <span data-ttu-id="dceb5-131">string</span><span class="sxs-lookup"><span data-stu-id="dceb5-131">string</span></span><br/>  | <span data-ttu-id="dceb5-132">no definido</span><span class="sxs-lookup"><span data-stu-id="dceb5-132">undefined</span></span><br/>       |
| <span data-ttu-id="dceb5-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="dceb5-133">MaxLength</span></span><br/>    | <span data-ttu-id="dceb5-134">integer</span><span class="sxs-lookup"><span data-stu-id="dceb5-134">integer</span></span><br/> | <span data-ttu-id="dceb5-135">no definido</span><span class="sxs-lookup"><span data-stu-id="dceb5-135">undefined</span></span><br/>       |
| <span data-ttu-id="dceb5-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="dceb5-136">MinLength</span></span><br/>    | <span data-ttu-id="dceb5-137">integer</span><span class="sxs-lookup"><span data-stu-id="dceb5-137">integer</span></span><br/> | <span data-ttu-id="dceb5-138">1</span><span class="sxs-lookup"><span data-stu-id="dceb5-138">1</span></span><br/>               |
| <span data-ttu-id="dceb5-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="dceb5-139">Mandatory</span></span><br/>    | <span data-ttu-id="dceb5-140">string</span><span class="sxs-lookup"><span data-stu-id="dceb5-140">string</span></span><br/>  | <span data-ttu-id="dceb5-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="dceb5-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dceb5-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="dceb5-142">UnitType</span></span><br/>     | <span data-ttu-id="dceb5-143">string</span><span class="sxs-lookup"><span data-stu-id="dceb5-143">string</span></span><br/>  | <span data-ttu-id="dceb5-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="dceb5-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="dceb5-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dceb5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dceb5-146">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="dceb5-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




