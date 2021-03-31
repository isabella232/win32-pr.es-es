---
title: Código de notificación de STN_DISABLE (Winuser. h)
description: '\_Se envía el código de notificación de deshabilitación de STN cuando se deshabilita un control estático.'
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- STN_DISABLE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2763fce96b043ec6aebf5339a9f93d6fdf4a8abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149982"
---
# <a name="stn_disable-notification-code"></a><span data-ttu-id="c5406-104">STN \_ deshabilitar código de notificación</span><span class="sxs-lookup"><span data-stu-id="c5406-104">STN\_DISABLE notification code</span></span>

<span data-ttu-id="c5406-105">\_Se envía el código de notificación de deshabilitación de STN cuando se deshabilita un control estático.</span><span class="sxs-lookup"><span data-stu-id="c5406-105">The STN\_DISABLE notification code is sent when a static control is disabled.</span></span> <span data-ttu-id="c5406-106">El control estático debe tener el estilo [**SS \_ Notify**](static-control-styles.md) para recibir este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c5406-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="c5406-107">La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c5406-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c5406-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5406-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5406-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5406-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5406-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="c5406-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="c5406-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c5406-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c5406-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5406-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5406-113">Identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="c5406-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5406-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5406-114">Requirements</span></span>



| <span data-ttu-id="c5406-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5406-115">Requirement</span></span> | <span data-ttu-id="c5406-116">Value</span><span class="sxs-lookup"><span data-stu-id="c5406-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5406-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5406-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5406-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5406-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5406-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5406-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5406-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5406-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5406-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5406-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5406-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5406-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5406-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5406-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5406-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c5406-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5406-125">\_habilitación de STN</span><span class="sxs-lookup"><span data-stu-id="c5406-125">STN\_ENABLE</span></span>](stn-enable.md)
</dt> <dt>

<span data-ttu-id="c5406-126">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c5406-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5406-127">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="c5406-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="c5406-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="c5406-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c5406-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5406-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c5406-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5406-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c5406-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c5406-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

