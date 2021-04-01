---
title: Código de notificación de LBN_SELCANCEL (Winuser. h)
description: Notifica a la aplicación que el usuario ha cancelado la selección en un cuadro de lista. La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de comando de WM \_ .
ms.assetid: 82e39f22-090e-4dda-8ddc-6a1fe4704fc7
keywords:
- LBN_SELCANCEL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LBN_SELCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c192fbdfdb7a351d51993bee89b9b6ec3dab387
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996919"
---
# <a name="lbn_selcancel-notification-code"></a><span data-ttu-id="70fc3-105">Código de notificación de SELCANCEL de LBN \_</span><span class="sxs-lookup"><span data-stu-id="70fc3-105">LBN\_SELCANCEL notification code</span></span>

<span data-ttu-id="70fc3-106">Notifica a la aplicación que el usuario ha cancelado la selección en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="70fc3-106">Notifies the application that the user has canceled the selection in a list box.</span></span> <span data-ttu-id="70fc3-107">La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="70fc3-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="70fc3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70fc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70fc3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70fc3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70fc3-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="70fc3-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="70fc3-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="70fc3-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="70fc3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70fc3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70fc3-113">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="70fc3-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70fc3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70fc3-114">Remarks</span></span>

<span data-ttu-id="70fc3-115">Este código de notificación solo se envía mediante un cuadro de lista que tiene el estilo de [**\_ notificación L BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="70fc3-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="70fc3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70fc3-116">Requirements</span></span>



| <span data-ttu-id="70fc3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="70fc3-117">Requirement</span></span> | <span data-ttu-id="70fc3-118">Value</span><span class="sxs-lookup"><span data-stu-id="70fc3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70fc3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70fc3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70fc3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70fc3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="70fc3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70fc3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70fc3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="70fc3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70fc3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70fc3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="70fc3-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70fc3-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70fc3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="70fc3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="70fc3-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="70fc3-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="70fc3-127">**LB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="70fc3-127">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="70fc3-128">LBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="70fc3-128">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="70fc3-129">LBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="70fc3-129">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="70fc3-130">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="70fc3-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="70fc3-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70fc3-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="70fc3-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70fc3-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="70fc3-133">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="70fc3-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

