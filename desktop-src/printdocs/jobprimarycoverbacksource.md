---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2145bae0843323928d8a7d016fc61f10c0e388ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993982"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="bdc20-104">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="bdc20-104">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="bdc20-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="bdc20-105">This topic is not current.</span></span> <span data-ttu-id="bdc20-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bdc20-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bdc20-107">Especifica el origen de una hoja principal de cobertura trasera personalizada para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bdc20-107">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="bdc20-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bdc20-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bdc20-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bdc20-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bdc20-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bdc20-110">Element Information</span></span>



| <span data-ttu-id="bdc20-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="bdc20-111">Name</span></span> | <span data-ttu-id="bdc20-112">Value</span><span class="sxs-lookup"><span data-stu-id="bdc20-112">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="bdc20-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bdc20-113">Element Type</span></span> <br/>   | <span data-ttu-id="bdc20-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bdc20-114">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="bdc20-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="bdc20-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bdc20-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="bdc20-116">Job</span></span><br/>                            |
| <span data-ttu-id="bdc20-117">Notas</span><span class="sxs-lookup"><span data-stu-id="bdc20-117">Notes</span></span> <br/>          | <span data-ttu-id="bdc20-118">Vinculado al elemento JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="bdc20-118">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bdc20-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bdc20-119">Structure Content</span></span>

<span data-ttu-id="bdc20-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="bdc20-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="bdc20-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="bdc20-121">Structure Properties</span></span>

<span data-ttu-id="bdc20-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="bdc20-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bdc20-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bdc20-123">Property</span></span>                | <span data-ttu-id="bdc20-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bdc20-124">xsi:type</span></span>           | <span data-ttu-id="bdc20-125">Value</span><span class="sxs-lookup"><span data-stu-id="bdc20-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="bdc20-126">DataType</span><span class="sxs-lookup"><span data-stu-id="bdc20-126">DataType</span></span><br/>     | <span data-ttu-id="bdc20-127">string</span><span class="sxs-lookup"><span data-stu-id="bdc20-127">string</span></span><br/>  | <span data-ttu-id="bdc20-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="bdc20-128">xs:string</span></span><br/>       |
| <span data-ttu-id="bdc20-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bdc20-129">DefaultValue</span></span><br/> | <span data-ttu-id="bdc20-130">string</span><span class="sxs-lookup"><span data-stu-id="bdc20-130">string</span></span><br/>  | <span data-ttu-id="bdc20-131">no definido</span><span class="sxs-lookup"><span data-stu-id="bdc20-131">undefined</span></span><br/>       |
| <span data-ttu-id="bdc20-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="bdc20-132">MaxLength</span></span><br/>    | <span data-ttu-id="bdc20-133">integer</span><span class="sxs-lookup"><span data-stu-id="bdc20-133">integer</span></span><br/> | <span data-ttu-id="bdc20-134">no definido</span><span class="sxs-lookup"><span data-stu-id="bdc20-134">undefined</span></span><br/>       |
| <span data-ttu-id="bdc20-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="bdc20-135">MinLength</span></span><br/>    | <span data-ttu-id="bdc20-136">integer</span><span class="sxs-lookup"><span data-stu-id="bdc20-136">integer</span></span><br/> | <span data-ttu-id="bdc20-137">1</span><span class="sxs-lookup"><span data-stu-id="bdc20-137">1</span></span><br/>               |
| <span data-ttu-id="bdc20-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="bdc20-138">Mandatory</span></span><br/>    | <span data-ttu-id="bdc20-139">string</span><span class="sxs-lookup"><span data-stu-id="bdc20-139">string</span></span><br/>  | <span data-ttu-id="bdc20-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="bdc20-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="bdc20-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="bdc20-141">UnitType</span></span><br/>     | <span data-ttu-id="bdc20-142">string</span><span class="sxs-lookup"><span data-stu-id="bdc20-142">string</span></span><br/>  | <span data-ttu-id="bdc20-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="bdc20-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="bdc20-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdc20-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc20-145">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="bdc20-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




