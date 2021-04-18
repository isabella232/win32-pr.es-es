---
title: Código de notificación de TVN_DELETEITEM (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que se está eliminando un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490840"
---
# <a name="tvn_deleteitem-notification-code"></a><span data-ttu-id="7e91f-105">Código de notificación de TVN \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="7e91f-105">TVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="7e91f-106">Notifica a la ventana primaria de un control de vista de árbol que se está eliminando un elemento.</span><span class="sxs-lookup"><span data-stu-id="7e91f-106">Notifies a tree-view control's parent window that an item is being deleted.</span></span> <span data-ttu-id="7e91f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7e91f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="7e91f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e91f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e91f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e91f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e91f-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="7e91f-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="7e91f-111">El miembro **itemOld** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **hItem** e **lParam** contienen información válida sobre el elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="7e91f-111">The **itemOld** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem** and **lParam** members contain valid information about the item being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e91f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e91f-112">Return value</span></span>

<span data-ttu-id="7e91f-113">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="7e91f-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e91f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e91f-114">Remarks</span></span>

<span data-ttu-id="7e91f-115">Si el miembro **lParam** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) apunta a la memoria asignada por la aplicación, puede liberarla cuando reciba el código de \_ notificación TVN DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="7e91f-115">If the **lParam** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure points to memory allocated by your application, you can free it when you receive the TVN\_DELETEITEM notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e91f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e91f-116">Requirements</span></span>



| <span data-ttu-id="7e91f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e91f-117">Requirement</span></span> | <span data-ttu-id="7e91f-118">Value</span><span class="sxs-lookup"><span data-stu-id="7e91f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e91f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e91f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7e91f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e91f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e91f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e91f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7e91f-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e91f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e91f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e91f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e91f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e91f-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7e91f-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="7e91f-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7e91f-126">**TVN \_ DELETEITEMW** (Unicode) y **TVN \_ DELETEITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7e91f-126">**TVN\_DELETEITEMW** (Unicode) and **TVN\_DELETEITEMA** (ANSI)</span></span><br/>             |



 

 





