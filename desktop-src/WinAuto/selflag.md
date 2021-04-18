---
title: Constantes SELFLAG (oleacc. h)
description: En este tema se describen los valores constantes que se usan para especificar cómo se selecciona un objeto accesible o se toma el foco.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718761"
---
# <a name="selflag-constants"></a><span data-ttu-id="22e8f-103">Constantes de SELFLAG</span><span class="sxs-lookup"><span data-stu-id="22e8f-103">SELFLAG Constants</span></span>

<span data-ttu-id="22e8f-104">En este tema se describen los valores constantes que se usan para especificar cómo se selecciona un objeto accesible o se toma el foco.</span><span class="sxs-lookup"><span data-stu-id="22e8f-104">This topic describes the constant values used to specify how an accessible object becomes selected or takes the focus.</span></span> <span data-ttu-id="22e8f-105">Las constantes se definen en oleacc. h y se usan con el método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .</span><span class="sxs-lookup"><span data-stu-id="22e8f-105">The constants are defined in oleacc.h and are used with the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method.</span></span>

<span data-ttu-id="22e8f-106">No se permiten las siguientes combinaciones:</span><span class="sxs-lookup"><span data-stu-id="22e8f-106">The following combinations are not allowed:</span></span>

-   <span data-ttu-id="22e8f-107">SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-107">SELFLAG\_ADDSELECTION \| SELFLAG\_REMOVESELECTION</span></span>
-   <span data-ttu-id="22e8f-108">SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-108">SELFLAG\_ADDSELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="22e8f-109">SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-109">SELFLAG\_REMOVESELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="22e8f-110">SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-110">SELFLAG\_EXTENDSELECTION \| SELFLAG\_TAKESELECTION</span></span>

<span data-ttu-id="22e8f-111">**Nota para los clientes:** Microsoft Active Accessibility no admite la selección del texto contenido en los controles de edición y edición enriquecida porque el texto se expone como una cadena en la [propiedad Value](value-property.md)del objeto.</span><span class="sxs-lookup"><span data-stu-id="22e8f-111">**Note to clients :** Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a string in the object's [Value property](value-property.md).</span></span>

<span data-ttu-id="22e8f-112">Para obtener información sobre cómo realizar operaciones de selección complejas, consulte [seleccionar objetos secundarios](selecting-child-objects.md).</span><span class="sxs-lookup"><span data-stu-id="22e8f-112">For information on how to perform complex selection operations, see [Selecting Child Objects](selecting-child-objects.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="22e8f-113">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="22e8f-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="22e8f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="22e8f-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <span data-ttu-id="22e8f-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="22e8f-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="22e8f-116">No realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="22e8f-116">Performs no action.</span></span> <span data-ttu-id="22e8f-117">Microsoft Active Accessibility no cambia la selección o el foco.</span><span class="sxs-lookup"><span data-stu-id="22e8f-117">Microsoft Active Accessibility does not change the selection or focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <span data-ttu-id="22e8f-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span><span class="sxs-lookup"><span data-stu-id="22e8f-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="22e8f-119">Establece el foco en el objeto y lo convierte en el delimitador de selección.</span><span class="sxs-lookup"><span data-stu-id="22e8f-119">Sets the focus to the object and makes it the selection anchor.</span></span> <span data-ttu-id="22e8f-120">Este marcador, que se usa por sí solo, no modifica la selección.</span><span class="sxs-lookup"><span data-stu-id="22e8f-120">Used by itself, this flag does not alter the selection.</span></span> <span data-ttu-id="22e8f-121">El efecto es similar a mover el foco manualmente presionando una tecla de dirección mientras mantiene presionada la tecla CTRL en el explorador de Windows o en cualquier cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="22e8f-121">The effect is similar to moving the focus manually by pressing an ARROW key while holding down the CTRL key in Windows Explorer or in any multiple-selection list box.</span></span> <br/> <span data-ttu-id="22e8f-122">Con los objetos que tienen el <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS se combina con los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="22e8f-122">With objects that have the <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS is combined with the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="22e8f-123">SELFLAG_TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-123">SELFLAG_TAKESELECTION</span></span></li>
<li><span data-ttu-id="22e8f-124">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-124">SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="22e8f-125">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-125">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="22e8f-126">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-126">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="22e8f-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="22e8f-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
</ul>
<span data-ttu-id="22e8f-129">Si se llama a <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> con la marca SELFLAG_TAKEFOCUS en un objeto que tiene un <strong>hWnd</strong>, la marca solo tendrá efecto si el elemento primario del objeto ya tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="22e8f-129">If you call <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> with the SELFLAG_TAKEFOCUS flag on an object that has an <strong>HWND</strong>, the flag will take effect only if the object's parent already has the focus.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <span data-ttu-id="22e8f-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0X2</dt> </span><span class="sxs-lookup"><span data-stu-id="22e8f-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="22e8f-131">Selecciona el objeto y quita la selección de todos los demás objetos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="22e8f-131">Selects the object and removes the selection from all other objects in the container.</span></span> <br/> <span data-ttu-id="22e8f-132">A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección.</span><span class="sxs-lookup"><span data-stu-id="22e8f-132">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="22e8f-133">El SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a hacer un solo clic en un elemento del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="22e8f-133">The SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to single-clicking an item in Windows Explorer.</span></span><br/> <span data-ttu-id="22e8f-134">Esta marca no debe combinarse con las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="22e8f-134">This flag must not be combined with the following flags:</span></span><br/>
<ul>
<li><span data-ttu-id="22e8f-135">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-135">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="22e8f-136">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-136">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="22e8f-137">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="22e8f-137">SELFLAG_EXTENDSELECTION</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <span data-ttu-id="22e8f-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span><span class="sxs-lookup"><span data-stu-id="22e8f-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="22e8f-139">Modifica la selección para que todos los objetos entre el delimitador de selección y este objeto tomen el estado de selección del objeto de delimitador.</span><span class="sxs-lookup"><span data-stu-id="22e8f-139">Alters the selection so that all objects between the selection anchor and this object take on the anchor object's selection state.</span></span> <span data-ttu-id="22e8f-140">Si el objeto delimitador no está seleccionado, los objetos se quitan de la selección.</span><span class="sxs-lookup"><span data-stu-id="22e8f-140">If the anchor object is not selected, the objects are removed from the selection.</span></span> <span data-ttu-id="22e8f-141">Si se selecciona el objeto delimitador, la selección se extiende para incluir este objeto y todos los objetos que hay entre ellos.</span><span class="sxs-lookup"><span data-stu-id="22e8f-141">If the anchor object is selected, the selection is extended to include this object and all the objects in between.</span></span> <span data-ttu-id="22e8f-142">Establezca el estado de selección mediante la combinación de esta marca con SELFLAG_ADDSELECTION o SELFLAG_REMOVESELECTION.</span><span class="sxs-lookup"><span data-stu-id="22e8f-142">Set the selection state by combining this flag with SELFLAG_ADDSELECTION or SELFLAG_REMOVESELECTION.</span></span> <br/> <span data-ttu-id="22e8f-143">A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección.</span><span class="sxs-lookup"><span data-stu-id="22e8f-143">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="22e8f-144">El SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a agregar un elemento a una selección manualmente manteniendo presionada la tecla Mayús y haciendo clic en un objeto no seleccionado en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="22e8f-144">The SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the SHIFT key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="22e8f-145">Esta marca no se combina con SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="22e8f-145">This flag is not combined with SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <span data-ttu-id="22e8f-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span><span class="sxs-lookup"><span data-stu-id="22e8f-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="22e8f-147">Agrega el objeto a la selección actual; el resultado posible es una selección no contigua.</span><span class="sxs-lookup"><span data-stu-id="22e8f-147">Adds the object to the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="22e8f-148">A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección.</span><span class="sxs-lookup"><span data-stu-id="22e8f-148">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="22e8f-149">El SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a agregar un elemento a una selección manualmente manteniendo presionada la tecla CTRL y haciendo clic en un objeto no seleccionado en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="22e8f-149">The SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the CTRL key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="22e8f-150">Esta marca no se combina con SELFLAG_REMOVESELECTION o SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="22e8f-150">This flag is not combined with SELFLAG_REMOVESELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <span data-ttu-id="22e8f-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span><span class="sxs-lookup"><span data-stu-id="22e8f-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="22e8f-152">Quita el objeto de la selección actual; el resultado posible es una selección no contigua.</span><span class="sxs-lookup"><span data-stu-id="22e8f-152">Removes the object from the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="22e8f-153">A menos que se combine con SELFLAG_TAKEFOCUS, esta marca no cambia el foco ni el delimitador de selección.</span><span class="sxs-lookup"><span data-stu-id="22e8f-153">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="22e8f-154">El SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinación es equivalente a quitar un elemento de una selección manualmente, manteniendo presionada la tecla CTRL mientras hace clic en un objeto seleccionado en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="22e8f-154">The SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to removing an item from a selection manually, by holding down the CTRL key while clicking a selected object in Windows Explorer.</span></span><br/> <span data-ttu-id="22e8f-155">Esta marca no se combina con SELFLAG_ADDSELECTION o SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="22e8f-155">This flag is not combined with SELFLAG_ADDSELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="22e8f-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22e8f-156">Requirements</span></span>



| <span data-ttu-id="22e8f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e8f-157">Requirement</span></span> | <span data-ttu-id="22e8f-158">Value</span><span class="sxs-lookup"><span data-stu-id="22e8f-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22e8f-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22e8f-159">Header</span></span><br/> | <dl> <span data-ttu-id="22e8f-160"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e8f-160"><dt>Oleacc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e8f-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="22e8f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e8f-162">**IAccessible:: accSelect**</span><span class="sxs-lookup"><span data-stu-id="22e8f-162">**IAccessible::accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[<span data-ttu-id="22e8f-163">Seleccionar objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="22e8f-163">Selecting Child Objects</span></span>](selecting-child-objects.md)
</dt> </dl>

 

 





