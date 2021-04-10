---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219a86f016edf820532c20fa473876265776a4ee
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279888"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="b34ac-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="b34ac-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="b34ac-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="b34ac-105">This topic is not current.</span></span> <span data-ttu-id="b34ac-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b34ac-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b34ac-107">Especifica el ancho del medianil de enlace.</span><span class="sxs-lookup"><span data-stu-id="b34ac-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="b34ac-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b34ac-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b34ac-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="b34ac-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b34ac-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b34ac-110">Element Information</span></span>



| <span data-ttu-id="b34ac-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="b34ac-111">Name</span></span>                       |                                         |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="b34ac-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b34ac-112">Element Type</span></span> <br/>   | <span data-ttu-id="b34ac-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b34ac-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="b34ac-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="b34ac-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b34ac-115">Trabajo</span><span class="sxs-lookup"><span data-stu-id="b34ac-115">Job</span></span> <br/>                         |
| <span data-ttu-id="b34ac-116">Notas</span><span class="sxs-lookup"><span data-stu-id="b34ac-116">Notes</span></span> <br/>          | <span data-ttu-id="b34ac-117">Vinculado al elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="b34ac-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b34ac-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="b34ac-118">Structure Content</span></span>

<span data-ttu-id="b34ac-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="b34ac-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="b34ac-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="b34ac-120">Structure Properties</span></span>

<span data-ttu-id="b34ac-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="b34ac-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b34ac-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b34ac-122">Property</span></span>                | <span data-ttu-id="b34ac-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b34ac-123">xsi:type</span></span>           | <span data-ttu-id="b34ac-124">Value</span><span class="sxs-lookup"><span data-stu-id="b34ac-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b34ac-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b34ac-125">DataType</span></span><br/>     | <span data-ttu-id="b34ac-126">string</span><span class="sxs-lookup"><span data-stu-id="b34ac-126">string</span></span><br/>  | <span data-ttu-id="b34ac-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b34ac-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="b34ac-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b34ac-128">DefaultValue</span></span><br/> | <span data-ttu-id="b34ac-129">integer</span><span class="sxs-lookup"><span data-stu-id="b34ac-129">integer</span></span><br/> | <span data-ttu-id="b34ac-130">no definido</span><span class="sxs-lookup"><span data-stu-id="b34ac-130">undefined</span></span><br/>       |
| <span data-ttu-id="b34ac-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b34ac-131">MaxValue</span></span><br/>     | <span data-ttu-id="b34ac-132">integer</span><span class="sxs-lookup"><span data-stu-id="b34ac-132">integer</span></span><br/> | <span data-ttu-id="b34ac-133">no definido</span><span class="sxs-lookup"><span data-stu-id="b34ac-133">undefined</span></span><br/>       |
| <span data-ttu-id="b34ac-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b34ac-134">MinValue</span></span><br/>     | <span data-ttu-id="b34ac-135">integer</span><span class="sxs-lookup"><span data-stu-id="b34ac-135">integer</span></span><br/> | <span data-ttu-id="b34ac-136">no definido</span><span class="sxs-lookup"><span data-stu-id="b34ac-136">undefined</span></span><br/>       |
| <span data-ttu-id="b34ac-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="b34ac-137">Mandatory</span></span><br/>    | <span data-ttu-id="b34ac-138">String</span><span class="sxs-lookup"><span data-stu-id="b34ac-138">String</span></span><br/>  | <span data-ttu-id="b34ac-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="b34ac-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b34ac-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="b34ac-140">Multiple</span></span><br/>     | <span data-ttu-id="b34ac-141">integer</span><span class="sxs-lookup"><span data-stu-id="b34ac-141">integer</span></span><br/> | <span data-ttu-id="b34ac-142">1</span><span class="sxs-lookup"><span data-stu-id="b34ac-142">1</span></span><br/>               |
| <span data-ttu-id="b34ac-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="b34ac-143">UnitType</span></span><br/>     | <span data-ttu-id="b34ac-144">string</span><span class="sxs-lookup"><span data-stu-id="b34ac-144">string</span></span><br/>  | <span data-ttu-id="b34ac-145">microns</span><span class="sxs-lookup"><span data-stu-id="b34ac-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b34ac-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b34ac-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b34ac-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b34ac-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




