---
title: Código de notificación de CBN_ERRSPACE (Winuser. h)
description: Se envía cuando un cuadro combinado no puede asignar suficiente memoria para satisfacer una solicitud concreta. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: c1c19c40-fc88-47d0-9676-7a267a48ae98
keywords:
- CBN_ERRSPACE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74e46e4435a03a0233ce6591d3c36cefb4d880a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151153"
---
# <a name="cbn_errspace-notification-code"></a><span data-ttu-id="34dfe-105">Código de notificación de ERRSPACE de CBN \_</span><span class="sxs-lookup"><span data-stu-id="34dfe-105">CBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="34dfe-106">Se envía cuando un cuadro combinado no puede asignar suficiente memoria para satisfacer una solicitud concreta.</span><span class="sxs-lookup"><span data-stu-id="34dfe-106">Sent when a combo box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="34dfe-107">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="34dfe-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="34dfe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34dfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34dfe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34dfe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34dfe-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="34dfe-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="34dfe-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="34dfe-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="34dfe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34dfe-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34dfe-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="34dfe-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34dfe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34dfe-114">Requirements</span></span>



| <span data-ttu-id="34dfe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="34dfe-115">Requirement</span></span> | <span data-ttu-id="34dfe-116">Value</span><span class="sxs-lookup"><span data-stu-id="34dfe-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34dfe-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34dfe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="34dfe-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="34dfe-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="34dfe-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34dfe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="34dfe-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34dfe-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34dfe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34dfe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="34dfe-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34dfe-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34dfe-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="34dfe-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="34dfe-124">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="34dfe-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="34dfe-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34dfe-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="34dfe-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34dfe-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="34dfe-127">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34dfe-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

