---
title: Código de notificación de LBN_KILLFOCUS (Winuser. h)
description: Notifica a la aplicación que el cuadro de lista ha perdido el foco de teclado. La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de comando de WM \_ .
ms.assetid: ef927b56-3c46-4ae7-87df-13295cf175a8
keywords:
- LBN_KILLFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba424efc2518d359c3d031561aeafee8c0348b65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150898"
---
# <a name="lbn_killfocus-notification-code"></a><span data-ttu-id="cfb4e-105">Código de notificación de KILLFOCUS de LBN \_</span><span class="sxs-lookup"><span data-stu-id="cfb4e-105">LBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="cfb4e-106">Notifica a la aplicación que el cuadro de lista ha perdido el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="cfb4e-106">Notifies the application that the list box has lost the keyboard focus.</span></span> <span data-ttu-id="cfb4e-107">La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="cfb4e-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cfb4e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfb4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb4e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfb4e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb4e-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="cfb4e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="cfb4e-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="cfb4e-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="cfb4e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfb4e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb4e-113">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="cfb4e-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfb4e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfb4e-114">Requirements</span></span>



| <span data-ttu-id="cfb4e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb4e-115">Requirement</span></span> | <span data-ttu-id="cfb4e-116">Value</span><span class="sxs-lookup"><span data-stu-id="cfb4e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb4e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb4e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb4e-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cfb4e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cfb4e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb4e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb4e-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfb4e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfb4e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfb4e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb4e-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfb4e-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb4e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfb4e-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfb4e-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cfb4e-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cfb4e-125">LBN ( \_ SETFOCUS)</span><span class="sxs-lookup"><span data-stu-id="cfb4e-125">LBN\_SETFOCUS</span></span>](lbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="cfb4e-126">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="cfb4e-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="cfb4e-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cfb4e-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="cfb4e-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cfb4e-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cfb4e-129">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cfb4e-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

