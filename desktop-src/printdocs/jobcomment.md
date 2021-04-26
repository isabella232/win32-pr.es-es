---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998352"
---
# <a name="jobcomment"></a><span data-ttu-id="1f039-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="1f039-104">JobComment</span></span>

<span data-ttu-id="1f039-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1f039-105">This topic is not current.</span></span> <span data-ttu-id="1f039-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1f039-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1f039-107">Especifica un comentario asociado al trabajo.</span><span class="sxs-lookup"><span data-stu-id="1f039-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="1f039-108">Ejemplo: "Entrega a la sala 1234 cuando haya finalizado".</span><span class="sxs-lookup"><span data-stu-id="1f039-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="1f039-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1f039-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1f039-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="1f039-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1f039-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1f039-111">Element Information</span></span>



| <span data-ttu-id="1f039-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f039-112">Name</span></span> | <span data-ttu-id="1f039-113">Value</span><span class="sxs-lookup"><span data-stu-id="1f039-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="1f039-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1f039-114">Element Type</span></span> <br/>   | <span data-ttu-id="1f039-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1f039-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="1f039-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="1f039-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1f039-117">Trabajo</span><span class="sxs-lookup"><span data-stu-id="1f039-117">Job</span></span><br/>          |
| <span data-ttu-id="1f039-118">Notas</span><span class="sxs-lookup"><span data-stu-id="1f039-118">Notes</span></span> <br/>          | <span data-ttu-id="1f039-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1f039-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="1f039-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="1f039-120">Structure Content</span></span>

<span data-ttu-id="1f039-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="1f039-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a><span data-ttu-id="1f039-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="1f039-122">Structure Properties</span></span>

<span data-ttu-id="1f039-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="1f039-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1f039-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f039-124">Property</span></span>                | <span data-ttu-id="1f039-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1f039-125">xsi:type</span></span>           | <span data-ttu-id="1f039-126">Value</span><span class="sxs-lookup"><span data-stu-id="1f039-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1f039-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1f039-127">DataType</span></span><br/>     | <span data-ttu-id="1f039-128">string</span><span class="sxs-lookup"><span data-stu-id="1f039-128">string</span></span><br/>  | <span data-ttu-id="1f039-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="1f039-129">xs:string</span></span><br/>       |
| <span data-ttu-id="1f039-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1f039-130">DefaultValue</span></span><br/> | <span data-ttu-id="1f039-131">string</span><span class="sxs-lookup"><span data-stu-id="1f039-131">string</span></span><br/>  | <span data-ttu-id="1f039-132">no definido</span><span class="sxs-lookup"><span data-stu-id="1f039-132">undefined</span></span><br/>       |
| <span data-ttu-id="1f039-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1f039-133">MaxLength</span></span><br/>    | <span data-ttu-id="1f039-134">integer</span><span class="sxs-lookup"><span data-stu-id="1f039-134">integer</span></span><br/> | <span data-ttu-id="1f039-135">no definido</span><span class="sxs-lookup"><span data-stu-id="1f039-135">undefined</span></span><br/>       |
| <span data-ttu-id="1f039-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="1f039-136">MinLength</span></span><br/>    | <span data-ttu-id="1f039-137">integer</span><span class="sxs-lookup"><span data-stu-id="1f039-137">integer</span></span><br/> | <span data-ttu-id="1f039-138">1</span><span class="sxs-lookup"><span data-stu-id="1f039-138">1</span></span><br/>               |
| <span data-ttu-id="1f039-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="1f039-139">Mandatory</span></span><br/>    | <span data-ttu-id="1f039-140">string</span><span class="sxs-lookup"><span data-stu-id="1f039-140">string</span></span><br/>  | <span data-ttu-id="1f039-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="1f039-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1f039-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="1f039-142">UnitType</span></span><br/>     | <span data-ttu-id="1f039-143">string</span><span class="sxs-lookup"><span data-stu-id="1f039-143">string</span></span><br/>  | <span data-ttu-id="1f039-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="1f039-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1f039-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f039-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f039-146">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1f039-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




