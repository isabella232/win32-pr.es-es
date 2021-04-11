---
title: Elemento LISTBOX
description: Elemento LISTBOX
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Aspectos de Windows Media Player, elemento LISTBOX
- máscaras, elemento LISTBOX
- Elemento LISTBOX
- referencia de las máscaras, elemento LISTBOX
- elementos, LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075509"
---
# <a name="listbox-element"></a><span data-ttu-id="b2071-108">Elemento LISTBOX</span><span class="sxs-lookup"><span data-stu-id="b2071-108">LISTBOX Element</span></span>

<span data-ttu-id="b2071-109">El elemento **ListBox** proporciona una manera para que los usuarios seleccionen elementos de una lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-109">The **LISTBOX** element provides a way for users to select items from a list.</span></span> <span data-ttu-id="b2071-110">Estos elementos se pueden especificar utilizando elementos **Item** como elementos secundarios del elemento **ListBox** .</span><span class="sxs-lookup"><span data-stu-id="b2071-110">These items can be specified by using **ITEM** elements as children of the **LISTBOX** element.</span></span> <span data-ttu-id="b2071-111">Si necesita un control de cuadro de lista que solo se muestre cuando sea necesario, use el elemento **popup** , que es idéntico al elemento **ListBox** excepto el valor predeterminado del atributo **popup** , que determina su comportamiento de presentación.</span><span class="sxs-lookup"><span data-stu-id="b2071-111">If you need a list box control that is displayed only when needed, use the **POPUP** element, which is identical to the **LISTBOX** element except for the default value of the **popUp** attribute, which dictates its display behavior.</span></span>

<span data-ttu-id="b2071-112">El elemento **ListBox** admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="b2071-112">The **LISTBOX** element supports the following attributes.</span></span>



| <span data-ttu-id="b2071-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="b2071-113">Attribute</span></span>                                        | <span data-ttu-id="b2071-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2071-114">Description</span></span>                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2071-115">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b2071-115">backgroundColor</span></span>](listbox-backgroundcolor.md)   | <span data-ttu-id="b2071-116">Especifica o recupera el color de fondo del control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-116">Specifies or retrieves the background color in the list box control.</span></span>                                                  |
| [<span data-ttu-id="b2071-117">PDA</span><span class="sxs-lookup"><span data-stu-id="b2071-117">border</span></span>](listbox-border.md)                     | <span data-ttu-id="b2071-118">Especifica o recupera un valor que indica si el control de cuadro de lista tiene un borde.</span><span class="sxs-lookup"><span data-stu-id="b2071-118">Specifies or retrieves a value indicating whether the list box control has a border.</span></span> <span data-ttu-id="b2071-119">Solo se puede establecer en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="b2071-119">Can only be set at design time.</span></span>  |
| [<span data-ttu-id="b2071-120">firstVisibleItem</span><span class="sxs-lookup"><span data-stu-id="b2071-120">firstVisibleItem</span></span>](listbox-firstvisibleitem.md) | <span data-ttu-id="b2071-121">Especifica o recupera el índice de la primera línea visible en el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-121">Specifies or retrieves the index of the first visible line in the list box control.</span></span>                                   |
| [<span data-ttu-id="b2071-122">focusItem</span><span class="sxs-lookup"><span data-stu-id="b2071-122">focusItem</span></span>](listbox-focusitem.md)               | <span data-ttu-id="b2071-123">Especifica o recupera la línea que contiene el foco.</span><span class="sxs-lookup"><span data-stu-id="b2071-123">Specifies or retrieves the line that contains focus.</span></span>                                                                  |
| [<span data-ttu-id="b2071-124">fontFace</span><span class="sxs-lookup"><span data-stu-id="b2071-124">fontFace</span></span>](listbox-fontface.md)                 | <span data-ttu-id="b2071-125">Especifica o recupera la fuente para el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-125">Specifies or retrieves the font for the list box control.</span></span>                                                             |
| [<span data-ttu-id="b2071-126">fontSize</span><span class="sxs-lookup"><span data-stu-id="b2071-126">fontSize</span></span>](listbox-fontsize.md)                 | <span data-ttu-id="b2071-127">Especifica o recupera el tamaño de fuente para el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-127">Specifies or retrieves the font size for the list box control.</span></span>                                                        |
| [<span data-ttu-id="b2071-128">fontStyle</span><span class="sxs-lookup"><span data-stu-id="b2071-128">fontStyle</span></span>](listbox-fontstyle.md)               | <span data-ttu-id="b2071-129">Especifica o recupera el estilo de fuente para el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-129">Specifies or retrieves the font style for the list box control.</span></span>                                                       |
| [<span data-ttu-id="b2071-130">foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b2071-130">foregroundColor</span></span>](listbox-foregroundcolor.md)   | <span data-ttu-id="b2071-131">Especifica o recupera el color del texto en el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-131">Specifies or retrieves the text color in the list box control.</span></span>                                                        |
| [<span data-ttu-id="b2071-132">itemCount</span><span class="sxs-lookup"><span data-stu-id="b2071-132">itemCount</span></span>](listbox-itemcount.md)               | <span data-ttu-id="b2071-133">Recupera el número de elementos del control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-133">Retrieves the number of items in the list box control.</span></span>                                                                |
| [<span data-ttu-id="b2071-134">Selección múltiple</span><span class="sxs-lookup"><span data-stu-id="b2071-134">multiSelect</span></span>](listbox-multiselect.md)           | <span data-ttu-id="b2071-135">Especifica o recupera un valor que indica si el usuario puede seleccionar varias líneas.</span><span class="sxs-lookup"><span data-stu-id="b2071-135">Specifies or retrieves a value indicating whether the user can select multiple lines.</span></span> <span data-ttu-id="b2071-136">Solo se puede establecer en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="b2071-136">Can only be set at design time.</span></span> |
| [<span data-ttu-id="b2071-137">Emergente</span><span class="sxs-lookup"><span data-stu-id="b2071-137">popUp</span></span>](listbox-popup.md)                       | <span data-ttu-id="b2071-138">Especifica un valor que indica si el elemento representa un control emergente o de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-138">Specifies a value indicating whether the element represents a popup or list box control.</span></span>                              |
| [<span data-ttu-id="b2071-139">readOnly</span><span class="sxs-lookup"><span data-stu-id="b2071-139">readOnly</span></span>](listbox-readonly.md)                 | <span data-ttu-id="b2071-140">Especifica o recupera un valor que indica si el texto es de solo lectura o si el usuario puede seleccionar texto.</span><span class="sxs-lookup"><span data-stu-id="b2071-140">Specifies or retrieves a value indicating whether text is read-only or text can be selected by the user.</span></span>              |
| [<span data-ttu-id="b2071-141">selectedItem</span><span class="sxs-lookup"><span data-stu-id="b2071-141">selectedItem</span></span>](listbox-selecteditem.md)         | <span data-ttu-id="b2071-142">Especifica o recupera el índice del elemento seleccionado en el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-142">Specifies or retrieves the index of the item selected in the list box control.</span></span>                                        |
| [<span data-ttu-id="b2071-143">ordenados</span><span class="sxs-lookup"><span data-stu-id="b2071-143">sorted</span></span>](listbox-sorted.md)                     | <span data-ttu-id="b2071-144">Especifica o recupera un valor que indica si el control de cuadro de lista está ordenado alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="b2071-144">Specifies or retrieves a value indicating whether the list box control is sorted alphabetically.</span></span>                      |



 

<span data-ttu-id="b2071-145">El elemento **ListBox** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b2071-145">The **LISTBOX** element supports the following methods.</span></span>



| <span data-ttu-id="b2071-146">Método</span><span class="sxs-lookup"><span data-stu-id="b2071-146">Method</span></span>                                                 | <span data-ttu-id="b2071-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2071-147">Description</span></span>                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2071-148">appendItem</span><span class="sxs-lookup"><span data-stu-id="b2071-148">appendItem</span></span>](listbox-appenditem.md)                   | <span data-ttu-id="b2071-149">Inserta texto nuevo al final del control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-149">Inserts new text at the end of the list box control.</span></span>                                                                  |
| [<span data-ttu-id="b2071-150">deleteAll</span><span class="sxs-lookup"><span data-stu-id="b2071-150">deleteAll</span></span>](listbox-deleteall.md)                     | <span data-ttu-id="b2071-151">Elimina todos los elementos del control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-151">Deletes all items from the list box control.</span></span>                                                                          |
| [<span data-ttu-id="b2071-152">deleteItem</span><span class="sxs-lookup"><span data-stu-id="b2071-152">deleteItem</span></span>](listbox-deleteitem.md)                   | <span data-ttu-id="b2071-153">Elimina el elemento de control de cuadro de lista en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="b2071-153">Deletes the list box control item at the specified index.</span></span>                                                             |
| [<span data-ttu-id="b2071-154">rechazar</span><span class="sxs-lookup"><span data-stu-id="b2071-154">dismiss</span></span>](listbox-dismiss.md)                         | <span data-ttu-id="b2071-155">Oculta el control.</span><span class="sxs-lookup"><span data-stu-id="b2071-155">Hides the control.</span></span>                                                                                                    |
| [<span data-ttu-id="b2071-156">findItem</span><span class="sxs-lookup"><span data-stu-id="b2071-156">findItem</span></span>](listbox-finditem.md)                       | <span data-ttu-id="b2071-157">Busca una cadena determinada empezando por el elemento que sigue al índice de elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="b2071-157">Searches for a given string starting with the item following the specified item index.</span></span>                                |
| [<span data-ttu-id="b2071-158">getItem</span><span class="sxs-lookup"><span data-stu-id="b2071-158">getItem</span></span>](listbox-getitem.md)                         | <span data-ttu-id="b2071-159">Recupera el texto del elemento con el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="b2071-159">Retrieves the text for the item with the specified index.</span></span>                                                             |
| [<span data-ttu-id="b2071-160">getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="b2071-160">getNextSelectedItem</span></span>](listbox-getnextselecteditem.md) | <span data-ttu-id="b2071-161">Recupera el siguiente elemento seleccionado en el control de cuadro de lista, empezando por el elemento que tiene el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="b2071-161">Retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span> |
| [<span data-ttu-id="b2071-162">insertItem</span><span class="sxs-lookup"><span data-stu-id="b2071-162">insertItem</span></span>](listbox-insertitem.md)                   | <span data-ttu-id="b2071-163">Inserta el texto especificado en el índice especificado del control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="b2071-163">Inserts the specified text at the specified index in the list box control.</span></span>                                            |
| [<span data-ttu-id="b2071-164">replaceItem</span><span class="sxs-lookup"><span data-stu-id="b2071-164">replaceItem</span></span>](listbox-replaceitem.md)                 | <span data-ttu-id="b2071-165">Reemplaza el texto que se encuentra en el índice especificado por el texto especificado.</span><span class="sxs-lookup"><span data-stu-id="b2071-165">Replaces the text at the specified index with the specified text.</span></span>                                                     |
| [<span data-ttu-id="b2071-166">setSelectedState</span><span class="sxs-lookup"><span data-stu-id="b2071-166">setSelectedState</span></span>](listbox-setselectedstate.md)       | <span data-ttu-id="b2071-167">Selecciona o anula la selección del elemento con el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="b2071-167">Selects or unselects the item with the specified index.</span></span>                                                               |
| [<span data-ttu-id="b2071-168">show</span><span class="sxs-lookup"><span data-stu-id="b2071-168">show</span></span>](listbox-show.md)                               | <span data-ttu-id="b2071-169">Muestra el control.</span><span class="sxs-lookup"><span data-stu-id="b2071-169">Displays the control.</span></span>                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="b2071-170">Este elemento requiere Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="b2071-170">This element requires Windows Media Player for Windows XP or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b2071-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2071-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2071-172">**Elemento POPUP**</span><span class="sxs-lookup"><span data-stu-id="b2071-172">**POPUP Element**</span></span>](popup-element.md)
</dt> <dt>

[<span data-ttu-id="b2071-173">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="b2071-173">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




