---
title: BN_DOUBLECLICKED de notificación (Winuser.h)
description: 'BN_DOUBLECLICKED de notificación: se envía cuando el usuario hace doble clic en un botón.'
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED código de notificación controles de Windows
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
ms.openlocfilehash: 64a11a4dec91a7a2f1d200c4c86c6989d846604a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104193"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="300f0-104">Código de notificación \_ DOUBLECLICKED de BN</span><span class="sxs-lookup"><span data-stu-id="300f0-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="300f0-105">Se envía cuando el usuario hace doble clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="300f0-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="300f0-106">Este código de notificación se envía automáticamente para los [**botones \_ BS USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)y [**BS \_ OWNERDRAW.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="300f0-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="300f0-107">Otros tipos de botón envían BN \_ DOUBLECLICKED solo si tienen el [**estilo \_ BS NOTIFY.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="300f0-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="300f0-108">La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="300f0-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="300f0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="300f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300f0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="300f0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="300f0-111">Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="300f0-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="300f0-112">[**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="300f0-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="300f0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="300f0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="300f0-114">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="300f0-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="300f0-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="300f0-115">Remarks</span></span>

<span data-ttu-id="300f0-116">BN \_ DOUBLECLICKED es el mismo que el código de [notificación \_ DBLCLK de BN.](bn-dblclk.md)</span><span class="sxs-lookup"><span data-stu-id="300f0-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="300f0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="300f0-117">Requirements</span></span>



| <span data-ttu-id="300f0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="300f0-118">Requirement</span></span> | <span data-ttu-id="300f0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="300f0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="300f0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="300f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="300f0-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="300f0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="300f0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="300f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="300f0-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="300f0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="300f0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="300f0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="300f0-125"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="300f0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

