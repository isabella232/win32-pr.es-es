---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f8be33f98b540cab56b88df49cfb1e3c067988
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103820418"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="2e0b2-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="2e0b2-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="2e0b2-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-105">This topic is not current.</span></span> <span data-ttu-id="2e0b2-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2e0b2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e0b2-107">Especifica el número de copias de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="2e0b2-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2e0b2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2e0b2-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2e0b2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2e0b2-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2e0b2-110">Element Information</span></span>



| <span data-ttu-id="2e0b2-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="2e0b2-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="2e0b2-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2e0b2-112">Element Type</span></span> <br/>   | <span data-ttu-id="2e0b2-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2e0b2-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="2e0b2-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2e0b2-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2e0b2-115">Trabajo</span><span class="sxs-lookup"><span data-stu-id="2e0b2-115">Job</span></span><br/>          |
| <span data-ttu-id="2e0b2-116">Notas</span><span class="sxs-lookup"><span data-stu-id="2e0b2-116">Notes</span></span> <br/>          | <span data-ttu-id="2e0b2-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2e0b2-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="2e0b2-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2e0b2-118">Structure Content</span></span>

<span data-ttu-id="2e0b2-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2e0b2-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2e0b2-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="2e0b2-120">Structure Properties</span></span>

<span data-ttu-id="2e0b2-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2e0b2-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2e0b2-122">Property</span></span>                | <span data-ttu-id="2e0b2-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2e0b2-123">xsi:type</span></span>           | <span data-ttu-id="2e0b2-124">Value</span><span class="sxs-lookup"><span data-stu-id="2e0b2-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="2e0b2-125">DataType</span><span class="sxs-lookup"><span data-stu-id="2e0b2-125">DataType</span></span><br/>     | <span data-ttu-id="2e0b2-126">string</span><span class="sxs-lookup"><span data-stu-id="2e0b2-126">string</span></span><br/>  | <span data-ttu-id="2e0b2-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2e0b2-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="2e0b2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2e0b2-128">DefaultValue</span></span><br/> | <span data-ttu-id="2e0b2-129">integer</span><span class="sxs-lookup"><span data-stu-id="2e0b2-129">integer</span></span><br/> | <span data-ttu-id="2e0b2-130">1</span><span class="sxs-lookup"><span data-stu-id="2e0b2-130">1</span></span><br/>                 |
| <span data-ttu-id="2e0b2-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2e0b2-131">MaxValue</span></span><br/>     | <span data-ttu-id="2e0b2-132">integer</span><span class="sxs-lookup"><span data-stu-id="2e0b2-132">integer</span></span><br/> | <span data-ttu-id="2e0b2-133">no definido</span><span class="sxs-lookup"><span data-stu-id="2e0b2-133">undefined</span></span><br/>         |
| <span data-ttu-id="2e0b2-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="2e0b2-134">MinValue</span></span><br/>     | <span data-ttu-id="2e0b2-135">integer</span><span class="sxs-lookup"><span data-stu-id="2e0b2-135">integer</span></span><br/> | <span data-ttu-id="2e0b2-136">1</span><span class="sxs-lookup"><span data-stu-id="2e0b2-136">1</span></span><br/>                 |
| <span data-ttu-id="2e0b2-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="2e0b2-137">Mandatory</span></span><br/>    | <span data-ttu-id="2e0b2-138">string</span><span class="sxs-lookup"><span data-stu-id="2e0b2-138">string</span></span><br/>  | <span data-ttu-id="2e0b2-139">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="2e0b2-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="2e0b2-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="2e0b2-140">Multiple</span></span><br/>     | <span data-ttu-id="2e0b2-141">integer</span><span class="sxs-lookup"><span data-stu-id="2e0b2-141">integer</span></span><br/> | <span data-ttu-id="2e0b2-142">1</span><span class="sxs-lookup"><span data-stu-id="2e0b2-142">1</span></span><br/>                 |
| <span data-ttu-id="2e0b2-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="2e0b2-143">UnitType</span></span><br/>     | <span data-ttu-id="2e0b2-144">string</span><span class="sxs-lookup"><span data-stu-id="2e0b2-144">string</span></span><br/>  | <span data-ttu-id="2e0b2-145">instantánea</span><span class="sxs-lookup"><span data-stu-id="2e0b2-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="2e0b2-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e0b2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e0b2-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2e0b2-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




