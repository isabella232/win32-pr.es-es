---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a6143bd934ebcb75c3e5455a30c7365f1a89
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083611"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="08d34-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="08d34-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="08d34-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="08d34-105">This topic is not current.</span></span> <span data-ttu-id="08d34-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="08d34-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="08d34-107">Especifica una referencia de URI relativa a un perfil de ICC que define el espacio de colores que se debe usar para la combinación.</span><span class="sxs-lookup"><span data-stu-id="08d34-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="08d34-108"><Uri>Es un nombre de parte absoluta \_ relativo a la raíz del paquete.</span><span class="sxs-lookup"><span data-stu-id="08d34-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="08d34-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="08d34-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="08d34-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="08d34-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="08d34-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="08d34-111">Element Information</span></span>



| <span data-ttu-id="08d34-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="08d34-112">Name</span></span>                       |                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d34-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="08d34-113">Element Type</span></span> <br/>   | <span data-ttu-id="08d34-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="08d34-114">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="08d34-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="08d34-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="08d34-116">Página</span><span class="sxs-lookup"><span data-stu-id="08d34-116">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="08d34-117">Notas</span><span class="sxs-lookup"><span data-stu-id="08d34-117">Notes</span></span> <br/>          | <span data-ttu-id="08d34-118">Esto se aplica a los documentos XPS únicamente y no se debe usar en elementos PrintTicket arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="08d34-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="08d34-119">Vinculado al elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="08d34-119">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="08d34-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="08d34-120">Structure Content</span></span>

<span data-ttu-id="08d34-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="08d34-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="08d34-122">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="08d34-122">Structure Properties</span></span>

<span data-ttu-id="08d34-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="08d34-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="08d34-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="08d34-124">Property</span></span>                | <span data-ttu-id="08d34-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="08d34-125">xsi:type</span></span>           | <span data-ttu-id="08d34-126">Value</span><span class="sxs-lookup"><span data-stu-id="08d34-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="08d34-127">DataType</span><span class="sxs-lookup"><span data-stu-id="08d34-127">DataType</span></span><br/>     | <span data-ttu-id="08d34-128">string</span><span class="sxs-lookup"><span data-stu-id="08d34-128">string</span></span><br/>  | <span data-ttu-id="08d34-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="08d34-129">xs:string</span></span><br/>       |
| <span data-ttu-id="08d34-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="08d34-130">DefaultValue</span></span><br/> | <span data-ttu-id="08d34-131">string</span><span class="sxs-lookup"><span data-stu-id="08d34-131">string</span></span><br/>  | <span data-ttu-id="08d34-132">no definido</span><span class="sxs-lookup"><span data-stu-id="08d34-132">undefined</span></span><br/>       |
| <span data-ttu-id="08d34-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="08d34-133">MaxLength</span></span><br/>    | <span data-ttu-id="08d34-134">integer</span><span class="sxs-lookup"><span data-stu-id="08d34-134">integer</span></span><br/> | <span data-ttu-id="08d34-135">no definido</span><span class="sxs-lookup"><span data-stu-id="08d34-135">undefined</span></span><br/>       |
| <span data-ttu-id="08d34-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="08d34-136">MinLength</span></span><br/>    | <span data-ttu-id="08d34-137">integer</span><span class="sxs-lookup"><span data-stu-id="08d34-137">integer</span></span><br/> | <span data-ttu-id="08d34-138">1</span><span class="sxs-lookup"><span data-stu-id="08d34-138">1</span></span><br/>               |
| <span data-ttu-id="08d34-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="08d34-139">Mandatory</span></span><br/>    | <span data-ttu-id="08d34-140">string</span><span class="sxs-lookup"><span data-stu-id="08d34-140">string</span></span><br/>  | <span data-ttu-id="08d34-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="08d34-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="08d34-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="08d34-142">UnitType</span></span><br/>     | <span data-ttu-id="08d34-143">string</span><span class="sxs-lookup"><span data-stu-id="08d34-143">string</span></span><br/>  | <span data-ttu-id="08d34-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="08d34-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="08d34-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08d34-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d34-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="08d34-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




