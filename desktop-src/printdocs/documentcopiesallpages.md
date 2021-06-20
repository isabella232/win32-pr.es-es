---
description: Obtenga información sobre el elemento DocumentCopiesAllPages, que especifica el número de copias de un documento.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf82c23b764f3fe1f8257f4cdb2e7fa03374bd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409448"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="4eb14-103">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="4eb14-103">DocumentCopiesAllPages</span></span>

<span data-ttu-id="4eb14-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4eb14-104">This topic is not current.</span></span> <span data-ttu-id="4eb14-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4eb14-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4eb14-106">Especifica el número de copias de un documento.</span><span class="sxs-lookup"><span data-stu-id="4eb14-106">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="4eb14-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4eb14-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4eb14-108">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4eb14-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4eb14-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4eb14-109">Element Information</span></span>



| <span data-ttu-id="4eb14-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="4eb14-110">Name</span></span> | <span data-ttu-id="4eb14-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4eb14-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="4eb14-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4eb14-112">Element Type</span></span> <br/>   | <span data-ttu-id="4eb14-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4eb14-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="4eb14-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="4eb14-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4eb14-115">Documento</span><span class="sxs-lookup"><span data-stu-id="4eb14-115">Document</span></span><br/>     |
| <span data-ttu-id="4eb14-116">Notas</span><span class="sxs-lookup"><span data-stu-id="4eb14-116">Notes</span></span> <br/>          | <span data-ttu-id="4eb14-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4eb14-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="4eb14-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="4eb14-118">Structure Content</span></span>

<span data-ttu-id="4eb14-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="4eb14-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4eb14-120">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="4eb14-120">Structure Properties</span></span>

<span data-ttu-id="4eb14-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="4eb14-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4eb14-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4eb14-122">Property</span></span>                | <span data-ttu-id="4eb14-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4eb14-123">xsi:type</span></span>           | <span data-ttu-id="4eb14-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4eb14-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="4eb14-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4eb14-125">DataType</span></span><br/>     | <span data-ttu-id="4eb14-126">string</span><span class="sxs-lookup"><span data-stu-id="4eb14-126">string</span></span><br/>  | <span data-ttu-id="4eb14-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4eb14-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="4eb14-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4eb14-128">DefaultValue</span></span><br/> | <span data-ttu-id="4eb14-129">integer</span><span class="sxs-lookup"><span data-stu-id="4eb14-129">integer</span></span><br/> | <span data-ttu-id="4eb14-130">1</span><span class="sxs-lookup"><span data-stu-id="4eb14-130">1</span></span><br/>                 |
| <span data-ttu-id="4eb14-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4eb14-131">MaxValue</span></span><br/>     | <span data-ttu-id="4eb14-132">integer</span><span class="sxs-lookup"><span data-stu-id="4eb14-132">integer</span></span><br/> | <span data-ttu-id="4eb14-133">no definido</span><span class="sxs-lookup"><span data-stu-id="4eb14-133">undefined</span></span><br/>         |
| <span data-ttu-id="4eb14-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="4eb14-134">MinValue</span></span><br/>     | <span data-ttu-id="4eb14-135">integer</span><span class="sxs-lookup"><span data-stu-id="4eb14-135">integer</span></span><br/> | <span data-ttu-id="4eb14-136">1</span><span class="sxs-lookup"><span data-stu-id="4eb14-136">1</span></span><br/>                 |
| <span data-ttu-id="4eb14-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="4eb14-137">Mandatory</span></span><br/>    | <span data-ttu-id="4eb14-138">string</span><span class="sxs-lookup"><span data-stu-id="4eb14-138">string</span></span><br/>  | <span data-ttu-id="4eb14-139">psk:Unconditional</span><span class="sxs-lookup"><span data-stu-id="4eb14-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="4eb14-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="4eb14-140">Multiple</span></span><br/>     | <span data-ttu-id="4eb14-141">integer</span><span class="sxs-lookup"><span data-stu-id="4eb14-141">integer</span></span><br/> | <span data-ttu-id="4eb14-142">1</span><span class="sxs-lookup"><span data-stu-id="4eb14-142">1</span></span><br/>                 |
| <span data-ttu-id="4eb14-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="4eb14-143">UnitType</span></span><br/>     | <span data-ttu-id="4eb14-144">string</span><span class="sxs-lookup"><span data-stu-id="4eb14-144">string</span></span><br/>  | <span data-ttu-id="4eb14-145">Copias</span><span class="sxs-lookup"><span data-stu-id="4eb14-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="4eb14-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4eb14-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb14-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4eb14-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




