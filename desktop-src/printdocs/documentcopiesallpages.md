---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723242ddd127113b573f167e6902b27fcca9665a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993992"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="5a78a-104">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="5a78a-104">DocumentCopiesAllPages</span></span>

<span data-ttu-id="5a78a-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="5a78a-105">This topic is not current.</span></span> <span data-ttu-id="5a78a-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a78a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a78a-107">Especifica el número de copias de un documento.</span><span class="sxs-lookup"><span data-stu-id="5a78a-107">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="5a78a-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5a78a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5a78a-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5a78a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5a78a-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5a78a-110">Element Information</span></span>



| <span data-ttu-id="5a78a-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="5a78a-111">Name</span></span> | <span data-ttu-id="5a78a-112">Value</span><span class="sxs-lookup"><span data-stu-id="5a78a-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="5a78a-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5a78a-113">Element Type</span></span> <br/>   | <span data-ttu-id="5a78a-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5a78a-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="5a78a-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5a78a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5a78a-116">Documento</span><span class="sxs-lookup"><span data-stu-id="5a78a-116">Document</span></span><br/>     |
| <span data-ttu-id="5a78a-117">Notas</span><span class="sxs-lookup"><span data-stu-id="5a78a-117">Notes</span></span> <br/>          | <span data-ttu-id="5a78a-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5a78a-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="5a78a-119">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5a78a-119">Structure Content</span></span>

<span data-ttu-id="5a78a-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5a78a-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
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

## <a name="structure-properties"></a><span data-ttu-id="5a78a-121">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="5a78a-121">Structure Properties</span></span>

<span data-ttu-id="5a78a-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5a78a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5a78a-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a78a-123">Property</span></span>                | <span data-ttu-id="5a78a-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5a78a-124">xsi:type</span></span>           | <span data-ttu-id="5a78a-125">Value</span><span class="sxs-lookup"><span data-stu-id="5a78a-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="5a78a-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5a78a-126">DataType</span></span><br/>     | <span data-ttu-id="5a78a-127">string</span><span class="sxs-lookup"><span data-stu-id="5a78a-127">string</span></span><br/>  | <span data-ttu-id="5a78a-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a78a-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="5a78a-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5a78a-129">DefaultValue</span></span><br/> | <span data-ttu-id="5a78a-130">integer</span><span class="sxs-lookup"><span data-stu-id="5a78a-130">integer</span></span><br/> | <span data-ttu-id="5a78a-131">1</span><span class="sxs-lookup"><span data-stu-id="5a78a-131">1</span></span><br/>                 |
| <span data-ttu-id="5a78a-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5a78a-132">MaxValue</span></span><br/>     | <span data-ttu-id="5a78a-133">integer</span><span class="sxs-lookup"><span data-stu-id="5a78a-133">integer</span></span><br/> | <span data-ttu-id="5a78a-134">no definido</span><span class="sxs-lookup"><span data-stu-id="5a78a-134">undefined</span></span><br/>         |
| <span data-ttu-id="5a78a-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="5a78a-135">MinValue</span></span><br/>     | <span data-ttu-id="5a78a-136">integer</span><span class="sxs-lookup"><span data-stu-id="5a78a-136">integer</span></span><br/> | <span data-ttu-id="5a78a-137">1</span><span class="sxs-lookup"><span data-stu-id="5a78a-137">1</span></span><br/>                 |
| <span data-ttu-id="5a78a-138">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5a78a-138">Mandatory</span></span><br/>    | <span data-ttu-id="5a78a-139">string</span><span class="sxs-lookup"><span data-stu-id="5a78a-139">string</span></span><br/>  | <span data-ttu-id="5a78a-140">psk:Unconditional</span><span class="sxs-lookup"><span data-stu-id="5a78a-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="5a78a-141">Múltiple</span><span class="sxs-lookup"><span data-stu-id="5a78a-141">Multiple</span></span><br/>     | <span data-ttu-id="5a78a-142">integer</span><span class="sxs-lookup"><span data-stu-id="5a78a-142">integer</span></span><br/> | <span data-ttu-id="5a78a-143">1</span><span class="sxs-lookup"><span data-stu-id="5a78a-143">1</span></span><br/>                 |
| <span data-ttu-id="5a78a-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="5a78a-144">UnitType</span></span><br/>     | <span data-ttu-id="5a78a-145">string</span><span class="sxs-lookup"><span data-stu-id="5a78a-145">string</span></span><br/>  | <span data-ttu-id="5a78a-146">Copias</span><span class="sxs-lookup"><span data-stu-id="5a78a-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="5a78a-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a78a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a78a-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5a78a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




