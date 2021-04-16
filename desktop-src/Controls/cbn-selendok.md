---
title: Código de notificación de CBN_SELENDOK (Winuser. h)
description: Se envía cuando el usuario selecciona un elemento de lista, o selecciona un elemento y, a continuación, cierra la lista. Indica que se va a procesar la selección del usuario. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- CBN_SELENDOK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658207"
---
# <a name="cbn_selendok-notification-code"></a><span data-ttu-id="d53dd-106">Código de notificación de SELENDOK de CBN \_</span><span class="sxs-lookup"><span data-stu-id="d53dd-106">CBN\_SELENDOK notification code</span></span>

<span data-ttu-id="d53dd-107">Se envía cuando el usuario selecciona un elemento de lista, o selecciona un elemento y, a continuación, cierra la lista.</span><span class="sxs-lookup"><span data-stu-id="d53dd-107">Sent when the user selects a list item, or selects an item and then closes the list.</span></span> <span data-ttu-id="d53dd-108">Indica que se va a procesar la selección del usuario.</span><span class="sxs-lookup"><span data-stu-id="d53dd-108">It indicates that the user's selection is to be processed.</span></span> <span data-ttu-id="d53dd-109">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d53dd-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d53dd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d53dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d53dd-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d53dd-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d53dd-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="d53dd-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d53dd-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="d53dd-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d53dd-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d53dd-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d53dd-115">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="d53dd-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d53dd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d53dd-116">Remarks</span></span>

<span data-ttu-id="d53dd-117">En un cuadro combinado con el [**estilo \_ simple CBS**](combo-box-styles.md) , el \_ código de notificación CBN SELENDOK se envía inmediatamente antes de cada código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="d53dd-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDOK notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d53dd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d53dd-118">Requirements</span></span>



| <span data-ttu-id="d53dd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d53dd-119">Requirement</span></span> | <span data-ttu-id="d53dd-120">Value</span><span class="sxs-lookup"><span data-stu-id="d53dd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d53dd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d53dd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d53dd-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d53dd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d53dd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d53dd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d53dd-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d53dd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d53dd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d53dd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d53dd-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d53dd-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d53dd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d53dd-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d53dd-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d53dd-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d53dd-129">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="d53dd-129">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="d53dd-130">CBN \_ SELENDCANCEL</span><span class="sxs-lookup"><span data-stu-id="d53dd-130">CBN\_SELENDCANCEL</span></span>](cbn-selendcancel.md)
</dt> <dt>

<span data-ttu-id="d53dd-131">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d53dd-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d53dd-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d53dd-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d53dd-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d53dd-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d53dd-134">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d53dd-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

