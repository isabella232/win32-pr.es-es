---
description: La interfaz IExtender proporciona un conjunto de propiedades básicas que se agregan a la interfaz de un control. Los programadores pueden utilizar estas propiedades como si formaran parte del control.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Interfaz IExtender
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660196"
---
# <a name="iextender-interface"></a><span data-ttu-id="d52bf-104">Interfaz IExtender</span><span class="sxs-lookup"><span data-stu-id="d52bf-104">IExtender interface</span></span>

<span data-ttu-id="d52bf-105">La interfaz **IExtender** proporciona un conjunto de propiedades básicas que se agregan a la interfaz de un control.</span><span class="sxs-lookup"><span data-stu-id="d52bf-105">The **IExtender** interface provides a set of basic properties that are added to the interface of a control.</span></span> <span data-ttu-id="d52bf-106">Los programadores pueden utilizar estas propiedades como si formaran parte del control.</span><span class="sxs-lookup"><span data-stu-id="d52bf-106">Programmers can use these properties as if they were part of the control.</span></span>

## <a name="members"></a><span data-ttu-id="d52bf-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d52bf-107">Members</span></span>

<span data-ttu-id="d52bf-108">La interfaz **IExtender** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d52bf-108">The **IExtender** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d52bf-109">**IExtender** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d52bf-109">**IExtender** also has these types of members:</span></span>

-   [<span data-ttu-id="d52bf-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d52bf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d52bf-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d52bf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d52bf-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d52bf-112">Methods</span></span>

<span data-ttu-id="d52bf-113">La interfaz **IExtender** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d52bf-113">The **IExtender** interface has these methods.</span></span>



| <span data-ttu-id="d52bf-114">Método</span><span class="sxs-lookup"><span data-stu-id="d52bf-114">Method</span></span>                         | <span data-ttu-id="d52bf-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d52bf-115">Description</span></span>                                    |
|:-------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="d52bf-116">**Move**</span><span class="sxs-lookup"><span data-stu-id="d52bf-116">**Move**</span></span>](iextender-move.md) | <span data-ttu-id="d52bf-117">Mueve un control MDIForm, Form o.</span><span class="sxs-lookup"><span data-stu-id="d52bf-117">Moves an MDIForm, form, or control.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d52bf-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d52bf-118">Properties</span></span>

<span data-ttu-id="d52bf-119">La interfaz **IExtender** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d52bf-119">The **IExtender** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d52bf-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d52bf-120">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d52bf-121">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d52bf-121">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d52bf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d52bf-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d52bf-123">Alinear</span><span class="sxs-lookup"><span data-stu-id="d52bf-123">Align</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d52bf-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-124">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d52bf-125">Devuelve o establece un valor que determina si un objeto se muestra en cualquier tamaño de un formulario o si se muestra en la parte superior, inferior, izquierda o derecha del formulario y se ajusta automáticamente para ajustarse al ancho del formulario.</span><span class="sxs-lookup"><span data-stu-id="d52bf-125">Returns or sets a value that determines whether an object is displayed in any size anywhere on a form or whether it is displayed at the top, bottom, left, or right of the form and is automatically sized to fit the width of the form.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d52bf-126">Constante</span><span class="sxs-lookup"><span data-stu-id="d52bf-126">Constant</span></span></th>
<th><span data-ttu-id="d52bf-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="d52bf-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d52bf-128">vbAlignNone 0</span><span class="sxs-lookup"><span data-stu-id="d52bf-128">vbAlignNone 0</span></span></td>
<td><span data-ttu-id="d52bf-129">(Valor predeterminado en un formulario no MDI) Ninguno: el tamaño y la ubicación se pueden establecer en tiempo de diseño o en código.</span><span class="sxs-lookup"><span data-stu-id="d52bf-129">(Default in a non-MDI form) None—size and location can be set at design time or in code.</span></span> <span data-ttu-id="d52bf-130">La configuración se omite si el objeto está en un formulario MDI.</span><span class="sxs-lookup"><span data-stu-id="d52bf-130">The setting is ignored if the object is on an MDI form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d52bf-131">vbAlignTop 1</span><span class="sxs-lookup"><span data-stu-id="d52bf-131">vbAlignTop 1</span></span></td>
<td><span data-ttu-id="d52bf-132">(Valor predeterminado en un formulario MDI) Top: el objeto se encuentra en la parte superior del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</span><span class="sxs-lookup"><span data-stu-id="d52bf-132">(Default in an MDI form) Top—the object is at the top of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d52bf-133">vbAlignBottom 2</span><span class="sxs-lookup"><span data-stu-id="d52bf-133">vbAlignBottom 2</span></span></td>
<td><span data-ttu-id="d52bf-134">Inferior: el objeto se encuentra en la parte inferior del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</span><span class="sxs-lookup"><span data-stu-id="d52bf-134">Bottom—the object is at the bottom of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d52bf-135">vbAlignLeft 3</span><span class="sxs-lookup"><span data-stu-id="d52bf-135">vbAlignLeft 3</span></span></td>
<td><span data-ttu-id="d52bf-136">Left: el objeto está a la izquierda del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</span><span class="sxs-lookup"><span data-stu-id="d52bf-136">Left—the object is at the left of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d52bf-137">vbAlignRight 4</span><span class="sxs-lookup"><span data-stu-id="d52bf-137">vbAlignRight 4</span></span></td>
<td><span data-ttu-id="d52bf-138">Right: el objeto está a la derecha del formulario y su ancho es igual al valor de la propiedad ScaleWidth del formulario.</span><span class="sxs-lookup"><span data-stu-id="d52bf-138">Right—the object is at the right of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-139">Contenedor</span><span class="sxs-lookup"><span data-stu-id="d52bf-139">Container</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-140">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d52bf-140">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-141">Devuelve el contenedor de un control en un formulario.</span><span class="sxs-lookup"><span data-stu-id="d52bf-141">Returns the container of a control on a form.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-142">habilitado</span><span class="sxs-lookup"><span data-stu-id="d52bf-142">Enabled</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-143">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-144">Devuelve o establece un valor que determina si un formulario o un control puede responder a los eventos generados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d52bf-144">Returns or sets a value that determines whether a form or control can respond to user-generated events.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-145">Alto</span><span class="sxs-lookup"><span data-stu-id="d52bf-145">Height</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-146">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-147">Devuelve o establece el alto de un objeto.</span><span class="sxs-lookup"><span data-stu-id="d52bf-147">Returns or sets the height of an object.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-148">Identificador</span><span class="sxs-lookup"><span data-stu-id="d52bf-148">Hwnd</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d52bf-149">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-150">Devuelve un identificador a un formulario o un control.</span><span class="sxs-lookup"><span data-stu-id="d52bf-150">Returns a handle to a form or control.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-151">Left</span><span class="sxs-lookup"><span data-stu-id="d52bf-151">Left</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-152">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-152">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-153">Devuelve o establece la distancia entre el borde izquierdo interno de un objeto y el borde izquierdo de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="d52bf-153">Returns or sets the distance between the internal left edge of an object and the left edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-154">Nombre</span><span class="sxs-lookup"><span data-stu-id="d52bf-154">Name</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d52bf-155">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-156">Devuelve el nombre utilizado en el código para identificar un formulario, un control o un objeto de acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="d52bf-156">Returns the name used in code to identify a form, control, or data access object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-157">Parent</span><span class="sxs-lookup"><span data-stu-id="d52bf-157">Parent</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d52bf-158">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-159">Devuelve el formulario, objeto o colección que contiene un control u otro objeto o colección.</span><span class="sxs-lookup"><span data-stu-id="d52bf-159">Returns the form, object, or collection that contains a control or another object or collection.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-160">TabStop</span><span class="sxs-lookup"><span data-stu-id="d52bf-160">TabStop</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-161">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-161">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-162">Devuelve o establece un valor que indica si un usuario puede usar la tecla <strong>Tab</strong> para dar el foco a un objeto.</span><span class="sxs-lookup"><span data-stu-id="d52bf-162">Returns or sets a value that indicates whether a user can use the <strong>Tab</strong> key to give the focus to an object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-163">Superior</span><span class="sxs-lookup"><span data-stu-id="d52bf-163">Top</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-164">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-164">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-165">Devuelve o establece la distancia entre el borde interno superior de un objeto y el borde superior de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="d52bf-165">Returns or sets the distance between the internal top edge of an object and the top edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-166">Visible</span><span class="sxs-lookup"><span data-stu-id="d52bf-166">Visible</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-167">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-167">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-168">Devuelve o establece un valor que indica si un objeto está visible u oculto.</span><span class="sxs-lookup"><span data-stu-id="d52bf-168">Returns or sets a value that indicates whether an object is visible or hidden.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="d52bf-169">Ancho</span><span class="sxs-lookup"><span data-stu-id="d52bf-169">Width</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-170">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d52bf-170">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="d52bf-171">Devuelve o establece el ancho de un objeto.</span><span class="sxs-lookup"><span data-stu-id="d52bf-171">Returns or sets the width of an object.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d52bf-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d52bf-172">Requirements</span></span>



| <span data-ttu-id="d52bf-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="d52bf-173">Requirement</span></span> | <span data-ttu-id="d52bf-174">Value</span><span class="sxs-lookup"><span data-stu-id="d52bf-174">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d52bf-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d52bf-175">DLL</span></span><br/> | <dl> <span data-ttu-id="d52bf-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d52bf-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span></span> </dl> |



 

 
