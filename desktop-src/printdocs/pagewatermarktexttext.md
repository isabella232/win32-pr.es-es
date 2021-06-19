---
description: Obtenga más información sobre el parámetro PageWatermarkTextText. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db5ef33008f0ccb66b6af34e2cc245b90c1ebea
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395970"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="03f83-105">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="03f83-105">PageWatermarkTextText</span></span>

<span data-ttu-id="03f83-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="03f83-106">This topic is not current.</span></span> <span data-ttu-id="03f83-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="03f83-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="03f83-108">Especifica el texto de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="03f83-108">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="03f83-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="03f83-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="03f83-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="03f83-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="03f83-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="03f83-111">Element Information</span></span>



| <span data-ttu-id="03f83-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="03f83-112">Name</span></span> | <span data-ttu-id="03f83-113">Valor</span><span class="sxs-lookup"><span data-stu-id="03f83-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="03f83-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="03f83-114">Element Type</span></span> <br/>   | <span data-ttu-id="03f83-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="03f83-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="03f83-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="03f83-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="03f83-117">Página</span><span class="sxs-lookup"><span data-stu-id="03f83-117">Page</span></span><br/>                            |
| <span data-ttu-id="03f83-118">Notas</span><span class="sxs-lookup"><span data-stu-id="03f83-118">Notes</span></span> <br/>          | <span data-ttu-id="03f83-119">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="03f83-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="03f83-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="03f83-120">Structure Content</span></span>

<span data-ttu-id="03f83-121">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="03f83-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="03f83-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="03f83-122">Structure Properties</span></span>

<span data-ttu-id="03f83-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="03f83-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="03f83-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="03f83-124">Property</span></span>                | <span data-ttu-id="03f83-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="03f83-125">xsi:type</span></span>           | <span data-ttu-id="03f83-126">Valor</span><span class="sxs-lookup"><span data-stu-id="03f83-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="03f83-127">DataType</span><span class="sxs-lookup"><span data-stu-id="03f83-127">DataType</span></span><br/>     | <span data-ttu-id="03f83-128">String</span><span class="sxs-lookup"><span data-stu-id="03f83-128">String</span></span><br/>  | <span data-ttu-id="03f83-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="03f83-129">xs:string</span></span><br/>       |
| <span data-ttu-id="03f83-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="03f83-130">DefaultValue</span></span><br/> | <span data-ttu-id="03f83-131">Entero</span><span class="sxs-lookup"><span data-stu-id="03f83-131">Integer</span></span><br/> | <span data-ttu-id="03f83-132">no definido</span><span class="sxs-lookup"><span data-stu-id="03f83-132">undefined</span></span><br/>       |
| <span data-ttu-id="03f83-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="03f83-133">MaxLength</span></span><br/>    | <span data-ttu-id="03f83-134">Entero</span><span class="sxs-lookup"><span data-stu-id="03f83-134">Integer</span></span><br/> | <span data-ttu-id="03f83-135">no definido</span><span class="sxs-lookup"><span data-stu-id="03f83-135">undefined</span></span><br/>       |
| <span data-ttu-id="03f83-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="03f83-136">MinLength</span></span><br/>    | <span data-ttu-id="03f83-137">Entero</span><span class="sxs-lookup"><span data-stu-id="03f83-137">Integer</span></span><br/> | <span data-ttu-id="03f83-138">1</span><span class="sxs-lookup"><span data-stu-id="03f83-138">1</span></span><br/>               |
| <span data-ttu-id="03f83-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="03f83-139">Mandatory</span></span><br/>    | <span data-ttu-id="03f83-140">String</span><span class="sxs-lookup"><span data-stu-id="03f83-140">String</span></span><br/>  | <span data-ttu-id="03f83-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="03f83-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="03f83-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="03f83-142">UnitType</span></span><br/>     | <span data-ttu-id="03f83-143">String</span><span class="sxs-lookup"><span data-stu-id="03f83-143">String</span></span><br/>  | <span data-ttu-id="03f83-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="03f83-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="03f83-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03f83-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03f83-146">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="03f83-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




