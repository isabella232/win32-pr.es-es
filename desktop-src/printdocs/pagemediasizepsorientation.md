---
description: Obtenga información sobre el parámetro PageMediaSizePSOrientation. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1b3aff1099199a98d6c8be899824dd1a1f17c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395730"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="5f825-105">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="5f825-105">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="5f825-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5f825-106">This topic is not current.</span></span> <span data-ttu-id="5f825-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5f825-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5f825-108">Especifica la orientación relativa a la dirección de orientación de la fuente (Especificación de formato de archivo de descripción de impresora [PostScript de referencia).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="5f825-108">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="5f825-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5f825-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5f825-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5f825-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5f825-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5f825-111">Element Information</span></span>



| <span data-ttu-id="5f825-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f825-112">Name</span></span> | <span data-ttu-id="5f825-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5f825-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5f825-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5f825-114">Element Type</span></span> <br/>   | <span data-ttu-id="5f825-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5f825-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="5f825-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5f825-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5f825-117">Página</span><span class="sxs-lookup"><span data-stu-id="5f825-117">Page</span></span><br/>                                             |
| <span data-ttu-id="5f825-118">Notas</span><span class="sxs-lookup"><span data-stu-id="5f825-118">Notes</span></span> <br/>          | <span data-ttu-id="5f825-119">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="5f825-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5f825-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5f825-120">Structure Content</span></span>

<span data-ttu-id="5f825-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5f825-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="5f825-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="5f825-122">Structure Properties</span></span>

<span data-ttu-id="5f825-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5f825-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5f825-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f825-124">Property</span></span>                | <span data-ttu-id="5f825-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5f825-125">xsi:type</span></span>           | <span data-ttu-id="5f825-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5f825-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="5f825-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5f825-127">DataType</span></span><br/>     | <span data-ttu-id="5f825-128">string</span><span class="sxs-lookup"><span data-stu-id="5f825-128">string</span></span><br/>  | <span data-ttu-id="5f825-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f825-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="5f825-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5f825-130">DefaultValue</span></span><br/> | <span data-ttu-id="5f825-131">integer</span><span class="sxs-lookup"><span data-stu-id="5f825-131">integer</span></span><br/> | <span data-ttu-id="5f825-132">0</span><span class="sxs-lookup"><span data-stu-id="5f825-132">0</span></span><br/>                 |
| <span data-ttu-id="5f825-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5f825-133">MaxValue</span></span><br/>     | <span data-ttu-id="5f825-134">integer</span><span class="sxs-lookup"><span data-stu-id="5f825-134">integer</span></span><br/> | <span data-ttu-id="5f825-135">3</span><span class="sxs-lookup"><span data-stu-id="5f825-135">3</span></span><br/>                 |
| <span data-ttu-id="5f825-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="5f825-136">MinValue</span></span><br/>     | <span data-ttu-id="5f825-137">integer</span><span class="sxs-lookup"><span data-stu-id="5f825-137">integer</span></span><br/> | <span data-ttu-id="5f825-138">0</span><span class="sxs-lookup"><span data-stu-id="5f825-138">0</span></span><br/>                 |
| <span data-ttu-id="5f825-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5f825-139">Mandatory</span></span><br/>    | <span data-ttu-id="5f825-140">string</span><span class="sxs-lookup"><span data-stu-id="5f825-140">string</span></span><br/>  | <span data-ttu-id="5f825-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5f825-141">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="5f825-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="5f825-142">Multiple</span></span><br/>     | <span data-ttu-id="5f825-143">integer</span><span class="sxs-lookup"><span data-stu-id="5f825-143">integer</span></span><br/> | <span data-ttu-id="5f825-144">1</span><span class="sxs-lookup"><span data-stu-id="5f825-144">1</span></span><br/>                 |
| <span data-ttu-id="5f825-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="5f825-145">UnitType</span></span><br/>     | <span data-ttu-id="5f825-146">string</span><span class="sxs-lookup"><span data-stu-id="5f825-146">string</span></span><br/>  | <span data-ttu-id="5f825-147">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="5f825-147">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5f825-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f825-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f825-149">Especificación de formato de archivo de descripción de impresora PostScript</span><span class="sxs-lookup"><span data-stu-id="5f825-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="5f825-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5f825-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




