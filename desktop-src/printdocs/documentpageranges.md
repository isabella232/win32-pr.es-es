---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997182"
---
# <a name="documentpageranges"></a><span data-ttu-id="99ad3-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="99ad3-104">DocumentPageRanges</span></span>

<span data-ttu-id="99ad3-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="99ad3-105">This topic is not current.</span></span> <span data-ttu-id="99ad3-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="99ad3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="99ad3-107">Describe el intervalo de salida del documento en páginas.</span><span class="sxs-lookup"><span data-stu-id="99ad3-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="99ad3-108">El valor del parámetro debe ajustarse a la estructura siguiente:</span><span class="sxs-lookup"><span data-stu-id="99ad3-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="99ad3-109">PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="99ad3-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="99ad3-110">PageRange: "*PageNumber*" o "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="99ad3-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="99ad3-111">PageNumber: de 1 a N, donde N es el número de páginas del documento.</span><span class="sxs-lookup"><span data-stu-id="99ad3-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="99ad3-112">Si *PageNumber* > N, *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="99ad3-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="99ad3-113">Se debe omitir el espacio en blanco de la cadena.</span><span class="sxs-lookup"><span data-stu-id="99ad3-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="99ad3-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="99ad3-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="99ad3-115">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="99ad3-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="99ad3-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="99ad3-116">Element Information</span></span>



| <span data-ttu-id="99ad3-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="99ad3-117">Name</span></span> | <span data-ttu-id="99ad3-118">Value</span><span class="sxs-lookup"><span data-stu-id="99ad3-118">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="99ad3-119">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="99ad3-119">Element Type</span></span> <br/>   | <span data-ttu-id="99ad3-120">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="99ad3-120">ParameterDef</span></span><br/> |
| <span data-ttu-id="99ad3-121">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="99ad3-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="99ad3-122">Documento</span><span class="sxs-lookup"><span data-stu-id="99ad3-122">Document</span></span><br/>     |
| <span data-ttu-id="99ad3-123">Notas</span><span class="sxs-lookup"><span data-stu-id="99ad3-123">Notes</span></span> <br/>          | <span data-ttu-id="99ad3-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="99ad3-124">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="99ad3-125">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="99ad3-125">Structural Content</span></span>

<span data-ttu-id="99ad3-126">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="99ad3-126">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="99ad3-127">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="99ad3-127">Structure Properties</span></span>

<span data-ttu-id="99ad3-128">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="99ad3-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="99ad3-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99ad3-129">Property</span></span>                | <span data-ttu-id="99ad3-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="99ad3-130">xsi:type</span></span>           | <span data-ttu-id="99ad3-131">Value</span><span class="sxs-lookup"><span data-stu-id="99ad3-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="99ad3-132">DataType</span><span class="sxs-lookup"><span data-stu-id="99ad3-132">DataType</span></span><br/>     | <span data-ttu-id="99ad3-133">string</span><span class="sxs-lookup"><span data-stu-id="99ad3-133">string</span></span><br/>  | <span data-ttu-id="99ad3-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="99ad3-134">xs:string</span></span><br/>       |
| <span data-ttu-id="99ad3-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="99ad3-135">DefaultValue</span></span><br/> | <span data-ttu-id="99ad3-136">string</span><span class="sxs-lookup"><span data-stu-id="99ad3-136">string</span></span><br/>  | <span data-ttu-id="99ad3-137">no definido</span><span class="sxs-lookup"><span data-stu-id="99ad3-137">undefined</span></span><br/>       |
| <span data-ttu-id="99ad3-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="99ad3-138">MaxLength</span></span><br/>    | <span data-ttu-id="99ad3-139">integer</span><span class="sxs-lookup"><span data-stu-id="99ad3-139">integer</span></span><br/> | <span data-ttu-id="99ad3-140">no definido</span><span class="sxs-lookup"><span data-stu-id="99ad3-140">undefined</span></span><br/>       |
| <span data-ttu-id="99ad3-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="99ad3-141">MinLength</span></span><br/>    | <span data-ttu-id="99ad3-142">integer</span><span class="sxs-lookup"><span data-stu-id="99ad3-142">integer</span></span><br/> | <span data-ttu-id="99ad3-143">1</span><span class="sxs-lookup"><span data-stu-id="99ad3-143">1</span></span><br/>               |
| <span data-ttu-id="99ad3-144">Mandatory</span><span class="sxs-lookup"><span data-stu-id="99ad3-144">Mandatory</span></span><br/>    | <span data-ttu-id="99ad3-145">string</span><span class="sxs-lookup"><span data-stu-id="99ad3-145">string</span></span><br/>  | <span data-ttu-id="99ad3-146">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="99ad3-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="99ad3-147">UnitType</span><span class="sxs-lookup"><span data-stu-id="99ad3-147">UnitType</span></span><br/>     | <span data-ttu-id="99ad3-148">string</span><span class="sxs-lookup"><span data-stu-id="99ad3-148">string</span></span><br/>  | <span data-ttu-id="99ad3-149">caracteres</span><span class="sxs-lookup"><span data-stu-id="99ad3-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="99ad3-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99ad3-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99ad3-151">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="99ad3-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




