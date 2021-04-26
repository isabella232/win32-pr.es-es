---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997562"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="2fc64-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="2fc64-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="2fc64-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="2fc64-105">This topic is not current.</span></span> <span data-ttu-id="2fc64-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2fc64-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2fc64-107">Especifica la orientación relativa a la dirección de orientación de la fuente (Referencia a la especificación de formato de archivo de descripción de impresora [PostScript).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="2fc64-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="2fc64-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2fc64-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2fc64-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2fc64-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2fc64-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2fc64-110">Element Information</span></span>



| <span data-ttu-id="2fc64-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="2fc64-111">Name</span></span> | <span data-ttu-id="2fc64-112">Value</span><span class="sxs-lookup"><span data-stu-id="2fc64-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2fc64-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2fc64-113">Element Type</span></span> <br/>   | <span data-ttu-id="2fc64-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2fc64-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="2fc64-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2fc64-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2fc64-116">Página</span><span class="sxs-lookup"><span data-stu-id="2fc64-116">Page</span></span><br/>                                             |
| <span data-ttu-id="2fc64-117">Notas</span><span class="sxs-lookup"><span data-stu-id="2fc64-117">Notes</span></span> <br/>          | <span data-ttu-id="2fc64-118">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="2fc64-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2fc64-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2fc64-119">Structure Content</span></span>

<span data-ttu-id="2fc64-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2fc64-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2fc64-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="2fc64-121">Structure Properties</span></span>

<span data-ttu-id="2fc64-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2fc64-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2fc64-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2fc64-123">Property</span></span>                | <span data-ttu-id="2fc64-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2fc64-124">xsi:type</span></span>           | <span data-ttu-id="2fc64-125">Value</span><span class="sxs-lookup"><span data-stu-id="2fc64-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="2fc64-126">DataType</span><span class="sxs-lookup"><span data-stu-id="2fc64-126">DataType</span></span><br/>     | <span data-ttu-id="2fc64-127">string</span><span class="sxs-lookup"><span data-stu-id="2fc64-127">string</span></span><br/>  | <span data-ttu-id="2fc64-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2fc64-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="2fc64-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2fc64-129">DefaultValue</span></span><br/> | <span data-ttu-id="2fc64-130">integer</span><span class="sxs-lookup"><span data-stu-id="2fc64-130">integer</span></span><br/> | <span data-ttu-id="2fc64-131">0</span><span class="sxs-lookup"><span data-stu-id="2fc64-131">0</span></span><br/>                 |
| <span data-ttu-id="2fc64-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2fc64-132">MaxValue</span></span><br/>     | <span data-ttu-id="2fc64-133">integer</span><span class="sxs-lookup"><span data-stu-id="2fc64-133">integer</span></span><br/> | <span data-ttu-id="2fc64-134">3</span><span class="sxs-lookup"><span data-stu-id="2fc64-134">3</span></span><br/>                 |
| <span data-ttu-id="2fc64-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="2fc64-135">MinValue</span></span><br/>     | <span data-ttu-id="2fc64-136">integer</span><span class="sxs-lookup"><span data-stu-id="2fc64-136">integer</span></span><br/> | <span data-ttu-id="2fc64-137">0</span><span class="sxs-lookup"><span data-stu-id="2fc64-137">0</span></span><br/>                 |
| <span data-ttu-id="2fc64-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="2fc64-138">Mandatory</span></span><br/>    | <span data-ttu-id="2fc64-139">string</span><span class="sxs-lookup"><span data-stu-id="2fc64-139">string</span></span><br/>  | <span data-ttu-id="2fc64-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="2fc64-140">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="2fc64-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="2fc64-141">Multiple</span></span><br/>     | <span data-ttu-id="2fc64-142">integer</span><span class="sxs-lookup"><span data-stu-id="2fc64-142">integer</span></span><br/> | <span data-ttu-id="2fc64-143">1</span><span class="sxs-lookup"><span data-stu-id="2fc64-143">1</span></span><br/>                 |
| <span data-ttu-id="2fc64-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="2fc64-144">UnitType</span></span><br/>     | <span data-ttu-id="2fc64-145">string</span><span class="sxs-lookup"><span data-stu-id="2fc64-145">string</span></span><br/>  | <span data-ttu-id="2fc64-146">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="2fc64-146">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2fc64-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fc64-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fc64-148">Especificación de formato de archivo de descripción de impresora PostScript</span><span class="sxs-lookup"><span data-stu-id="2fc64-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="2fc64-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2fc64-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




