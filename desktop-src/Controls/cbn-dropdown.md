---
title: Código de notificación de CBN_DROPDOWN (Winuser. h)
description: Se envía cuando el cuadro de lista de un cuadro combinado está a punto de hacerse visible. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658239"
---
# <a name="cbn_dropdown-notification-code"></a><span data-ttu-id="cf675-105">\_Código de notificación de desplegable CBN</span><span class="sxs-lookup"><span data-stu-id="cf675-105">CBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="cf675-106">Se envía cuando el cuadro de lista de un cuadro combinado está a punto de hacerse visible.</span><span class="sxs-lookup"><span data-stu-id="cf675-106">Sent when the list box of a combo box is about to be made visible.</span></span> <span data-ttu-id="cf675-107">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="cf675-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cf675-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf675-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf675-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf675-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf675-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cf675-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="cf675-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="cf675-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="cf675-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf675-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf675-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cf675-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf675-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf675-114">Remarks</span></span>

<span data-ttu-id="cf675-115">Este código de notificación solo se envía si el cuadro combinado tiene el estilo de la [**\_ lista desplegable CBS**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="cf675-115">This notification code is only sent if the combo box has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf675-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf675-116">Requirements</span></span>



| <span data-ttu-id="cf675-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf675-117">Requirement</span></span> | <span data-ttu-id="cf675-118">Value</span><span class="sxs-lookup"><span data-stu-id="cf675-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf675-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf675-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf675-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf675-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cf675-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf675-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf675-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf675-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cf675-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf675-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf675-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf675-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf675-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf675-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf675-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cf675-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf675-127">CBN \_ primer plano</span><span class="sxs-lookup"><span data-stu-id="cf675-127">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

<span data-ttu-id="cf675-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="cf675-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="cf675-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf675-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="cf675-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf675-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cf675-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cf675-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

