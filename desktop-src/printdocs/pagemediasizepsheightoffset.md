---
description: Obtenga información sobre el parámetro PageMediaSizePSHeightOffset. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2c0e3802a6c461fe2f9eec68b28677c254be9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395740"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="e39e2-105">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="e39e2-105">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="e39e2-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="e39e2-106">This topic is not current.</span></span> <span data-ttu-id="e39e2-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e39e2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e39e2-108">Especifica el desplazamiento, paralelo a la dirección de orientación de la fuente (Especificación de formato de archivo de descripción de impresora [PostScript de referencia).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="e39e2-108">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="e39e2-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e39e2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e39e2-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e39e2-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e39e2-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e39e2-111">Element Information</span></span>



| <span data-ttu-id="e39e2-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="e39e2-112">Name</span></span> | <span data-ttu-id="e39e2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e39e2-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e39e2-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e39e2-114">Element Type</span></span> <br/>   | <span data-ttu-id="e39e2-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e39e2-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="e39e2-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="e39e2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e39e2-117">Página</span><span class="sxs-lookup"><span data-stu-id="e39e2-117">Page</span></span><br/>                                             |
| <span data-ttu-id="e39e2-118">Notas</span><span class="sxs-lookup"><span data-stu-id="e39e2-118">Notes</span></span> <br/>          | <span data-ttu-id="e39e2-119">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="e39e2-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e39e2-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="e39e2-120">Structure Content</span></span>

<span data-ttu-id="e39e2-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="e39e2-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="e39e2-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="e39e2-122">Structure Properties</span></span>

<span data-ttu-id="e39e2-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="e39e2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e39e2-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e39e2-124">Property</span></span>                | <span data-ttu-id="e39e2-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e39e2-125">xsi:type</span></span>           | <span data-ttu-id="e39e2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e39e2-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e39e2-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e39e2-127">DataType</span></span><br/>     | <span data-ttu-id="e39e2-128">string</span><span class="sxs-lookup"><span data-stu-id="e39e2-128">string</span></span><br/>  | <span data-ttu-id="e39e2-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e39e2-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="e39e2-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e39e2-130">DefaultValue</span></span><br/> | <span data-ttu-id="e39e2-131">integer</span><span class="sxs-lookup"><span data-stu-id="e39e2-131">integer</span></span><br/> | <span data-ttu-id="e39e2-132">no definido</span><span class="sxs-lookup"><span data-stu-id="e39e2-132">undefined</span></span><br/>       |
| <span data-ttu-id="e39e2-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e39e2-133">MaxValue</span></span><br/>     | <span data-ttu-id="e39e2-134">integer</span><span class="sxs-lookup"><span data-stu-id="e39e2-134">integer</span></span><br/> | <span data-ttu-id="e39e2-135">no definido</span><span class="sxs-lookup"><span data-stu-id="e39e2-135">undefined</span></span><br/>       |
| <span data-ttu-id="e39e2-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="e39e2-136">MinValue</span></span><br/>     | <span data-ttu-id="e39e2-137">integer</span><span class="sxs-lookup"><span data-stu-id="e39e2-137">integer</span></span><br/> | <span data-ttu-id="e39e2-138">no definido</span><span class="sxs-lookup"><span data-stu-id="e39e2-138">undefined</span></span><br/>       |
| <span data-ttu-id="e39e2-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="e39e2-139">Mandatory</span></span><br/>    | <span data-ttu-id="e39e2-140">string</span><span class="sxs-lookup"><span data-stu-id="e39e2-140">string</span></span><br/>  | <span data-ttu-id="e39e2-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e39e2-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e39e2-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="e39e2-142">Multiple</span></span><br/>     | <span data-ttu-id="e39e2-143">integer</span><span class="sxs-lookup"><span data-stu-id="e39e2-143">integer</span></span><br/> | <span data-ttu-id="e39e2-144">1</span><span class="sxs-lookup"><span data-stu-id="e39e2-144">1</span></span><br/>               |
| <span data-ttu-id="e39e2-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="e39e2-145">UnitType</span></span><br/>     | <span data-ttu-id="e39e2-146">string</span><span class="sxs-lookup"><span data-stu-id="e39e2-146">string</span></span><br/>  | <span data-ttu-id="e39e2-147">Micras</span><span class="sxs-lookup"><span data-stu-id="e39e2-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e39e2-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e39e2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e39e2-149">Especificación de formato de archivo de descripción de impresora PostScript</span><span class="sxs-lookup"><span data-stu-id="e39e2-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="e39e2-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e39e2-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




