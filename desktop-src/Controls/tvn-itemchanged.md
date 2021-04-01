---
title: Código de notificación de TVN_ITEMCHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento han cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905284"
---
# <a name="tvn_itemchanged-notification-code"></a><span data-ttu-id="45c21-105">Código de notificación de TVN \_ ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="45c21-105">TVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="45c21-106">Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento han cambiado.</span><span class="sxs-lookup"><span data-stu-id="45c21-106">Notifies a tree-view control's parent window that item attributes have changed.</span></span> <span data-ttu-id="45c21-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="45c21-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="45c21-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45c21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c21-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45c21-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45c21-110">Puntero a una estructura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que describe el elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="45c21-110">Pointer to a [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that changed.</span></span> <span data-ttu-id="45c21-111">El miembro **uChanged** se establece en el \_ Estado TVIF.</span><span class="sxs-lookup"><span data-stu-id="45c21-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c21-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45c21-112">Return value</span></span>

<span data-ttu-id="45c21-113">Devuelve **false** para aceptar el cambio o **true** para evitar el cambio.</span><span class="sxs-lookup"><span data-stu-id="45c21-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c21-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c21-114">Requirements</span></span>



| <span data-ttu-id="45c21-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c21-115">Requirement</span></span> | <span data-ttu-id="45c21-116">Value</span><span class="sxs-lookup"><span data-stu-id="45c21-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45c21-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45c21-117">Minimum supported client</span></span><br/> | <span data-ttu-id="45c21-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45c21-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45c21-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45c21-119">Minimum supported server</span></span><br/> | <span data-ttu-id="45c21-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="45c21-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45c21-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45c21-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="45c21-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c21-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="45c21-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="45c21-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="45c21-124">**TVN \_ ITEMCHANGEDW** (Unicode) y **TVN \_ ITEMCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="45c21-124">**TVN\_ITEMCHANGEDW** (Unicode) and **TVN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="45c21-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="45c21-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c21-126">TVN \_ ITEMCHANGING</span><span class="sxs-lookup"><span data-stu-id="45c21-126">TVN\_ITEMCHANGING</span></span>](tvn-itemchanging.md)
</dt> </dl>

 

 





