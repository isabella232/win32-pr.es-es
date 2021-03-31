---
title: Código de notificación de CBN_EDITUPDATE (Winuser. h)
description: Se envía cuando la parte del control de edición de un cuadro combinado está a punto de mostrar el texto modificado.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- CBN_EDITUPDATE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151154"
---
# <a name="cbn_editupdate-notification-code"></a><span data-ttu-id="01148-104">Código de notificación de EDITUPDATE de CBN \_</span><span class="sxs-lookup"><span data-stu-id="01148-104">CBN\_EDITUPDATE notification code</span></span>

<span data-ttu-id="01148-105">Se envía cuando la parte del control de edición de un cuadro combinado está a punto de mostrar el texto modificado.</span><span class="sxs-lookup"><span data-stu-id="01148-105">Sent when the edit control portion of a combo box is about to display altered text.</span></span> <span data-ttu-id="01148-106">Este código de notificación se envía una vez que el control ha dado formato al texto, pero antes de que muestre el texto.</span><span class="sxs-lookup"><span data-stu-id="01148-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="01148-107">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="01148-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="01148-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01148-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01148-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01148-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01148-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="01148-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="01148-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="01148-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="01148-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01148-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01148-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="01148-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01148-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01148-114">Remarks</span></span>

<span data-ttu-id="01148-115">Si el cuadro combinado tiene el estilo [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , no se envía este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="01148-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="01148-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01148-116">Requirements</span></span>



| <span data-ttu-id="01148-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="01148-117">Requirement</span></span> | <span data-ttu-id="01148-118">Value</span><span class="sxs-lookup"><span data-stu-id="01148-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01148-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01148-119">Minimum supported client</span></span><br/> | <span data-ttu-id="01148-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="01148-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="01148-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01148-121">Minimum supported server</span></span><br/> | <span data-ttu-id="01148-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="01148-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01148-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01148-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="01148-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01148-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01148-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="01148-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="01148-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="01148-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="01148-127">CBN \_ EDITCHANGE</span><span class="sxs-lookup"><span data-stu-id="01148-127">CBN\_EDITCHANGE</span></span>](cbn-editchange.md)
</dt> <dt>

<span data-ttu-id="01148-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="01148-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="01148-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01148-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="01148-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01148-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="01148-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="01148-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

