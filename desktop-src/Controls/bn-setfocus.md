---
title: Código de notificación de BN_SETFOCUS (Winuser. h)
description: Se envía cuando un botón recibe el foco de teclado. El botón debe tener el estilo de notificación BS \_ para enviar este código de notificación. La ventana primaria del botón recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- BN_SETFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb9204f5b23b62b6cee9fb2652a16d546f6ef62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656492"
---
# <a name="bn_setfocus-notification-code"></a><span data-ttu-id="fc8e5-106">Código de notificación de SETFOCUS de BN \_</span><span class="sxs-lookup"><span data-stu-id="fc8e5-106">BN\_SETFOCUS notification code</span></span>

<span data-ttu-id="fc8e5-107">Se envía cuando un botón recibe el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="fc8e5-107">Sent when a button receives the keyboard focus.</span></span> <span data-ttu-id="fc8e5-108">El botón debe tener el [**estilo \_ de notificación BS**](button-styles.md) para enviar este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="fc8e5-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="fc8e5-109">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="fc8e5-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fc8e5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc8e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc8e5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc8e5-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc8e5-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="fc8e5-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="fc8e5-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="fc8e5-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="fc8e5-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc8e5-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc8e5-115">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="fc8e5-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc8e5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc8e5-116">Requirements</span></span>



| <span data-ttu-id="fc8e5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc8e5-117">Requirement</span></span> | <span data-ttu-id="fc8e5-118">Value</span><span class="sxs-lookup"><span data-stu-id="fc8e5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8e5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc8e5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8e5-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fc8e5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc8e5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc8e5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8e5-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc8e5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc8e5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc8e5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc8e5-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8e5-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc8e5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc8e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8e5-126">BN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="fc8e5-126">BN\_KILLFOCUS</span></span>](bn-killfocus.md)
</dt> </dl>

 

