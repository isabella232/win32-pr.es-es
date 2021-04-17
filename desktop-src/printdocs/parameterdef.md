---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698004"
---
# <a name="parameterdef"></a><span data-ttu-id="73dd0-104">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="73dd0-104">ParameterDef</span></span>

<span data-ttu-id="73dd0-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="73dd0-105">This topic is not current.</span></span> <span data-ttu-id="73dd0-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="73dd0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="73dd0-107">Un elemento ParameterDef define las características válidas de la entrada de parámetros.</span><span class="sxs-lookup"><span data-stu-id="73dd0-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="73dd0-108">El valor se especifica por medio de un elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="73dd0-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="73dd0-109">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="73dd0-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="73dd0-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="73dd0-110">XML Attributes</span></span>

<span data-ttu-id="73dd0-111">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="73dd0-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="73dd0-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="73dd0-112">XML Attribute</span></span>   | <span data-ttu-id="73dd0-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="73dd0-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73dd0-114">name</span><span class="sxs-lookup"><span data-stu-id="73dd0-114">name</span></span><br/> | <span data-ttu-id="73dd0-115">Define un nombre único para el parámetro en el contexto del documento actual.</span><span class="sxs-lookup"><span data-stu-id="73dd0-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="73dd0-116">Los atributos de nombre de ParameterDef duplicados representan el documento de PrintCapabilities no válido.</span><span class="sxs-lookup"><span data-stu-id="73dd0-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="73dd0-117">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="73dd0-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="73dd0-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="73dd0-118">Element Information</span></span>

<span data-ttu-id="73dd0-119">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="73dd0-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73dd0-120">Category</span><span class="sxs-lookup"><span data-stu-id="73dd0-120">Category</span></span></th>
<th><span data-ttu-id="73dd0-121">Detalles</span><span class="sxs-lookup"><span data-stu-id="73dd0-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73dd0-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="73dd0-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="73dd0-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="73dd0-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73dd0-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="73dd0-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="73dd0-125">Property (uno o varios)</span><span class="sxs-lookup"><span data-stu-id="73dd0-125">Property (one or more)</span></span><br/> <span data-ttu-id="73dd0-126">Los siguientes elementos de propiedad estándar deben aparecer como contenido de un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="73dd0-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="73dd0-127">DataType</span><span class="sxs-lookup"><span data-stu-id="73dd0-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="73dd0-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="73dd0-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="73dd0-129">Mandatory</span><span class="sxs-lookup"><span data-stu-id="73dd0-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="73dd0-130">MaxLength o MaxValue</span><span class="sxs-lookup"><span data-stu-id="73dd0-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="73dd0-131">MinLength o MinValue</span><span class="sxs-lookup"><span data-stu-id="73dd0-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="73dd0-132">Diversos</span><span class="sxs-lookup"><span data-stu-id="73dd0-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="73dd0-133">UnitType</span><span class="sxs-lookup"><span data-stu-id="73dd0-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73dd0-134">Este elemento</span><span class="sxs-lookup"><span data-stu-id="73dd0-134">This element</span></span><br/></td>
<td><span data-ttu-id="73dd0-135">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="73dd0-135">No character data is permitted.</span></span><br/> <span data-ttu-id="73dd0-136">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="73dd0-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="73dd0-137">\*Obligatorio cuando DataType es un valor entero o decimal.</span><span class="sxs-lookup"><span data-stu-id="73dd0-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="73dd0-138">Opcional cuando DataType es una cadena.</span><span class="sxs-lookup"><span data-stu-id="73dd0-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="73dd0-139">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="73dd0-139">Configuration Dependencies</span></span>

<span data-ttu-id="73dd0-140">Un ParameterDef y su contenido a cualquier nivel de anidamiento no pueden tener dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="73dd0-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="73dd0-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73dd0-141">Example</span></span>

<span data-ttu-id="73dd0-142">En el ejemplo siguiente se establecen todos los elementos de propiedad necesarios para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="73dd0-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="73dd0-143">En el ejemplo de [ParameterInit](parameterinit.md) se muestra cómo inicializar este parámetro.</span><span class="sxs-lookup"><span data-stu-id="73dd0-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a><span data-ttu-id="73dd0-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73dd0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73dd0-145">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="73dd0-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




