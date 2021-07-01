---
description: Obtenga información sobre el parámetro DocumentImpositionColor. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b747487c19160d29778f306a91b62cf43d245f65
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120010"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="845ef-105">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="845ef-105">DocumentImpositionColor</span></span>

<span data-ttu-id="845ef-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="845ef-106">This topic is not current.</span></span> <span data-ttu-id="845ef-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="845ef-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="845ef-108">El contenido de la aplicación etiquetado con el color con nombre especificado DEBE aparecer en todas las separaciones de colores.</span><span class="sxs-lookup"><span data-stu-id="845ef-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="845ef-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="845ef-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="845ef-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="845ef-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="845ef-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="845ef-111">Element Information</span></span>



| <span data-ttu-id="845ef-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="845ef-112">Name</span></span> | <span data-ttu-id="845ef-113">Valor</span><span class="sxs-lookup"><span data-stu-id="845ef-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="845ef-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="845ef-114">Element Type</span></span> <br/>   | <span data-ttu-id="845ef-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="845ef-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="845ef-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="845ef-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="845ef-117">Documento</span><span class="sxs-lookup"><span data-stu-id="845ef-117">Document</span></span><br/>     |
| <span data-ttu-id="845ef-118">Notas</span><span class="sxs-lookup"><span data-stu-id="845ef-118">Notes</span></span> <br/>          | <span data-ttu-id="845ef-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="845ef-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="845ef-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="845ef-120">Structure Content</span></span>

<span data-ttu-id="845ef-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="845ef-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
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

## <a name="structure-properties"></a><span data-ttu-id="845ef-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="845ef-122">Structure Properties</span></span>

<span data-ttu-id="845ef-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="845ef-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="845ef-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="845ef-124">Property</span></span>                | <span data-ttu-id="845ef-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="845ef-125">xsi:type</span></span>           | <span data-ttu-id="845ef-126">Valor</span><span class="sxs-lookup"><span data-stu-id="845ef-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="845ef-127">DataType</span><span class="sxs-lookup"><span data-stu-id="845ef-127">DataType</span></span><br/>     | <span data-ttu-id="845ef-128">string</span><span class="sxs-lookup"><span data-stu-id="845ef-128">string</span></span><br/>  | <span data-ttu-id="845ef-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="845ef-129">xs:string</span></span><br/>       |
| <span data-ttu-id="845ef-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="845ef-130">DefaultValue</span></span><br/> | <span data-ttu-id="845ef-131">string</span><span class="sxs-lookup"><span data-stu-id="845ef-131">string</span></span><br/>  | <span data-ttu-id="845ef-132">no definido</span><span class="sxs-lookup"><span data-stu-id="845ef-132">undefined</span></span><br/>       |
| <span data-ttu-id="845ef-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="845ef-133">MaxLength</span></span><br/>    | <span data-ttu-id="845ef-134">integer</span><span class="sxs-lookup"><span data-stu-id="845ef-134">integer</span></span><br/> | <span data-ttu-id="845ef-135">no definido</span><span class="sxs-lookup"><span data-stu-id="845ef-135">undefined</span></span><br/>       |
| <span data-ttu-id="845ef-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="845ef-136">MinLength</span></span><br/>    | <span data-ttu-id="845ef-137">integer</span><span class="sxs-lookup"><span data-stu-id="845ef-137">integer</span></span><br/> | <span data-ttu-id="845ef-138">1</span><span class="sxs-lookup"><span data-stu-id="845ef-138">1</span></span><br/>               |
| <span data-ttu-id="845ef-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="845ef-139">Mandatory</span></span><br/>    | <span data-ttu-id="845ef-140">string</span><span class="sxs-lookup"><span data-stu-id="845ef-140">string</span></span><br/>  | <span data-ttu-id="845ef-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="845ef-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="845ef-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="845ef-142">UnitType</span></span><br/>     | <span data-ttu-id="845ef-143">string</span><span class="sxs-lookup"><span data-stu-id="845ef-143">string</span></span><br/>  | <span data-ttu-id="845ef-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="845ef-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="845ef-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="845ef-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="845ef-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="845ef-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




