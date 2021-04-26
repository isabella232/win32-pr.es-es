---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515fca037e58c0794f20bc1dd1afee8a779fb49
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996902"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="e3860-104">PageSourceColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="e3860-104">PageSourceColorProfileURI</span></span>

<span data-ttu-id="e3860-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e3860-105">This topic is not current.</span></span> <span data-ttu-id="e3860-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3860-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3860-107">Especifica el origen del perfil de color.</span><span class="sxs-lookup"><span data-stu-id="e3860-107">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="e3860-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e3860-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3860-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e3860-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e3860-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e3860-110">Element Information</span></span>



| <span data-ttu-id="e3860-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3860-111">Name</span></span> | <span data-ttu-id="e3860-112">Value</span><span class="sxs-lookup"><span data-stu-id="e3860-112">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="e3860-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e3860-113">Element Type</span></span> <br/>   | <span data-ttu-id="e3860-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e3860-114">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="e3860-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e3860-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3860-116">Página</span><span class="sxs-lookup"><span data-stu-id="e3860-116">Page</span></span><br/>                                     |
| <span data-ttu-id="e3860-117">Notas</span><span class="sxs-lookup"><span data-stu-id="e3860-117">Notes</span></span> <br/>          | <span data-ttu-id="e3860-118">Vinculado al elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="e3860-118">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e3860-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e3860-119">Structure Content</span></span>

<span data-ttu-id="e3860-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e3860-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="e3860-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="e3860-121">Structure Properties</span></span>

<span data-ttu-id="e3860-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e3860-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3860-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3860-123">Property</span></span>                | <span data-ttu-id="e3860-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e3860-124">xsi:type</span></span>           | <span data-ttu-id="e3860-125">Value</span><span class="sxs-lookup"><span data-stu-id="e3860-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e3860-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e3860-126">DataType</span></span><br/>     | <span data-ttu-id="e3860-127">string</span><span class="sxs-lookup"><span data-stu-id="e3860-127">string</span></span><br/>  | <span data-ttu-id="e3860-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e3860-128">xs:string</span></span><br/>       |
| <span data-ttu-id="e3860-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e3860-129">DefaultValue</span></span><br/> | <span data-ttu-id="e3860-130">string</span><span class="sxs-lookup"><span data-stu-id="e3860-130">string</span></span><br/>  | <span data-ttu-id="e3860-131">no definido</span><span class="sxs-lookup"><span data-stu-id="e3860-131">undefined</span></span><br/>       |
| <span data-ttu-id="e3860-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e3860-132">MaxLength</span></span><br/>    | <span data-ttu-id="e3860-133">integer</span><span class="sxs-lookup"><span data-stu-id="e3860-133">integer</span></span><br/> | <span data-ttu-id="e3860-134">no definido</span><span class="sxs-lookup"><span data-stu-id="e3860-134">undefined</span></span><br/>       |
| <span data-ttu-id="e3860-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="e3860-135">MinLength</span></span><br/>    | <span data-ttu-id="e3860-136">integer</span><span class="sxs-lookup"><span data-stu-id="e3860-136">integer</span></span><br/> | <span data-ttu-id="e3860-137">1</span><span class="sxs-lookup"><span data-stu-id="e3860-137">1</span></span><br/>               |
| <span data-ttu-id="e3860-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="e3860-138">Mandatory</span></span><br/>    | <span data-ttu-id="e3860-139">string</span><span class="sxs-lookup"><span data-stu-id="e3860-139">string</span></span><br/>  | <span data-ttu-id="e3860-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e3860-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e3860-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="e3860-141">UnitType</span></span><br/>     | <span data-ttu-id="e3860-142">string</span><span class="sxs-lookup"><span data-stu-id="e3860-142">string</span></span><br/>  | <span data-ttu-id="e3860-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="e3860-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e3860-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3860-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3860-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e3860-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




