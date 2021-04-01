---
title: Código de notificación de TVN_BEGINRDRAG (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol sobre la iniciación de una operación de arrastrar y colocar con el botón secundario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997016"
---
# <a name="tvn_beginrdrag-notification-code"></a><span data-ttu-id="89afd-105">Código de notificación de BEGINRDRAG de TVN \_</span><span class="sxs-lookup"><span data-stu-id="89afd-105">TVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="89afd-106">Notifica a la ventana primaria de un control de vista de árbol sobre la iniciación de una operación de arrastrar y colocar con el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="89afd-106">Notifies a tree-view control's parent window about the initiation of a drag-and-drop operation involving the right mouse button.</span></span> <span data-ttu-id="89afd-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="89afd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="89afd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89afd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89afd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89afd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89afd-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="89afd-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="89afd-111">El miembro **itemNew** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida en los miembros **hItem**, **State** y **lParam** sobre el elemento que se va a arrastrar.</span><span class="sxs-lookup"><span data-stu-id="89afd-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information in the **hItem**, **state**, and **lParam** members about the item to be dragged.</span></span> <span data-ttu-id="89afd-112">El miembro **ptDrag** especifica las coordenadas de pantalla actuales del mouse.</span><span class="sxs-lookup"><span data-stu-id="89afd-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89afd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89afd-113">Return value</span></span>

<span data-ttu-id="89afd-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="89afd-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="89afd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89afd-115">Requirements</span></span>



| <span data-ttu-id="89afd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89afd-116">Requirement</span></span> | <span data-ttu-id="89afd-117">Value</span><span class="sxs-lookup"><span data-stu-id="89afd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89afd-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89afd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89afd-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="89afd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89afd-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89afd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89afd-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="89afd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89afd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89afd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89afd-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89afd-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="89afd-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="89afd-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="89afd-125">**TVN \_ BEGINRDRAGW** (Unicode) y **TVN \_ BEGINRDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="89afd-125">**TVN\_BEGINRDRAGW** (Unicode) and **TVN\_BEGINRDRAGA** (ANSI)</span></span><br/>             |



 

 





