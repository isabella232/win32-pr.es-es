---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563ed1746743d3329e0cd31c84c32bb8b407c56c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361960"
---
# <a name="documentpageranges"></a><span data-ttu-id="3ce1e-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="3ce1e-104">DocumentPageRanges</span></span>

<span data-ttu-id="3ce1e-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-105">This topic is not current.</span></span> <span data-ttu-id="3ce1e-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3ce1e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3ce1e-107">Describe el intervalo de salida del documento en páginas.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="3ce1e-108">El valor del parámetro debe ajustarse a la siguiente estructura:</span><span class="sxs-lookup"><span data-stu-id="3ce1e-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="3ce1e-109">PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="3ce1e-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="3ce1e-110">PageRange: "*PageNumber*" o "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="3ce1e-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="3ce1e-111">PageNumber: 1 a N, donde N es el número de páginas del documento.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="3ce1e-112">Si *pagenumber* > n, *PageNumber* = n.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="3ce1e-113">Se debe omitir el espacio en blanco de la cadena.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="3ce1e-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3ce1e-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3ce1e-115">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3ce1e-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="3ce1e-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3ce1e-116">Element Information</span></span>



| <span data-ttu-id="3ce1e-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ce1e-117">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="3ce1e-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3ce1e-118">Element Type</span></span> <br/>   | <span data-ttu-id="3ce1e-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3ce1e-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="3ce1e-120">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="3ce1e-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3ce1e-121">Documento</span><span class="sxs-lookup"><span data-stu-id="3ce1e-121">Document</span></span><br/>     |
| <span data-ttu-id="3ce1e-122">Notas</span><span class="sxs-lookup"><span data-stu-id="3ce1e-122">Notes</span></span> <br/>          | <span data-ttu-id="3ce1e-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3ce1e-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="3ce1e-124">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3ce1e-124">Structural Content</span></span>

<span data-ttu-id="3ce1e-125">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="3ce1e-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3ce1e-126">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="3ce1e-126">Structure Properties</span></span>

<span data-ttu-id="3ce1e-127">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="3ce1e-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3ce1e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3ce1e-128">Property</span></span>                | <span data-ttu-id="3ce1e-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3ce1e-129">xsi:type</span></span>           | <span data-ttu-id="3ce1e-130">Value</span><span class="sxs-lookup"><span data-stu-id="3ce1e-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3ce1e-131">DataType</span><span class="sxs-lookup"><span data-stu-id="3ce1e-131">DataType</span></span><br/>     | <span data-ttu-id="3ce1e-132">string</span><span class="sxs-lookup"><span data-stu-id="3ce1e-132">string</span></span><br/>  | <span data-ttu-id="3ce1e-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ce1e-133">xs:string</span></span><br/>       |
| <span data-ttu-id="3ce1e-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3ce1e-134">DefaultValue</span></span><br/> | <span data-ttu-id="3ce1e-135">string</span><span class="sxs-lookup"><span data-stu-id="3ce1e-135">string</span></span><br/>  | <span data-ttu-id="3ce1e-136">no definido</span><span class="sxs-lookup"><span data-stu-id="3ce1e-136">undefined</span></span><br/>       |
| <span data-ttu-id="3ce1e-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3ce1e-137">MaxLength</span></span><br/>    | <span data-ttu-id="3ce1e-138">integer</span><span class="sxs-lookup"><span data-stu-id="3ce1e-138">integer</span></span><br/> | <span data-ttu-id="3ce1e-139">no definido</span><span class="sxs-lookup"><span data-stu-id="3ce1e-139">undefined</span></span><br/>       |
| <span data-ttu-id="3ce1e-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="3ce1e-140">MinLength</span></span><br/>    | <span data-ttu-id="3ce1e-141">integer</span><span class="sxs-lookup"><span data-stu-id="3ce1e-141">integer</span></span><br/> | <span data-ttu-id="3ce1e-142">1</span><span class="sxs-lookup"><span data-stu-id="3ce1e-142">1</span></span><br/>               |
| <span data-ttu-id="3ce1e-143">Mandatory</span><span class="sxs-lookup"><span data-stu-id="3ce1e-143">Mandatory</span></span><br/>    | <span data-ttu-id="3ce1e-144">string</span><span class="sxs-lookup"><span data-stu-id="3ce1e-144">string</span></span><br/>  | <span data-ttu-id="3ce1e-145">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="3ce1e-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3ce1e-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="3ce1e-146">UnitType</span></span><br/>     | <span data-ttu-id="3ce1e-147">string</span><span class="sxs-lookup"><span data-stu-id="3ce1e-147">string</span></span><br/>  | <span data-ttu-id="3ce1e-148">caracteres</span><span class="sxs-lookup"><span data-stu-id="3ce1e-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3ce1e-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ce1e-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ce1e-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="3ce1e-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




