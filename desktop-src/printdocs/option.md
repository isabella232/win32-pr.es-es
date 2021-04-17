---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717429"
---
# <a name="option"></a><span data-ttu-id="972dd-104">Opción</span><span class="sxs-lookup"><span data-stu-id="972dd-104">Option</span></span>

<span data-ttu-id="972dd-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="972dd-105">This topic is not current.</span></span> <span data-ttu-id="972dd-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="972dd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="972dd-107">Un elemento OPTION contiene todos los elementos Property y ScoredProperty asociados a esta opción.</span><span class="sxs-lookup"><span data-stu-id="972dd-107">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="972dd-108">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="972dd-108">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="972dd-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="972dd-109">XML Attributes</span></span>

<span data-ttu-id="972dd-110">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="972dd-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="972dd-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="972dd-111">XML Attribute</span></span>          | <span data-ttu-id="972dd-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="972dd-112">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="972dd-113">restringida</span><span class="sxs-lookup"><span data-stu-id="972dd-113">constrained</span></span><br/> | <span data-ttu-id="972dd-114">Este atributo es opcional para un documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="972dd-114">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="972dd-115">Este atributo indica si la opción está disponible para la selección o el uso.</span><span class="sxs-lookup"><span data-stu-id="972dd-115">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="972dd-116">Este atributo XML se puede establecer en uno de los siguientes valores: None, PrintTicketSettings, AdminSetting o DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="972dd-116">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="972dd-117">Vea [atributos XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="972dd-117">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="972dd-118">name</span><span class="sxs-lookup"><span data-stu-id="972dd-118">name</span></span><br/>        | <span data-ttu-id="972dd-119">Contiene el nombre de la opción, ya sea una opción estándar o una opción definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="972dd-119">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="972dd-120">El atributo XML se utiliza de esta manera para diferenciar entre las instancias de opción.</span><span class="sxs-lookup"><span data-stu-id="972dd-120">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="972dd-121">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="972dd-121">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="972dd-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="972dd-122">Element Information</span></span>

<span data-ttu-id="972dd-123">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="972dd-123">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="972dd-124">Category</span><span class="sxs-lookup"><span data-stu-id="972dd-124">Category</span></span>                   | <span data-ttu-id="972dd-125">Detalles</span><span class="sxs-lookup"><span data-stu-id="972dd-125">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="972dd-126">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="972dd-126">Parent elements</span></span><br/> | <span data-ttu-id="972dd-127">Característica</span><span class="sxs-lookup"><span data-stu-id="972dd-127">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="972dd-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="972dd-128">Child elements</span></span><br/>  | <span data-ttu-id="972dd-129">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="972dd-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="972dd-130">*ScoredProperty* (cero o más para las opciones con el atributo XML ' name '; una o más para las opciones que no usan el atributo XML ' name ' \* )</span><span class="sxs-lookup"><span data-stu-id="972dd-130">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="972dd-131">\* solo las opciones públicas definidas en el esquema de impresión no pueden tener ningún atributo ' name ', como DocumentNUp)</span><span class="sxs-lookup"><span data-stu-id="972dd-131">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="972dd-132">Este elemento</span><span class="sxs-lookup"><span data-stu-id="972dd-132">This element</span></span><br/>    | <span data-ttu-id="972dd-133">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="972dd-133">No character data is permitted.</span></span><br/> <span data-ttu-id="972dd-134">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="972dd-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="972dd-135">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="972dd-135">Configuration Dependencies</span></span>

<span data-ttu-id="972dd-136">Un elemento de definición de opción no puede tener ninguna dependencia de configuración.</span><span class="sxs-lookup"><span data-stu-id="972dd-136">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="972dd-137">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="972dd-137">Element Usage</span></span>

<span data-ttu-id="972dd-138">El propósito del elemento OPTION es caracterizar uno de los Estados que puede asumir un atributo de configuración de dispositivo, representado por un elemento de característica.</span><span class="sxs-lookup"><span data-stu-id="972dd-138">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="972dd-139">Cada definición de elemento de opción contiene uno o más elementos ScoredProperty que describen la característica intrínseca o esencial de esa opción.</span><span class="sxs-lookup"><span data-stu-id="972dd-139">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="972dd-140">Para facilitar la portabilidad y la preservación de la intención, el esquema de impresión define muchos elementos de características comunes y una variedad de elementos de opción para cada característica.</span><span class="sxs-lookup"><span data-stu-id="972dd-140">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="972dd-141">Por lo tanto, es importante usar elementos de opción de impresión definidos por el esquema, si es posible, antes de crear sus propias definiciones de opciones.</span><span class="sxs-lookup"><span data-stu-id="972dd-141">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="972dd-142">Entender el proceso de definición de los elementos de opción proporciona información útil sobre la manera en que se usan el documento y elementos PrintTicket de PrintCapabilities en la arquitectura de impresión de Microsoft .NET Framework 3,0 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="972dd-142">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="972dd-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="972dd-143">Example</span></span>

<span data-ttu-id="972dd-144">En el ejemplo siguiente se define un nombre para la opción.</span><span class="sxs-lookup"><span data-stu-id="972dd-144">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="972dd-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="972dd-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="972dd-146">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="972dd-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




