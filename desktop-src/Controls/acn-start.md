---
title: Código de notificación de ACN_START (commctrl. h)
description: Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha empezado a reproducirse. Este código de notificación se envía en forma de mensaje de \_ comando de WM.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801538"
---
# <a name="acn_start-notification-code"></a><span data-ttu-id="704e1-105">Código de notificación de inicio de ACN \_</span><span class="sxs-lookup"><span data-stu-id="704e1-105">ACN\_START notification code</span></span>

<span data-ttu-id="704e1-106">Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha empezado a reproducirse.</span><span class="sxs-lookup"><span data-stu-id="704e1-106">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="704e1-107">Este código de notificación se envía en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="704e1-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="704e1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="704e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="704e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="704e1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="704e1-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de animación.</span><span class="sxs-lookup"><span data-stu-id="704e1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="704e1-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="704e1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="704e1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="704e1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="704e1-113">**HWnd** que especifica el identificador del control de animación.</span><span class="sxs-lookup"><span data-stu-id="704e1-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="704e1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="704e1-114">Requirements</span></span>



| <span data-ttu-id="704e1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="704e1-115">Requirement</span></span> | <span data-ttu-id="704e1-116">Value</span><span class="sxs-lookup"><span data-stu-id="704e1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="704e1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="704e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="704e1-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="704e1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="704e1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="704e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="704e1-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="704e1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="704e1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="704e1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="704e1-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="704e1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

