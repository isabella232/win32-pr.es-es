---
title: Código de notificación de ACN_STOP (commctrl. h)
description: Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha dejado de reproducirse. Este código de notificación se envía en forma de mensaje de \_ comando de WM.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079079"
---
# <a name="acn_stop-notification-code"></a><span data-ttu-id="b71ee-105">ACN \_ código de notificación de detención</span><span class="sxs-lookup"><span data-stu-id="b71ee-105">ACN\_STOP notification code</span></span>

<span data-ttu-id="b71ee-106">Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha dejado de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="b71ee-106">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="b71ee-107">Este código de notificación se envía en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b71ee-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b71ee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b71ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b71ee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b71ee-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b71ee-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de animación.</span><span class="sxs-lookup"><span data-stu-id="b71ee-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="b71ee-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="b71ee-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b71ee-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b71ee-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b71ee-113">**HWnd** que especifica el identificador del control de animación.</span><span class="sxs-lookup"><span data-stu-id="b71ee-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b71ee-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b71ee-114">Requirements</span></span>



| <span data-ttu-id="b71ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b71ee-115">Requirement</span></span> | <span data-ttu-id="b71ee-116">Value</span><span class="sxs-lookup"><span data-stu-id="b71ee-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b71ee-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b71ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b71ee-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b71ee-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b71ee-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b71ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b71ee-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b71ee-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b71ee-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b71ee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b71ee-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b71ee-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

