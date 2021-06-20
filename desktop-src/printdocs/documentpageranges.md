---
description: Obtenga información sobre el elemento DocumentPageRanges, que describe el intervalo de salida del documento en páginas.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409258"
---
# <a name="documentpageranges"></a><span data-ttu-id="56780-103">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="56780-103">DocumentPageRanges</span></span>

<span data-ttu-id="56780-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="56780-104">This topic is not current.</span></span> <span data-ttu-id="56780-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56780-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56780-106">Describe el intervalo de salida del documento en páginas.</span><span class="sxs-lookup"><span data-stu-id="56780-106">Describes the output range of the document in pages.</span></span> <span data-ttu-id="56780-107">El valor del parámetro debe ajustarse a la estructura siguiente:</span><span class="sxs-lookup"><span data-stu-id="56780-107">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="56780-108">PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="56780-108">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="56780-109">PageRange: "*PageNumber*" o "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="56780-109">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="56780-110">PageNumber: de 1 a N, donde N es el número de páginas del documento.</span><span class="sxs-lookup"><span data-stu-id="56780-110">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="56780-111">Si *PageNumber* > N, *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="56780-111">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="56780-112">Se debe omitir el espacio en blanco de la cadena.</span><span class="sxs-lookup"><span data-stu-id="56780-112">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="56780-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="56780-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="56780-114">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="56780-114">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="56780-115">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="56780-115">Element Information</span></span>



| <span data-ttu-id="56780-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="56780-116">Name</span></span> | <span data-ttu-id="56780-117">Valor</span><span class="sxs-lookup"><span data-stu-id="56780-117">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="56780-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="56780-118">Element Type</span></span> <br/>   | <span data-ttu-id="56780-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="56780-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="56780-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="56780-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56780-121">Documento</span><span class="sxs-lookup"><span data-stu-id="56780-121">Document</span></span><br/>     |
| <span data-ttu-id="56780-122">Notas</span><span class="sxs-lookup"><span data-stu-id="56780-122">Notes</span></span> <br/>          | <span data-ttu-id="56780-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="56780-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="56780-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="56780-124">Structural Content</span></span>

<span data-ttu-id="56780-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="56780-125">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
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

## <a name="structure-properties"></a><span data-ttu-id="56780-126">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="56780-126">Structure Properties</span></span>

<span data-ttu-id="56780-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="56780-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56780-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56780-128">Property</span></span>                | <span data-ttu-id="56780-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="56780-129">xsi:type</span></span>           | <span data-ttu-id="56780-130">Valor</span><span class="sxs-lookup"><span data-stu-id="56780-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="56780-131">DataType</span><span class="sxs-lookup"><span data-stu-id="56780-131">DataType</span></span><br/>     | <span data-ttu-id="56780-132">string</span><span class="sxs-lookup"><span data-stu-id="56780-132">string</span></span><br/>  | <span data-ttu-id="56780-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="56780-133">xs:string</span></span><br/>       |
| <span data-ttu-id="56780-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="56780-134">DefaultValue</span></span><br/> | <span data-ttu-id="56780-135">string</span><span class="sxs-lookup"><span data-stu-id="56780-135">string</span></span><br/>  | <span data-ttu-id="56780-136">no definido</span><span class="sxs-lookup"><span data-stu-id="56780-136">undefined</span></span><br/>       |
| <span data-ttu-id="56780-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="56780-137">MaxLength</span></span><br/>    | <span data-ttu-id="56780-138">integer</span><span class="sxs-lookup"><span data-stu-id="56780-138">integer</span></span><br/> | <span data-ttu-id="56780-139">no definido</span><span class="sxs-lookup"><span data-stu-id="56780-139">undefined</span></span><br/>       |
| <span data-ttu-id="56780-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="56780-140">MinLength</span></span><br/>    | <span data-ttu-id="56780-141">integer</span><span class="sxs-lookup"><span data-stu-id="56780-141">integer</span></span><br/> | <span data-ttu-id="56780-142">1</span><span class="sxs-lookup"><span data-stu-id="56780-142">1</span></span><br/>               |
| <span data-ttu-id="56780-143">Mandatory</span><span class="sxs-lookup"><span data-stu-id="56780-143">Mandatory</span></span><br/>    | <span data-ttu-id="56780-144">string</span><span class="sxs-lookup"><span data-stu-id="56780-144">string</span></span><br/>  | <span data-ttu-id="56780-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="56780-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="56780-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="56780-146">UnitType</span></span><br/>     | <span data-ttu-id="56780-147">string</span><span class="sxs-lookup"><span data-stu-id="56780-147">string</span></span><br/>  | <span data-ttu-id="56780-148">caracteres</span><span class="sxs-lookup"><span data-stu-id="56780-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="56780-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56780-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56780-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="56780-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




