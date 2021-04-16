---
title: Código de notificación de CBN_DBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en una cadena en el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- CBN_DBLCLK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658401"
---
# <a name="cbn_dblclk-notification-code"></a><span data-ttu-id="db010-105">Código de notificación de DBLCLK de CBN \_</span><span class="sxs-lookup"><span data-stu-id="db010-105">CBN\_DBLCLK notification code</span></span>

<span data-ttu-id="db010-106">Se envía cuando el usuario hace doble clic en una cadena en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="db010-106">Sent when the user double-clicks a string in the list box of a combo box.</span></span> <span data-ttu-id="db010-107">La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="db010-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="db010-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db010-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db010-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db010-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db010-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="db010-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="db010-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="db010-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="db010-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db010-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db010-113">Identificador del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="db010-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db010-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db010-114">Remarks</span></span>

<span data-ttu-id="db010-115">Este código de notificación solo se produce para un cuadro combinado con el estilo [**\_ simple CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="db010-115">This notification code occurs only for a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="db010-116">En un cuadro combinado con la [**lista \_ desplegable CBS**](combo-box-styles.md) o el estilo de [**\_ DROPDOWNLIST de CBS**](combo-box-styles.md) , no se puede producir un doble clic porque un solo clic cierra el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="db010-116">In a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, a double-click cannot occur because a single click closes the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="db010-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db010-117">Requirements</span></span>



| <span data-ttu-id="db010-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db010-118">Requirement</span></span> | <span data-ttu-id="db010-119">Value</span><span class="sxs-lookup"><span data-stu-id="db010-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db010-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db010-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db010-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db010-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db010-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db010-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db010-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db010-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db010-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db010-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db010-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db010-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db010-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="db010-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="db010-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="db010-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="db010-128">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="db010-128">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="db010-129">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="db010-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="db010-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db010-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="db010-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db010-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="db010-132">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="db010-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

