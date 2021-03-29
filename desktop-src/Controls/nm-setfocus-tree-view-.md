---
title: Código de notificación de NM_SETFOCUS (vista de árbol) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 4bdd6cd2-afd3-4c0b-914b-8fff55e474a9
keywords:
- Código de notificación de NM_SETFOCUS (vista de árbol) controles de Windows
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
ms.openlocfilehash: 1b9e24d95b95b3c66fe43920f780b2e8d0f66679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905308"
---
# <a name="nm_setfocus-tree-view-notification-code"></a><span data-ttu-id="73096-105">NM \_ código de notificación de SETFOCUS (vista de árbol)</span><span class="sxs-lookup"><span data-stu-id="73096-105">NM\_SETFOCUS (tree view) notification code</span></span>

<span data-ttu-id="73096-106">Notifica a la ventana primaria de un control de vista de árbol que el control ha recibido el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="73096-106">Notifies a tree-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="73096-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="73096-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="73096-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73096-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73096-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73096-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73096-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="73096-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73096-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73096-111">Return value</span></span>

<span data-ttu-id="73096-112">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="73096-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="73096-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73096-113">Requirements</span></span>



| <span data-ttu-id="73096-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="73096-114">Requirement</span></span> | <span data-ttu-id="73096-115">Value</span><span class="sxs-lookup"><span data-stu-id="73096-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73096-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73096-116">Minimum supported client</span></span><br/> | <span data-ttu-id="73096-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73096-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73096-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73096-118">Minimum supported server</span></span><br/> | <span data-ttu-id="73096-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="73096-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73096-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73096-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="73096-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73096-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





