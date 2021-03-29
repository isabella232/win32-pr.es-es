---
description: La tabla de propiedades contiene los nombres de propiedad y los valores de todas las propiedades definidas en la instalación de. Las propiedades con valores NULL no están presentes en la tabla.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Tabla de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813667"
---
# <a name="property-table"></a><span data-ttu-id="fa679-104">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="fa679-104">Property Table</span></span>

<span data-ttu-id="fa679-105">La tabla de propiedades contiene los nombres de propiedad y los valores de todas las propiedades definidas en la instalación de.</span><span class="sxs-lookup"><span data-stu-id="fa679-105">The Property table contains the property names and values for all defined properties in the installation.</span></span> <span data-ttu-id="fa679-106">Las propiedades con valores NULL no están presentes en la tabla.</span><span class="sxs-lookup"><span data-stu-id="fa679-106">Properties with Null values are not present in the table.</span></span>

<span data-ttu-id="fa679-107">La tabla de propiedades tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="fa679-107">The Property table has the following columns.</span></span>



| <span data-ttu-id="fa679-108">Columna</span><span class="sxs-lookup"><span data-stu-id="fa679-108">Column</span></span>   | <span data-ttu-id="fa679-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa679-109">Type</span></span>                         | <span data-ttu-id="fa679-110">Clave</span><span class="sxs-lookup"><span data-stu-id="fa679-110">Key</span></span> | <span data-ttu-id="fa679-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="fa679-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="fa679-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa679-112">Property</span></span> | [<span data-ttu-id="fa679-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="fa679-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="fa679-114">Y</span><span class="sxs-lookup"><span data-stu-id="fa679-114">Y</span></span>   | <span data-ttu-id="fa679-115">N</span><span class="sxs-lookup"><span data-stu-id="fa679-115">N</span></span>        |
| <span data-ttu-id="fa679-116">Value</span><span class="sxs-lookup"><span data-stu-id="fa679-116">Value</span></span>    | [<span data-ttu-id="fa679-117">Texto</span><span class="sxs-lookup"><span data-stu-id="fa679-117">Text</span></span>](text.md)             | <span data-ttu-id="fa679-118">N</span><span class="sxs-lookup"><span data-stu-id="fa679-118">N</span></span>   | <span data-ttu-id="fa679-119">N</span><span class="sxs-lookup"><span data-stu-id="fa679-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fa679-120">Columnas</span><span class="sxs-lookup"><span data-stu-id="fa679-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fa679-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa679-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="fa679-122">Nombre de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="fa679-122">The name of a property.</span></span> <span data-ttu-id="fa679-123">Vea [propiedades](properties.md).</span><span class="sxs-lookup"><span data-stu-id="fa679-123">See [Properties](properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa679-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="fa679-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="fa679-125">Un valor de cadena localizable para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fa679-125">A localizable string value for the property.</span></span> <span data-ttu-id="fa679-126">Esto nunca puede ser null ni una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="fa679-126">This may never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa679-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa679-127">Remarks</span></span>

<span data-ttu-id="fa679-128">Tenga en cuenta que no puede utilizar la tabla de propiedades para establecer una propiedad en el valor de otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="fa679-128">Note that you cannot use the Property table to set a property to the value of another property.</span></span> <span data-ttu-id="fa679-129">El instalador no realiza ninguna acción en la cadena de texto especificada en la columna valor antes de establecer la propiedad en la columna propiedad.</span><span class="sxs-lookup"><span data-stu-id="fa679-129">The installer does nothing to the text string entered in the Value column before setting the property in the Property column.</span></span> <span data-ttu-id="fa679-130">Si FirstProperty se especifica en la columna propiedad y \[ SecondProperty \] en la columna valor, el valor de FirstProperty se establece en la cadena de texto " \[ SecondProperty \] " y no en el valor de la propiedad SecondProperty.</span><span class="sxs-lookup"><span data-stu-id="fa679-130">If FirstProperty is entered into the Property column and \[SecondProperty\] in the Value column, the value of FirstProperty is set to the text string "\[SecondProperty\]" and not to the value of the SecondProperty property.</span></span> <span data-ttu-id="fa679-131">Esto es necesario para evitar la creación de referencias circulares en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fa679-131">This is necessary to prevent creating circular references in the Property table.</span></span> <span data-ttu-id="fa679-132">En su lugar, puede establecer una propiedad en otra mediante un [tipo de acción personalizada 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="fa679-132">Instead, you can set one property to another by using a [Custom Action Type 51](custom-action-type-51.md).</span></span>

<span data-ttu-id="fa679-133">Tenga en cuenta que la propiedad [**AdminProperties**](adminproperties.md) se puede usar para invalidar los valores de la tabla de propiedades durante una [instalación administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="fa679-133">Note that the [**AdminProperties**](adminproperties.md) property can be used to override the values in the Property table during an [Administrative Installation](administrative-installation.md).</span></span>

<span data-ttu-id="fa679-134">No use propiedades para contraseñas u otra información que deba permanecer segura.</span><span class="sxs-lookup"><span data-stu-id="fa679-134">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="fa679-135">El instalador puede escribir el valor de una propiedad creada en la tabla de propiedades, o bien crearse en tiempo de ejecución, en un registro o en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="fa679-135">The installer may write the value of a property authored into the Property table, or created at runtime, into a log or the system registry.</span></span>

## <a name="validation"></a><span data-ttu-id="fa679-136">Validación</span><span class="sxs-lookup"><span data-stu-id="fa679-136">Validation</span></span>

<dl>

[<span data-ttu-id="fa679-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="fa679-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fa679-138">ICE05</span><span class="sxs-lookup"><span data-stu-id="fa679-138">ICE05</span></span>](ice05.md)  
[<span data-ttu-id="fa679-139">ICE06</span><span class="sxs-lookup"><span data-stu-id="fa679-139">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fa679-140">ICE16</span><span class="sxs-lookup"><span data-stu-id="fa679-140">ICE16</span></span>](ice16.md)  
[<span data-ttu-id="fa679-141">ICE24</span><span class="sxs-lookup"><span data-stu-id="fa679-141">ICE24</span></span>](ice24.md)  
[<span data-ttu-id="fa679-142">ICE31</span><span class="sxs-lookup"><span data-stu-id="fa679-142">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="fa679-143">ICE34</span><span class="sxs-lookup"><span data-stu-id="fa679-143">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="fa679-144">ICE36</span><span class="sxs-lookup"><span data-stu-id="fa679-144">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="fa679-145">ICE40</span><span class="sxs-lookup"><span data-stu-id="fa679-145">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="fa679-146">ICE46</span><span class="sxs-lookup"><span data-stu-id="fa679-146">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fa679-147">ICE48</span><span class="sxs-lookup"><span data-stu-id="fa679-147">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="fa679-148">ICE52</span><span class="sxs-lookup"><span data-stu-id="fa679-148">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="fa679-149">:</span><span class="sxs-lookup"><span data-stu-id="fa679-149">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="fa679-150">ICE73</span><span class="sxs-lookup"><span data-stu-id="fa679-150">ICE73</span></span>](ice73.md)  
[<span data-ttu-id="fa679-151">ICE74</span><span class="sxs-lookup"><span data-stu-id="fa679-151">ICE74</span></span>](ice74.md)  
[<span data-ttu-id="fa679-152">ICE80</span><span class="sxs-lookup"><span data-stu-id="fa679-152">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="fa679-153">ICE87</span><span class="sxs-lookup"><span data-stu-id="fa679-153">ICE87</span></span>](ice87.md)  
[<span data-ttu-id="fa679-154">ICE88</span><span class="sxs-lookup"><span data-stu-id="fa679-154">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="fa679-155">ICE91</span><span class="sxs-lookup"><span data-stu-id="fa679-155">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="fa679-156">ICE99</span><span class="sxs-lookup"><span data-stu-id="fa679-156">ICE99</span></span>](ice99.md)  
</dl>

 

 



