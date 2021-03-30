---
title: Código de notificación de NM_SETFOCUS (vista de lista) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- NM_SETFOCUS (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99cc84e76c0203a6e2930d3d9f50bc61a1e31395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079201"
---
# <a name="nm_setfocus-list-view-notification-code"></a><span data-ttu-id="b530c-105">NM \_ código de notificación de SETFOCUS (vista de lista)</span><span class="sxs-lookup"><span data-stu-id="b530c-105">NM\_SETFOCUS (list view) notification code</span></span>

<span data-ttu-id="b530c-106">Notifica a la ventana primaria de un control de vista de lista que el control ha recibido el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="b530c-106">Notifies a list-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="b530c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b530c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b530c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b530c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b530c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b530c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b530c-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="b530c-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b530c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b530c-111">Return value</span></span>

<span data-ttu-id="b530c-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="b530c-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b530c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b530c-113">Requirements</span></span>



| <span data-ttu-id="b530c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b530c-114">Requirement</span></span> | <span data-ttu-id="b530c-115">Value</span><span class="sxs-lookup"><span data-stu-id="b530c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b530c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b530c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b530c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b530c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b530c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b530c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b530c-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b530c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b530c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b530c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b530c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b530c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





