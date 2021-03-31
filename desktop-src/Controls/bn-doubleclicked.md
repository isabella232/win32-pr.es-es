---
title: Código de notificación de BN_DOUBLECLICKED (Winuser. h)
description: Se envía cuando el usuario hace doble clic en un botón.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905108"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="031f4-104">Código de notificación de BN \_</span><span class="sxs-lookup"><span data-stu-id="031f4-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="031f4-105">Se envía cuando el usuario hace doble clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="031f4-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="031f4-106">Este código de notificación se envía automáticamente para los botones [**BS \_ USERBUTTON**](button-styles.md), [**BS \_**](button-styles.md)y [**BS \_**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="031f4-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="031f4-107">Otros tipos de botón envían BN \_ solo si tienen el estilo de [**\_ notificación BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="031f4-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="031f4-108">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="031f4-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="031f4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="031f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031f4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="031f4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="031f4-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="031f4-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="031f4-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="031f4-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="031f4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="031f4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="031f4-114">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="031f4-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="031f4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="031f4-115">Remarks</span></span>

<span data-ttu-id="031f4-116">BN al \_ es el mismo que el código de notificación [BN \_ DBLCLK](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="031f4-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="031f4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="031f4-117">Requirements</span></span>



| <span data-ttu-id="031f4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="031f4-118">Requirement</span></span> | <span data-ttu-id="031f4-119">Value</span><span class="sxs-lookup"><span data-stu-id="031f4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="031f4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="031f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="031f4-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="031f4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="031f4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="031f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="031f4-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="031f4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="031f4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="031f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="031f4-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="031f4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

