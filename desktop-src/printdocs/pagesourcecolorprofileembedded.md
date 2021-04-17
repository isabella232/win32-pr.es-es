---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409b101d944152fa28c8972da4d8515e8cdfb05b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698024"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="67a27-104">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="67a27-104">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="67a27-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="67a27-105">This topic is not current.</span></span> <span data-ttu-id="67a27-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="67a27-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="67a27-107">Especifica el perfil de color de origen incrustado.</span><span class="sxs-lookup"><span data-stu-id="67a27-107">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="67a27-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="67a27-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="67a27-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="67a27-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="67a27-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="67a27-110">Element Information</span></span>



| <span data-ttu-id="67a27-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="67a27-111">Name</span></span>                       |                                                     |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="67a27-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="67a27-112">Element Type</span></span> <br/>   | <span data-ttu-id="67a27-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="67a27-113">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="67a27-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="67a27-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="67a27-115">Página</span><span class="sxs-lookup"><span data-stu-id="67a27-115">Page</span></span><br/>                                     |
| <span data-ttu-id="67a27-116">Notas</span><span class="sxs-lookup"><span data-stu-id="67a27-116">Notes</span></span> <br/>          | <span data-ttu-id="67a27-117">Vinculado al elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="67a27-117">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="67a27-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="67a27-118">Structure Content</span></span>

<span data-ttu-id="67a27-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="67a27-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="67a27-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="67a27-120">Structure Properties</span></span>

<span data-ttu-id="67a27-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="67a27-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="67a27-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67a27-122">Property</span></span>                | <span data-ttu-id="67a27-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="67a27-123">xsi:type</span></span>           | <span data-ttu-id="67a27-124">Value</span><span class="sxs-lookup"><span data-stu-id="67a27-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="67a27-125">DataType</span><span class="sxs-lookup"><span data-stu-id="67a27-125">DataType</span></span><br/>     | <span data-ttu-id="67a27-126">string</span><span class="sxs-lookup"><span data-stu-id="67a27-126">string</span></span><br/>  | <span data-ttu-id="67a27-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="67a27-127">xs:string</span></span><br/>       |
| <span data-ttu-id="67a27-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="67a27-128">DefaultValue</span></span><br/> | <span data-ttu-id="67a27-129">string</span><span class="sxs-lookup"><span data-stu-id="67a27-129">string</span></span><br/>  | <span data-ttu-id="67a27-130">no definido</span><span class="sxs-lookup"><span data-stu-id="67a27-130">undefined</span></span><br/>       |
| <span data-ttu-id="67a27-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="67a27-131">MaxLength</span></span><br/>    | <span data-ttu-id="67a27-132">integer</span><span class="sxs-lookup"><span data-stu-id="67a27-132">integer</span></span><br/> | <span data-ttu-id="67a27-133">no definido</span><span class="sxs-lookup"><span data-stu-id="67a27-133">undefined</span></span><br/>       |
| <span data-ttu-id="67a27-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="67a27-134">MinLength</span></span><br/>    | <span data-ttu-id="67a27-135">integer</span><span class="sxs-lookup"><span data-stu-id="67a27-135">integer</span></span><br/> | <span data-ttu-id="67a27-136">1</span><span class="sxs-lookup"><span data-stu-id="67a27-136">1</span></span><br/>               |
| <span data-ttu-id="67a27-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="67a27-137">Mandatory</span></span><br/>    | <span data-ttu-id="67a27-138">string</span><span class="sxs-lookup"><span data-stu-id="67a27-138">string</span></span><br/>  | <span data-ttu-id="67a27-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="67a27-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="67a27-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="67a27-140">UnitType</span></span><br/>     | <span data-ttu-id="67a27-141">string</span><span class="sxs-lookup"><span data-stu-id="67a27-141">string</span></span><br/>  | <span data-ttu-id="67a27-142">caracteres</span><span class="sxs-lookup"><span data-stu-id="67a27-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="67a27-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67a27-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a27-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="67a27-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




