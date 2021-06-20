---
description: Para que un cliente construya un PrintTicket, el documento PrintCapabilities debe proporcionar propiedades de instancias de características e instancias de opción en la característica.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instancias de propiedad importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409128"
---
# <a name="important-property-instances"></a><span data-ttu-id="4be4d-103">Instancias de propiedad importantes</span><span class="sxs-lookup"><span data-stu-id="4be4d-103">Important Property Instances</span></span>

<span data-ttu-id="4be4d-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="4be4d-104">This topic is not current.</span></span> <span data-ttu-id="4be4d-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4be4d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4be4d-106">Para que un cliente PrintCapabilities pueda construir un PrintTicket razonable, el documento PrintCapabilities debe proporcionar determinadas propiedades de instancias de características, así como instancias de option dentro de la característica.</span><span class="sxs-lookup"><span data-stu-id="4be4d-106">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="4be4d-107">Un módulo de interfaz de usuario (UI) genérico requiere dicha información para construir una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4be4d-107">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="4be4d-108">Esto, a su vez, requiere que las palabras clave de esquema de impresión definan algunas instancias de propiedad que aparecen como elementos secundarios de los elementos Feature y Option.</span><span class="sxs-lookup"><span data-stu-id="4be4d-108">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="4be4d-109">Los elementos feature pueden contener la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="4be4d-109">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="4be4d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4be4d-110">Property</span></span>                  | <span data-ttu-id="4be4d-111">Valores</span><span class="sxs-lookup"><span data-stu-id="4be4d-111">Values</span></span>                                 | <span data-ttu-id="4be4d-112">Propósito</span><span class="sxs-lookup"><span data-stu-id="4be4d-112">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be4d-113">SelectionType</span><span class="sxs-lookup"><span data-stu-id="4be4d-113">SelectionType</span></span> <br/> | <span data-ttu-id="4be4d-114">PickOne</span><span class="sxs-lookup"><span data-stu-id="4be4d-114">PickOne</span></span><br/> <span data-ttu-id="4be4d-115">PickMany</span><span class="sxs-lookup"><span data-stu-id="4be4d-115">PickMany</span></span><br/> | <span data-ttu-id="4be4d-116">Especifica el número de opciones que se pueden seleccionar para esta característica en un momento dado, uno (PickOne) o más de uno (PickMany).</span><span class="sxs-lookup"><span data-stu-id="4be4d-116">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="4be4d-117">El cliente puede usar esta información para construir un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4be4d-117">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="4be4d-118">Esta información afecta al comportamiento de la interfaz de usuario, así como a la validación de PrintTicket por parte del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4be4d-118">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="4be4d-119">Los elementos Option pueden contener la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="4be4d-119">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="4be4d-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4be4d-120">Property</span></span>                   | <span data-ttu-id="4be4d-121">Valores</span><span class="sxs-lookup"><span data-stu-id="4be4d-121">Values</span></span>                           | <span data-ttu-id="4be4d-122">Propósito</span><span class="sxs-lookup"><span data-stu-id="4be4d-122">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be4d-123">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="4be4d-123">IdentityOption</span></span> <br/> | <span data-ttu-id="4be4d-124">True</span><span class="sxs-lookup"><span data-stu-id="4be4d-124">True</span></span><br/> <span data-ttu-id="4be4d-125">False</span><span class="sxs-lookup"><span data-stu-id="4be4d-125">False</span></span><br/> | <span data-ttu-id="4be4d-126">La selección de la propiedad IdentityOption se interpreta como "deshabilitar esta característica".</span><span class="sxs-lookup"><span data-stu-id="4be4d-126">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="4be4d-127">Una característica que contiene una propiedad SelectionType cuyo valor es PickMany también debe contener una opción que tenga una propiedad IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="4be4d-127">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="4be4d-128">El código de la interfaz de usuario (o el cliente que construye un PrintTicket) debe anular la selección de cualquier otra opción si está seleccionada la propiedad IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="4be4d-128">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="4be4d-129">Los elementos Feature, Option y ParameterDef pueden contener la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="4be4d-129">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="4be4d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4be4d-130">Property</span></span>              | <span data-ttu-id="4be4d-131">Valores</span><span class="sxs-lookup"><span data-stu-id="4be4d-131">Values</span></span>                          | <span data-ttu-id="4be4d-132">Propósito</span><span class="sxs-lookup"><span data-stu-id="4be4d-132">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be4d-133">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="4be4d-133">DisplayUI</span></span> <br/> | <span data-ttu-id="4be4d-134">Mostrar</span><span class="sxs-lookup"><span data-stu-id="4be4d-134">Show</span></span><br/> <span data-ttu-id="4be4d-135">Ocultar</span><span class="sxs-lookup"><span data-stu-id="4be4d-135">Hide</span></span><br/> | <span data-ttu-id="4be4d-136">Especifica si el elemento primario debe mostrarse en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4be4d-136">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="4be4d-137">Mostrar indica que el elemento debe mostrarse en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4be4d-137">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="4be4d-138">Ocultar indica que el elemento no debe mostrarse en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4be4d-138">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="4be4d-139">Si esta propiedad no está definida para un elemento, la interpretación predeterminada es Show, lo que significa que se muestra el elemento .</span><span class="sxs-lookup"><span data-stu-id="4be4d-139">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="4be4d-140">Los elementos Feature, Option y ParameterDef pueden contener la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="4be4d-140">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="4be4d-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4be4d-141">Property</span></span>                | <span data-ttu-id="4be4d-142">Value</span><span class="sxs-lookup"><span data-stu-id="4be4d-142">Value</span></span>             | <span data-ttu-id="4be4d-143">Propósito</span><span class="sxs-lookup"><span data-stu-id="4be4d-143">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be4d-144">DisplayName</span><span class="sxs-lookup"><span data-stu-id="4be4d-144">DisplayName</span></span> <br/> | <span data-ttu-id="4be4d-145">String</span><span class="sxs-lookup"><span data-stu-id="4be4d-145">String</span></span><br/> | <span data-ttu-id="4be4d-146">Especifica la cadena para mostrar del elemento primario, reemplazando el nombre para mostrar predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4be4d-146">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="4be4d-147">Los proveedores de PrintCapabilities pueden usar para presentar un nombre para mostrar localizado y descriptivo.</span><span class="sxs-lookup"><span data-stu-id="4be4d-147">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="4be4d-148">El valor predeterminado del nombre para mostrar es el atributo name del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="4be4d-148">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="4be4d-149">En el caso de los elementos Option, si no se proporciona el atributo name, debe estar presente la propiedad DisplayName.</span><span class="sxs-lookup"><span data-stu-id="4be4d-149">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4be4d-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4be4d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4be4d-151">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4be4d-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




