---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Value
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105653129"
---
# <a name="value"></a><span data-ttu-id="a474c-104">Value</span><span class="sxs-lookup"><span data-stu-id="a474c-104">Value</span></span>

<span data-ttu-id="a474c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="a474c-105">This topic is not current.</span></span> <span data-ttu-id="a474c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a474c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a474c-107">Un elemento de valor asocia un literal a un tipo.</span><span class="sxs-lookup"><span data-stu-id="a474c-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="a474c-108">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="a474c-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="a474c-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="a474c-109">XML Attributes</span></span>

<span data-ttu-id="a474c-110">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="a474c-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="a474c-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="a474c-111">XML Attribute</span></span>       | <span data-ttu-id="a474c-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="a474c-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a474c-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a474c-113">xsi:type</span></span><br/> | <span data-ttu-id="a474c-114">Especifica el tipo de datos de Value, que debe ser uno de los siguientes tipos definidos por XSD: String, integer, decimal, QName.</span><span class="sxs-lookup"><span data-stu-id="a474c-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="a474c-115">Si falta, el tipo de datos predeterminado es String.</span><span class="sxs-lookup"><span data-stu-id="a474c-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="a474c-116">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="a474c-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="a474c-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a474c-117">Element Information</span></span>

<span data-ttu-id="a474c-118">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="a474c-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="a474c-119">Category</span><span class="sxs-lookup"><span data-stu-id="a474c-119">Category</span></span>                   | <span data-ttu-id="a474c-120">Detalles</span><span class="sxs-lookup"><span data-stu-id="a474c-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a474c-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a474c-121">Parent elements</span></span><br/> | <span data-ttu-id="a474c-122">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="a474c-122">ParameterInit</span></span> <br/> <span data-ttu-id="a474c-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a474c-123">Property</span></span><br/> <span data-ttu-id="a474c-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="a474c-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="a474c-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a474c-125">Child elements</span></span><br/>  | <span data-ttu-id="a474c-126">Solo se permite el contenido de caracteres o enteros.</span><span class="sxs-lookup"><span data-stu-id="a474c-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="a474c-127">Este elemento</span><span class="sxs-lookup"><span data-stu-id="a474c-127">This element</span></span><br/>    | <span data-ttu-id="a474c-128">Se permite el contenido null.</span><span class="sxs-lookup"><span data-stu-id="a474c-128">Null content is allowed.</span></span> <span data-ttu-id="a474c-129">El contenido de los caracteres debe ajustarse a la sintaxis definida por el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a474c-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="a474c-130">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="a474c-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="a474c-131">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="a474c-131">Configuration Dependencies</span></span>

<span data-ttu-id="a474c-132">Los elementos de valor que aparecen en el elemento ScoredProperty no pueden tener dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="a474c-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="a474c-133">Los elementos de valor que aparecen dentro de los elementos de propiedad pueden tener dependencias arbitrarias en la configuración.</span><span class="sxs-lookup"><span data-stu-id="a474c-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="a474c-134">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="a474c-134">Element Usage</span></span>

<span data-ttu-id="a474c-135">Un elemento de valor puede aparecer dentro de una propiedad o un elemento ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="a474c-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="a474c-136">El propósito del elemento Value es representar un valor como un tipo de datos XML estándar.</span><span class="sxs-lookup"><span data-stu-id="a474c-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="a474c-137">El tipo de datos se especifica como un atributo XML del elemento Value, xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="a474c-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="a474c-138">Tenga en cuenta que no se admiten todos los tipos definidos por XSD o definidos por XML.</span><span class="sxs-lookup"><span data-stu-id="a474c-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="a474c-139">Para obtener una lista de los tipos admitidos, vea [Resumen de tipos de elementos](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="a474c-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="a474c-140">Un elemento de valor solo puede contener contenido de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a474c-140">A Value element can contain only character content.</span></span> <span data-ttu-id="a474c-141">Nada más puede aparecer como contenido en un elemento de valor.</span><span class="sxs-lookup"><span data-stu-id="a474c-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="a474c-142">Algunos elementos ScoredProperty y de propiedad definidos por el esquema de impresión no contienen un elemento de valor, porque su finalidad es simplemente ser elementos primarios de subpropiedades.</span><span class="sxs-lookup"><span data-stu-id="a474c-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="a474c-143">No debe agregar un elemento de valor a tales propiedades, como las propiedades que no contienen un elemento de valor.</span><span class="sxs-lookup"><span data-stu-id="a474c-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="a474c-144">Para cumplir con el marco de trabajo del esquema de impresión, que requiere que haya un elemento de valor o subelementos en los elementos que admiten valores, se debe representar un valor ausente o indefinido presentando el elemento de valor como un elemento vacío. es decir, como</span><span class="sxs-lookup"><span data-stu-id="a474c-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="a474c-145">.</span><span class="sxs-lookup"><span data-stu-id="a474c-145">.</span></span>

## <a name="example"></a><span data-ttu-id="a474c-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a474c-146">Example</span></span>

<span data-ttu-id="a474c-147">Defina un valor de tipo decimal e Inicialícelo en "128,5".</span><span class="sxs-lookup"><span data-stu-id="a474c-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="a474c-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a474c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a474c-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="a474c-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




