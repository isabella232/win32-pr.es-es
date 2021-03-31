---
title: Código de notificación de CBN_SELENDCANCEL (Winuser. h)
description: Se envía cuando el usuario selecciona un elemento, pero selecciona otro control o cierra el cuadro de diálogo. Indica que la selección inicial del usuario se va a omitir. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803434"
---
# <a name="cbn_selendcancel-notification-code"></a><span data-ttu-id="fa991-106">Código de notificación de SELENDCANCEL de CBN \_</span><span class="sxs-lookup"><span data-stu-id="fa991-106">CBN\_SELENDCANCEL notification code</span></span>

<span data-ttu-id="fa991-107">Se envía cuando el usuario selecciona un elemento, pero selecciona otro control o cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fa991-107">Sent when the user selects an item, but then selects another control or closes the dialog box.</span></span> <span data-ttu-id="fa991-108">Indica que la selección inicial del usuario se va a omitir.</span><span class="sxs-lookup"><span data-stu-id="fa991-108">It indicates the user's initial selection is to be ignored.</span></span> <span data-ttu-id="fa991-109">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="fa991-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fa991-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa991-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa991-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa991-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa991-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="fa991-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="fa991-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="fa991-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="fa991-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa991-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa991-115">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="fa991-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa991-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa991-116">Remarks</span></span>

<span data-ttu-id="fa991-117">En un cuadro combinado con el [**estilo \_ simple CBS**](combo-box-styles.md) , \_ no se envía el código de notificación SELENDCANCEL de CBN.</span><span class="sxs-lookup"><span data-stu-id="fa991-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDCANCEL notification code is not sent.</span></span> <span data-ttu-id="fa991-118">El código de notificación de [ \_ SELENDOK de CBN](cbn-selendok.md) se envía inmediatamente antes de cada código de notificación de [CBN \_ SELCHANGE](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="fa991-118">The [CBN\_SELENDOK](cbn-selendok.md) notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa991-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa991-119">Requirements</span></span>



| <span data-ttu-id="fa991-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa991-120">Requirement</span></span> | <span data-ttu-id="fa991-121">Value</span><span class="sxs-lookup"><span data-stu-id="fa991-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa991-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa991-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa991-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fa991-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa991-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa991-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa991-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa991-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa991-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa991-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa991-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa991-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa991-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa991-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa991-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="fa991-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa991-130">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="fa991-130">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="fa991-131">CBN \_ SELENDOK</span><span class="sxs-lookup"><span data-stu-id="fa991-131">CBN\_SELENDOK</span></span>](cbn-selendok.md)
</dt> <dt>

<span data-ttu-id="fa991-132">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="fa991-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="fa991-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fa991-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fa991-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fa991-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fa991-135">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="fa991-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

