---
description: Las líneas de un control ListView no se tratan como controles individuales, pero forman parte de un control ListView que funciona como un control. La tabla ListView define los valores para todos los controles ListView.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tabla ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687370"
---
# <a name="listview-table"></a><span data-ttu-id="abe12-104">Tabla ListView</span><span class="sxs-lookup"><span data-stu-id="abe12-104">ListView Table</span></span>

<span data-ttu-id="abe12-105">Las líneas de un control ListView no se tratan como controles individuales, pero forman parte de un control ListView que funciona como un control.</span><span class="sxs-lookup"><span data-stu-id="abe12-105">The lines of a listview are not treated as individual controls, but they are part of a listview that functions as a control.</span></span> <span data-ttu-id="abe12-106">La tabla ListView define los valores para todos los controles ListView.</span><span class="sxs-lookup"><span data-stu-id="abe12-106">The ListView table defines the values for all listviews.</span></span>

<span data-ttu-id="abe12-107">La tabla ListView tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="abe12-107">The ListView table has the following columns.</span></span>



| <span data-ttu-id="abe12-108">Columna</span><span class="sxs-lookup"><span data-stu-id="abe12-108">Column</span></span>   | <span data-ttu-id="abe12-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="abe12-109">Type</span></span>                         | <span data-ttu-id="abe12-110">Clave</span><span class="sxs-lookup"><span data-stu-id="abe12-110">Key</span></span> | <span data-ttu-id="abe12-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="abe12-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="abe12-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abe12-112">Property</span></span> | [<span data-ttu-id="abe12-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="abe12-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="abe12-114">Y</span><span class="sxs-lookup"><span data-stu-id="abe12-114">Y</span></span>   | <span data-ttu-id="abe12-115">N</span><span class="sxs-lookup"><span data-stu-id="abe12-115">N</span></span>        |
| <span data-ttu-id="abe12-116">Pedido</span><span class="sxs-lookup"><span data-stu-id="abe12-116">Order</span></span>    | [<span data-ttu-id="abe12-117">Entero</span><span class="sxs-lookup"><span data-stu-id="abe12-117">Integer</span></span>](integer.md)       | <span data-ttu-id="abe12-118">Y</span><span class="sxs-lookup"><span data-stu-id="abe12-118">Y</span></span>   | <span data-ttu-id="abe12-119">N</span><span class="sxs-lookup"><span data-stu-id="abe12-119">N</span></span>        |
| <span data-ttu-id="abe12-120">Value</span><span class="sxs-lookup"><span data-stu-id="abe12-120">Value</span></span>    | [<span data-ttu-id="abe12-121">Formatea</span><span class="sxs-lookup"><span data-stu-id="abe12-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="abe12-122">N</span><span class="sxs-lookup"><span data-stu-id="abe12-122">N</span></span>   | <span data-ttu-id="abe12-123">N</span><span class="sxs-lookup"><span data-stu-id="abe12-123">N</span></span>        |
| <span data-ttu-id="abe12-124">Texto</span><span class="sxs-lookup"><span data-stu-id="abe12-124">Text</span></span>     | [<span data-ttu-id="abe12-125">Formatea</span><span class="sxs-lookup"><span data-stu-id="abe12-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="abe12-126">N</span><span class="sxs-lookup"><span data-stu-id="abe12-126">N</span></span>   | <span data-ttu-id="abe12-127">Y</span><span class="sxs-lookup"><span data-stu-id="abe12-127">Y</span></span>        |
| <span data-ttu-id="abe12-128">Binary\_</span><span class="sxs-lookup"><span data-stu-id="abe12-128">Binary\_</span></span> | [<span data-ttu-id="abe12-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="abe12-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="abe12-130">N</span><span class="sxs-lookup"><span data-stu-id="abe12-130">N</span></span>   | <span data-ttu-id="abe12-131">Y</span><span class="sxs-lookup"><span data-stu-id="abe12-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="abe12-132">Columnas</span><span class="sxs-lookup"><span data-stu-id="abe12-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="abe12-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad</span><span class="sxs-lookup"><span data-stu-id="abe12-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="abe12-134">Propiedad con nombre que se va a asociar a este elemento.</span><span class="sxs-lookup"><span data-stu-id="abe12-134">A named property to be tied to this item.</span></span> <span data-ttu-id="abe12-135">Todos los elementos vinculados a la misma propiedad forman parte del mismo ListView.</span><span class="sxs-lookup"><span data-stu-id="abe12-135">All the items tied to the same property become part of the same listview.</span></span>

</dd> <dt>

<span data-ttu-id="abe12-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden</span><span class="sxs-lookup"><span data-stu-id="abe12-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="abe12-137">Un entero positivo que se usa para determinar el orden de los elementos que aparecen en una única lista de ListView.</span><span class="sxs-lookup"><span data-stu-id="abe12-137">A positive integer used to determine the ordering of the items that appear in a single listview list.</span></span> <span data-ttu-id="abe12-138">Los enteros no tienen que ser consecutivos.</span><span class="sxs-lookup"><span data-stu-id="abe12-138">The integers do not have to be consecutive.</span></span> <span data-ttu-id="abe12-139">Si un control ListView se define como ordenado, todos los elementos deben tener un valor de ordenación.</span><span class="sxs-lookup"><span data-stu-id="abe12-139">If a listview is defined as ordered, then all the items should have an Ordering value.</span></span> <span data-ttu-id="abe12-140">Si ListView se define como sin ordenar, se omite esta columna.</span><span class="sxs-lookup"><span data-stu-id="abe12-140">If the listview is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="abe12-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="abe12-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="abe12-142">Cadena de valor asociada a este elemento.</span><span class="sxs-lookup"><span data-stu-id="abe12-142">The value string associated with this item.</span></span> <span data-ttu-id="abe12-143">Al seleccionar la línea, se establece la propiedad asociada en este valor.</span><span class="sxs-lookup"><span data-stu-id="abe12-143">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="abe12-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita</span><span class="sxs-lookup"><span data-stu-id="abe12-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="abe12-145">Texto visible y localizable que se va a asignar al elemento.</span><span class="sxs-lookup"><span data-stu-id="abe12-145">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="abe12-146">Si falta esta entrada o toda la columna, el valor predeterminado del texto es la entrada correspondiente en Value.</span><span class="sxs-lookup"><span data-stu-id="abe12-146">If this entry or the entire column is missing, then the text defaults to the corresponding entry in Value.</span></span>

</dd> <dt>

<span data-ttu-id="abe12-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binario\_</span><span class="sxs-lookup"><span data-stu-id="abe12-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binary\_</span></span>
</dt> <dd>

<span data-ttu-id="abe12-148">Datos de imagen para el icono.</span><span class="sxs-lookup"><span data-stu-id="abe12-148">The image data for the icon.</span></span> <span data-ttu-id="abe12-149">Se trata de una clave externa de la [tabla binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="abe12-149">This is a foreign key to the [Binary table](binary-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abe12-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abe12-150">Remarks</span></span>

<span data-ttu-id="abe12-151">La función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) da formato al contenido de los campos de texto y de valor cuando se crea el control, por lo que puede contener cualquier expresión que pueda interpretar la función MsiFormatRecord.</span><span class="sxs-lookup"><span data-stu-id="abe12-151">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the MsiFormatRecord function can interpret.</span></span> <span data-ttu-id="abe12-152">El formato solo se produce cuando se crea el control y no se actualiza si se modifica una propiedad implicada en la expresión durante la vida del control.</span><span class="sxs-lookup"><span data-stu-id="abe12-152">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="abe12-153">Validación</span><span class="sxs-lookup"><span data-stu-id="abe12-153">Validation</span></span>

<dl>

[<span data-ttu-id="abe12-154">ICE03</span><span class="sxs-lookup"><span data-stu-id="abe12-154">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="abe12-155">ICE06</span><span class="sxs-lookup"><span data-stu-id="abe12-155">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="abe12-156">ICE17</span><span class="sxs-lookup"><span data-stu-id="abe12-156">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="abe12-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="abe12-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



