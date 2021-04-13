---
title: Código de notificación de BN_PUSHED (Winuser. h)
description: Se envía cuando el estado de inserción de un botón se establece en insertado.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359699"
---
# <a name="bn_pushed-notification-code"></a><span data-ttu-id="aefb5-104">\_Código de notificación push BN</span><span class="sxs-lookup"><span data-stu-id="aefb5-104">BN\_PUSHED notification code</span></span>

<span data-ttu-id="aefb5-105">Se envía cuando el estado de inserción de un botón se establece en insertado.</span><span class="sxs-lookup"><span data-stu-id="aefb5-105">Sent when the push state of a button is set to pushed.</span></span>

> [!Note]  
> <span data-ttu-id="aefb5-106">Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0.</span><span class="sxs-lookup"><span data-stu-id="aefb5-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="aefb5-107">Las aplicaciones deben usar el estilo de botón [**BS \_ OWNERDRAW**](button-styles.md) y la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="aefb5-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="aefb5-108">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="aefb5-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="aefb5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aefb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aefb5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aefb5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aefb5-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="aefb5-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="aefb5-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="aefb5-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="aefb5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aefb5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aefb5-114">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="aefb5-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aefb5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aefb5-115">Remarks</span></span>

<span data-ttu-id="aefb5-116">BN \_ Push es el mismo que el código de notificación [BN \_ HILITE](bn-hilite.md) .</span><span class="sxs-lookup"><span data-stu-id="aefb5-116">BN\_PUSHED is the same as the [BN\_HILITE](bn-hilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aefb5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aefb5-117">Requirements</span></span>



| <span data-ttu-id="aefb5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aefb5-118">Requirement</span></span> | <span data-ttu-id="aefb5-119">Value</span><span class="sxs-lookup"><span data-stu-id="aefb5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aefb5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aefb5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aefb5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aefb5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aefb5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aefb5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aefb5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="aefb5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aefb5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aefb5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aefb5-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aefb5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aefb5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="aefb5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aefb5-127">**BN no \_ presionado**</span><span class="sxs-lookup"><span data-stu-id="aefb5-127">**BN\_UNPUSHED**</span></span>](bn-unpushed.md)
</dt> </dl>

 

