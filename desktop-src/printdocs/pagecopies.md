---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6feef0745e3f9a86b3697b7e0ab65111fc3dfcb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279871"
---
# <a name="pagecopies"></a><span data-ttu-id="fbf27-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="fbf27-104">PageCopies</span></span>

<span data-ttu-id="fbf27-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="fbf27-105">This topic is not current.</span></span> <span data-ttu-id="fbf27-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fbf27-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fbf27-107">Especifica el número de copias de una página.</span><span class="sxs-lookup"><span data-stu-id="fbf27-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="fbf27-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fbf27-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fbf27-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="fbf27-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fbf27-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fbf27-110">Element Information</span></span>



| <span data-ttu-id="fbf27-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbf27-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="fbf27-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="fbf27-112">Element Type</span></span> <br/>   | <span data-ttu-id="fbf27-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fbf27-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="fbf27-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="fbf27-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fbf27-115">Página</span><span class="sxs-lookup"><span data-stu-id="fbf27-115">Page</span></span><br/>         |
| <span data-ttu-id="fbf27-116">Notas</span><span class="sxs-lookup"><span data-stu-id="fbf27-116">Notes</span></span> <br/>          | <span data-ttu-id="fbf27-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fbf27-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="fbf27-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="fbf27-118">Structure Content</span></span>

<span data-ttu-id="fbf27-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="fbf27-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="fbf27-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="fbf27-120">Structure Properties</span></span>

<span data-ttu-id="fbf27-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="fbf27-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fbf27-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbf27-122">Property</span></span>                | <span data-ttu-id="fbf27-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fbf27-123">xsi:type</span></span>           | <span data-ttu-id="fbf27-124">Value</span><span class="sxs-lookup"><span data-stu-id="fbf27-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="fbf27-125">DataType</span><span class="sxs-lookup"><span data-stu-id="fbf27-125">DataType</span></span><br/>     | <span data-ttu-id="fbf27-126">string</span><span class="sxs-lookup"><span data-stu-id="fbf27-126">string</span></span><br/>  | <span data-ttu-id="fbf27-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fbf27-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="fbf27-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fbf27-128">DefaultValue</span></span><br/> | <span data-ttu-id="fbf27-129">integer</span><span class="sxs-lookup"><span data-stu-id="fbf27-129">integer</span></span><br/> | <span data-ttu-id="fbf27-130">1</span><span class="sxs-lookup"><span data-stu-id="fbf27-130">1</span></span><br/>                 |
| <span data-ttu-id="fbf27-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fbf27-131">MaxValue</span></span><br/>     | <span data-ttu-id="fbf27-132">integer</span><span class="sxs-lookup"><span data-stu-id="fbf27-132">integer</span></span><br/> | <span data-ttu-id="fbf27-133">no definido</span><span class="sxs-lookup"><span data-stu-id="fbf27-133">undefined</span></span><br/>         |
| <span data-ttu-id="fbf27-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="fbf27-134">MinValue</span></span><br/>     | <span data-ttu-id="fbf27-135">integer</span><span class="sxs-lookup"><span data-stu-id="fbf27-135">integer</span></span><br/> | <span data-ttu-id="fbf27-136">1</span><span class="sxs-lookup"><span data-stu-id="fbf27-136">1</span></span><br/>                 |
| <span data-ttu-id="fbf27-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="fbf27-137">Mandatory</span></span><br/>    | <span data-ttu-id="fbf27-138">string</span><span class="sxs-lookup"><span data-stu-id="fbf27-138">string</span></span><br/>  | <span data-ttu-id="fbf27-139">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="fbf27-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="fbf27-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="fbf27-140">Multiple</span></span><br/>     | <span data-ttu-id="fbf27-141">integer</span><span class="sxs-lookup"><span data-stu-id="fbf27-141">integer</span></span><br/> | <span data-ttu-id="fbf27-142">1</span><span class="sxs-lookup"><span data-stu-id="fbf27-142">1</span></span><br/>                 |
| <span data-ttu-id="fbf27-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="fbf27-143">UnitType</span></span><br/>     | <span data-ttu-id="fbf27-144">string</span><span class="sxs-lookup"><span data-stu-id="fbf27-144">string</span></span><br/>  | <span data-ttu-id="fbf27-145">instantánea</span><span class="sxs-lookup"><span data-stu-id="fbf27-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="fbf27-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fbf27-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbf27-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="fbf27-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




