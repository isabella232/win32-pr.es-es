---
title: BN_DBLCLK de notificación (Winuser.h)
description: 'BN_DBLCLK de notificación: se envía cuando el usuario hace doble clic en un botón.'
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK código de notificación Controles de Windows
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
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096853"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="51649-104">Código de notificación \_ DBLCLK de BN</span><span class="sxs-lookup"><span data-stu-id="51649-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="51649-105">Se envía cuando el usuario hace doble clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="51649-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="51649-106">Este código de notificación se envía automáticamente para los [**botones \_ BS USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)y [**BS \_ OWNERDRAW.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="51649-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="51649-107">Otros tipos de botón envían \_ DBLCLK de BN solo si tienen el [**estilo \_ NOTIFY de BS.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="51649-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="51649-108">La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="51649-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="51649-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51649-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51649-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51649-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51649-111">Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="51649-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="51649-112">[**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="51649-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="51649-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51649-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51649-114">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="51649-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51649-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51649-115">Remarks</span></span>

<span data-ttu-id="51649-116">\_DBLCLK de BN es igual que el [código de notificación \_ DOUBLECLICKED de BN.](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="51649-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51649-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51649-117">Requirements</span></span>



| <span data-ttu-id="51649-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="51649-118">Requirement</span></span> | <span data-ttu-id="51649-119">Valor</span><span class="sxs-lookup"><span data-stu-id="51649-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51649-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51649-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51649-121">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="51649-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51649-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51649-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51649-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="51649-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51649-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51649-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="51649-125"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="51649-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51649-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="51649-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="51649-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="51649-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51649-128">BN \_ EN EL QUE SE HIZO CLIC</span><span class="sxs-lookup"><span data-stu-id="51649-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="51649-129">BN \_ DOUBLECLICKED</span><span class="sxs-lookup"><span data-stu-id="51649-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="51649-130">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="51649-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="51649-131">**COMANDO \_ WM**</span><span class="sxs-lookup"><span data-stu-id="51649-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

