---
title: Código de notificación de CBN_EDITCHANGE (Winuser. h)
description: Se envía una vez que el usuario ha realizado una acción que puede haber alterado el texto en la parte del control de edición de un cuadro combinado.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- CBN_EDITCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658392"
---
# <a name="cbn_editchange-notification-code"></a><span data-ttu-id="7fbf6-104">Código de notificación de EDITCHANGE de CBN \_</span><span class="sxs-lookup"><span data-stu-id="7fbf6-104">CBN\_EDITCHANGE notification code</span></span>

<span data-ttu-id="7fbf6-105">Se envía una vez que el usuario ha realizado una acción que puede haber alterado el texto en la parte del control de edición de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="7fbf6-105">Sent after the user has taken an action that may have altered the text in the edit control portion of a combo box.</span></span> <span data-ttu-id="7fbf6-106">A diferencia del código de notificación de [CBN \_ EDITUPDATE](cbn-editupdate.md) , este código de notificación se envía cuando el sistema actualiza la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7fbf6-106">Unlike the [CBN\_EDITUPDATE](cbn-editupdate.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="7fbf6-107">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7fbf6-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7fbf6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fbf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbf6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fbf6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbf6-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="7fbf6-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="7fbf6-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7fbf6-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7fbf6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fbf6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbf6-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="7fbf6-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fbf6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fbf6-114">Remarks</span></span>

<span data-ttu-id="7fbf6-115">Si el cuadro combinado tiene el estilo [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , no se envía este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7fbf6-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbf6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbf6-116">Requirements</span></span>



| <span data-ttu-id="7fbf6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbf6-117">Requirement</span></span> | <span data-ttu-id="7fbf6-118">Value</span><span class="sxs-lookup"><span data-stu-id="7fbf6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbf6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fbf6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbf6-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7fbf6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7fbf6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fbf6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbf6-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fbf6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7fbf6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fbf6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fbf6-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf6-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbf6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fbf6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7fbf6-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7fbf6-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7fbf6-127">CBN \_ EDITUPDATE</span><span class="sxs-lookup"><span data-stu-id="7fbf6-127">CBN\_EDITUPDATE</span></span>](cbn-editupdate.md)
</dt> <dt>

<span data-ttu-id="7fbf6-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="7fbf6-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7fbf6-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7fbf6-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="7fbf6-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7fbf6-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7fbf6-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7fbf6-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

