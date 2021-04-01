---
title: Código de notificación de LVN_KEYDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se ha presionado una tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- LVN_KEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997183"
---
# <a name="lvn_keydown-notification-code"></a><span data-ttu-id="cc77d-105">\_Código de notificación KEYDOWN de LVN</span><span class="sxs-lookup"><span data-stu-id="cc77d-105">LVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="cc77d-106">Notifica a la ventana primaria de un control de vista de lista que se ha presionado una tecla.</span><span class="sxs-lookup"><span data-stu-id="cc77d-106">Notifies a list-view control's parent window that a key has been pressed.</span></span> <span data-ttu-id="cc77d-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cc77d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cc77d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc77d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc77d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc77d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc77d-110">Puntero a una estructura [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="cc77d-110">Pointer to an [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc77d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc77d-111">Return value</span></span>

<span data-ttu-id="cc77d-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cc77d-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc77d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc77d-113">Requirements</span></span>



| <span data-ttu-id="cc77d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc77d-114">Requirement</span></span> | <span data-ttu-id="cc77d-115">Value</span><span class="sxs-lookup"><span data-stu-id="cc77d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc77d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc77d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cc77d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc77d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc77d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc77d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cc77d-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc77d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc77d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc77d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc77d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc77d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





