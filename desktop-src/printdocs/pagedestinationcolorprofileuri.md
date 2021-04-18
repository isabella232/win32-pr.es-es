---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fff2ca269eaed9331f6c2077e6b396cca5a01c4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707627"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="58277-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="58277-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="58277-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="58277-105">This topic is not current.</span></span> <span data-ttu-id="58277-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="58277-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="58277-107">Especifica una referencia de URI relativa a un perfil de ICC incluido en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="58277-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="58277-108">El procesamiento de esta opción depende del valor de la característica PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="58277-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="58277-109">Se supone que todos los elementos que usan ese perfil ya están en el espacio de colores del dispositivo adecuado y no se administrarán en color en el controlador o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58277-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="58277-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="58277-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="58277-111">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="58277-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="58277-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="58277-112">Element Information</span></span>



| <span data-ttu-id="58277-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="58277-113">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="58277-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="58277-114">Element Type</span></span> <br/>   | <span data-ttu-id="58277-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="58277-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="58277-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="58277-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="58277-117">Página</span><span class="sxs-lookup"><span data-stu-id="58277-117">Page</span></span><br/>                                          |
| <span data-ttu-id="58277-118">Notas</span><span class="sxs-lookup"><span data-stu-id="58277-118">Notes</span></span> <br/>          | <span data-ttu-id="58277-119">Vinculado al elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="58277-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="58277-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="58277-120">Structure Content</span></span>

<span data-ttu-id="58277-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="58277-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="58277-122">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="58277-122">Structure Properties</span></span>

<span data-ttu-id="58277-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="58277-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="58277-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="58277-124">Property</span></span>                | <span data-ttu-id="58277-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="58277-125">xsi:type</span></span>           | <span data-ttu-id="58277-126">Value</span><span class="sxs-lookup"><span data-stu-id="58277-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="58277-127">DataType</span><span class="sxs-lookup"><span data-stu-id="58277-127">DataType</span></span><br/>     | <span data-ttu-id="58277-128">string</span><span class="sxs-lookup"><span data-stu-id="58277-128">string</span></span><br/>  | <span data-ttu-id="58277-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="58277-129">xs:string</span></span><br/>       |
| <span data-ttu-id="58277-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="58277-130">DefaultValue</span></span><br/> | <span data-ttu-id="58277-131">string</span><span class="sxs-lookup"><span data-stu-id="58277-131">string</span></span><br/>  | <span data-ttu-id="58277-132">no definido</span><span class="sxs-lookup"><span data-stu-id="58277-132">undefined</span></span><br/>       |
| <span data-ttu-id="58277-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="58277-133">MaxLength</span></span><br/>    | <span data-ttu-id="58277-134">integer</span><span class="sxs-lookup"><span data-stu-id="58277-134">integer</span></span><br/> | <span data-ttu-id="58277-135">no definido</span><span class="sxs-lookup"><span data-stu-id="58277-135">undefined</span></span><br/>       |
| <span data-ttu-id="58277-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="58277-136">MinLength</span></span><br/>    | <span data-ttu-id="58277-137">integer</span><span class="sxs-lookup"><span data-stu-id="58277-137">integer</span></span><br/> | <span data-ttu-id="58277-138">1</span><span class="sxs-lookup"><span data-stu-id="58277-138">1</span></span><br/>               |
| <span data-ttu-id="58277-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="58277-139">Mandatory</span></span><br/>    | <span data-ttu-id="58277-140">string</span><span class="sxs-lookup"><span data-stu-id="58277-140">string</span></span><br/>  | <span data-ttu-id="58277-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="58277-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="58277-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="58277-142">UnitType</span></span><br/>     | <span data-ttu-id="58277-143">string</span><span class="sxs-lookup"><span data-stu-id="58277-143">string</span></span><br/>  | <span data-ttu-id="58277-144">caracteres</span><span class="sxs-lookup"><span data-stu-id="58277-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="58277-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58277-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58277-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="58277-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




