---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ebfbd2e62c18153dd0930197b6f49cbb3480d6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105649333"
---
# <a name="jobcomment"></a><span data-ttu-id="02895-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="02895-104">JobComment</span></span>

<span data-ttu-id="02895-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="02895-105">This topic is not current.</span></span> <span data-ttu-id="02895-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="02895-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="02895-107">Especifica un comentario asociado al trabajo.</span><span class="sxs-lookup"><span data-stu-id="02895-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="02895-108">Ejemplo: "entregue al salón 1234 cuando se complete".</span><span class="sxs-lookup"><span data-stu-id="02895-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="02895-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="02895-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="02895-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="02895-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="02895-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="02895-111">Element Information</span></span>



| <span data-ttu-id="02895-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="02895-112">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="02895-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="02895-113">Element Type</span></span> <br/>   | <span data-ttu-id="02895-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="02895-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="02895-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="02895-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="02895-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="02895-116">Job</span></span><br/>          |
| <span data-ttu-id="02895-117">Notas</span><span class="sxs-lookup"><span data-stu-id="02895-117">Notes</span></span> <br/>          | <span data-ttu-id="02895-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="02895-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="02895-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="02895-119">Structure Content</span></span>

<span data-ttu-id="02895-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="02895-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="02895-121">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="02895-121">Structure Properties</span></span>

<span data-ttu-id="02895-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="02895-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="02895-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="02895-123">Property</span></span>                | <span data-ttu-id="02895-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="02895-124">xsi:type</span></span>           | <span data-ttu-id="02895-125">Value</span><span class="sxs-lookup"><span data-stu-id="02895-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="02895-126">DataType</span><span class="sxs-lookup"><span data-stu-id="02895-126">DataType</span></span><br/>     | <span data-ttu-id="02895-127">string</span><span class="sxs-lookup"><span data-stu-id="02895-127">string</span></span><br/>  | <span data-ttu-id="02895-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="02895-128">xs:string</span></span><br/>       |
| <span data-ttu-id="02895-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="02895-129">DefaultValue</span></span><br/> | <span data-ttu-id="02895-130">string</span><span class="sxs-lookup"><span data-stu-id="02895-130">string</span></span><br/>  | <span data-ttu-id="02895-131">no definido</span><span class="sxs-lookup"><span data-stu-id="02895-131">undefined</span></span><br/>       |
| <span data-ttu-id="02895-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="02895-132">MaxLength</span></span><br/>    | <span data-ttu-id="02895-133">integer</span><span class="sxs-lookup"><span data-stu-id="02895-133">integer</span></span><br/> | <span data-ttu-id="02895-134">no definido</span><span class="sxs-lookup"><span data-stu-id="02895-134">undefined</span></span><br/>       |
| <span data-ttu-id="02895-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="02895-135">MinLength</span></span><br/>    | <span data-ttu-id="02895-136">integer</span><span class="sxs-lookup"><span data-stu-id="02895-136">integer</span></span><br/> | <span data-ttu-id="02895-137">1</span><span class="sxs-lookup"><span data-stu-id="02895-137">1</span></span><br/>               |
| <span data-ttu-id="02895-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="02895-138">Mandatory</span></span><br/>    | <span data-ttu-id="02895-139">string</span><span class="sxs-lookup"><span data-stu-id="02895-139">string</span></span><br/>  | <span data-ttu-id="02895-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="02895-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="02895-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="02895-141">UnitType</span></span><br/>     | <span data-ttu-id="02895-142">string</span><span class="sxs-lookup"><span data-stu-id="02895-142">string</span></span><br/>  | <span data-ttu-id="02895-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="02895-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="02895-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02895-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02895-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="02895-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




