---
title: Código de notificación de STN_ENABLE (Winuser. h)
description: El \_ código de notificación de habilitación de STN se envía cuando se habilita un control estático.
ms.assetid: daac2ed3-c7cd-46f8-abfa-78754b277ef4
keywords:
- STN_ENABLE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- STN_ENABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9cc21e884a8a7e907054daa48a21678efa65e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489220"
---
# <a name="stn_enable-notification-code"></a><span data-ttu-id="7e986-104">STN \_ Habilitar código de notificación</span><span class="sxs-lookup"><span data-stu-id="7e986-104">STN\_ENABLE notification code</span></span>

<span data-ttu-id="7e986-105">El \_ código de notificación de habilitación de STN se envía cuando se habilita un control estático.</span><span class="sxs-lookup"><span data-stu-id="7e986-105">The STN\_ENABLE notification code is sent when a static control is enabled.</span></span> <span data-ttu-id="7e986-106">El control estático debe tener el estilo [**SS \_ Notify**](static-control-styles.md) para recibir este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7e986-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="7e986-107">La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7e986-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_ENABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7e986-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e986-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e986-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e986-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="7e986-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="7e986-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7e986-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7e986-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e986-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e986-113">Identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="7e986-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e986-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e986-114">Requirements</span></span>



| <span data-ttu-id="7e986-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e986-115">Requirement</span></span> | <span data-ttu-id="7e986-116">Value</span><span class="sxs-lookup"><span data-stu-id="7e986-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e986-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e986-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7e986-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e986-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7e986-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e986-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7e986-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e986-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e986-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e986-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e986-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e986-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e986-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e986-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e986-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7e986-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e986-125">Deshabilitación de STN \_</span><span class="sxs-lookup"><span data-stu-id="7e986-125">STN\_DISABLE</span></span>](stn-disable.md)
</dt> <dt>

<span data-ttu-id="7e986-126">**Vista**</span><span class="sxs-lookup"><span data-stu-id="7e986-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7e986-127">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="7e986-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="7e986-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="7e986-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7e986-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e986-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="7e986-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e986-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7e986-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7e986-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

