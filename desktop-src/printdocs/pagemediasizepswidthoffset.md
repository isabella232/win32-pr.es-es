---
description: Obtenga información sobre el parámetro PageMediaSizePSWidthOffset. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549113"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="7770d-105">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="7770d-105">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="7770d-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="7770d-106">This topic is not current.</span></span> <span data-ttu-id="7770d-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7770d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7770d-108">Especifica el desplazamiento hasta la dirección de orientación de la fuente (Referencia [PostScript especificación de formato de archivo de](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)descripción de impresora ).</span><span class="sxs-lookup"><span data-stu-id="7770d-108">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="7770d-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7770d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7770d-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7770d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7770d-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7770d-111">Element Information</span></span>



| <span data-ttu-id="7770d-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="7770d-112">Name</span></span> | <span data-ttu-id="7770d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7770d-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7770d-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7770d-114">Element Type</span></span> <br/>   | <span data-ttu-id="7770d-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7770d-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="7770d-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="7770d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7770d-117">Página</span><span class="sxs-lookup"><span data-stu-id="7770d-117">Page</span></span><br/>                                             |
| <span data-ttu-id="7770d-118">Notas</span><span class="sxs-lookup"><span data-stu-id="7770d-118">Notes</span></span> <br/>          | <span data-ttu-id="7770d-119">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="7770d-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7770d-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="7770d-120">Structure Content</span></span>

<span data-ttu-id="7770d-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="7770d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="7770d-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="7770d-122">Structure Properties</span></span>

<span data-ttu-id="7770d-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="7770d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7770d-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7770d-124">Property</span></span>                | <span data-ttu-id="7770d-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7770d-125">xsi:type</span></span>           | <span data-ttu-id="7770d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7770d-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7770d-127">DataType</span><span class="sxs-lookup"><span data-stu-id="7770d-127">DataType</span></span><br/>     | <span data-ttu-id="7770d-128">string</span><span class="sxs-lookup"><span data-stu-id="7770d-128">string</span></span><br/>  | <span data-ttu-id="7770d-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7770d-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="7770d-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7770d-130">DefaultValue</span></span><br/> | <span data-ttu-id="7770d-131">integer</span><span class="sxs-lookup"><span data-stu-id="7770d-131">integer</span></span><br/> | <span data-ttu-id="7770d-132">no definido</span><span class="sxs-lookup"><span data-stu-id="7770d-132">undefined</span></span><br/>       |
| <span data-ttu-id="7770d-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7770d-133">MaxValue</span></span><br/>     | <span data-ttu-id="7770d-134">integer</span><span class="sxs-lookup"><span data-stu-id="7770d-134">integer</span></span><br/> | <span data-ttu-id="7770d-135">no definido</span><span class="sxs-lookup"><span data-stu-id="7770d-135">undefined</span></span><br/>       |
| <span data-ttu-id="7770d-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="7770d-136">MinValue</span></span><br/>     | <span data-ttu-id="7770d-137">integer</span><span class="sxs-lookup"><span data-stu-id="7770d-137">integer</span></span><br/> | <span data-ttu-id="7770d-138">no definido</span><span class="sxs-lookup"><span data-stu-id="7770d-138">undefined</span></span><br/>       |
| <span data-ttu-id="7770d-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="7770d-139">Mandatory</span></span><br/>    | <span data-ttu-id="7770d-140">string</span><span class="sxs-lookup"><span data-stu-id="7770d-140">string</span></span><br/>  | <span data-ttu-id="7770d-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7770d-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7770d-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="7770d-142">Multiple</span></span><br/>     | <span data-ttu-id="7770d-143">integer</span><span class="sxs-lookup"><span data-stu-id="7770d-143">integer</span></span><br/> | <span data-ttu-id="7770d-144">1</span><span class="sxs-lookup"><span data-stu-id="7770d-144">1</span></span><br/>               |
| <span data-ttu-id="7770d-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="7770d-145">UnitType</span></span><br/>     | <span data-ttu-id="7770d-146">string</span><span class="sxs-lookup"><span data-stu-id="7770d-146">string</span></span><br/>  | <span data-ttu-id="7770d-147">Micras</span><span class="sxs-lookup"><span data-stu-id="7770d-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7770d-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7770d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7770d-149">PostScript Especificación de formato de archivo de descripción de impresora</span><span class="sxs-lookup"><span data-stu-id="7770d-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="7770d-150">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="7770d-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




