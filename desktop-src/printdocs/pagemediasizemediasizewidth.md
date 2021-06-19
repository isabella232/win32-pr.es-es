---
description: Obtenga información sobre el parámetro PageMediaSizeMediaSizeWidth. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f84e36f689d4b3c5ca060020327d78b12f7d6
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395840"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="bc9ed-105">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="bc9ed-105">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="bc9ed-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="bc9ed-106">This topic is not current.</span></span> <span data-ttu-id="bc9ed-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bc9ed-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc9ed-108">Especifica la dirección mediasizewidth de la dimensión para la opción MediaSize personalizada.</span><span class="sxs-lookup"><span data-stu-id="bc9ed-108">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="bc9ed-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bc9ed-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bc9ed-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bc9ed-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bc9ed-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bc9ed-111">Element Information</span></span>



| <span data-ttu-id="bc9ed-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc9ed-112">Name</span></span> | <span data-ttu-id="bc9ed-113">Valor</span><span class="sxs-lookup"><span data-stu-id="bc9ed-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc9ed-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bc9ed-114">Element Type</span></span> <br/>   | <span data-ttu-id="bc9ed-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bc9ed-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="bc9ed-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="bc9ed-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bc9ed-117">Página</span><span class="sxs-lookup"><span data-stu-id="bc9ed-117">Page</span></span><br/>                                           |
| <span data-ttu-id="bc9ed-118">Notas</span><span class="sxs-lookup"><span data-stu-id="bc9ed-118">Notes</span></span> <br/>          | <span data-ttu-id="bc9ed-119">Vinculado al elemento PageMediaSize, opción Personalizada</span><span class="sxs-lookup"><span data-stu-id="bc9ed-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bc9ed-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="bc9ed-120">Structure Content</span></span>

<span data-ttu-id="bc9ed-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="bc9ed-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="bc9ed-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="bc9ed-122">Structure Properties</span></span>

<span data-ttu-id="bc9ed-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="bc9ed-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bc9ed-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc9ed-124">Property</span></span>                | <span data-ttu-id="bc9ed-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bc9ed-125">xsi:type</span></span>           | <span data-ttu-id="bc9ed-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bc9ed-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="bc9ed-127">DataType</span><span class="sxs-lookup"><span data-stu-id="bc9ed-127">DataType</span></span><br/>     | <span data-ttu-id="bc9ed-128">string</span><span class="sxs-lookup"><span data-stu-id="bc9ed-128">string</span></span><br/>  | <span data-ttu-id="bc9ed-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bc9ed-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="bc9ed-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bc9ed-130">DefaultValue</span></span><br/> | <span data-ttu-id="bc9ed-131">integer</span><span class="sxs-lookup"><span data-stu-id="bc9ed-131">integer</span></span><br/> | <span data-ttu-id="bc9ed-132">no definido</span><span class="sxs-lookup"><span data-stu-id="bc9ed-132">undefined</span></span><br/>       |
| <span data-ttu-id="bc9ed-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="bc9ed-133">MaxValue</span></span><br/>     | <span data-ttu-id="bc9ed-134">integer</span><span class="sxs-lookup"><span data-stu-id="bc9ed-134">integer</span></span><br/> | <span data-ttu-id="bc9ed-135">no definido</span><span class="sxs-lookup"><span data-stu-id="bc9ed-135">undefined</span></span><br/>       |
| <span data-ttu-id="bc9ed-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="bc9ed-136">MinValue</span></span><br/>     | <span data-ttu-id="bc9ed-137">integer</span><span class="sxs-lookup"><span data-stu-id="bc9ed-137">integer</span></span><br/> | <span data-ttu-id="bc9ed-138">no definido</span><span class="sxs-lookup"><span data-stu-id="bc9ed-138">undefined</span></span><br/>       |
| <span data-ttu-id="bc9ed-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="bc9ed-139">Mandatory</span></span><br/>    | <span data-ttu-id="bc9ed-140">string</span><span class="sxs-lookup"><span data-stu-id="bc9ed-140">string</span></span><br/>  | <span data-ttu-id="bc9ed-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="bc9ed-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="bc9ed-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="bc9ed-142">Multiple</span></span><br/>     | <span data-ttu-id="bc9ed-143">integer</span><span class="sxs-lookup"><span data-stu-id="bc9ed-143">integer</span></span><br/> | <span data-ttu-id="bc9ed-144">1</span><span class="sxs-lookup"><span data-stu-id="bc9ed-144">1</span></span><br/>               |
| <span data-ttu-id="bc9ed-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="bc9ed-145">UnitType</span></span><br/>     | <span data-ttu-id="bc9ed-146">string</span><span class="sxs-lookup"><span data-stu-id="bc9ed-146">string</span></span><br/>  | <span data-ttu-id="bc9ed-147">Micras</span><span class="sxs-lookup"><span data-stu-id="bc9ed-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="bc9ed-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc9ed-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc9ed-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="bc9ed-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




