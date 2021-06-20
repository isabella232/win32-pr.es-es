---
description: Obtenga información sobre el elemento Value, que asocia un literal a un tipo. El tipo de datos de Value debe ser string, integer, decimal o QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272bee4d7a5f88899f83e439d8e1630b4026713d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405988"
---
# <a name="value"></a><span data-ttu-id="91357-104">Valor</span><span class="sxs-lookup"><span data-stu-id="91357-104">Value</span></span>

<span data-ttu-id="91357-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="91357-105">This topic is not current.</span></span> <span data-ttu-id="91357-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="91357-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="91357-107">Un elemento Value asocia un literal a un tipo.</span><span class="sxs-lookup"><span data-stu-id="91357-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="91357-108">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="91357-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="91357-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="91357-109">XML Attributes</span></span>

<span data-ttu-id="91357-110">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="91357-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="91357-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="91357-111">XML Attribute</span></span>       | <span data-ttu-id="91357-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="91357-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91357-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="91357-113">xsi:type</span></span><br/> | <span data-ttu-id="91357-114">Especifica el tipo de datos value, que debe ser uno de los siguientes tipos definidos por XSD: cadena, entero, decimal, QName.</span><span class="sxs-lookup"><span data-stu-id="91357-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="91357-115">Si falta, el tipo de datos predeterminado es string.</span><span class="sxs-lookup"><span data-stu-id="91357-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="91357-116">Para más información, consulte la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="91357-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="91357-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="91357-117">Element Information</span></span>

<span data-ttu-id="91357-118">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="91357-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="91357-119">Category</span><span class="sxs-lookup"><span data-stu-id="91357-119">Category</span></span>                   | <span data-ttu-id="91357-120">Detalles</span><span class="sxs-lookup"><span data-stu-id="91357-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91357-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="91357-121">Parent elements</span></span><br/> | <span data-ttu-id="91357-122">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="91357-122">ParameterInit</span></span> <br/> <span data-ttu-id="91357-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="91357-123">Property</span></span><br/> <span data-ttu-id="91357-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="91357-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="91357-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="91357-125">Child elements</span></span><br/>  | <span data-ttu-id="91357-126">Solo se permite el contenido de caracteres o enteros.</span><span class="sxs-lookup"><span data-stu-id="91357-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="91357-127">Este elemento</span><span class="sxs-lookup"><span data-stu-id="91357-127">This element</span></span><br/>    | <span data-ttu-id="91357-128">Se permite el contenido NULL.</span><span class="sxs-lookup"><span data-stu-id="91357-128">Null content is allowed.</span></span> <span data-ttu-id="91357-129">El contenido de caracteres debe ajustarse a la sintaxis definida por el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="91357-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="91357-130">No se permiten elementos secundarios duplicados relacionados.</span><span class="sxs-lookup"><span data-stu-id="91357-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="91357-131">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="91357-131">Configuration Dependencies</span></span>

<span data-ttu-id="91357-132">Es posible que los elementos de valor que aparecen en el elemento ScoredProperty no tengan dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="91357-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="91357-133">Los elementos de valor que aparecen en los elementos Property pueden tener dependencias arbitrarias en la configuración.</span><span class="sxs-lookup"><span data-stu-id="91357-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="91357-134">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="91357-134">Element Usage</span></span>

<span data-ttu-id="91357-135">Un elemento Value puede aparecer dentro de un elemento Property o ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="91357-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="91357-136">El propósito del elemento Value es representar un valor como un tipo de datos XML estándar.</span><span class="sxs-lookup"><span data-stu-id="91357-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="91357-137">El tipo de datos se especifica como un atributo XML del elemento Value, xsi:type.</span><span class="sxs-lookup"><span data-stu-id="91357-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="91357-138">Tenga en cuenta que no se admiten todos los tipos definidos por XSD o XML.</span><span class="sxs-lookup"><span data-stu-id="91357-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="91357-139">Para obtener una lista de los tipos admitidos, [vea Resumen de tipos de elementos](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="91357-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="91357-140">Un elemento Value solo puede contener contenido de caracteres.</span><span class="sxs-lookup"><span data-stu-id="91357-140">A Value element can contain only character content.</span></span> <span data-ttu-id="91357-141">No puede aparecer nada más como contenido en un elemento Value.</span><span class="sxs-lookup"><span data-stu-id="91357-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="91357-142">Algunos elementos Print Schema-defined Property y ScoredProperty no contienen un elemento Value, porque su finalidad es simplemente ser elementos primarios de subpropiedades.</span><span class="sxs-lookup"><span data-stu-id="91357-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="91357-143">No debe agregar un elemento Value a propiedades como estas, propiedades que no contienen un elemento Value.</span><span class="sxs-lookup"><span data-stu-id="91357-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="91357-144">Para cumplir con el marco de esquema de impresión, que requiere que un elemento Value o subelementos esté presente en los elementos que admiten valores, se debe representar un valor ausente o no definido mediante la presentación del elemento Value como un elemento vacío; es decir, como</span><span class="sxs-lookup"><span data-stu-id="91357-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="91357-145">.</span><span class="sxs-lookup"><span data-stu-id="91357-145">.</span></span>

## <a name="example"></a><span data-ttu-id="91357-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91357-146">Example</span></span>

<span data-ttu-id="91357-147">Defina un valor de tipo decimal e inicialízcalo en "128.5".</span><span class="sxs-lookup"><span data-stu-id="91357-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="91357-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91357-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91357-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="91357-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




