---
description: Lea información de referencia sobre el parámetro PageCopies. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5002850fa1df5a86b0022a941e3b2a1f7e414a44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396690"
---
# <a name="pagecopies"></a><span data-ttu-id="ff220-105">PageCopies</span><span class="sxs-lookup"><span data-stu-id="ff220-105">PageCopies</span></span>

<span data-ttu-id="ff220-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="ff220-106">This topic is not current.</span></span> <span data-ttu-id="ff220-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ff220-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ff220-108">Especifica el número de copias de una página.</span><span class="sxs-lookup"><span data-stu-id="ff220-108">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="ff220-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ff220-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ff220-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ff220-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ff220-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ff220-111">Element Information</span></span>



| <span data-ttu-id="ff220-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff220-112">Name</span></span> | <span data-ttu-id="ff220-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ff220-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="ff220-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ff220-114">Element Type</span></span> <br/>   | <span data-ttu-id="ff220-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ff220-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="ff220-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="ff220-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ff220-117">Página</span><span class="sxs-lookup"><span data-stu-id="ff220-117">Page</span></span><br/>         |
| <span data-ttu-id="ff220-118">Notas</span><span class="sxs-lookup"><span data-stu-id="ff220-118">Notes</span></span> <br/>          | <span data-ttu-id="ff220-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ff220-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="ff220-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="ff220-120">Structure Content</span></span>

<span data-ttu-id="ff220-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="ff220-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ff220-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="ff220-122">Structure Properties</span></span>

<span data-ttu-id="ff220-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="ff220-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ff220-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff220-124">Property</span></span>                | <span data-ttu-id="ff220-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ff220-125">xsi:type</span></span>           | <span data-ttu-id="ff220-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ff220-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="ff220-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ff220-127">DataType</span></span><br/>     | <span data-ttu-id="ff220-128">string</span><span class="sxs-lookup"><span data-stu-id="ff220-128">string</span></span><br/>  | <span data-ttu-id="ff220-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ff220-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="ff220-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ff220-130">DefaultValue</span></span><br/> | <span data-ttu-id="ff220-131">integer</span><span class="sxs-lookup"><span data-stu-id="ff220-131">integer</span></span><br/> | <span data-ttu-id="ff220-132">1</span><span class="sxs-lookup"><span data-stu-id="ff220-132">1</span></span><br/>                 |
| <span data-ttu-id="ff220-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ff220-133">MaxValue</span></span><br/>     | <span data-ttu-id="ff220-134">integer</span><span class="sxs-lookup"><span data-stu-id="ff220-134">integer</span></span><br/> | <span data-ttu-id="ff220-135">no definido</span><span class="sxs-lookup"><span data-stu-id="ff220-135">undefined</span></span><br/>         |
| <span data-ttu-id="ff220-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="ff220-136">MinValue</span></span><br/>     | <span data-ttu-id="ff220-137">integer</span><span class="sxs-lookup"><span data-stu-id="ff220-137">integer</span></span><br/> | <span data-ttu-id="ff220-138">1</span><span class="sxs-lookup"><span data-stu-id="ff220-138">1</span></span><br/>                 |
| <span data-ttu-id="ff220-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="ff220-139">Mandatory</span></span><br/>    | <span data-ttu-id="ff220-140">string</span><span class="sxs-lookup"><span data-stu-id="ff220-140">string</span></span><br/>  | <span data-ttu-id="ff220-141">psk:Unconditional</span><span class="sxs-lookup"><span data-stu-id="ff220-141">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="ff220-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="ff220-142">Multiple</span></span><br/>     | <span data-ttu-id="ff220-143">integer</span><span class="sxs-lookup"><span data-stu-id="ff220-143">integer</span></span><br/> | <span data-ttu-id="ff220-144">1</span><span class="sxs-lookup"><span data-stu-id="ff220-144">1</span></span><br/>                 |
| <span data-ttu-id="ff220-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="ff220-145">UnitType</span></span><br/>     | <span data-ttu-id="ff220-146">string</span><span class="sxs-lookup"><span data-stu-id="ff220-146">string</span></span><br/>  | <span data-ttu-id="ff220-147">Copias</span><span class="sxs-lookup"><span data-stu-id="ff220-147">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="ff220-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff220-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff220-149">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="ff220-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




