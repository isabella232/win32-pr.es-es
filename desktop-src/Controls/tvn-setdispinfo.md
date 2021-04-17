---
title: Código de notificación de TVN_SETDISPINFO (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que debe actualizar la información que mantiene sobre un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656485"
---
# <a name="tvn_setdispinfo-notification-code"></a><span data-ttu-id="c9c6a-105">Código de notificación de SETDISPINFO de TVN \_</span><span class="sxs-lookup"><span data-stu-id="c9c6a-105">TVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="c9c6a-106">Notifica a la ventana primaria de un control de vista de árbol que debe actualizar la información que mantiene sobre un elemento.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-106">Notifies a tree-view control's parent window that it must update the information it maintains about an item.</span></span> <span data-ttu-id="c9c6a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c6a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="c9c6a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9c6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c6a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9c6a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c6a-110">Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) que describe el elemento que se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure that describes the item being updated.</span></span> <span data-ttu-id="c9c6a-111">El miembro **hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica el elemento que se va a actualizar y el miembro **Mask** especifica los atributos del elemento que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-111">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure specifies the item being updated, and the **mask** member specifies which attributes of the item are being updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c6a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9c6a-112">Return value</span></span>

<span data-ttu-id="c9c6a-113">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c6a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9c6a-114">Remarks</span></span>

<span data-ttu-id="c9c6a-115">Si el miembro **miembros pszText** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor LPSTR TEXTCALLBACK, el control envía esta notificación para establecer el texto del elemento.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-115">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification to set the item's text.</span></span> <span data-ttu-id="c9c6a-116">En este caso, el miembro de **máscara** de *lParam* tendrá establecido el \_ indicador de texto TVIF.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-116">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>

<span data-ttu-id="c9c6a-117">Si el miembro **iImage** o **iSelectedImage** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) del elemento es el \_ valor I IMAGECALLBACK, el control envía esta notificación para recuperar el índice de la imagen del icono que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-117">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification to retrieve the index of the icon image to display.</span></span> <span data-ttu-id="c9c6a-118">En este caso, el miembro de **máscara** de *lParam* tendrá la \_ marca TVIF o TVIF \_ SELECTEDIMAGE establecida.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-118">In this case, the **mask** member of *lParam* will have the TVIF\_IMAGE or TVIF\_SELECTEDIMAGE flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c6a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9c6a-119">Requirements</span></span>



| <span data-ttu-id="c9c6a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9c6a-120">Requirement</span></span> | <span data-ttu-id="c9c6a-121">Value</span><span class="sxs-lookup"><span data-stu-id="c9c6a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c6a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9c6a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9c6a-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9c6a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9c6a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9c6a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9c6a-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9c6a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9c6a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9c6a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9c6a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c6a-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c9c6a-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c9c6a-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c9c6a-129">**TVN \_ SETDISPINFOW** (Unicode) y **TVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c9c6a-129">**TVN\_SETDISPINFOW** (Unicode) and **TVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c9c6a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9c6a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c6a-131">**TVITEM**</span><span class="sxs-lookup"><span data-stu-id="c9c6a-131">**TVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[<span data-ttu-id="c9c6a-132">**TVITEMEX**</span><span class="sxs-lookup"><span data-stu-id="c9c6a-132">**TVITEMEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[<span data-ttu-id="c9c6a-133">TVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="c9c6a-133">TVN\_GETDISPINFO</span></span>](tvn-getdispinfo.md)
</dt> </dl>

 

 





