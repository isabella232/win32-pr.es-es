---
title: Código de notificación de TVN_SELCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que la selección está a punto de cambiar de un elemento a otro. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079260"
---
# <a name="tvn_selchanging-notification-code"></a><span data-ttu-id="c6c0c-105">Código de notificación de SELCHANGING de TVN \_</span><span class="sxs-lookup"><span data-stu-id="c6c0c-105">TVN\_SELCHANGING notification code</span></span>

<span data-ttu-id="c6c0c-106">Notifica a la ventana primaria de un control de vista de árbol que la selección está a punto de cambiar de un elemento a otro.</span><span class="sxs-lookup"><span data-stu-id="c6c0c-106">Notifies a tree-view control's parent window that the selection is about to change from one item to another.</span></span> <span data-ttu-id="c6c0c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c6c0c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="c6c0c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6c0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c0c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6c0c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c0c-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="c6c0c-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="c6c0c-111">Los miembros **itemOld** y **itemNew** contienen información válida sobre el elemento seleccionado actualmente y el elemento recién seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c6c0c-111">The **itemOld** and **itemNew** members contain valid information about the currently selected item and the newly selected item.</span></span> <span data-ttu-id="c6c0c-112">El miembro de **acción** indica si una acción del mouse o del teclado está provocando la modificación de la selección.</span><span class="sxs-lookup"><span data-stu-id="c6c0c-112">The **action** member indicates whether a mouse or keyboard action is causing the selection to change.</span></span> <span data-ttu-id="c6c0c-113">Para obtener una lista de los valores posibles, vea la descripción del código de notificación [ \_ SELCHANGED de TVN](tvn-selchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="c6c0c-113">For a list of possible values, see the description of the [TVN\_SELCHANGED](tvn-selchanged.md) notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c0c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6c0c-114">Return value</span></span>

<span data-ttu-id="c6c0c-115">Devuelve **true** para evitar que la selección cambie.</span><span class="sxs-lookup"><span data-stu-id="c6c0c-115">Returns **TRUE** to prevent the selection from changing.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c0c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6c0c-116">Remarks</span></span>

<span data-ttu-id="c6c0c-117">Cuando responde a este código de notificación, las aplicaciones no deben eliminar los elementos que obtienen o pierden la selección.</span><span class="sxs-lookup"><span data-stu-id="c6c0c-117">When responding to this notification code, applications should not delete the items that are gaining or losing the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c0c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6c0c-118">Requirements</span></span>



| <span data-ttu-id="c6c0c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c0c-119">Requirement</span></span> | <span data-ttu-id="c6c0c-120">Value</span><span class="sxs-lookup"><span data-stu-id="c6c0c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c0c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6c0c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c0c-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6c0c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6c0c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6c0c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c0c-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6c0c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6c0c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6c0c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c0c-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c0c-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c6c0c-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c6c0c-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c6c0c-128">**TVN \_ SELCHANGINGW** (Unicode) y **TVN \_ SELCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c6c0c-128">**TVN\_SELCHANGINGW** (Unicode) and **TVN\_SELCHANGINGA** (ANSI)</span></span><br/>           |



 

 





