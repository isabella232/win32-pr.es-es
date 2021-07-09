---
description: Obtenga información sobre el parámetro PageBlendColorSpaceICCProfileURI. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db89757737ff5aa6a1358af418ee33809b960e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549323"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="38db3-105">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="38db3-105">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="38db3-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="38db3-106">This topic is not current.</span></span> <span data-ttu-id="38db3-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="38db3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="38db3-108">Especifica una referencia de URI relativa a un perfil DE CIA que define el espacio de color que se debe usar para la combinación.</span><span class="sxs-lookup"><span data-stu-id="38db3-108">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="38db3-109">es <Uri> un nombre de elemento absoluto relativo a la raíz del \_ paquete.</span><span class="sxs-lookup"><span data-stu-id="38db3-109">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="38db3-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="38db3-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="38db3-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="38db3-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="38db3-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="38db3-112">Element Information</span></span>



| <span data-ttu-id="38db3-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="38db3-113">Name</span></span> | <span data-ttu-id="38db3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="38db3-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38db3-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="38db3-115">Element Type</span></span> <br/>   | <span data-ttu-id="38db3-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="38db3-116">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="38db3-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="38db3-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="38db3-118">Página</span><span class="sxs-lookup"><span data-stu-id="38db3-118">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="38db3-119">Notas</span><span class="sxs-lookup"><span data-stu-id="38db3-119">Notes</span></span> <br/>          | <span data-ttu-id="38db3-120">Esto solo se aplica a los documentos XPS y no se debe usar en PrintTickets arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="38db3-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="38db3-121">Vinculado al elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="38db3-121">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="38db3-122">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="38db3-122">Structure Content</span></span>

<span data-ttu-id="38db3-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="38db3-123">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="38db3-124">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="38db3-124">Structure Properties</span></span>

<span data-ttu-id="38db3-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="38db3-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="38db3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38db3-126">Property</span></span>                | <span data-ttu-id="38db3-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="38db3-127">xsi:type</span></span>           | <span data-ttu-id="38db3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="38db3-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="38db3-129">DataType</span><span class="sxs-lookup"><span data-stu-id="38db3-129">DataType</span></span><br/>     | <span data-ttu-id="38db3-130">string</span><span class="sxs-lookup"><span data-stu-id="38db3-130">string</span></span><br/>  | <span data-ttu-id="38db3-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="38db3-131">xs:string</span></span><br/>       |
| <span data-ttu-id="38db3-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="38db3-132">DefaultValue</span></span><br/> | <span data-ttu-id="38db3-133">string</span><span class="sxs-lookup"><span data-stu-id="38db3-133">string</span></span><br/>  | <span data-ttu-id="38db3-134">no definido</span><span class="sxs-lookup"><span data-stu-id="38db3-134">undefined</span></span><br/>       |
| <span data-ttu-id="38db3-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="38db3-135">MaxLength</span></span><br/>    | <span data-ttu-id="38db3-136">integer</span><span class="sxs-lookup"><span data-stu-id="38db3-136">integer</span></span><br/> | <span data-ttu-id="38db3-137">no definido</span><span class="sxs-lookup"><span data-stu-id="38db3-137">undefined</span></span><br/>       |
| <span data-ttu-id="38db3-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="38db3-138">MinLength</span></span><br/>    | <span data-ttu-id="38db3-139">integer</span><span class="sxs-lookup"><span data-stu-id="38db3-139">integer</span></span><br/> | <span data-ttu-id="38db3-140">1</span><span class="sxs-lookup"><span data-stu-id="38db3-140">1</span></span><br/>               |
| <span data-ttu-id="38db3-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="38db3-141">Mandatory</span></span><br/>    | <span data-ttu-id="38db3-142">string</span><span class="sxs-lookup"><span data-stu-id="38db3-142">string</span></span><br/>  | <span data-ttu-id="38db3-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="38db3-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="38db3-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="38db3-144">UnitType</span></span><br/>     | <span data-ttu-id="38db3-145">string</span><span class="sxs-lookup"><span data-stu-id="38db3-145">string</span></span><br/>  | <span data-ttu-id="38db3-146">caracteres</span><span class="sxs-lookup"><span data-stu-id="38db3-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="38db3-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38db3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38db3-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="38db3-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




