---
title: Código de notificación de STN_DBLCLK (Winuser. h)
description: El \_ código de notificación STN DBLCLK se envía cuando el usuario hace doble clic en un control estático que tenga el \_ estilo SS Notify. La ventana primaria del control recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079073"
---
# <a name="stn_dblclk-notification-code"></a><span data-ttu-id="8913b-105">Código de notificación de DBLCLK de STN \_</span><span class="sxs-lookup"><span data-stu-id="8913b-105">STN\_DBLCLK notification code</span></span>

<span data-ttu-id="8913b-106">El \_ código de notificación STN DBLCLK se envía cuando el usuario hace doble clic en un control estático que tenga el estilo [**SS \_ Notify**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8913b-106">The STN\_DBLCLK notification code is sent when the user double-clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="8913b-107">La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8913b-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8913b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8913b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8913b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8913b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8913b-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="8913b-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="8913b-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="8913b-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8913b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8913b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8913b-113">Identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="8913b-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8913b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8913b-114">Requirements</span></span>



| <span data-ttu-id="8913b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8913b-115">Requirement</span></span> | <span data-ttu-id="8913b-116">Value</span><span class="sxs-lookup"><span data-stu-id="8913b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8913b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8913b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8913b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8913b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8913b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8913b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8913b-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8913b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8913b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8913b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8913b-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8913b-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8913b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8913b-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="8913b-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8913b-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8913b-125">STN \_ clic</span><span class="sxs-lookup"><span data-stu-id="8913b-125">STN\_CLICKED</span></span>](stn-clicked.md)
</dt> <dt>

<span data-ttu-id="8913b-126">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8913b-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8913b-127">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="8913b-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="8913b-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="8913b-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="8913b-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8913b-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8913b-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8913b-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8913b-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8913b-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

