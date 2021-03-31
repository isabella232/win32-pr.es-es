---
title: Código de notificación de STN_CLICKED (Winuser. h)
description: El \_ código de notificación en el que se hace clic en STN se envía cuando el usuario hace clic en un control estático que tenga el \_ estilo SS Notify. La ventana primaria del control recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905026"
---
# <a name="stn_clicked-notification-code"></a><span data-ttu-id="35cd9-105">STN \_ código de notificación en el que se hizo clic</span><span class="sxs-lookup"><span data-stu-id="35cd9-105">STN\_CLICKED notification code</span></span>

<span data-ttu-id="35cd9-106">El \_ código de notificación en el que se hace clic en STN se envía cuando el usuario hace clic en un control estático que tenga el estilo [**SS \_ Notify**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="35cd9-106">The STN\_CLICKED notification code is sent when the user clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="35cd9-107">La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="35cd9-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="35cd9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35cd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35cd9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35cd9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35cd9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="35cd9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="35cd9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="35cd9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="35cd9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35cd9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35cd9-113">Identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="35cd9-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35cd9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35cd9-114">Requirements</span></span>



| <span data-ttu-id="35cd9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35cd9-115">Requirement</span></span> | <span data-ttu-id="35cd9-116">Value</span><span class="sxs-lookup"><span data-stu-id="35cd9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35cd9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35cd9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35cd9-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="35cd9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35cd9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35cd9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35cd9-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="35cd9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35cd9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35cd9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35cd9-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35cd9-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35cd9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="35cd9-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="35cd9-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="35cd9-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35cd9-125">STN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="35cd9-125">STN\_DBLCLK</span></span>](stn-dblclk.md)
</dt> <dt>

<span data-ttu-id="35cd9-126">**Vista**</span><span class="sxs-lookup"><span data-stu-id="35cd9-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35cd9-127">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="35cd9-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="35cd9-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="35cd9-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="35cd9-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35cd9-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="35cd9-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35cd9-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="35cd9-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="35cd9-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

