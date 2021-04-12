---
title: Código de notificación de LVN_DELETEITEM (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento está a punto de eliminarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009d39e78aa93d5c5230e9c1b06b84d2854a0d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151283"
---
# <a name="lvn_deleteitem-notification-code"></a><span data-ttu-id="dae99-105">Código de notificación de LVN \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="dae99-105">LVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="dae99-106">Notifica a la ventana primaria de un control de vista de lista que un elemento está a punto de eliminarse.</span><span class="sxs-lookup"><span data-stu-id="dae99-106">Notifies a list-view control's parent window that an item is about to be deleted.</span></span> <span data-ttu-id="dae99-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="dae99-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="dae99-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dae99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae99-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dae99-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dae99-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="dae99-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="dae99-111">El miembro **iItem** identifica el elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="dae99-111">The **iItem** member identifies the item being deleted.</span></span> <span data-ttu-id="dae99-112">Si el control no tiene el estilo **LVS \_ OWNERDATA** , *lParam* son los datos definidos por la aplicación asociados al elemento.</span><span class="sxs-lookup"><span data-stu-id="dae99-112">If the control does not have the **LVS\_OWNERDATA** style, then the *lParam* is the application-defined data associated with the item.</span></span> <span data-ttu-id="dae99-113">Todos los demás miembros de esta estructura son cero.</span><span class="sxs-lookup"><span data-stu-id="dae99-113">All other members of this structure are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae99-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dae99-114">Return value</span></span>

<span data-ttu-id="dae99-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dae99-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae99-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dae99-116">Remarks</span></span>

<span data-ttu-id="dae99-117">No agregue, elimine ni reorganice los elementos de la vista de lista mientras procesa este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="dae99-117">Do not add, delete, or rearrange items in the list view while processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae99-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae99-118">Requirements</span></span>



| <span data-ttu-id="dae99-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae99-119">Requirement</span></span> | <span data-ttu-id="dae99-120">Value</span><span class="sxs-lookup"><span data-stu-id="dae99-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dae99-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dae99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dae99-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dae99-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dae99-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dae99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dae99-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dae99-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dae99-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dae99-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dae99-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dae99-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





