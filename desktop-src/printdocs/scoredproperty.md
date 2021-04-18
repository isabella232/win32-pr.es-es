---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721391"
---
# <a name="scoredproperty"></a><span data-ttu-id="8c064-104">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="8c064-104">ScoredProperty</span></span>

<span data-ttu-id="8c064-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="8c064-105">This topic is not current.</span></span> <span data-ttu-id="8c064-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8c064-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8c064-107">Un elemento ScoredProperty declara una propiedad que es intrínseca a una definición de opción.</span><span class="sxs-lookup"><span data-stu-id="8c064-107">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="8c064-108">Estas propiedades se deben comparar al evaluar el grado en que una opción solicitada coincide con una opción admitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c064-108">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="8c064-109">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="8c064-109">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="8c064-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="8c064-110">XML Attributes</span></span>

<span data-ttu-id="8c064-111">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="8c064-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="8c064-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="8c064-112">XML Attribute</span></span>   | <span data-ttu-id="8c064-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="8c064-113">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c064-114">name</span><span class="sxs-lookup"><span data-stu-id="8c064-114">name</span></span><br/> | <span data-ttu-id="8c064-115">Contiene el atributo de nombre del ScoredProperty, ya sea una propiedad estándar o una propiedad definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="8c064-115">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="8c064-116">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="8c064-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="8c064-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8c064-117">Element Information</span></span>

<span data-ttu-id="8c064-118">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="8c064-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="8c064-119">Category</span><span class="sxs-lookup"><span data-stu-id="8c064-119">Category</span></span>                   | <span data-ttu-id="8c064-120">Detalles</span><span class="sxs-lookup"><span data-stu-id="8c064-120">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c064-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8c064-121">Parent elements</span></span><br/> | <span data-ttu-id="8c064-122">*Opción*</span><span class="sxs-lookup"><span data-stu-id="8c064-122">*Option*</span></span><br/> <span data-ttu-id="8c064-123">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="8c064-123">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="8c064-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c064-124">Child elements</span></span><br/>  | <span data-ttu-id="8c064-125">Es posible usar el</span><span class="sxs-lookup"><span data-stu-id="8c064-125">Either</span></span><br/> <span data-ttu-id="8c064-126">*ParameterRef* (uno)</span><span class="sxs-lookup"><span data-stu-id="8c064-126">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="8c064-127">or</span><span class="sxs-lookup"><span data-stu-id="8c064-127">or</span></span><br/> <span data-ttu-id="8c064-128">*Valor* (uno)</span><span class="sxs-lookup"><span data-stu-id="8c064-128">*Value* (one)</span></span><br/> <span data-ttu-id="8c064-129">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="8c064-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="8c064-130">*ScoredProperty* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="8c064-130">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="8c064-131">Este elemento</span><span class="sxs-lookup"><span data-stu-id="8c064-131">This element</span></span><br/>    | <span data-ttu-id="8c064-132">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8c064-132">No character data is permitted.</span></span><br/> <span data-ttu-id="8c064-133">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="8c064-133">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="8c064-134">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="8c064-134">Configuration Dependencies</span></span>

<span data-ttu-id="8c064-135">Un elemento ScoredProperty no puede tener dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="8c064-135">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="8c064-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c064-136">Example</span></span>

<span data-ttu-id="8c064-137">Declare un elemento ScoredProperty denominado MediaSizeWidth con un valor de 11.</span><span class="sxs-lookup"><span data-stu-id="8c064-137">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="8c064-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c064-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c064-139">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="8c064-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




