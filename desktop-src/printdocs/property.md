---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propiedad (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361972"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="1e9d1-104">Propiedad (documentos e impresión)</span><span class="sxs-lookup"><span data-stu-id="1e9d1-104">Property (Documents and Printing)</span></span>

<span data-ttu-id="1e9d1-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-105">This topic is not current.</span></span> <span data-ttu-id="1e9d1-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1e9d1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1e9d1-107">Un elemento Property declara un dispositivo, un formato de trabajo u otra propiedad pertinente cuyo nombre se proporciona mediante su atributo name.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-107">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="1e9d1-108">Un elemento Value se utiliza para asignar un valor a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-108">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="1e9d1-109">Una propiedad puede ser compleja, posiblemente con varias subpropiedades.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-109">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="1e9d1-110">Las subpropiedades también se representan mediante elementos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-110">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="1e9d1-111">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="1e9d1-111">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="1e9d1-112">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="1e9d1-112">XML Attributes</span></span>

<span data-ttu-id="1e9d1-113">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-113">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="1e9d1-114">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="1e9d1-114">XML Attribute</span></span>   | <span data-ttu-id="1e9d1-115">Detalles</span><span class="sxs-lookup"><span data-stu-id="1e9d1-115">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9d1-116">name</span><span class="sxs-lookup"><span data-stu-id="1e9d1-116">name</span></span><br/> | <span data-ttu-id="1e9d1-117">Contiene el atributo de nombre de la propiedad, que es una propiedad estándar o una propiedad definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-117">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="1e9d1-118">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="1e9d1-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="1e9d1-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1e9d1-119">Element Information</span></span>

<span data-ttu-id="1e9d1-120">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="1e9d1-121">Category</span><span class="sxs-lookup"><span data-stu-id="1e9d1-121">Category</span></span>                   | <span data-ttu-id="1e9d1-122">Detalles</span><span class="sxs-lookup"><span data-stu-id="1e9d1-122">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9d1-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1e9d1-123">Parent elements</span></span><br/> | <span data-ttu-id="1e9d1-124">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="1e9d1-124">PrintCapabilities</span></span> <br/> <span data-ttu-id="1e9d1-125">Característica</span><span class="sxs-lookup"><span data-stu-id="1e9d1-125">Feature</span></span><br/> <span data-ttu-id="1e9d1-126">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="1e9d1-126">PrintTicket</span></span><br/> <span data-ttu-id="1e9d1-127">Opción</span><span class="sxs-lookup"><span data-stu-id="1e9d1-127">Option</span></span><br/> <span data-ttu-id="1e9d1-128">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1e9d1-128">ParameterDef</span></span><br/> <span data-ttu-id="1e9d1-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e9d1-129">Property</span></span><br/> <span data-ttu-id="1e9d1-130">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="1e9d1-130">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="1e9d1-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1e9d1-131">Child elements</span></span><br/>  | <span data-ttu-id="1e9d1-132">El sistema no asigna importancia al orden de los elementos.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-132">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="1e9d1-133">Si los clientes optan por tener alguna importancia en el orden de los elementos, pueden hacerlo de forma gratuita.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-133">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="1e9d1-134">*Propiedad* (uno o varios *valores* ) (cero o más)</span><span class="sxs-lookup"><span data-stu-id="1e9d1-134">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="1e9d1-135">or</span><span class="sxs-lookup"><span data-stu-id="1e9d1-135">or</span></span> <br/> <span data-ttu-id="1e9d1-136">*Propiedad* (cero o más) *valor* (uno o varios)</span><span class="sxs-lookup"><span data-stu-id="1e9d1-136">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="1e9d1-137">Este elemento</span><span class="sxs-lookup"><span data-stu-id="1e9d1-137">This element</span></span><br/>    | <span data-ttu-id="1e9d1-138">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-138">No character data is permitted.</span></span><br/> <span data-ttu-id="1e9d1-139">Se permiten elementos de valor secundario duplicados que son del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-139">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="1e9d1-140">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="1e9d1-140">Configuration Dependencies</span></span>

<span data-ttu-id="1e9d1-141">Una propiedad puede tener dependencias de configuración, excepto cuando aparece dentro de un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-141">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="1e9d1-142">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="1e9d1-142">Element Usage</span></span>

<span data-ttu-id="1e9d1-143">Además de aparecer en elementos de características y opciones, los elementos de propiedad pueden aparecer en el nivel raíz de las tecnologías subyacentes respectivas.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-143">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="1e9d1-144">El esquema de impresión define un conjunto de elementos de propiedad que se pueden usar para describir un dispositivo de manera portátil.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-144">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="1e9d1-145">Sin embargo, si estas propiedades no son suficientes para sus necesidades como un proveedor de PrintCapabilities (normalmente porque el dispositivo que se está admitiendo tiene aspectos nuevos no previstos por el esquema de impresión), puede introducir sus propios elementos de propiedad privados.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-145">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="1e9d1-146">Puede mejorar o elaborar la información proporcionada por una propiedad pública agregando una o más subpropiedades privadas como contenido del elemento de la propiedad pública.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-146">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="1e9d1-147">Los elementos de propiedad se definen mediante una etiqueta de elemento XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="1e9d1-147">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="1e9d1-148">A cada propiedad se le asigna un nombre por medio de su atributo name.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-148">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="1e9d1-149">El nombre debe ser un QName XML y debe ajustarse a la Convención de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-149">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="1e9d1-150">Para obtener más información, consulte [atributos XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1e9d1-150">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="1e9d1-151">El atributo de nombre de propiedad y su ubicación dentro de la jerarquía de elementos de propiedad primarios (si es una subpropiedad) identifican de forma única la propiedad dentro del documento PrintCapabilities o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-151">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="1e9d1-152">Una propiedad puede contener uno o más elementos de valor, o uno o varios elementos de propiedad secundarios (denominados subpropiedades) o una combinación de ambos.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-152">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="1e9d1-153">Las subpropiedades son útiles cuando la propiedad se compone de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-153">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="1e9d1-154">Por ejemplo, una propiedad "ConsumableColor" podría tener los componentes "C", "M" y "Y".</span><span class="sxs-lookup"><span data-stu-id="1e9d1-154">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="1e9d1-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e9d1-155">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="1e9d1-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e9d1-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e9d1-157">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1e9d1-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




