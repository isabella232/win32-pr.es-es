---
title: Código de notificación de BN_DBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en un botón.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079137"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="2046f-104">Código de notificación de DBLCLK de BN \_</span><span class="sxs-lookup"><span data-stu-id="2046f-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="2046f-105">Se envía cuando el usuario hace doble clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="2046f-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="2046f-106">Este código de notificación se envía automáticamente para los botones [**BS \_ USERBUTTON**](button-styles.md), [**BS \_**](button-styles.md)y [**BS \_**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2046f-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="2046f-107">Otros tipos de botón envían BN \_ DBLCLK solo si tienen el estilo de [**\_ notificación de BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2046f-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="2046f-108">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2046f-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="2046f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2046f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2046f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2046f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2046f-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="2046f-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="2046f-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="2046f-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2046f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2046f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2046f-114">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="2046f-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2046f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2046f-115">Remarks</span></span>

<span data-ttu-id="2046f-116">BN \_ DBLCLK es el mismo que el código de notificación de [BN \_ ](bn-doubleclicked.md) .</span><span class="sxs-lookup"><span data-stu-id="2046f-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2046f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2046f-117">Requirements</span></span>



| <span data-ttu-id="2046f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2046f-118">Requirement</span></span> | <span data-ttu-id="2046f-119">Value</span><span class="sxs-lookup"><span data-stu-id="2046f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2046f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2046f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2046f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2046f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2046f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2046f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2046f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2046f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2046f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2046f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2046f-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2046f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2046f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2046f-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="2046f-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2046f-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2046f-128">BN \_ clic</span><span class="sxs-lookup"><span data-stu-id="2046f-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="2046f-129">BN \_</span><span class="sxs-lookup"><span data-stu-id="2046f-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="2046f-130">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="2046f-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2046f-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2046f-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

