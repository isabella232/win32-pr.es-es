---
description: Obtenga información sobre el parámetro JobErrorSheetSource. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656d71422c46800d6155c1dea1e221f9c6dfe021
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549393"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="5afb5-105">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="5afb5-105">JobErrorSheetSource</span></span>

<span data-ttu-id="5afb5-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5afb5-106">This topic is not current.</span></span> <span data-ttu-id="5afb5-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5afb5-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5afb5-108">Especifica el origen de una hoja de errores personalizada.</span><span class="sxs-lookup"><span data-stu-id="5afb5-108">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="5afb5-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5afb5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5afb5-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5afb5-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5afb5-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5afb5-111">Element Information</span></span>



| <span data-ttu-id="5afb5-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="5afb5-112">Name</span></span> | <span data-ttu-id="5afb5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5afb5-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="5afb5-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5afb5-114">Element Type</span></span> <br/>   | <span data-ttu-id="5afb5-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5afb5-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="5afb5-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5afb5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5afb5-117">Documento</span><span class="sxs-lookup"><span data-stu-id="5afb5-117">Document</span></span><br/>                        |
| <span data-ttu-id="5afb5-118">Notas</span><span class="sxs-lookup"><span data-stu-id="5afb5-118">Notes</span></span> <br/>          | <span data-ttu-id="5afb5-119">Vinculado al elemento JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="5afb5-119">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5afb5-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5afb5-120">Structure Content</span></span>

<span data-ttu-id="5afb5-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5afb5-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobErrorSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="5afb5-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="5afb5-122">Structure Properties</span></span>

<span data-ttu-id="5afb5-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5afb5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5afb5-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5afb5-124">Property</span></span>                | <span data-ttu-id="5afb5-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5afb5-125">xsi:type</span></span>           | <span data-ttu-id="5afb5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5afb5-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5afb5-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5afb5-127">DataType</span></span><br/>     | <span data-ttu-id="5afb5-128">string</span><span class="sxs-lookup"><span data-stu-id="5afb5-128">string</span></span><br/>  | <span data-ttu-id="5afb5-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="5afb5-129">xs:string</span></span><br/>       |
| <span data-ttu-id="5afb5-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5afb5-130">DefaultValue</span></span><br/> | <span data-ttu-id="5afb5-131">string</span><span class="sxs-lookup"><span data-stu-id="5afb5-131">string</span></span><br/>  | <span data-ttu-id="5afb5-132">no definido</span><span class="sxs-lookup"><span data-stu-id="5afb5-132">undefined</span></span><br/>       |
| <span data-ttu-id="5afb5-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="5afb5-133">MaxLength</span></span><br/>    | <span data-ttu-id="5afb5-134">integer</span><span class="sxs-lookup"><span data-stu-id="5afb5-134">integer</span></span><br/> | <span data-ttu-id="5afb5-135">no definido</span><span class="sxs-lookup"><span data-stu-id="5afb5-135">undefined</span></span><br/>       |
| <span data-ttu-id="5afb5-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="5afb5-136">MinLength</span></span><br/>    | <span data-ttu-id="5afb5-137">integer</span><span class="sxs-lookup"><span data-stu-id="5afb5-137">integer</span></span><br/> | <span data-ttu-id="5afb5-138">1</span><span class="sxs-lookup"><span data-stu-id="5afb5-138">1</span></span><br/>               |
| <span data-ttu-id="5afb5-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5afb5-139">Mandatory</span></span><br/>    | <span data-ttu-id="5afb5-140">string</span><span class="sxs-lookup"><span data-stu-id="5afb5-140">string</span></span><br/>  | <span data-ttu-id="5afb5-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5afb5-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5afb5-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="5afb5-142">UnitType</span></span><br/>     | <span data-ttu-id="5afb5-143">string</span><span class="sxs-lookup"><span data-stu-id="5afb5-143">string</span></span><br/>  | <span data-ttu-id="5afb5-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="5afb5-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="5afb5-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5afb5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5afb5-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5afb5-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




