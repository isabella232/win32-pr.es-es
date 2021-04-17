---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instancias de propiedad importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721381"
---
# <a name="important-property-instances"></a><span data-ttu-id="72d32-104">Instancias de propiedad importantes</span><span class="sxs-lookup"><span data-stu-id="72d32-104">Important Property Instances</span></span>

<span data-ttu-id="72d32-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="72d32-105">This topic is not current.</span></span> <span data-ttu-id="72d32-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="72d32-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72d32-107">Para que un cliente de PrintCapabilities pueda construir un PrintTicket razonable, el documento de PrintCapabilities debe proporcionar ciertas propiedades de instancias de características, así como instancias de opciones dentro de la característica.</span><span class="sxs-lookup"><span data-stu-id="72d32-107">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="72d32-108">Un módulo de interfaz de usuario (IU) genérico requiere tal información para construir una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="72d32-108">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="72d32-109">Esto a su vez requiere que las palabras clave de esquema de impresión definan algunas instancias de propiedad que aparecen como elementos secundarios de los elementos de opción y de característica.</span><span class="sxs-lookup"><span data-stu-id="72d32-109">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="72d32-110">Los elementos de característica pueden contener la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="72d32-110">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="72d32-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72d32-111">Property</span></span>                  | <span data-ttu-id="72d32-112">Valores</span><span class="sxs-lookup"><span data-stu-id="72d32-112">Values</span></span>                                 | <span data-ttu-id="72d32-113">Propósito</span><span class="sxs-lookup"><span data-stu-id="72d32-113">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d32-114">SelectionType</span><span class="sxs-lookup"><span data-stu-id="72d32-114">SelectionType</span></span> <br/> | <span data-ttu-id="72d32-115">PickOne</span><span class="sxs-lookup"><span data-stu-id="72d32-115">PickOne</span></span><br/> <span data-ttu-id="72d32-116">PickMany</span><span class="sxs-lookup"><span data-stu-id="72d32-116">PickMany</span></span><br/> | <span data-ttu-id="72d32-117">Especifica el número de opciones que se pueden seleccionar para esta característica en un momento dado, ya sea una (PickOne) o más de una (PickMany).</span><span class="sxs-lookup"><span data-stu-id="72d32-117">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="72d32-118">El cliente puede utilizar esta información para construir un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="72d32-118">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="72d32-119">Esta información afecta al comportamiento de la interfaz de usuario, así como a la validación de PrintTicket por parte del proveedor.</span><span class="sxs-lookup"><span data-stu-id="72d32-119">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="72d32-120">Los elementos de opción pueden contener la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="72d32-120">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="72d32-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72d32-121">Property</span></span>                   | <span data-ttu-id="72d32-122">Valores</span><span class="sxs-lookup"><span data-stu-id="72d32-122">Values</span></span>                           | <span data-ttu-id="72d32-123">Propósito</span><span class="sxs-lookup"><span data-stu-id="72d32-123">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d32-124">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="72d32-124">IdentityOption</span></span> <br/> | <span data-ttu-id="72d32-125">True</span><span class="sxs-lookup"><span data-stu-id="72d32-125">True</span></span><br/> <span data-ttu-id="72d32-126">False</span><span class="sxs-lookup"><span data-stu-id="72d32-126">False</span></span><br/> | <span data-ttu-id="72d32-127">La selección de la propiedad IdentityOption se interpreta para indicar "deshabilitar esta característica".</span><span class="sxs-lookup"><span data-stu-id="72d32-127">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="72d32-128">Una característica que contiene una propiedad SelectionType cuyo valor es PickMany también debe contener una opción que tenga una propiedad IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="72d32-128">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="72d32-129">El código de la interfaz de usuario (o el cliente que crea un PrintTicket) debe anular la selección de cualquier otra opción si la propiedad IdentityOption está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="72d32-129">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="72d32-130">Los elementos Feature, Option y ParameterDef pueden contener la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="72d32-130">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="72d32-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72d32-131">Property</span></span>              | <span data-ttu-id="72d32-132">Valores</span><span class="sxs-lookup"><span data-stu-id="72d32-132">Values</span></span>                          | <span data-ttu-id="72d32-133">Propósito</span><span class="sxs-lookup"><span data-stu-id="72d32-133">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d32-134">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="72d32-134">DisplayUI</span></span> <br/> | <span data-ttu-id="72d32-135">Mostrar</span><span class="sxs-lookup"><span data-stu-id="72d32-135">Show</span></span><br/> <span data-ttu-id="72d32-136">Ocultar</span><span class="sxs-lookup"><span data-stu-id="72d32-136">Hide</span></span><br/> | <span data-ttu-id="72d32-137">Especifica si el elemento primario se debe mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="72d32-137">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="72d32-138">Mostrar indica que el elemento debe mostrarse en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="72d32-138">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="72d32-139">Hide indica que el elemento no se debe mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="72d32-139">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="72d32-140">Si esta propiedad no está definida para un elemento, se muestra la interpretación predeterminada, lo que significa que se muestra el elemento.</span><span class="sxs-lookup"><span data-stu-id="72d32-140">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="72d32-141">Los elementos Feature, Option y ParameterDef pueden contener la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="72d32-141">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="72d32-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72d32-142">Property</span></span>                | <span data-ttu-id="72d32-143">Value</span><span class="sxs-lookup"><span data-stu-id="72d32-143">Value</span></span>             | <span data-ttu-id="72d32-144">Propósito</span><span class="sxs-lookup"><span data-stu-id="72d32-144">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d32-145">DisplayName</span><span class="sxs-lookup"><span data-stu-id="72d32-145">DisplayName</span></span> <br/> | <span data-ttu-id="72d32-146">String</span><span class="sxs-lookup"><span data-stu-id="72d32-146">String</span></span><br/> | <span data-ttu-id="72d32-147">Especifica la cadena de presentación para el elemento primario, invalidando el nombre para mostrar predeterminado.</span><span class="sxs-lookup"><span data-stu-id="72d32-147">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="72d32-148">Los proveedores de PrintCapabilities pueden utilizar para presentar un nombre para mostrar localizado y descriptivo para el usuario.</span><span class="sxs-lookup"><span data-stu-id="72d32-148">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="72d32-149">El valor de nombre para mostrar predeterminado es el atributo de nombre del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="72d32-149">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="72d32-150">En el caso de los elementos Option, si no se proporciona el atributo name, la propiedad DisplayName debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="72d32-150">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="72d32-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72d32-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72d32-152">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="72d32-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




