---
title: Código de notificación de LBN_SETFOCUS (Winuser. h)
description: Notifica a la aplicación que el cuadro de lista ha recibido el foco de teclado. La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de comando de WM \_ .
ms.assetid: d9e5e035-98a5-4ece-ba40-6d341c101859
keywords:
- LBN_SETFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e56043982cec6606f7c78d3469ab2583951f88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905263"
---
# <a name="lbn_setfocus-notification-code"></a><span data-ttu-id="e37e2-105">Código de notificación de SETFOCUS de LBN \_</span><span class="sxs-lookup"><span data-stu-id="e37e2-105">LBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="e37e2-106">Notifica a la aplicación que el cuadro de lista ha recibido el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="e37e2-106">Notifies the application that the list box has received the keyboard focus.</span></span> <span data-ttu-id="e37e2-107">La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e37e2-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e37e2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e37e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e37e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e37e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e37e2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="e37e2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="e37e2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e37e2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e37e2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e37e2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e37e2-113">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="e37e2-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e37e2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e37e2-114">Requirements</span></span>



| <span data-ttu-id="e37e2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e37e2-115">Requirement</span></span> | <span data-ttu-id="e37e2-116">Value</span><span class="sxs-lookup"><span data-stu-id="e37e2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e37e2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e37e2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e37e2-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e37e2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e37e2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e37e2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e37e2-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e37e2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e37e2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e37e2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e37e2-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e37e2-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e37e2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e37e2-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="e37e2-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e37e2-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e37e2-125">LBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="e37e2-125">LBN\_KILLFOCUS</span></span>](lbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="e37e2-126">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="e37e2-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e37e2-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e37e2-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e37e2-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e37e2-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e37e2-129">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e37e2-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

