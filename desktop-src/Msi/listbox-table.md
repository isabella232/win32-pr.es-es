---
description: Las líneas de un cuadro de lista no se tratan como controles individuales, pero forman parte de un cuadro de lista que funciona como un control. La tabla ListBox define los valores para todos los cuadros de lista.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Tabla ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002250"
---
# <a name="listbox-table"></a><span data-ttu-id="2758b-104">Tabla ListBox</span><span class="sxs-lookup"><span data-stu-id="2758b-104">ListBox Table</span></span>

<span data-ttu-id="2758b-105">Las líneas de un cuadro de lista no se tratan como controles individuales, pero forman parte de un cuadro de lista que funciona como un control.</span><span class="sxs-lookup"><span data-stu-id="2758b-105">The lines of a list box are not treated as individual controls, but they are part of a list box that functions as a control.</span></span> <span data-ttu-id="2758b-106">La tabla ListBox define los valores para todos los cuadros de lista.</span><span class="sxs-lookup"><span data-stu-id="2758b-106">The ListBox table defines the values for all list boxes.</span></span>

<span data-ttu-id="2758b-107">La tabla ListBox tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2758b-107">The ListBox table has the following columns.</span></span>



| <span data-ttu-id="2758b-108">Columna</span><span class="sxs-lookup"><span data-stu-id="2758b-108">Column</span></span>   | <span data-ttu-id="2758b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2758b-109">Type</span></span>                         | <span data-ttu-id="2758b-110">Clave</span><span class="sxs-lookup"><span data-stu-id="2758b-110">Key</span></span> | <span data-ttu-id="2758b-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="2758b-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="2758b-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2758b-112">Property</span></span> | [<span data-ttu-id="2758b-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="2758b-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="2758b-114">Y</span><span class="sxs-lookup"><span data-stu-id="2758b-114">Y</span></span>   | <span data-ttu-id="2758b-115">N</span><span class="sxs-lookup"><span data-stu-id="2758b-115">N</span></span>        |
| <span data-ttu-id="2758b-116">Pedido</span><span class="sxs-lookup"><span data-stu-id="2758b-116">Order</span></span>    | [<span data-ttu-id="2758b-117">Entero</span><span class="sxs-lookup"><span data-stu-id="2758b-117">Integer</span></span>](integer.md)       | <span data-ttu-id="2758b-118">Y</span><span class="sxs-lookup"><span data-stu-id="2758b-118">Y</span></span>   | <span data-ttu-id="2758b-119">N</span><span class="sxs-lookup"><span data-stu-id="2758b-119">N</span></span>        |
| <span data-ttu-id="2758b-120">Value</span><span class="sxs-lookup"><span data-stu-id="2758b-120">Value</span></span>    | [<span data-ttu-id="2758b-121">Formatea</span><span class="sxs-lookup"><span data-stu-id="2758b-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2758b-122">N</span><span class="sxs-lookup"><span data-stu-id="2758b-122">N</span></span>   | <span data-ttu-id="2758b-123">N</span><span class="sxs-lookup"><span data-stu-id="2758b-123">N</span></span>        |
| <span data-ttu-id="2758b-124">Texto</span><span class="sxs-lookup"><span data-stu-id="2758b-124">Text</span></span>     | [<span data-ttu-id="2758b-125">Formatea</span><span class="sxs-lookup"><span data-stu-id="2758b-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2758b-126">N</span><span class="sxs-lookup"><span data-stu-id="2758b-126">N</span></span>   | <span data-ttu-id="2758b-127">Y</span><span class="sxs-lookup"><span data-stu-id="2758b-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2758b-128">Columnas</span><span class="sxs-lookup"><span data-stu-id="2758b-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2758b-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad</span><span class="sxs-lookup"><span data-stu-id="2758b-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="2758b-130">Propiedad con nombre que se va a asociar a este elemento.</span><span class="sxs-lookup"><span data-stu-id="2758b-130">A named property to be tied to this item.</span></span> <span data-ttu-id="2758b-131">Todos los elementos vinculados a la misma propiedad forman parte del mismo cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2758b-131">All the items tied to the same property become part of the same list box.</span></span>

</dd> <dt>

<span data-ttu-id="2758b-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden</span><span class="sxs-lookup"><span data-stu-id="2758b-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="2758b-133">Un entero positivo que se usa para determinar el orden de los elementos que aparecen en un solo cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2758b-133">A positive integer used to determine the ordering of the items that appear in a single list box.</span></span> <span data-ttu-id="2758b-134">Si el cuadro de lista se define como ordenado, todos los elementos deben tener un valor de orden.</span><span class="sxs-lookup"><span data-stu-id="2758b-134">If the list box is defined as ordered, then all items should have an Order value.</span></span> <span data-ttu-id="2758b-135">Los enteros no tienen que ser consecutivos.</span><span class="sxs-lookup"><span data-stu-id="2758b-135">The integers do not have to be consecutive.</span></span> <span data-ttu-id="2758b-136">Si el cuadro de lista se define como sin ordenar, se omitirá esta columna.</span><span class="sxs-lookup"><span data-stu-id="2758b-136">If the list box is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2758b-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="2758b-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="2758b-138">Cadena de valor asociada a este elemento.</span><span class="sxs-lookup"><span data-stu-id="2758b-138">The value string associated with this item.</span></span> <span data-ttu-id="2758b-139">Al seleccionar la línea, se establece la propiedad asociada en este valor.</span><span class="sxs-lookup"><span data-stu-id="2758b-139">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="2758b-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita</span><span class="sxs-lookup"><span data-stu-id="2758b-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="2758b-141">Texto visible localizable que se va a asignar al elemento.</span><span class="sxs-lookup"><span data-stu-id="2758b-141">The localizable, visible text to be assigned to the item.</span></span> <span data-ttu-id="2758b-142">Si falta esta entrada o toda la columna, el valor predeterminado del texto es la entrada correspondiente en Value.</span><span class="sxs-lookup"><span data-stu-id="2758b-142">If this entry or the entire column is missing, the text defaults to the corresponding entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2758b-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2758b-143">Remarks</span></span>

<span data-ttu-id="2758b-144">La función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) da formato al contenido de los campos de texto y de valor cuando se crea el control, por lo que puede contener cualquier expresión que pueda interpretar la función **MsiFormatRecord** .</span><span class="sxs-lookup"><span data-stu-id="2758b-144">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="2758b-145">El formato solo se produce cuando se crea el control y no se actualiza si se modifica una propiedad implicada en la expresión durante la vida del control.</span><span class="sxs-lookup"><span data-stu-id="2758b-145">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="2758b-146">Validación</span><span class="sxs-lookup"><span data-stu-id="2758b-146">Validation</span></span>

<dl>

[<span data-ttu-id="2758b-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="2758b-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2758b-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="2758b-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2758b-149">ICE17</span><span class="sxs-lookup"><span data-stu-id="2758b-149">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="2758b-150">ICE20</span><span class="sxs-lookup"><span data-stu-id="2758b-150">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="2758b-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="2758b-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



