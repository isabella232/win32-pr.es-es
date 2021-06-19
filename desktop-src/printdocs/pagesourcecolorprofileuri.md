---
description: Obtenga información sobre el parámetro PageSourceColorProfileURI. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b6acd064a6b0652720a6c0d783f10a7467fa16
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395630"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="dafbf-105">PageSourceColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="dafbf-105">PageSourceColorProfileURI</span></span>

<span data-ttu-id="dafbf-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="dafbf-106">This topic is not current.</span></span> <span data-ttu-id="dafbf-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dafbf-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dafbf-108">Especifica el origen del perfil de color.</span><span class="sxs-lookup"><span data-stu-id="dafbf-108">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="dafbf-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dafbf-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dafbf-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dafbf-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dafbf-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dafbf-111">Element Information</span></span>



| <span data-ttu-id="dafbf-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="dafbf-112">Name</span></span> | <span data-ttu-id="dafbf-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dafbf-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="dafbf-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dafbf-114">Element Type</span></span> <br/>   | <span data-ttu-id="dafbf-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dafbf-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="dafbf-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="dafbf-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dafbf-117">Página</span><span class="sxs-lookup"><span data-stu-id="dafbf-117">Page</span></span><br/>                                     |
| <span data-ttu-id="dafbf-118">Notas</span><span class="sxs-lookup"><span data-stu-id="dafbf-118">Notes</span></span> <br/>          | <span data-ttu-id="dafbf-119">Vinculado al elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="dafbf-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dafbf-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="dafbf-120">Structure Content</span></span>

<span data-ttu-id="dafbf-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="dafbf-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="dafbf-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="dafbf-122">Structure Properties</span></span>

<span data-ttu-id="dafbf-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="dafbf-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dafbf-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dafbf-124">Property</span></span>                | <span data-ttu-id="dafbf-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dafbf-125">xsi:type</span></span>           | <span data-ttu-id="dafbf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dafbf-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dafbf-127">DataType</span><span class="sxs-lookup"><span data-stu-id="dafbf-127">DataType</span></span><br/>     | <span data-ttu-id="dafbf-128">string</span><span class="sxs-lookup"><span data-stu-id="dafbf-128">string</span></span><br/>  | <span data-ttu-id="dafbf-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="dafbf-129">xs:string</span></span><br/>       |
| <span data-ttu-id="dafbf-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dafbf-130">DefaultValue</span></span><br/> | <span data-ttu-id="dafbf-131">string</span><span class="sxs-lookup"><span data-stu-id="dafbf-131">string</span></span><br/>  | <span data-ttu-id="dafbf-132">no definido</span><span class="sxs-lookup"><span data-stu-id="dafbf-132">undefined</span></span><br/>       |
| <span data-ttu-id="dafbf-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="dafbf-133">MaxLength</span></span><br/>    | <span data-ttu-id="dafbf-134">integer</span><span class="sxs-lookup"><span data-stu-id="dafbf-134">integer</span></span><br/> | <span data-ttu-id="dafbf-135">no definido</span><span class="sxs-lookup"><span data-stu-id="dafbf-135">undefined</span></span><br/>       |
| <span data-ttu-id="dafbf-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="dafbf-136">MinLength</span></span><br/>    | <span data-ttu-id="dafbf-137">integer</span><span class="sxs-lookup"><span data-stu-id="dafbf-137">integer</span></span><br/> | <span data-ttu-id="dafbf-138">1</span><span class="sxs-lookup"><span data-stu-id="dafbf-138">1</span></span><br/>               |
| <span data-ttu-id="dafbf-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="dafbf-139">Mandatory</span></span><br/>    | <span data-ttu-id="dafbf-140">string</span><span class="sxs-lookup"><span data-stu-id="dafbf-140">string</span></span><br/>  | <span data-ttu-id="dafbf-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="dafbf-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dafbf-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="dafbf-142">UnitType</span></span><br/>     | <span data-ttu-id="dafbf-143">string</span><span class="sxs-lookup"><span data-stu-id="dafbf-143">string</span></span><br/>  | <span data-ttu-id="dafbf-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="dafbf-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="dafbf-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dafbf-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dafbf-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="dafbf-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




