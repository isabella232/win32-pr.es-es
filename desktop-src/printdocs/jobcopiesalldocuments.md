---
description: Obtenga información sobre el elemento JobCopiesAllDocuments, que especifica el número de copias de un trabajo.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05166715a5985c5ddee33fa6808d0fb6b150774b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409038"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="7f6e3-103">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="7f6e3-103">JobCopiesAllDocuments</span></span>

<span data-ttu-id="7f6e3-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="7f6e3-104">This topic is not current.</span></span> <span data-ttu-id="7f6e3-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7f6e3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7f6e3-106">Especifica el número de copias de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="7f6e3-106">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="7f6e3-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7f6e3-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7f6e3-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7f6e3-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7f6e3-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7f6e3-109">Element Information</span></span>



| <span data-ttu-id="7f6e3-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="7f6e3-110">Name</span></span> | <span data-ttu-id="7f6e3-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7f6e3-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="7f6e3-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7f6e3-112">Element Type</span></span> <br/>   | <span data-ttu-id="7f6e3-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7f6e3-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="7f6e3-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="7f6e3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7f6e3-115">Trabajo</span><span class="sxs-lookup"><span data-stu-id="7f6e3-115">Job</span></span><br/>          |
| <span data-ttu-id="7f6e3-116">Notas</span><span class="sxs-lookup"><span data-stu-id="7f6e3-116">Notes</span></span> <br/>          | <span data-ttu-id="7f6e3-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7f6e3-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="7f6e3-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7f6e3-118">Structure Content</span></span>

<span data-ttu-id="7f6e3-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="7f6e3-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="7f6e3-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="7f6e3-120">Structure Properties</span></span>

<span data-ttu-id="7f6e3-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="7f6e3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7f6e3-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7f6e3-122">Property</span></span>                | <span data-ttu-id="7f6e3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7f6e3-123">xsi:type</span></span>           | <span data-ttu-id="7f6e3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7f6e3-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="7f6e3-125">DataType</span><span class="sxs-lookup"><span data-stu-id="7f6e3-125">DataType</span></span><br/>     | <span data-ttu-id="7f6e3-126">string</span><span class="sxs-lookup"><span data-stu-id="7f6e3-126">string</span></span><br/>  | <span data-ttu-id="7f6e3-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7f6e3-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="7f6e3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7f6e3-128">DefaultValue</span></span><br/> | <span data-ttu-id="7f6e3-129">integer</span><span class="sxs-lookup"><span data-stu-id="7f6e3-129">integer</span></span><br/> | <span data-ttu-id="7f6e3-130">1</span><span class="sxs-lookup"><span data-stu-id="7f6e3-130">1</span></span><br/>                 |
| <span data-ttu-id="7f6e3-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7f6e3-131">MaxValue</span></span><br/>     | <span data-ttu-id="7f6e3-132">integer</span><span class="sxs-lookup"><span data-stu-id="7f6e3-132">integer</span></span><br/> | <span data-ttu-id="7f6e3-133">no definido</span><span class="sxs-lookup"><span data-stu-id="7f6e3-133">undefined</span></span><br/>         |
| <span data-ttu-id="7f6e3-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="7f6e3-134">MinValue</span></span><br/>     | <span data-ttu-id="7f6e3-135">integer</span><span class="sxs-lookup"><span data-stu-id="7f6e3-135">integer</span></span><br/> | <span data-ttu-id="7f6e3-136">1</span><span class="sxs-lookup"><span data-stu-id="7f6e3-136">1</span></span><br/>                 |
| <span data-ttu-id="7f6e3-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="7f6e3-137">Mandatory</span></span><br/>    | <span data-ttu-id="7f6e3-138">string</span><span class="sxs-lookup"><span data-stu-id="7f6e3-138">string</span></span><br/>  | <span data-ttu-id="7f6e3-139">psk:Unconditional</span><span class="sxs-lookup"><span data-stu-id="7f6e3-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="7f6e3-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="7f6e3-140">Multiple</span></span><br/>     | <span data-ttu-id="7f6e3-141">integer</span><span class="sxs-lookup"><span data-stu-id="7f6e3-141">integer</span></span><br/> | <span data-ttu-id="7f6e3-142">1</span><span class="sxs-lookup"><span data-stu-id="7f6e3-142">1</span></span><br/>                 |
| <span data-ttu-id="7f6e3-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="7f6e3-143">UnitType</span></span><br/>     | <span data-ttu-id="7f6e3-144">string</span><span class="sxs-lookup"><span data-stu-id="7f6e3-144">string</span></span><br/>  | <span data-ttu-id="7f6e3-145">Copias</span><span class="sxs-lookup"><span data-stu-id="7f6e3-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="7f6e3-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f6e3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f6e3-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="7f6e3-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




