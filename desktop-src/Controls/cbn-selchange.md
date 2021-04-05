---
title: Código de notificación de CBN_SELCHANGE (Winuser. h)
description: Se envía cuando el usuario cambia la selección actual en el cuadro de lista de un cuadro combinado.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997114"
---
# <a name="cbn_selchange-notification-code"></a><span data-ttu-id="acbd9-104">Código de notificación de SELCHANGE de CBN \_</span><span class="sxs-lookup"><span data-stu-id="acbd9-104">CBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="acbd9-105">Se envía cuando el usuario cambia la selección actual en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="acbd9-105">Sent when the user changes the current selection in the list box of a combo box.</span></span> <span data-ttu-id="acbd9-106">El usuario puede cambiar la selección haciendo clic en el cuadro de lista o usando las teclas de dirección.</span><span class="sxs-lookup"><span data-stu-id="acbd9-106">The user can change the selection by clicking in the list box or by using the arrow keys.</span></span> <span data-ttu-id="acbd9-107">La ventana primaria del cuadro combinado recibe este código de notificación en forma de mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="acbd9-107">The parent window of the combo box receives this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="acbd9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acbd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acbd9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acbd9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acbd9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="acbd9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="acbd9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="acbd9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="acbd9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acbd9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acbd9-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="acbd9-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acbd9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acbd9-114">Remarks</span></span>

<span data-ttu-id="acbd9-115">Para obtener el índice de la selección actual, envíe el mensaje [**CB \_ GETCURSEL**](cb-getcursel.md) al control.</span><span class="sxs-lookup"><span data-stu-id="acbd9-115">To get the index of the current selection, send the [**CB\_GETCURSEL**](cb-getcursel.md) message to the control.</span></span>

<span data-ttu-id="acbd9-116">El \_ código de notificación CBN SELCHANGE no se envía cuando la selección actual se establece mediante el mensaje [**CB \_ SETCURSEL**](cb-setcursel.md) .</span><span class="sxs-lookup"><span data-stu-id="acbd9-116">The CBN\_SELCHANGE notification code is not sent when the current selection is set using the [**CB\_SETCURSEL**](cb-setcursel.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="acbd9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acbd9-117">Requirements</span></span>



| <span data-ttu-id="acbd9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="acbd9-118">Requirement</span></span> | <span data-ttu-id="acbd9-119">Value</span><span class="sxs-lookup"><span data-stu-id="acbd9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acbd9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acbd9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="acbd9-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="acbd9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="acbd9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acbd9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="acbd9-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="acbd9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="acbd9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acbd9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="acbd9-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acbd9-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbd9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="acbd9-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="acbd9-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="acbd9-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="acbd9-128">CBN \_ primer plano</span><span class="sxs-lookup"><span data-stu-id="acbd9-128">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

[<span data-ttu-id="acbd9-129">CBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="acbd9-129">CBN\_DBLCLK</span></span>](cbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="acbd9-130">**CB \_ GETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="acbd9-130">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="acbd9-131">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="acbd9-131">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

<span data-ttu-id="acbd9-132">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="acbd9-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="acbd9-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="acbd9-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="acbd9-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="acbd9-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="acbd9-135">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="acbd9-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

