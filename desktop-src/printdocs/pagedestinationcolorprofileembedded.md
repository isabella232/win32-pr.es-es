---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47eaa810cd23462433c52292506999f90797d659
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707628"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="be5b2-104">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="be5b2-104">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="be5b2-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="be5b2-105">This topic is not current.</span></span> <span data-ttu-id="be5b2-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="be5b2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="be5b2-107">Especifica el perfil de color de destino incrustado.</span><span class="sxs-lookup"><span data-stu-id="be5b2-107">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="be5b2-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="be5b2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="be5b2-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="be5b2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="be5b2-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="be5b2-110">Element Information</span></span>



| <span data-ttu-id="be5b2-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="be5b2-111">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="be5b2-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="be5b2-112">Element Type</span></span> <br/>   | <span data-ttu-id="be5b2-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="be5b2-113">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="be5b2-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="be5b2-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="be5b2-115">Página</span><span class="sxs-lookup"><span data-stu-id="be5b2-115">Page</span></span><br/>                                          |
| <span data-ttu-id="be5b2-116">Notas</span><span class="sxs-lookup"><span data-stu-id="be5b2-116">Notes</span></span> <br/>          | <span data-ttu-id="be5b2-117">Vinculado al elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="be5b2-117">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="be5b2-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="be5b2-118">Structure Content</span></span>

<span data-ttu-id="be5b2-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="be5b2-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="be5b2-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="be5b2-120">Structure Properties</span></span>

<span data-ttu-id="be5b2-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="be5b2-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="be5b2-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be5b2-122">Property</span></span>                | <span data-ttu-id="be5b2-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="be5b2-123">xsi:type</span></span>           | <span data-ttu-id="be5b2-124">Value</span><span class="sxs-lookup"><span data-stu-id="be5b2-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="be5b2-125">DataType</span><span class="sxs-lookup"><span data-stu-id="be5b2-125">DataType</span></span><br/>     | <span data-ttu-id="be5b2-126">string</span><span class="sxs-lookup"><span data-stu-id="be5b2-126">string</span></span><br/>  | <span data-ttu-id="be5b2-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="be5b2-127">xs:string</span></span><br/>       |
| <span data-ttu-id="be5b2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="be5b2-128">DefaultValue</span></span><br/> | <span data-ttu-id="be5b2-129">string</span><span class="sxs-lookup"><span data-stu-id="be5b2-129">string</span></span><br/>  | <span data-ttu-id="be5b2-130">no definido</span><span class="sxs-lookup"><span data-stu-id="be5b2-130">undefined</span></span><br/>       |
| <span data-ttu-id="be5b2-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="be5b2-131">MaxLength</span></span><br/>    | <span data-ttu-id="be5b2-132">integer</span><span class="sxs-lookup"><span data-stu-id="be5b2-132">integer</span></span><br/> | <span data-ttu-id="be5b2-133">no definido</span><span class="sxs-lookup"><span data-stu-id="be5b2-133">undefined</span></span><br/>       |
| <span data-ttu-id="be5b2-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="be5b2-134">MinLength</span></span><br/>    | <span data-ttu-id="be5b2-135">integer</span><span class="sxs-lookup"><span data-stu-id="be5b2-135">integer</span></span><br/> | <span data-ttu-id="be5b2-136">1</span><span class="sxs-lookup"><span data-stu-id="be5b2-136">1</span></span><br/>               |
| <span data-ttu-id="be5b2-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="be5b2-137">Mandatory</span></span><br/>    | <span data-ttu-id="be5b2-138">string</span><span class="sxs-lookup"><span data-stu-id="be5b2-138">string</span></span><br/>  | <span data-ttu-id="be5b2-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="be5b2-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="be5b2-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="be5b2-140">UnitType</span></span><br/>     | <span data-ttu-id="be5b2-141">string</span><span class="sxs-lookup"><span data-stu-id="be5b2-141">string</span></span><br/>  | <span data-ttu-id="be5b2-142">caracteres</span><span class="sxs-lookup"><span data-stu-id="be5b2-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="be5b2-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be5b2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be5b2-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="be5b2-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




