---
title: Código de notificación de TVN_BEGINDRAG (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que se está iniciando una operación de arrastrar y colocar que implique el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905285"
---
# <a name="tvn_begindrag-notification-code"></a><span data-ttu-id="d5147-105">Código de notificación de BEGINDRAG de TVN \_</span><span class="sxs-lookup"><span data-stu-id="d5147-105">TVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="d5147-106">Notifica a la ventana primaria de un control de vista de árbol que se está iniciando una operación de arrastrar y colocar que implique el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="d5147-106">Notifies a tree-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="d5147-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d5147-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="d5147-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5147-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5147-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5147-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5147-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="d5147-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="d5147-111">El miembro **itemNew** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento que se está arrastrando en los miembros **hItem**, **State** y **lParam** .</span><span class="sxs-lookup"><span data-stu-id="d5147-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being dragged in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="d5147-112">El miembro **ptDrag** especifica las coordenadas de pantalla actuales del mouse.</span><span class="sxs-lookup"><span data-stu-id="d5147-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5147-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5147-113">Return value</span></span>

<span data-ttu-id="d5147-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d5147-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5147-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5147-115">Remarks</span></span>

<span data-ttu-id="d5147-116">Un control de vista de árbol con el [**estilo \_ DISABLEDRAGDROP de TV**](tree-view-control-window-styles.md) no envía este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="d5147-116">A tree-view control that has the [**TVS\_DISABLEDRAGDROP**](tree-view-control-window-styles.md) style does not send this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5147-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5147-117">Requirements</span></span>



| <span data-ttu-id="d5147-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5147-118">Requirement</span></span> | <span data-ttu-id="d5147-119">Value</span><span class="sxs-lookup"><span data-stu-id="d5147-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5147-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5147-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5147-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5147-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5147-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5147-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5147-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5147-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5147-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5147-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5147-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5147-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d5147-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d5147-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5147-127">**TVN \_ BEGINDRAGW** (Unicode) y **TVN \_ BEGINDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d5147-127">**TVN\_BEGINDRAGW** (Unicode) and **TVN\_BEGINDRAGA** (ANSI)</span></span><br/>               |



 

 





