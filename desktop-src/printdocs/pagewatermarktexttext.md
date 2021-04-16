---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef2310efaa91532493f7add14de8c2510e24e9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678655"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="8f6fd-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="8f6fd-104">PageWatermarkTextText</span></span>

<span data-ttu-id="8f6fd-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="8f6fd-105">This topic is not current.</span></span> <span data-ttu-id="8f6fd-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8f6fd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8f6fd-107">Especifica el texto de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="8f6fd-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="8f6fd-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8f6fd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8f6fd-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="8f6fd-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8f6fd-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8f6fd-110">Element Information</span></span>



| <span data-ttu-id="8f6fd-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f6fd-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="8f6fd-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8f6fd-112">Element Type</span></span> <br/>   | <span data-ttu-id="8f6fd-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8f6fd-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="8f6fd-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="8f6fd-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8f6fd-115">Página</span><span class="sxs-lookup"><span data-stu-id="8f6fd-115">Page</span></span><br/>                            |
| <span data-ttu-id="8f6fd-116">Notas</span><span class="sxs-lookup"><span data-stu-id="8f6fd-116">Notes</span></span> <br/>          | <span data-ttu-id="8f6fd-117">Vinculado al elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="8f6fd-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8f6fd-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="8f6fd-118">Structure Content</span></span>

<span data-ttu-id="8f6fd-119">La estructura XML de este elemento es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8f6fd-119">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8f6fd-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="8f6fd-120">Structure Properties</span></span>

<span data-ttu-id="8f6fd-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="8f6fd-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8f6fd-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f6fd-122">Property</span></span>                | <span data-ttu-id="8f6fd-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8f6fd-123">xsi:type</span></span>           | <span data-ttu-id="8f6fd-124">Value</span><span class="sxs-lookup"><span data-stu-id="8f6fd-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8f6fd-125">DataType</span><span class="sxs-lookup"><span data-stu-id="8f6fd-125">DataType</span></span><br/>     | <span data-ttu-id="8f6fd-126">String</span><span class="sxs-lookup"><span data-stu-id="8f6fd-126">String</span></span><br/>  | <span data-ttu-id="8f6fd-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="8f6fd-127">xs:string</span></span><br/>       |
| <span data-ttu-id="8f6fd-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8f6fd-128">DefaultValue</span></span><br/> | <span data-ttu-id="8f6fd-129">Entero</span><span class="sxs-lookup"><span data-stu-id="8f6fd-129">Integer</span></span><br/> | <span data-ttu-id="8f6fd-130">no definido</span><span class="sxs-lookup"><span data-stu-id="8f6fd-130">undefined</span></span><br/>       |
| <span data-ttu-id="8f6fd-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="8f6fd-131">MaxLength</span></span><br/>    | <span data-ttu-id="8f6fd-132">Entero</span><span class="sxs-lookup"><span data-stu-id="8f6fd-132">Integer</span></span><br/> | <span data-ttu-id="8f6fd-133">no definido</span><span class="sxs-lookup"><span data-stu-id="8f6fd-133">undefined</span></span><br/>       |
| <span data-ttu-id="8f6fd-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="8f6fd-134">MinLength</span></span><br/>    | <span data-ttu-id="8f6fd-135">Entero</span><span class="sxs-lookup"><span data-stu-id="8f6fd-135">Integer</span></span><br/> | <span data-ttu-id="8f6fd-136">1</span><span class="sxs-lookup"><span data-stu-id="8f6fd-136">1</span></span><br/>               |
| <span data-ttu-id="8f6fd-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="8f6fd-137">Mandatory</span></span><br/>    | <span data-ttu-id="8f6fd-138">String</span><span class="sxs-lookup"><span data-stu-id="8f6fd-138">String</span></span><br/>  | <span data-ttu-id="8f6fd-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="8f6fd-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8f6fd-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="8f6fd-140">UnitType</span></span><br/>     | <span data-ttu-id="8f6fd-141">String</span><span class="sxs-lookup"><span data-stu-id="8f6fd-141">String</span></span><br/>  | <span data-ttu-id="8f6fd-142">caracteres</span><span class="sxs-lookup"><span data-stu-id="8f6fd-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="8f6fd-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f6fd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f6fd-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8f6fd-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




