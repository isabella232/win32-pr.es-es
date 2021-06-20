---
description: Obtenga información sobre el elemento JobComment, que especifica un comentario asociado al trabajo, por ejemplo, Please deliver to room 1234 when completed (Entregar a la sala 1234 cuando haya finalizado).
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1decf4cf3af7b3a992b07d8008579ac005d3d14e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409048"
---
# <a name="jobcomment"></a><span data-ttu-id="3b143-103">JobComment</span><span class="sxs-lookup"><span data-stu-id="3b143-103">JobComment</span></span>

<span data-ttu-id="3b143-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="3b143-104">This topic is not current.</span></span> <span data-ttu-id="3b143-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3b143-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3b143-106">Especifica un comentario asociado al trabajo.</span><span class="sxs-lookup"><span data-stu-id="3b143-106">Specifies a comment associated with the job.</span></span> <span data-ttu-id="3b143-107">Ejemplo: "Entrega a la sala 1234 cuando haya finalizado".</span><span class="sxs-lookup"><span data-stu-id="3b143-107">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="3b143-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3b143-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3b143-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="3b143-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3b143-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3b143-110">Element Information</span></span>



| <span data-ttu-id="3b143-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="3b143-111">Name</span></span> | <span data-ttu-id="3b143-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3b143-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="3b143-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3b143-113">Element Type</span></span> <br/>   | <span data-ttu-id="3b143-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3b143-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="3b143-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="3b143-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3b143-116">Trabajo</span><span class="sxs-lookup"><span data-stu-id="3b143-116">Job</span></span><br/>          |
| <span data-ttu-id="3b143-117">Notas</span><span class="sxs-lookup"><span data-stu-id="3b143-117">Notes</span></span> <br/>          | <span data-ttu-id="3b143-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3b143-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="3b143-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="3b143-119">Structure Content</span></span>

<span data-ttu-id="3b143-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="3b143-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3b143-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="3b143-121">Structure Properties</span></span>

<span data-ttu-id="3b143-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="3b143-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3b143-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3b143-123">Property</span></span>                | <span data-ttu-id="3b143-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3b143-124">xsi:type</span></span>           | <span data-ttu-id="3b143-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3b143-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3b143-126">DataType</span><span class="sxs-lookup"><span data-stu-id="3b143-126">DataType</span></span><br/>     | <span data-ttu-id="3b143-127">string</span><span class="sxs-lookup"><span data-stu-id="3b143-127">string</span></span><br/>  | <span data-ttu-id="3b143-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="3b143-128">xs:string</span></span><br/>       |
| <span data-ttu-id="3b143-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3b143-129">DefaultValue</span></span><br/> | <span data-ttu-id="3b143-130">string</span><span class="sxs-lookup"><span data-stu-id="3b143-130">string</span></span><br/>  | <span data-ttu-id="3b143-131">no definido</span><span class="sxs-lookup"><span data-stu-id="3b143-131">undefined</span></span><br/>       |
| <span data-ttu-id="3b143-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3b143-132">MaxLength</span></span><br/>    | <span data-ttu-id="3b143-133">integer</span><span class="sxs-lookup"><span data-stu-id="3b143-133">integer</span></span><br/> | <span data-ttu-id="3b143-134">no definido</span><span class="sxs-lookup"><span data-stu-id="3b143-134">undefined</span></span><br/>       |
| <span data-ttu-id="3b143-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="3b143-135">MinLength</span></span><br/>    | <span data-ttu-id="3b143-136">integer</span><span class="sxs-lookup"><span data-stu-id="3b143-136">integer</span></span><br/> | <span data-ttu-id="3b143-137">1</span><span class="sxs-lookup"><span data-stu-id="3b143-137">1</span></span><br/>               |
| <span data-ttu-id="3b143-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="3b143-138">Mandatory</span></span><br/>    | <span data-ttu-id="3b143-139">string</span><span class="sxs-lookup"><span data-stu-id="3b143-139">string</span></span><br/>  | <span data-ttu-id="3b143-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="3b143-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3b143-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="3b143-141">UnitType</span></span><br/>     | <span data-ttu-id="3b143-142">string</span><span class="sxs-lookup"><span data-stu-id="3b143-142">string</span></span><br/>  | <span data-ttu-id="3b143-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="3b143-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3b143-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b143-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b143-145">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="3b143-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




