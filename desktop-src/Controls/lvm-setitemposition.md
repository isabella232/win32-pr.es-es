---
title: Mensaje de LVM_SETITEMPOSITION (commctrl. h)
description: Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños). Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemPosition de ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905291"
---
# <a name="lvm_setitemposition-message"></a><span data-ttu-id="bc400-105">\_Mensaje SETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="bc400-105">LVM\_SETITEMPOSITION message</span></span>

<span data-ttu-id="bc400-106">Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños).</span><span class="sxs-lookup"><span data-stu-id="bc400-106">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="bc400-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemPosition de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .</span><span class="sxs-lookup"><span data-stu-id="bc400-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc400-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc400-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc400-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc400-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc400-110">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="bc400-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="bc400-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc400-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc400-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la nueva posición x de la esquina superior izquierda del elemento, en coordenadas de la vista.</span><span class="sxs-lookup"><span data-stu-id="bc400-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new x-position of the item's upper-left corner, in view coordinates.</span></span> <span data-ttu-id="bc400-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la nueva posición y de la esquina superior izquierda del elemento, en coordenadas de la vista.</span><span class="sxs-lookup"><span data-stu-id="bc400-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new y-position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc400-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc400-114">Return value</span></span>

<span data-ttu-id="bc400-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc400-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc400-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc400-116">Remarks</span></span>

<span data-ttu-id="bc400-117">Si el control de vista de lista tiene el estilo [**LVS \_ AutoArrange**](list-view-window-styles.md) , los elementos del control de vista de lista se organizan una vez establecida la posición del elemento.</span><span class="sxs-lookup"><span data-stu-id="bc400-117">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, the items in the list-view control are arranged after the position of the item is set.</span></span>

<span data-ttu-id="bc400-118">En Windows Vista, el envío de este mensaje a un control de vista de lista con el estilo [**LVS \_ AutoArrange**](list-view-window-styles.md) no hace nada y el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="bc400-118">On Windows Vista, sending this message to a list-view control with the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style does nothing, and the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc400-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc400-119">Requirements</span></span>



| <span data-ttu-id="bc400-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc400-120">Requirement</span></span> | <span data-ttu-id="bc400-121">Value</span><span class="sxs-lookup"><span data-stu-id="bc400-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc400-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc400-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bc400-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bc400-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc400-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc400-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bc400-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc400-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc400-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc400-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc400-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc400-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

