---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1f72e667f3de3bce86beb1c65c5fde4ebc8669
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361956"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="296bd-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="296bd-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="296bd-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="296bd-105">This topic is not current.</span></span> <span data-ttu-id="296bd-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="296bd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="296bd-107">Especifica la dirección MediaSizeWidth de la dimensión para la opción MediaSize personalizada.</span><span class="sxs-lookup"><span data-stu-id="296bd-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="296bd-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="296bd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="296bd-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="296bd-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="296bd-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="296bd-110">Element Information</span></span>



| <span data-ttu-id="296bd-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="296bd-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="296bd-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="296bd-112">Element Type</span></span> <br/>   | <span data-ttu-id="296bd-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="296bd-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="296bd-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="296bd-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="296bd-115">Página</span><span class="sxs-lookup"><span data-stu-id="296bd-115">Page</span></span><br/>                                           |
| <span data-ttu-id="296bd-116">Notas</span><span class="sxs-lookup"><span data-stu-id="296bd-116">Notes</span></span> <br/>          | <span data-ttu-id="296bd-117">Vinculado a elemento PageMediaSize, opción personalizada</span><span class="sxs-lookup"><span data-stu-id="296bd-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="296bd-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="296bd-118">Structure Content</span></span>

<span data-ttu-id="296bd-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="296bd-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="296bd-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="296bd-120">Structure Properties</span></span>

<span data-ttu-id="296bd-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="296bd-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="296bd-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="296bd-122">Property</span></span>                | <span data-ttu-id="296bd-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="296bd-123">xsi:type</span></span>           | <span data-ttu-id="296bd-124">Value</span><span class="sxs-lookup"><span data-stu-id="296bd-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="296bd-125">DataType</span><span class="sxs-lookup"><span data-stu-id="296bd-125">DataType</span></span><br/>     | <span data-ttu-id="296bd-126">string</span><span class="sxs-lookup"><span data-stu-id="296bd-126">string</span></span><br/>  | <span data-ttu-id="296bd-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="296bd-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="296bd-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="296bd-128">DefaultValue</span></span><br/> | <span data-ttu-id="296bd-129">integer</span><span class="sxs-lookup"><span data-stu-id="296bd-129">integer</span></span><br/> | <span data-ttu-id="296bd-130">no definido</span><span class="sxs-lookup"><span data-stu-id="296bd-130">undefined</span></span><br/>       |
| <span data-ttu-id="296bd-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="296bd-131">MaxValue</span></span><br/>     | <span data-ttu-id="296bd-132">integer</span><span class="sxs-lookup"><span data-stu-id="296bd-132">integer</span></span><br/> | <span data-ttu-id="296bd-133">no definido</span><span class="sxs-lookup"><span data-stu-id="296bd-133">undefined</span></span><br/>       |
| <span data-ttu-id="296bd-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="296bd-134">MinValue</span></span><br/>     | <span data-ttu-id="296bd-135">integer</span><span class="sxs-lookup"><span data-stu-id="296bd-135">integer</span></span><br/> | <span data-ttu-id="296bd-136">no definido</span><span class="sxs-lookup"><span data-stu-id="296bd-136">undefined</span></span><br/>       |
| <span data-ttu-id="296bd-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="296bd-137">Mandatory</span></span><br/>    | <span data-ttu-id="296bd-138">string</span><span class="sxs-lookup"><span data-stu-id="296bd-138">string</span></span><br/>  | <span data-ttu-id="296bd-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="296bd-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="296bd-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="296bd-140">Multiple</span></span><br/>     | <span data-ttu-id="296bd-141">integer</span><span class="sxs-lookup"><span data-stu-id="296bd-141">integer</span></span><br/> | <span data-ttu-id="296bd-142">1</span><span class="sxs-lookup"><span data-stu-id="296bd-142">1</span></span><br/>               |
| <span data-ttu-id="296bd-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="296bd-143">UnitType</span></span><br/>     | <span data-ttu-id="296bd-144">string</span><span class="sxs-lookup"><span data-stu-id="296bd-144">string</span></span><br/>  | <span data-ttu-id="296bd-145">microns</span><span class="sxs-lookup"><span data-stu-id="296bd-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="296bd-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="296bd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="296bd-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="296bd-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




