---
title: Código de notificación de CBN_CLOSEUP (Winuser. h)
description: Se envía cuando se ha cerrado el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151207"
---
# <a name="cbn_closeup-notification-code"></a><span data-ttu-id="4c863-105">Código de notificación de primer plano de CBN \_</span><span class="sxs-lookup"><span data-stu-id="4c863-105">CBN\_CLOSEUP notification code</span></span>

<span data-ttu-id="4c863-106">Se envía cuando se ha cerrado el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="4c863-106">Sent when the list box of a combo box has been closed.</span></span> <span data-ttu-id="4c863-107">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="4c863-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4c863-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c863-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c863-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c863-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="4c863-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="4c863-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="4c863-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="4c863-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c863-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c863-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="4c863-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c863-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c863-114">Remarks</span></span>

<span data-ttu-id="4c863-115">Si el usuario ha cambiado la selección actual, el cuadro combinado también enviará el código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) cuando se cierre la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="4c863-115">If the user changed the current selection, the combo box also sends the [CBN\_SELCHANGE](cbn-selchange.md) notification code when the drop-down list closes.</span></span> <span data-ttu-id="4c863-116">En general, no puede predecir el orden en el que se enviarán los códigos de notificación.</span><span class="sxs-lookup"><span data-stu-id="4c863-116">In general, you cannot predict the order in which notification codes will be sent.</span></span> <span data-ttu-id="4c863-117">En concreto, un código de notificación de CBN \_ SELCHANGE puede producirse antes o después de un código de notificación de CBN \_ primer plano.</span><span class="sxs-lookup"><span data-stu-id="4c863-117">In particular, a CBN\_SELCHANGE notification code may occur either before or after a CBN\_CLOSEUP notification code.</span></span>

<span data-ttu-id="4c863-118">Para ejecutar un proceso específico cada vez que el usuario selecciona un elemento de lista, puede controlar el código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) o CBN \_ primer plano.</span><span class="sxs-lookup"><span data-stu-id="4c863-118">To execute a specific process each time the user selects a list item, you can handle either the [CBN\_SELCHANGE](cbn-selchange.md) or CBN\_CLOSEUP notification code.</span></span> <span data-ttu-id="4c863-119">Normalmente, se espera el \_ código de notificación primer plano de CBN antes de procesar un cambio en la selección actual.</span><span class="sxs-lookup"><span data-stu-id="4c863-119">Typically, you would wait for the CBN\_CLOSEUP notification code before processing a change in the current selection.</span></span> <span data-ttu-id="4c863-120">Esto puede ser especialmente importante si se requiere una cantidad significativa de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="4c863-120">This can be particularly important if a significant amount of processing is required.</span></span>

<span data-ttu-id="4c863-121">Este código de notificación no se envía a un cuadro combinado que tenga el estilo [**\_ simple CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4c863-121">This notification code is not sent to a combo box that has the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c863-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c863-122">Requirements</span></span>



| <span data-ttu-id="4c863-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c863-123">Requirement</span></span> | <span data-ttu-id="4c863-124">Value</span><span class="sxs-lookup"><span data-stu-id="4c863-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c863-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c863-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4c863-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4c863-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4c863-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c863-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4c863-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c863-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c863-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c863-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c863-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c863-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c863-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c863-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c863-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4c863-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4c863-133">\_lista desplegable CBN</span><span class="sxs-lookup"><span data-stu-id="4c863-133">CBN\_DROPDOWN</span></span>](cbn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="4c863-134">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="4c863-134">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="4c863-135">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="4c863-135">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4c863-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c863-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="4c863-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c863-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4c863-138">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4c863-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

