---
title: Código de notificación de BN_KILLFOCUS (Winuser. h)
description: Se envía cuando un botón pierde el foco del teclado. El botón debe tener el estilo de notificación BS \_ para enviar este código de notificación. La ventana primaria del botón recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489646"
---
# <a name="bn_killfocus-notification-code"></a><span data-ttu-id="0d05e-106">Código de notificación de KILLFOCUS de BN \_</span><span class="sxs-lookup"><span data-stu-id="0d05e-106">BN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="0d05e-107">Se envía cuando un botón pierde el foco del teclado.</span><span class="sxs-lookup"><span data-stu-id="0d05e-107">Sent when a button loses the keyboard focus.</span></span> <span data-ttu-id="0d05e-108">El botón debe tener el [**estilo \_ de notificación BS**](button-styles.md) para enviar este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="0d05e-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="0d05e-109">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0d05e-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0d05e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d05e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d05e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d05e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d05e-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="0d05e-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="0d05e-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="0d05e-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0d05e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d05e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d05e-115">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="0d05e-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d05e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d05e-116">Requirements</span></span>



| <span data-ttu-id="0d05e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d05e-117">Requirement</span></span> | <span data-ttu-id="0d05e-118">Value</span><span class="sxs-lookup"><span data-stu-id="0d05e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d05e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d05e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0d05e-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d05e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d05e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d05e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0d05e-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d05e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d05e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d05e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d05e-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d05e-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d05e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d05e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d05e-126">BN ( \_ SETFOCUS)</span><span class="sxs-lookup"><span data-stu-id="0d05e-126">BN\_SETFOCUS</span></span>](bn-setfocus.md)
</dt> </dl>

 

