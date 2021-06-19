---
description: Obtenga información sobre el parámetro PageDestinationColorProfileURI. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3cf719a97f8f8086e88425c1667199815efbbb
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396680"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="60e00-105">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="60e00-105">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="60e00-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="60e00-106">This topic is not current.</span></span> <span data-ttu-id="60e00-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="60e00-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="60e00-108">Especifica una referencia de URI relativa a un perfil DEERT incluido en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="60e00-108">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="60e00-109">El procesamiento de esta opción depende de la configuración de la característica PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="60e00-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="60e00-110">Se supone que todos los elementos que usan ese perfil ya están en el espacio de color del dispositivo adecuado y no se administrarán por colores en el controlador o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60e00-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="60e00-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="60e00-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="60e00-112">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="60e00-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="60e00-113">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="60e00-113">Element Information</span></span>



| <span data-ttu-id="60e00-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="60e00-114">Name</span></span> | <span data-ttu-id="60e00-115">Valor</span><span class="sxs-lookup"><span data-stu-id="60e00-115">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="60e00-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="60e00-116">Element Type</span></span> <br/>   | <span data-ttu-id="60e00-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="60e00-117">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="60e00-118">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="60e00-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="60e00-119">Página</span><span class="sxs-lookup"><span data-stu-id="60e00-119">Page</span></span><br/>                                          |
| <span data-ttu-id="60e00-120">Notas</span><span class="sxs-lookup"><span data-stu-id="60e00-120">Notes</span></span> <br/>          | <span data-ttu-id="60e00-121">Vinculado al elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="60e00-121">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="60e00-122">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="60e00-122">Structure Content</span></span>

<span data-ttu-id="60e00-123">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="60e00-123">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="60e00-124">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="60e00-124">Structure Properties</span></span>

<span data-ttu-id="60e00-125">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="60e00-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="60e00-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60e00-126">Property</span></span>                | <span data-ttu-id="60e00-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="60e00-127">xsi:type</span></span>           | <span data-ttu-id="60e00-128">Valor</span><span class="sxs-lookup"><span data-stu-id="60e00-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="60e00-129">DataType</span><span class="sxs-lookup"><span data-stu-id="60e00-129">DataType</span></span><br/>     | <span data-ttu-id="60e00-130">string</span><span class="sxs-lookup"><span data-stu-id="60e00-130">string</span></span><br/>  | <span data-ttu-id="60e00-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="60e00-131">xs:string</span></span><br/>       |
| <span data-ttu-id="60e00-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="60e00-132">DefaultValue</span></span><br/> | <span data-ttu-id="60e00-133">string</span><span class="sxs-lookup"><span data-stu-id="60e00-133">string</span></span><br/>  | <span data-ttu-id="60e00-134">no definido</span><span class="sxs-lookup"><span data-stu-id="60e00-134">undefined</span></span><br/>       |
| <span data-ttu-id="60e00-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="60e00-135">MaxLength</span></span><br/>    | <span data-ttu-id="60e00-136">integer</span><span class="sxs-lookup"><span data-stu-id="60e00-136">integer</span></span><br/> | <span data-ttu-id="60e00-137">no definido</span><span class="sxs-lookup"><span data-stu-id="60e00-137">undefined</span></span><br/>       |
| <span data-ttu-id="60e00-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="60e00-138">MinLength</span></span><br/>    | <span data-ttu-id="60e00-139">integer</span><span class="sxs-lookup"><span data-stu-id="60e00-139">integer</span></span><br/> | <span data-ttu-id="60e00-140">1</span><span class="sxs-lookup"><span data-stu-id="60e00-140">1</span></span><br/>               |
| <span data-ttu-id="60e00-141">Mandatory</span><span class="sxs-lookup"><span data-stu-id="60e00-141">Mandatory</span></span><br/>    | <span data-ttu-id="60e00-142">string</span><span class="sxs-lookup"><span data-stu-id="60e00-142">string</span></span><br/>  | <span data-ttu-id="60e00-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="60e00-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="60e00-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="60e00-144">UnitType</span></span><br/>     | <span data-ttu-id="60e00-145">string</span><span class="sxs-lookup"><span data-stu-id="60e00-145">string</span></span><br/>  | <span data-ttu-id="60e00-146">caracteres</span><span class="sxs-lookup"><span data-stu-id="60e00-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="60e00-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60e00-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60e00-148">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="60e00-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




