---
description: Obtenga información sobre el parámetro PageSourceColorProfileEmbedded. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0633fa061601c1d575f174ab5572582efdf9a89e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395640"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="ae563-105">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="ae563-105">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="ae563-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ae563-106">This topic is not current.</span></span> <span data-ttu-id="ae563-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ae563-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ae563-108">Especifica el perfil de color de origen incrustado.</span><span class="sxs-lookup"><span data-stu-id="ae563-108">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="ae563-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ae563-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ae563-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ae563-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ae563-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ae563-111">Element Information</span></span>



| <span data-ttu-id="ae563-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae563-112">Name</span></span> | <span data-ttu-id="ae563-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ae563-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="ae563-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ae563-114">Element Type</span></span> <br/>   | <span data-ttu-id="ae563-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ae563-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="ae563-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ae563-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ae563-117">Página</span><span class="sxs-lookup"><span data-stu-id="ae563-117">Page</span></span><br/>                                     |
| <span data-ttu-id="ae563-118">Notas</span><span class="sxs-lookup"><span data-stu-id="ae563-118">Notes</span></span> <br/>          | <span data-ttu-id="ae563-119">Vinculado al elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="ae563-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ae563-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ae563-120">Structure Content</span></span>

<span data-ttu-id="ae563-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="ae563-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ae563-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="ae563-122">Structure Properties</span></span>

<span data-ttu-id="ae563-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ae563-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ae563-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae563-124">Property</span></span>                | <span data-ttu-id="ae563-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ae563-125">xsi:type</span></span>           | <span data-ttu-id="ae563-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ae563-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ae563-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ae563-127">DataType</span></span><br/>     | <span data-ttu-id="ae563-128">string</span><span class="sxs-lookup"><span data-stu-id="ae563-128">string</span></span><br/>  | <span data-ttu-id="ae563-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="ae563-129">xs:string</span></span><br/>       |
| <span data-ttu-id="ae563-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ae563-130">DefaultValue</span></span><br/> | <span data-ttu-id="ae563-131">string</span><span class="sxs-lookup"><span data-stu-id="ae563-131">string</span></span><br/>  | <span data-ttu-id="ae563-132">no definido</span><span class="sxs-lookup"><span data-stu-id="ae563-132">undefined</span></span><br/>       |
| <span data-ttu-id="ae563-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="ae563-133">MaxLength</span></span><br/>    | <span data-ttu-id="ae563-134">integer</span><span class="sxs-lookup"><span data-stu-id="ae563-134">integer</span></span><br/> | <span data-ttu-id="ae563-135">no definido</span><span class="sxs-lookup"><span data-stu-id="ae563-135">undefined</span></span><br/>       |
| <span data-ttu-id="ae563-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="ae563-136">MinLength</span></span><br/>    | <span data-ttu-id="ae563-137">integer</span><span class="sxs-lookup"><span data-stu-id="ae563-137">integer</span></span><br/> | <span data-ttu-id="ae563-138">1</span><span class="sxs-lookup"><span data-stu-id="ae563-138">1</span></span><br/>               |
| <span data-ttu-id="ae563-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="ae563-139">Mandatory</span></span><br/>    | <span data-ttu-id="ae563-140">string</span><span class="sxs-lookup"><span data-stu-id="ae563-140">string</span></span><br/>  | <span data-ttu-id="ae563-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="ae563-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ae563-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="ae563-142">UnitType</span></span><br/>     | <span data-ttu-id="ae563-143">string</span><span class="sxs-lookup"><span data-stu-id="ae563-143">string</span></span><br/>  | <span data-ttu-id="ae563-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="ae563-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="ae563-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae563-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae563-146">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ae563-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




