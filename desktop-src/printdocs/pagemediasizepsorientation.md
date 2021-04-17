---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a188c61d3bb3c47286b887406174a3fc41f3c58a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707578"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="dab75-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="dab75-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="dab75-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="dab75-105">This topic is not current.</span></span> <span data-ttu-id="dab75-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dab75-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dab75-107">Especifica la orientación relativa a la dirección de la orientación de la fuente (referencia a la [especificación de formato de archivo de descripción de impresora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="dab75-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="dab75-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dab75-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dab75-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dab75-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dab75-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dab75-110">Element Information</span></span>



| <span data-ttu-id="dab75-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="dab75-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="dab75-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dab75-112">Element Type</span></span> <br/>   | <span data-ttu-id="dab75-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dab75-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="dab75-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="dab75-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dab75-115">Página</span><span class="sxs-lookup"><span data-stu-id="dab75-115">Page</span></span><br/>                                             |
| <span data-ttu-id="dab75-116">Notas</span><span class="sxs-lookup"><span data-stu-id="dab75-116">Notes</span></span> <br/>          | <span data-ttu-id="dab75-117">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="dab75-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dab75-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dab75-118">Structure Content</span></span>

<span data-ttu-id="dab75-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="dab75-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="dab75-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="dab75-120">Structure Properties</span></span>

<span data-ttu-id="dab75-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="dab75-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dab75-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dab75-122">Property</span></span>                | <span data-ttu-id="dab75-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dab75-123">xsi:type</span></span>           | <span data-ttu-id="dab75-124">Value</span><span class="sxs-lookup"><span data-stu-id="dab75-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="dab75-125">DataType</span><span class="sxs-lookup"><span data-stu-id="dab75-125">DataType</span></span><br/>     | <span data-ttu-id="dab75-126">string</span><span class="sxs-lookup"><span data-stu-id="dab75-126">string</span></span><br/>  | <span data-ttu-id="dab75-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dab75-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="dab75-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dab75-128">DefaultValue</span></span><br/> | <span data-ttu-id="dab75-129">integer</span><span class="sxs-lookup"><span data-stu-id="dab75-129">integer</span></span><br/> | <span data-ttu-id="dab75-130">0</span><span class="sxs-lookup"><span data-stu-id="dab75-130">0</span></span><br/>                 |
| <span data-ttu-id="dab75-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dab75-131">MaxValue</span></span><br/>     | <span data-ttu-id="dab75-132">integer</span><span class="sxs-lookup"><span data-stu-id="dab75-132">integer</span></span><br/> | <span data-ttu-id="dab75-133">3</span><span class="sxs-lookup"><span data-stu-id="dab75-133">3</span></span><br/>                 |
| <span data-ttu-id="dab75-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="dab75-134">MinValue</span></span><br/>     | <span data-ttu-id="dab75-135">integer</span><span class="sxs-lookup"><span data-stu-id="dab75-135">integer</span></span><br/> | <span data-ttu-id="dab75-136">0</span><span class="sxs-lookup"><span data-stu-id="dab75-136">0</span></span><br/>                 |
| <span data-ttu-id="dab75-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="dab75-137">Mandatory</span></span><br/>    | <span data-ttu-id="dab75-138">string</span><span class="sxs-lookup"><span data-stu-id="dab75-138">string</span></span><br/>  | <span data-ttu-id="dab75-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="dab75-139">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="dab75-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="dab75-140">Multiple</span></span><br/>     | <span data-ttu-id="dab75-141">integer</span><span class="sxs-lookup"><span data-stu-id="dab75-141">integer</span></span><br/> | <span data-ttu-id="dab75-142">1</span><span class="sxs-lookup"><span data-stu-id="dab75-142">1</span></span><br/>                 |
| <span data-ttu-id="dab75-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="dab75-143">UnitType</span></span><br/>     | <span data-ttu-id="dab75-144">string</span><span class="sxs-lookup"><span data-stu-id="dab75-144">string</span></span><br/>  | <span data-ttu-id="dab75-145">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="dab75-145">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="dab75-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dab75-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab75-147">Especificación de formato de archivo de descripción de impresora PostScript</span><span class="sxs-lookup"><span data-stu-id="dab75-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="dab75-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="dab75-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




