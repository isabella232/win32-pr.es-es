---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e97e768561fd13d5033b12f69a9bc481448e0e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999147"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="a4e97-104">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="a4e97-104">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="a4e97-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="a4e97-105">This topic is not current.</span></span> <span data-ttu-id="a4e97-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a4e97-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4e97-107">Especifica el perfil de color de origen incrustado.</span><span class="sxs-lookup"><span data-stu-id="a4e97-107">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="a4e97-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a4e97-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a4e97-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="a4e97-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a4e97-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a4e97-110">Element Information</span></span>



| <span data-ttu-id="a4e97-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="a4e97-111">Name</span></span> | <span data-ttu-id="a4e97-112">Value</span><span class="sxs-lookup"><span data-stu-id="a4e97-112">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="a4e97-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a4e97-113">Element Type</span></span> <br/>   | <span data-ttu-id="a4e97-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a4e97-114">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="a4e97-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="a4e97-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a4e97-116">Página</span><span class="sxs-lookup"><span data-stu-id="a4e97-116">Page</span></span><br/>                                     |
| <span data-ttu-id="a4e97-117">Notas</span><span class="sxs-lookup"><span data-stu-id="a4e97-117">Notes</span></span> <br/>          | <span data-ttu-id="a4e97-118">Vinculado al elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="a4e97-118">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a4e97-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="a4e97-119">Structure Content</span></span>

<span data-ttu-id="a4e97-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="a4e97-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a4e97-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="a4e97-121">Structure Properties</span></span>

<span data-ttu-id="a4e97-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="a4e97-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a4e97-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4e97-123">Property</span></span>                | <span data-ttu-id="a4e97-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a4e97-124">xsi:type</span></span>           | <span data-ttu-id="a4e97-125">Value</span><span class="sxs-lookup"><span data-stu-id="a4e97-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a4e97-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a4e97-126">DataType</span></span><br/>     | <span data-ttu-id="a4e97-127">string</span><span class="sxs-lookup"><span data-stu-id="a4e97-127">string</span></span><br/>  | <span data-ttu-id="a4e97-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4e97-128">xs:string</span></span><br/>       |
| <span data-ttu-id="a4e97-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a4e97-129">DefaultValue</span></span><br/> | <span data-ttu-id="a4e97-130">string</span><span class="sxs-lookup"><span data-stu-id="a4e97-130">string</span></span><br/>  | <span data-ttu-id="a4e97-131">no definido</span><span class="sxs-lookup"><span data-stu-id="a4e97-131">undefined</span></span><br/>       |
| <span data-ttu-id="a4e97-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a4e97-132">MaxLength</span></span><br/>    | <span data-ttu-id="a4e97-133">integer</span><span class="sxs-lookup"><span data-stu-id="a4e97-133">integer</span></span><br/> | <span data-ttu-id="a4e97-134">no definido</span><span class="sxs-lookup"><span data-stu-id="a4e97-134">undefined</span></span><br/>       |
| <span data-ttu-id="a4e97-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="a4e97-135">MinLength</span></span><br/>    | <span data-ttu-id="a4e97-136">integer</span><span class="sxs-lookup"><span data-stu-id="a4e97-136">integer</span></span><br/> | <span data-ttu-id="a4e97-137">1</span><span class="sxs-lookup"><span data-stu-id="a4e97-137">1</span></span><br/>               |
| <span data-ttu-id="a4e97-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="a4e97-138">Mandatory</span></span><br/>    | <span data-ttu-id="a4e97-139">string</span><span class="sxs-lookup"><span data-stu-id="a4e97-139">string</span></span><br/>  | <span data-ttu-id="a4e97-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a4e97-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a4e97-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="a4e97-141">UnitType</span></span><br/>     | <span data-ttu-id="a4e97-142">string</span><span class="sxs-lookup"><span data-stu-id="a4e97-142">string</span></span><br/>  | <span data-ttu-id="a4e97-143">caracteres</span><span class="sxs-lookup"><span data-stu-id="a4e97-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a4e97-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4e97-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e97-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="a4e97-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




