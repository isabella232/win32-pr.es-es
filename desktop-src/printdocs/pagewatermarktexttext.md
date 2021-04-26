---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb19f5965347e79732aa116e5be51f90e4ef6943
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996082"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="bee96-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="bee96-104">PageWatermarkTextText</span></span>

<span data-ttu-id="bee96-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="bee96-105">This topic is not current.</span></span> <span data-ttu-id="bee96-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bee96-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bee96-107">Especifica el texto de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="bee96-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="bee96-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bee96-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bee96-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bee96-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bee96-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bee96-110">Element Information</span></span>



| <span data-ttu-id="bee96-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="bee96-111">Name</span></span> | <span data-ttu-id="bee96-112">Value</span><span class="sxs-lookup"><span data-stu-id="bee96-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="bee96-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bee96-113">Element Type</span></span> <br/>   | <span data-ttu-id="bee96-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bee96-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="bee96-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="bee96-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bee96-116">Página</span><span class="sxs-lookup"><span data-stu-id="bee96-116">Page</span></span><br/>                            |
| <span data-ttu-id="bee96-117">Notas</span><span class="sxs-lookup"><span data-stu-id="bee96-117">Notes</span></span> <br/>          | <span data-ttu-id="bee96-118">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="bee96-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bee96-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bee96-119">Structure Content</span></span>

<span data-ttu-id="bee96-120">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="bee96-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="bee96-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="bee96-121">Structure Properties</span></span>

<span data-ttu-id="bee96-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="bee96-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bee96-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bee96-123">Property</span></span>                | <span data-ttu-id="bee96-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bee96-124">xsi:type</span></span>           | <span data-ttu-id="bee96-125">Value</span><span class="sxs-lookup"><span data-stu-id="bee96-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="bee96-126">DataType</span><span class="sxs-lookup"><span data-stu-id="bee96-126">DataType</span></span><br/>     | <span data-ttu-id="bee96-127">String</span><span class="sxs-lookup"><span data-stu-id="bee96-127">String</span></span><br/>  | <span data-ttu-id="bee96-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="bee96-128">xs:string</span></span><br/>       |
| <span data-ttu-id="bee96-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bee96-129">DefaultValue</span></span><br/> | <span data-ttu-id="bee96-130">Entero</span><span class="sxs-lookup"><span data-stu-id="bee96-130">Integer</span></span><br/> | <span data-ttu-id="bee96-131">no definido</span><span class="sxs-lookup"><span data-stu-id="bee96-131">undefined</span></span><br/>       |
| <span data-ttu-id="bee96-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="bee96-132">MaxLength</span></span><br/>    | <span data-ttu-id="bee96-133">Entero</span><span class="sxs-lookup"><span data-stu-id="bee96-133">Integer</span></span><br/> | <span data-ttu-id="bee96-134">no definido</span><span class="sxs-lookup"><span data-stu-id="bee96-134">undefined</span></span><br/>       |
| <span data-ttu-id="bee96-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="bee96-135">MinLength</span></span><br/>    | <span data-ttu-id="bee96-136">Entero</span><span class="sxs-lookup"><span data-stu-id="bee96-136">Integer</span></span><br/> | <span data-ttu-id="bee96-137">1</span><span class="sxs-lookup"><span data-stu-id="bee96-137">1</span></span><br/>               |
| <span data-ttu-id="bee96-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="bee96-138">Mandatory</span></span><br/>    | <span data-ttu-id="bee96-139">String</span><span class="sxs-lookup"><span data-stu-id="bee96-139">String</span></span><br/>  | <span data-ttu-id="bee96-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="bee96-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="bee96-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="bee96-141">UnitType</span></span><br/>     | <span data-ttu-id="bee96-142">String</span><span class="sxs-lookup"><span data-stu-id="bee96-142">String</span></span><br/>  | <span data-ttu-id="bee96-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="bee96-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="bee96-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bee96-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee96-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="bee96-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




