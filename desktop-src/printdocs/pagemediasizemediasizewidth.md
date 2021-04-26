---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50df088fd25a69ee566e1406d3f1b833aa6131f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997572"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="98753-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="98753-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="98753-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="98753-105">This topic is not current.</span></span> <span data-ttu-id="98753-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="98753-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="98753-107">Especifica la dirección mediaSizeWidth de la dimensión para la opción MediaSize personalizada.</span><span class="sxs-lookup"><span data-stu-id="98753-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="98753-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="98753-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="98753-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="98753-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="98753-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="98753-110">Element Information</span></span>



| <span data-ttu-id="98753-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="98753-111">Name</span></span> | <span data-ttu-id="98753-112">Value</span><span class="sxs-lookup"><span data-stu-id="98753-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="98753-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="98753-113">Element Type</span></span> <br/>   | <span data-ttu-id="98753-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="98753-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="98753-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="98753-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="98753-116">Página</span><span class="sxs-lookup"><span data-stu-id="98753-116">Page</span></span><br/>                                           |
| <span data-ttu-id="98753-117">Notas</span><span class="sxs-lookup"><span data-stu-id="98753-117">Notes</span></span> <br/>          | <span data-ttu-id="98753-118">Vinculado al elemento PageMediaSize, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="98753-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="98753-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="98753-119">Structure Content</span></span>

<span data-ttu-id="98753-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="98753-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="98753-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="98753-121">Structure Properties</span></span>

<span data-ttu-id="98753-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="98753-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="98753-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98753-123">Property</span></span>                | <span data-ttu-id="98753-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="98753-124">xsi:type</span></span>           | <span data-ttu-id="98753-125">Value</span><span class="sxs-lookup"><span data-stu-id="98753-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="98753-126">DataType</span><span class="sxs-lookup"><span data-stu-id="98753-126">DataType</span></span><br/>     | <span data-ttu-id="98753-127">string</span><span class="sxs-lookup"><span data-stu-id="98753-127">string</span></span><br/>  | <span data-ttu-id="98753-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="98753-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="98753-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="98753-129">DefaultValue</span></span><br/> | <span data-ttu-id="98753-130">integer</span><span class="sxs-lookup"><span data-stu-id="98753-130">integer</span></span><br/> | <span data-ttu-id="98753-131">no definido</span><span class="sxs-lookup"><span data-stu-id="98753-131">undefined</span></span><br/>       |
| <span data-ttu-id="98753-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="98753-132">MaxValue</span></span><br/>     | <span data-ttu-id="98753-133">integer</span><span class="sxs-lookup"><span data-stu-id="98753-133">integer</span></span><br/> | <span data-ttu-id="98753-134">no definido</span><span class="sxs-lookup"><span data-stu-id="98753-134">undefined</span></span><br/>       |
| <span data-ttu-id="98753-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="98753-135">MinValue</span></span><br/>     | <span data-ttu-id="98753-136">integer</span><span class="sxs-lookup"><span data-stu-id="98753-136">integer</span></span><br/> | <span data-ttu-id="98753-137">no definido</span><span class="sxs-lookup"><span data-stu-id="98753-137">undefined</span></span><br/>       |
| <span data-ttu-id="98753-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="98753-138">Mandatory</span></span><br/>    | <span data-ttu-id="98753-139">string</span><span class="sxs-lookup"><span data-stu-id="98753-139">string</span></span><br/>  | <span data-ttu-id="98753-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="98753-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="98753-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="98753-141">Multiple</span></span><br/>     | <span data-ttu-id="98753-142">integer</span><span class="sxs-lookup"><span data-stu-id="98753-142">integer</span></span><br/> | <span data-ttu-id="98753-143">1</span><span class="sxs-lookup"><span data-stu-id="98753-143">1</span></span><br/>               |
| <span data-ttu-id="98753-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="98753-144">UnitType</span></span><br/>     | <span data-ttu-id="98753-145">string</span><span class="sxs-lookup"><span data-stu-id="98753-145">string</span></span><br/>  | <span data-ttu-id="98753-146">Micras</span><span class="sxs-lookup"><span data-stu-id="98753-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="98753-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98753-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98753-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="98753-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




