---
title: Código de notificación de BN_CLICKED (Winuser. h)
description: Se envía cuando el usuario hace clic en un botón. La ventana primaria del botón recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- BN_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150070"
---
# <a name="bn_clicked-notification-code"></a><span data-ttu-id="0f7f1-105">BN \_ código de notificación en el que se hizo clic</span><span class="sxs-lookup"><span data-stu-id="0f7f1-105">BN\_CLICKED notification code</span></span>

<span data-ttu-id="0f7f1-106">Se envía cuando el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-106">Sent when the user clicks a button.</span></span>

<span data-ttu-id="0f7f1-107">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0f7f1-107">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0f7f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f7f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f7f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7f1-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="0f7f1-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0f7f1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f7f1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7f1-113">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-113">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f7f1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f7f1-114">Remarks</span></span>

<span data-ttu-id="0f7f1-115">Un botón deshabilitado no envía un \_ código de notificación con el BN clic a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-115">A disabled button does not send a BN\_CLICKED notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f7f1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f7f1-116">Requirements</span></span>



| <span data-ttu-id="0f7f1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f7f1-117">Requirement</span></span> | <span data-ttu-id="0f7f1-118">Value</span><span class="sxs-lookup"><span data-stu-id="0f7f1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7f1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f7f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f7f1-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0f7f1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0f7f1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f7f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f7f1-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f7f1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f7f1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f7f1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f7f1-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7f1-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f7f1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f7f1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f7f1-126">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="0f7f1-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0f7f1-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f7f1-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0f7f1-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f7f1-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0f7f1-129">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="0f7f1-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

