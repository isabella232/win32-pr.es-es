---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7fef8b9e3740c5f12045e449f2a6b8100d7fc1d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707601"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="19655-104">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="19655-104">PageMediaSizePSWidth</span></span>

<span data-ttu-id="19655-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="19655-105">This topic is not current.</span></span> <span data-ttu-id="19655-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="19655-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19655-107">Especifica el ancho de la página perpendicular a la dirección de la orientación de la fuente (referencia de la [especificación de formato de archivo de descripción de impresora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="19655-107">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="19655-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="19655-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="19655-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="19655-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="19655-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="19655-110">Element Information</span></span>



| <span data-ttu-id="19655-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="19655-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="19655-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="19655-112">Element Type</span></span> <br/>   | <span data-ttu-id="19655-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="19655-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="19655-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="19655-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="19655-115">Página</span><span class="sxs-lookup"><span data-stu-id="19655-115">Page</span></span><br/>                                             |
| <span data-ttu-id="19655-116">Notas</span><span class="sxs-lookup"><span data-stu-id="19655-116">Notes</span></span> <br/>          | <span data-ttu-id="19655-117">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="19655-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="19655-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="19655-118">Structure Content</span></span>

<span data-ttu-id="19655-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="19655-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="19655-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="19655-120">Structure Properties</span></span>

<span data-ttu-id="19655-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="19655-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="19655-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19655-122">Property</span></span>                | <span data-ttu-id="19655-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="19655-123">xsi:type</span></span>           | <span data-ttu-id="19655-124">Value</span><span class="sxs-lookup"><span data-stu-id="19655-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="19655-125">DataType</span><span class="sxs-lookup"><span data-stu-id="19655-125">DataType</span></span><br/>     | <span data-ttu-id="19655-126">string</span><span class="sxs-lookup"><span data-stu-id="19655-126">string</span></span><br/>  | <span data-ttu-id="19655-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="19655-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="19655-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="19655-128">DefaultValue</span></span><br/> | <span data-ttu-id="19655-129">integer</span><span class="sxs-lookup"><span data-stu-id="19655-129">integer</span></span><br/> | <span data-ttu-id="19655-130">no definido</span><span class="sxs-lookup"><span data-stu-id="19655-130">undefined</span></span><br/>       |
| <span data-ttu-id="19655-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="19655-131">MaxValue</span></span><br/>     | <span data-ttu-id="19655-132">integer</span><span class="sxs-lookup"><span data-stu-id="19655-132">integer</span></span><br/> | <span data-ttu-id="19655-133">no definido</span><span class="sxs-lookup"><span data-stu-id="19655-133">undefined</span></span><br/>       |
| <span data-ttu-id="19655-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="19655-134">MinValue</span></span><br/>     | <span data-ttu-id="19655-135">integer</span><span class="sxs-lookup"><span data-stu-id="19655-135">integer</span></span><br/> | <span data-ttu-id="19655-136">no definido</span><span class="sxs-lookup"><span data-stu-id="19655-136">undefined</span></span><br/>       |
| <span data-ttu-id="19655-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="19655-137">Mandatory</span></span><br/>    | <span data-ttu-id="19655-138">string</span><span class="sxs-lookup"><span data-stu-id="19655-138">string</span></span><br/>  | <span data-ttu-id="19655-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="19655-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="19655-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="19655-140">Multiple</span></span><br/>     | <span data-ttu-id="19655-141">integer</span><span class="sxs-lookup"><span data-stu-id="19655-141">integer</span></span><br/> | <span data-ttu-id="19655-142">1</span><span class="sxs-lookup"><span data-stu-id="19655-142">1</span></span><br/>               |
| <span data-ttu-id="19655-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="19655-143">UnitType</span></span><br/>     | <span data-ttu-id="19655-144">string</span><span class="sxs-lookup"><span data-stu-id="19655-144">string</span></span><br/>  | <span data-ttu-id="19655-145">microns</span><span class="sxs-lookup"><span data-stu-id="19655-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="19655-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19655-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19655-147">Especificación de formato de archivo de descripción de impresora PostScript</span><span class="sxs-lookup"><span data-stu-id="19655-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="19655-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="19655-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




