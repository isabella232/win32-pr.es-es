---
title: Mensaje de LVM_SETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Establece los estilos extendidos en los controles de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetExtendedListViewStyle o ListView \_ SetExtendedListViewStyleEx de ListView.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995937"
---
# <a name="lvm_setextendedlistviewstyle-message"></a><span data-ttu-id="61fdf-105">\_Mensaje SETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="61fdf-105">LVM\_SETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="61fdf-106">Establece los estilos extendidos en los controles de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="61fdf-106">Sets extended styles in list-view controls.</span></span> <span data-ttu-id="61fdf-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) o [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) de ListView.</span><span class="sxs-lookup"><span data-stu-id="61fdf-107">You can send this message explicitly or use the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) or [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61fdf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61fdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61fdf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61fdf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61fdf-110">Valor **DWORD** que especifica los estilos de *lParam* que se van a ver afectados.</span><span class="sxs-lookup"><span data-stu-id="61fdf-110">**DWORD** value that specifies which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="61fdf-111">Este parámetro puede ser una combinación de [**estilos de List-View extendidos**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="61fdf-111">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="61fdf-112">Solo se cambiarán los estilos extendidos de *wParam* .</span><span class="sxs-lookup"><span data-stu-id="61fdf-112">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="61fdf-113">Todos los demás estilos se conservarán tal como están.</span><span class="sxs-lookup"><span data-stu-id="61fdf-113">All other styles will be maintained as they are.</span></span> <span data-ttu-id="61fdf-114">Si este parámetro es cero, se verán afectados todos los estilos de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="61fdf-114">If this parameter is zero, all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="61fdf-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61fdf-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61fdf-116">Valor **DWORD** que especifica los estilos extendidos de control de vista de lista que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="61fdf-116">**DWORD** value that specifies the extended list-view control styles to set.</span></span> <span data-ttu-id="61fdf-117">Este parámetro puede ser una combinación de [**estilos de List-View extendidos**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="61fdf-117">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="61fdf-118">Los estilos que no están establecidos, pero que se especifican en *wParam*, se quitan.</span><span class="sxs-lookup"><span data-stu-id="61fdf-118">Styles that are not set, but that are specified in *wParam*, are removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61fdf-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61fdf-119">Return value</span></span>

<span data-ttu-id="61fdf-120">Devuelve un valor **DWORD** que contiene los estilos de control extendidos anteriores de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="61fdf-120">Returns a **DWORD** value that contains the previous extended list-view control styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="61fdf-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61fdf-121">Remarks</span></span>

<span data-ttu-id="61fdf-122">El parámetro *wParam* permite modificar uno o más estilos extendidos sin tener que recuperar primero los estilos existentes.</span><span class="sxs-lookup"><span data-stu-id="61fdf-122">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="61fdf-123">Por ejemplo, si pasa [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **LVS \_ ex \_ FULLROWSELECT** , pero el resto de los estilos permanecerán iguales.</span><span class="sxs-lookup"><span data-stu-id="61fdf-123">For example, if you pass [**LVS\_EX\_FULLROWSELECT**](extended-list-view-styles.md) for *wParam* and 0 for *lParam*, the **LVS\_EX\_FULLROWSELECT** style will be cleared but all other styles will remain the same.</span></span>

<span data-ttu-id="61fdf-124">Por motivos de compatibilidad con versiones anteriores, la macro [**\_ SetExtendedListViewStyle de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) no se ha actualizado para usar *wParam*.</span><span class="sxs-lookup"><span data-stu-id="61fdf-124">For backward compatibility reasons, the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) macro has not been updated to use *wParam*.</span></span> <span data-ttu-id="61fdf-125">Para usar el valor *wParam* , use la [**macro \_ SetExtendedListViewStyleEx de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="61fdf-125">To use the *wParam* value, use the [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

<span data-ttu-id="61fdf-126">Cuando se usa este mensaje para establecer el [**estilo \_ \_ casillas de LVS ex**](extended-list-view-styles.md) , se descartará cualquier índice de imagen de estado establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="61fdf-126">When you use this message to set the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style, any previously set state image index will be discarded.</span></span> <span data-ttu-id="61fdf-127">Todas las casillas se inicializarán en estado desactivado.</span><span class="sxs-lookup"><span data-stu-id="61fdf-127">All check boxes will be initialized to the unchecked state.</span></span> <span data-ttu-id="61fdf-128">El índice de la imagen de estado se encuentra en los bits 12 a 15 del miembro **State** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="61fdf-128">The state image index is contained in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="61fdf-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61fdf-129">Requirements</span></span>



| <span data-ttu-id="61fdf-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="61fdf-130">Requirement</span></span> | <span data-ttu-id="61fdf-131">Value</span><span class="sxs-lookup"><span data-stu-id="61fdf-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61fdf-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61fdf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="61fdf-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="61fdf-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61fdf-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61fdf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="61fdf-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="61fdf-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61fdf-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61fdf-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="61fdf-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61fdf-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





