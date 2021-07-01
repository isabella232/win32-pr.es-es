---
description: Busque información sobre el elemento ScoredProperty. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119120"
---
# <a name="scoredproperty"></a><span data-ttu-id="c136a-105">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="c136a-105">ScoredProperty</span></span>

<span data-ttu-id="c136a-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="c136a-106">This topic is not current.</span></span> <span data-ttu-id="c136a-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c136a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c136a-108">Un elemento ScoredProperty declara una propiedad intrínseca a una definición de opción.</span><span class="sxs-lookup"><span data-stu-id="c136a-108">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="c136a-109">Estas propiedades se deben comparar al evaluar la coincidencia de una opción solicitada con una opción compatible con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c136a-109">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="c136a-110">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="c136a-110">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="c136a-111">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="c136a-111">XML Attributes</span></span>

<span data-ttu-id="c136a-112">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="c136a-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="c136a-113">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="c136a-113">XML Attribute</span></span>   | <span data-ttu-id="c136a-114">Detalles</span><span class="sxs-lookup"><span data-stu-id="c136a-114">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c136a-115">name</span><span class="sxs-lookup"><span data-stu-id="c136a-115">name</span></span><br/> | <span data-ttu-id="c136a-116">Contiene el atributo name de ScoredProperty, ya sea una propiedad estándar o una propiedad definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="c136a-116">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="c136a-117">Para más información, consulte la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="c136a-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="c136a-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c136a-118">Element Information</span></span>

<span data-ttu-id="c136a-119">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="c136a-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="c136a-120">Category</span><span class="sxs-lookup"><span data-stu-id="c136a-120">Category</span></span>                   | <span data-ttu-id="c136a-121">Detalles</span><span class="sxs-lookup"><span data-stu-id="c136a-121">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c136a-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="c136a-122">Parent elements</span></span><br/> | <span data-ttu-id="c136a-123">*Opción*</span><span class="sxs-lookup"><span data-stu-id="c136a-123">*Option*</span></span><br/> <span data-ttu-id="c136a-124">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="c136a-124">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="c136a-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c136a-125">Child elements</span></span><br/>  | <span data-ttu-id="c136a-126">Es posible usar el</span><span class="sxs-lookup"><span data-stu-id="c136a-126">Either</span></span><br/> <span data-ttu-id="c136a-127">*ParameterRef* (uno)</span><span class="sxs-lookup"><span data-stu-id="c136a-127">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="c136a-128">or</span><span class="sxs-lookup"><span data-stu-id="c136a-128">or</span></span><br/> <span data-ttu-id="c136a-129">*Valor* (uno)</span><span class="sxs-lookup"><span data-stu-id="c136a-129">*Value* (one)</span></span><br/> <span data-ttu-id="c136a-130">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="c136a-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="c136a-131">*ScoredProperty* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="c136a-131">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="c136a-132">Este elemento</span><span class="sxs-lookup"><span data-stu-id="c136a-132">This element</span></span><br/>    | <span data-ttu-id="c136a-133">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c136a-133">No character data is permitted.</span></span><br/> <span data-ttu-id="c136a-134">No se permiten elementos secundarios duplicados relacionados.</span><span class="sxs-lookup"><span data-stu-id="c136a-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="c136a-135">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="c136a-135">Configuration Dependencies</span></span>

<span data-ttu-id="c136a-136">Es posible que un elemento ScoredProperty no tenga dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="c136a-136">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="c136a-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c136a-137">Example</span></span>

<span data-ttu-id="c136a-138">Declare un elemento ScoredProperty denominado MediaSizeWidth con un valor de 11.</span><span class="sxs-lookup"><span data-stu-id="c136a-138">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="c136a-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c136a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c136a-140">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c136a-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




