---
description: Obtenga información sobre el elemento Option. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549383"
---
# <a name="option"></a><span data-ttu-id="32846-105">Opción</span><span class="sxs-lookup"><span data-stu-id="32846-105">Option</span></span>

<span data-ttu-id="32846-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="32846-106">This topic is not current.</span></span> <span data-ttu-id="32846-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="32846-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="32846-108">Un elemento Option contiene todos los elementos Property y ScoredProperty asociados a esta opción.</span><span class="sxs-lookup"><span data-stu-id="32846-108">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="32846-109">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="32846-109">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="32846-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="32846-110">XML Attributes</span></span>

<span data-ttu-id="32846-111">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="32846-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="32846-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="32846-112">XML Attribute</span></span>          | <span data-ttu-id="32846-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="32846-113">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32846-114">Limitada</span><span class="sxs-lookup"><span data-stu-id="32846-114">constrained</span></span><br/> | <span data-ttu-id="32846-115">Este atributo es opcional para un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="32846-115">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="32846-116">Este atributo indica si la opción está disponible para su selección o uso.</span><span class="sxs-lookup"><span data-stu-id="32846-116">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="32846-117">Este atributo XML se puede establecer en uno de los valores siguientes: None, PrintTicketSettings, AdminSetting o DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="32846-117">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="32846-118">Vea [Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="32846-118">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="32846-119">name</span><span class="sxs-lookup"><span data-stu-id="32846-119">name</span></span><br/>        | <span data-ttu-id="32846-120">Contiene el nombre de la opción, ya sea una opción estándar o una opción definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="32846-120">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="32846-121">El atributo XML se usa de esta manera para diferenciar entre las instancias de Option.</span><span class="sxs-lookup"><span data-stu-id="32846-121">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="32846-122">Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="32846-122">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="32846-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="32846-123">Element Information</span></span>

<span data-ttu-id="32846-124">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="32846-124">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="32846-125">Category</span><span class="sxs-lookup"><span data-stu-id="32846-125">Category</span></span>                   | <span data-ttu-id="32846-126">Detalles</span><span class="sxs-lookup"><span data-stu-id="32846-126">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32846-127">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="32846-127">Parent elements</span></span><br/> | <span data-ttu-id="32846-128">Característica</span><span class="sxs-lookup"><span data-stu-id="32846-128">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="32846-129">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="32846-129">Child elements</span></span><br/>  | <span data-ttu-id="32846-130">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="32846-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="32846-131">*ScoredProperty* (cero o más para Opciones con el atributo XML 'name'; una o varias para Opciones que no utilizan el atributo XML 'name' \* )</span><span class="sxs-lookup"><span data-stu-id="32846-131">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="32846-132">\* solo las opciones públicas definidas en el esquema de impresión no pueden tener ningún atributo 'name', como DocumentNUp)</span><span class="sxs-lookup"><span data-stu-id="32846-132">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="32846-133">Este elemento</span><span class="sxs-lookup"><span data-stu-id="32846-133">This element</span></span><br/>    | <span data-ttu-id="32846-134">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="32846-134">No character data is permitted.</span></span><br/> <span data-ttu-id="32846-135">No se permiten elementos secundarios duplicados del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="32846-135">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="32846-136">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="32846-136">Configuration Dependencies</span></span>

<span data-ttu-id="32846-137">Es posible que un elemento de definición de opción no tenga dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="32846-137">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="32846-138">Uso de elementos</span><span class="sxs-lookup"><span data-stu-id="32846-138">Element Usage</span></span>

<span data-ttu-id="32846-139">El propósito del elemento Option es caracterizar uno de los estados que un atributo de configuración de dispositivo, representado por un elemento Feature, puede asumir.</span><span class="sxs-lookup"><span data-stu-id="32846-139">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="32846-140">Cada definición de elemento Option contiene uno o varios elementos ScoredProperty que describen una característica intrínseca o esencial de esa opción.</span><span class="sxs-lookup"><span data-stu-id="32846-140">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="32846-141">Para facilitar la portabilidad y la conservación de la intención, el esquema de impresión define muchos elementos de características comunes y una variedad de elementos Option para cada característica.</span><span class="sxs-lookup"><span data-stu-id="32846-141">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="32846-142">Por lo tanto, es importante usar elementos Option definidos por el esquema de impresión, si es posible, antes de crear sus propias definiciones de opción.</span><span class="sxs-lookup"><span data-stu-id="32846-142">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="32846-143">Comprender el proceso de definición de elementos Option proporciona información útil sobre cómo se usan el documento PrintCapabilities y PrintTickets en la arquitectura de impresión de Microsoft .NET Framework versión 3.0 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32846-143">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="32846-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32846-144">Example</span></span>

<span data-ttu-id="32846-145">En el ejemplo siguiente se define un nombre para option.</span><span class="sxs-lookup"><span data-stu-id="32846-145">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="32846-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32846-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32846-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="32846-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




