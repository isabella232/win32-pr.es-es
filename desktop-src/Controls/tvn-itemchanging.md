---
title: Código de notificación de TVN_ITEMCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento están a punto de cambiar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534210"
---
# <a name="tvn_itemchanging-notification-code"></a><span data-ttu-id="1b313-105">Código de notificación de ITEMCHANGING de TVN \_</span><span class="sxs-lookup"><span data-stu-id="1b313-105">TVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="1b313-106">Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento están a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="1b313-106">Notifies a tree-view control's parent window that item attributes are about to change.</span></span> <span data-ttu-id="1b313-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1b313-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1b313-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b313-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b313-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b313-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b313-110">Puntero a una estructura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que describe el elemento que está cambiando.</span><span class="sxs-lookup"><span data-stu-id="1b313-110">Pointer to an [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that is changing.</span></span> <span data-ttu-id="1b313-111">El miembro **uChanged** se establece en el \_ Estado TVIF.</span><span class="sxs-lookup"><span data-stu-id="1b313-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b313-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b313-112">Return value</span></span>

<span data-ttu-id="1b313-113">Devuelve **false** para aceptar el cambio o **true** para evitar el cambio.</span><span class="sxs-lookup"><span data-stu-id="1b313-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b313-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b313-114">Requirements</span></span>



| <span data-ttu-id="1b313-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b313-115">Requirement</span></span> | <span data-ttu-id="1b313-116">Value</span><span class="sxs-lookup"><span data-stu-id="1b313-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b313-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b313-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1b313-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1b313-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b313-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b313-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1b313-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b313-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b313-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b313-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b313-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b313-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1b313-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1b313-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1b313-124">**TVN \_ ITEMCHANGINGW** (Unicode) y **TVN \_ ITEMCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1b313-124">**TVN\_ITEMCHANGINGW** (Unicode) and **TVN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1b313-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b313-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b313-126">TVN \_ ITEMCHANGED</span><span class="sxs-lookup"><span data-stu-id="1b313-126">TVN\_ITEMCHANGED</span></span>](tvn-itemchanged.md)
</dt> </dl>

 

 





