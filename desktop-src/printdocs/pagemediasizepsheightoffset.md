---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2e1e0a75c5bb6ec95a611d304d575fcf91a13e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998062"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="4e3da-104">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="4e3da-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="4e3da-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4e3da-105">This topic is not current.</span></span> <span data-ttu-id="4e3da-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4e3da-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4e3da-107">Especifica el desplazamiento, paralelo a la dirección de orientación de la fuente (Especificación de formato de archivo de descripción de impresora [PostScript de referencia).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="4e3da-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="4e3da-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4e3da-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4e3da-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4e3da-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4e3da-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4e3da-110">Element Information</span></span>



| <span data-ttu-id="4e3da-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e3da-111">Name</span></span> | <span data-ttu-id="4e3da-112">Value</span><span class="sxs-lookup"><span data-stu-id="4e3da-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="4e3da-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4e3da-113">Element Type</span></span> <br/>   | <span data-ttu-id="4e3da-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4e3da-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="4e3da-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="4e3da-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4e3da-116">Página</span><span class="sxs-lookup"><span data-stu-id="4e3da-116">Page</span></span><br/>                                             |
| <span data-ttu-id="4e3da-117">Notas</span><span class="sxs-lookup"><span data-stu-id="4e3da-117">Notes</span></span> <br/>          | <span data-ttu-id="4e3da-118">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="4e3da-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4e3da-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4e3da-119">Structure Content</span></span>

<span data-ttu-id="4e3da-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="4e3da-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4e3da-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="4e3da-121">Structure Properties</span></span>

<span data-ttu-id="4e3da-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="4e3da-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4e3da-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4e3da-123">Property</span></span>                | <span data-ttu-id="4e3da-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4e3da-124">xsi:type</span></span>           | <span data-ttu-id="4e3da-125">Value</span><span class="sxs-lookup"><span data-stu-id="4e3da-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4e3da-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4e3da-126">DataType</span></span><br/>     | <span data-ttu-id="4e3da-127">string</span><span class="sxs-lookup"><span data-stu-id="4e3da-127">string</span></span><br/>  | <span data-ttu-id="4e3da-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4e3da-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="4e3da-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4e3da-129">DefaultValue</span></span><br/> | <span data-ttu-id="4e3da-130">integer</span><span class="sxs-lookup"><span data-stu-id="4e3da-130">integer</span></span><br/> | <span data-ttu-id="4e3da-131">no definido</span><span class="sxs-lookup"><span data-stu-id="4e3da-131">undefined</span></span><br/>       |
| <span data-ttu-id="4e3da-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4e3da-132">MaxValue</span></span><br/>     | <span data-ttu-id="4e3da-133">integer</span><span class="sxs-lookup"><span data-stu-id="4e3da-133">integer</span></span><br/> | <span data-ttu-id="4e3da-134">no definido</span><span class="sxs-lookup"><span data-stu-id="4e3da-134">undefined</span></span><br/>       |
| <span data-ttu-id="4e3da-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="4e3da-135">MinValue</span></span><br/>     | <span data-ttu-id="4e3da-136">integer</span><span class="sxs-lookup"><span data-stu-id="4e3da-136">integer</span></span><br/> | <span data-ttu-id="4e3da-137">no definido</span><span class="sxs-lookup"><span data-stu-id="4e3da-137">undefined</span></span><br/>       |
| <span data-ttu-id="4e3da-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="4e3da-138">Mandatory</span></span><br/>    | <span data-ttu-id="4e3da-139">string</span><span class="sxs-lookup"><span data-stu-id="4e3da-139">string</span></span><br/>  | <span data-ttu-id="4e3da-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4e3da-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4e3da-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="4e3da-141">Multiple</span></span><br/>     | <span data-ttu-id="4e3da-142">integer</span><span class="sxs-lookup"><span data-stu-id="4e3da-142">integer</span></span><br/> | <span data-ttu-id="4e3da-143">1</span><span class="sxs-lookup"><span data-stu-id="4e3da-143">1</span></span><br/>               |
| <span data-ttu-id="4e3da-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="4e3da-144">UnitType</span></span><br/>     | <span data-ttu-id="4e3da-145">string</span><span class="sxs-lookup"><span data-stu-id="4e3da-145">string</span></span><br/>  | <span data-ttu-id="4e3da-146">Micras</span><span class="sxs-lookup"><span data-stu-id="4e3da-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4e3da-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e3da-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e3da-148">Especificación de formato de archivo de descripción de impresora PostScript</span><span class="sxs-lookup"><span data-stu-id="4e3da-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="4e3da-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4e3da-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




