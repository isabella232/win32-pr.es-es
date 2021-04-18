---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea74db8ac616bc9ca6b7f6cde22f62bea742e7fb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717410"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="d580c-104">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="d580c-104">DocumentImpositionColor</span></span>

<span data-ttu-id="d580c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="d580c-105">This topic is not current.</span></span> <span data-ttu-id="d580c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d580c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d580c-107">El contenido de la aplicación etiquetado con el color con nombre especificado debe aparecer en todas las separaciones de color.</span><span class="sxs-lookup"><span data-stu-id="d580c-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="d580c-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d580c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d580c-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="d580c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d580c-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d580c-110">Element Information</span></span>



| <span data-ttu-id="d580c-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="d580c-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="d580c-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d580c-112">Element Type</span></span> <br/>   | <span data-ttu-id="d580c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d580c-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="d580c-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="d580c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d580c-115">Documento</span><span class="sxs-lookup"><span data-stu-id="d580c-115">Document</span></span><br/>     |
| <span data-ttu-id="d580c-116">Notas</span><span class="sxs-lookup"><span data-stu-id="d580c-116">Notes</span></span> <br/>          | <span data-ttu-id="d580c-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d580c-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="d580c-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="d580c-118">Structure Content</span></span>

<span data-ttu-id="d580c-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="d580c-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d580c-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="d580c-120">Structure Properties</span></span>

<span data-ttu-id="d580c-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="d580c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d580c-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d580c-122">Property</span></span>                | <span data-ttu-id="d580c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d580c-123">xsi:type</span></span>           | <span data-ttu-id="d580c-124">Value</span><span class="sxs-lookup"><span data-stu-id="d580c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d580c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="d580c-125">DataType</span></span><br/>     | <span data-ttu-id="d580c-126">string</span><span class="sxs-lookup"><span data-stu-id="d580c-126">string</span></span><br/>  | <span data-ttu-id="d580c-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="d580c-127">xs:string</span></span><br/>       |
| <span data-ttu-id="d580c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d580c-128">DefaultValue</span></span><br/> | <span data-ttu-id="d580c-129">string</span><span class="sxs-lookup"><span data-stu-id="d580c-129">string</span></span><br/>  | <span data-ttu-id="d580c-130">no definido</span><span class="sxs-lookup"><span data-stu-id="d580c-130">undefined</span></span><br/>       |
| <span data-ttu-id="d580c-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="d580c-131">MaxLength</span></span><br/>    | <span data-ttu-id="d580c-132">integer</span><span class="sxs-lookup"><span data-stu-id="d580c-132">integer</span></span><br/> | <span data-ttu-id="d580c-133">no definido</span><span class="sxs-lookup"><span data-stu-id="d580c-133">undefined</span></span><br/>       |
| <span data-ttu-id="d580c-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="d580c-134">MinLength</span></span><br/>    | <span data-ttu-id="d580c-135">integer</span><span class="sxs-lookup"><span data-stu-id="d580c-135">integer</span></span><br/> | <span data-ttu-id="d580c-136">1</span><span class="sxs-lookup"><span data-stu-id="d580c-136">1</span></span><br/>               |
| <span data-ttu-id="d580c-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="d580c-137">Mandatory</span></span><br/>    | <span data-ttu-id="d580c-138">string</span><span class="sxs-lookup"><span data-stu-id="d580c-138">string</span></span><br/>  | <span data-ttu-id="d580c-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="d580c-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d580c-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="d580c-140">UnitType</span></span><br/>     | <span data-ttu-id="d580c-141">string</span><span class="sxs-lookup"><span data-stu-id="d580c-141">string</span></span><br/>  | <span data-ttu-id="d580c-142">caracteres</span><span class="sxs-lookup"><span data-stu-id="d580c-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="d580c-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d580c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d580c-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d580c-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




