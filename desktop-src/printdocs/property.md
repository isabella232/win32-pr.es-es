---
description: Obtenga información sobre el elemento Property en documentos e impresión. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propiedad (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120300"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="78704-105">Propiedad (documentos e impresión)</span><span class="sxs-lookup"><span data-stu-id="78704-105">Property (Documents and Printing)</span></span>

<span data-ttu-id="78704-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="78704-106">This topic is not current.</span></span> <span data-ttu-id="78704-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="78704-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="78704-108">Un elemento Property declara un dispositivo, un formato de trabajo u otra propiedad pertinente cuyo nombre se proporciona mediante su atributo name.</span><span class="sxs-lookup"><span data-stu-id="78704-108">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="78704-109">Se usa un elemento Value para asignar un valor a la propiedad .</span><span class="sxs-lookup"><span data-stu-id="78704-109">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="78704-110">Una propiedad puede ser compleja, posiblemente que contenga varias subpropiedades.</span><span class="sxs-lookup"><span data-stu-id="78704-110">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="78704-111">Las subpropiedades también se representan mediante elementos Property.</span><span class="sxs-lookup"><span data-stu-id="78704-111">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="78704-112">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="78704-112">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="78704-113">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="78704-113">XML Attributes</span></span>

<span data-ttu-id="78704-114">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="78704-114">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="78704-115">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="78704-115">XML Attribute</span></span>   | <span data-ttu-id="78704-116">Detalles</span><span class="sxs-lookup"><span data-stu-id="78704-116">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78704-117">name</span><span class="sxs-lookup"><span data-stu-id="78704-117">name</span></span><br/> | <span data-ttu-id="78704-118">Contiene el atributo name de la propiedad , que es una propiedad estándar o una propiedad definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="78704-118">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="78704-119">Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="78704-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="78704-120">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="78704-120">Element Information</span></span>

<span data-ttu-id="78704-121">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="78704-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="78704-122">Category</span><span class="sxs-lookup"><span data-stu-id="78704-122">Category</span></span>                   | <span data-ttu-id="78704-123">Detalles</span><span class="sxs-lookup"><span data-stu-id="78704-123">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78704-124">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="78704-124">Parent elements</span></span><br/> | <span data-ttu-id="78704-125">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="78704-125">PrintCapabilities</span></span> <br/> <span data-ttu-id="78704-126">Característica</span><span class="sxs-lookup"><span data-stu-id="78704-126">Feature</span></span><br/> <span data-ttu-id="78704-127">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="78704-127">PrintTicket</span></span><br/> <span data-ttu-id="78704-128">Opción</span><span class="sxs-lookup"><span data-stu-id="78704-128">Option</span></span><br/> <span data-ttu-id="78704-129">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="78704-129">ParameterDef</span></span><br/> <span data-ttu-id="78704-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78704-130">Property</span></span><br/> <span data-ttu-id="78704-131">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="78704-131">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="78704-132">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="78704-132">Child elements</span></span><br/>  | <span data-ttu-id="78704-133">El sistema no asigna ninguna importancia a la ordenación de los elementos.</span><span class="sxs-lookup"><span data-stu-id="78704-133">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="78704-134">Si los clientes deciden atribuir cierta importancia en el orden de los elementos, pueden hacerlo libremente.</span><span class="sxs-lookup"><span data-stu-id="78704-134">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="78704-135">*Valor* de propiedad (uno o *más)* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="78704-135">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="78704-136">or</span><span class="sxs-lookup"><span data-stu-id="78704-136">or</span></span> <br/> <span data-ttu-id="78704-137">*Valor* de propiedad (cero o *más)* (uno o más)</span><span class="sxs-lookup"><span data-stu-id="78704-137">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="78704-138">Este elemento</span><span class="sxs-lookup"><span data-stu-id="78704-138">This element</span></span><br/>    | <span data-ttu-id="78704-139">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="78704-139">No character data is permitted.</span></span><br/> <span data-ttu-id="78704-140">Se permiten elementos value secundarios duplicados que son elementos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="78704-140">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="78704-141">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="78704-141">Configuration Dependencies</span></span>

<span data-ttu-id="78704-142">Una propiedad puede tener dependencias de configuración, excepto cuando aparece dentro de un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="78704-142">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="78704-143">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="78704-143">Element Usage</span></span>

<span data-ttu-id="78704-144">Además de aparecer en los elementos Feature y Option, los elementos Property pueden aparecer en el nivel raíz de las tecnologías subyacentes respectivas.</span><span class="sxs-lookup"><span data-stu-id="78704-144">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="78704-145">El esquema de impresión define un conjunto de elementos Property que se pueden usar para describir un dispositivo de una manera portátil.</span><span class="sxs-lookup"><span data-stu-id="78704-145">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="78704-146">Sin embargo, si estas propiedades no son suficientes para sus necesidades como proveedor printCapabilities (normalmente porque el dispositivo que se admite tiene aspectos nuevos no previstos por el esquema de impresión), puede introducir sus propios elementos property privados.</span><span class="sxs-lookup"><span data-stu-id="78704-146">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="78704-147">Puede mejorar o elaborar la información proporcionada por una propiedad pública agregando una o varias subpropiedades privadas como contenido de elemento de la propiedad pública.</span><span class="sxs-lookup"><span data-stu-id="78704-147">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="78704-148">Los elementos de propiedad se definen mediante una etiqueta de elemento XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="78704-148">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="78704-149">A cada propiedad se le asigna un nombre por medio de su atributo name.</span><span class="sxs-lookup"><span data-stu-id="78704-149">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="78704-150">El nombre debe ser un QName XML y debe cumplir la Convención de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="78704-150">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="78704-151">Para obtener más información, vea [Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="78704-151">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="78704-152">El atributo Nombre de propiedad y su ubicación dentro de la jerarquía de elementos Property primarios (si es una subpropiedad) identifican de forma única la propiedad dentro del documento PrintCapabilities o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="78704-152">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="78704-153">Una propiedad puede contener uno o varios elementos Value, uno o varios elementos Property secundarios (denominados subpropiedades) o una combinación de ambos.</span><span class="sxs-lookup"><span data-stu-id="78704-153">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="78704-154">Las subpropiedades son útiles cuando la propiedad se compone de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="78704-154">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="78704-155">Por ejemplo, una propiedad "ConsumableColor" podría tener componentes "C", "M" e "Y".</span><span class="sxs-lookup"><span data-stu-id="78704-155">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="78704-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78704-156">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="78704-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78704-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78704-158">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="78704-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




