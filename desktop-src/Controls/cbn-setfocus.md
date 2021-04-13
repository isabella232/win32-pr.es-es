---
title: Código de notificación de CBN_SETFOCUS (Winuser. h)
description: Se envía cuando un cuadro combinado recibe el foco de teclado. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 8072edc6-aedc-4daf-80df-d3acd82fcffa
keywords:
- CBN_SETFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885bbaebac0a79fc600cbcc2b7864cbdfd19ea93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359874"
---
# <a name="cbn_setfocus-notification-code"></a><span data-ttu-id="a3621-105">Código de notificación de SETFOCUS de CBN \_</span><span class="sxs-lookup"><span data-stu-id="a3621-105">CBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="a3621-106">Se envía cuando un cuadro combinado recibe el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="a3621-106">Sent when a combo box receives the keyboard focus.</span></span> <span data-ttu-id="a3621-107">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a3621-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a3621-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3621-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3621-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3621-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3621-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="a3621-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="a3621-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="a3621-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a3621-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3621-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3621-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="a3621-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3621-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3621-114">Requirements</span></span>



| <span data-ttu-id="a3621-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3621-115">Requirement</span></span> | <span data-ttu-id="a3621-116">Value</span><span class="sxs-lookup"><span data-stu-id="a3621-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3621-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3621-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3621-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a3621-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a3621-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3621-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3621-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3621-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3621-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3621-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3621-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3621-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3621-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3621-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3621-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a3621-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a3621-125">CBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="a3621-125">CBN\_KILLFOCUS</span></span>](cbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="a3621-126">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="a3621-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a3621-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3621-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a3621-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3621-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a3621-129">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a3621-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

