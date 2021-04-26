---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b321cba1608b1098dcc91f3800ef11f4968fb3f2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996102"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="2a799-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="2a799-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="2a799-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="2a799-105">This topic is not current.</span></span> <span data-ttu-id="2a799-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2a799-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2a799-107">Especifica una referencia de URI relativa a un perfil DEERT incluido en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2a799-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="2a799-108">El procesamiento de esta opción depende de la configuración de la característica PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="2a799-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="2a799-109">Se supone que todos los elementos que usan ese perfil ya están en el espacio de color del dispositivo adecuado y no se administrarán por colores en el controlador o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a799-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="2a799-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2a799-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2a799-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2a799-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2a799-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2a799-112">Element Information</span></span>



| <span data-ttu-id="2a799-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a799-113">Name</span></span> | <span data-ttu-id="2a799-114">Value</span><span class="sxs-lookup"><span data-stu-id="2a799-114">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="2a799-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2a799-115">Element Type</span></span> <br/>   | <span data-ttu-id="2a799-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2a799-116">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="2a799-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="2a799-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2a799-118">Página</span><span class="sxs-lookup"><span data-stu-id="2a799-118">Page</span></span><br/>                                          |
| <span data-ttu-id="2a799-119">Notas</span><span class="sxs-lookup"><span data-stu-id="2a799-119">Notes</span></span> <br/>          | <span data-ttu-id="2a799-120">Vinculado al elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="2a799-120">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2a799-121">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="2a799-121">Structure Content</span></span>

<span data-ttu-id="2a799-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="2a799-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2a799-123">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="2a799-123">Structure Properties</span></span>

<span data-ttu-id="2a799-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="2a799-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2a799-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2a799-125">Property</span></span>                | <span data-ttu-id="2a799-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2a799-126">xsi:type</span></span>           | <span data-ttu-id="2a799-127">Value</span><span class="sxs-lookup"><span data-stu-id="2a799-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2a799-128">DataType</span><span class="sxs-lookup"><span data-stu-id="2a799-128">DataType</span></span><br/>     | <span data-ttu-id="2a799-129">string</span><span class="sxs-lookup"><span data-stu-id="2a799-129">string</span></span><br/>  | <span data-ttu-id="2a799-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="2a799-130">xs:string</span></span><br/>       |
| <span data-ttu-id="2a799-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2a799-131">DefaultValue</span></span><br/> | <span data-ttu-id="2a799-132">string</span><span class="sxs-lookup"><span data-stu-id="2a799-132">string</span></span><br/>  | <span data-ttu-id="2a799-133">no definido</span><span class="sxs-lookup"><span data-stu-id="2a799-133">undefined</span></span><br/>       |
| <span data-ttu-id="2a799-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="2a799-134">MaxLength</span></span><br/>    | <span data-ttu-id="2a799-135">integer</span><span class="sxs-lookup"><span data-stu-id="2a799-135">integer</span></span><br/> | <span data-ttu-id="2a799-136">no definido</span><span class="sxs-lookup"><span data-stu-id="2a799-136">undefined</span></span><br/>       |
| <span data-ttu-id="2a799-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="2a799-137">MinLength</span></span><br/>    | <span data-ttu-id="2a799-138">integer</span><span class="sxs-lookup"><span data-stu-id="2a799-138">integer</span></span><br/> | <span data-ttu-id="2a799-139">1</span><span class="sxs-lookup"><span data-stu-id="2a799-139">1</span></span><br/>               |
| <span data-ttu-id="2a799-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="2a799-140">Mandatory</span></span><br/>    | <span data-ttu-id="2a799-141">string</span><span class="sxs-lookup"><span data-stu-id="2a799-141">string</span></span><br/>  | <span data-ttu-id="2a799-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="2a799-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2a799-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="2a799-143">UnitType</span></span><br/>     | <span data-ttu-id="2a799-144">string</span><span class="sxs-lookup"><span data-stu-id="2a799-144">string</span></span><br/>  | <span data-ttu-id="2a799-145">caracteres</span><span class="sxs-lookup"><span data-stu-id="2a799-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="2a799-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a799-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a799-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="2a799-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




