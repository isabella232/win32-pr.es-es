---
title: Código de notificación de BN_PAINT (Winuser. h)
description: Se envía cuando se debe pintar un botón.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078878"
---
# <a name="bn_paint-notification-code"></a><span data-ttu-id="229a4-104">Código de notificación de Paint de BN \_</span><span class="sxs-lookup"><span data-stu-id="229a4-104">BN\_PAINT notification code</span></span>

<span data-ttu-id="229a4-105">Se envía cuando se debe pintar un botón.</span><span class="sxs-lookup"><span data-stu-id="229a4-105">Sent when a button should be painted.</span></span>

> [!Note]  
> <span data-ttu-id="229a4-106">Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0.</span><span class="sxs-lookup"><span data-stu-id="229a4-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="229a4-107">Las aplicaciones deben usar el estilo de botón [**BS \_ OWNERDRAW**](button-styles.md) y la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="229a4-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="229a4-108">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="229a4-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PAINT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="229a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="229a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="229a4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="229a4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="229a4-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="229a4-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="229a4-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="229a4-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="229a4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="229a4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="229a4-114">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="229a4-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="229a4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="229a4-115">Requirements</span></span>



| <span data-ttu-id="229a4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="229a4-116">Requirement</span></span> | <span data-ttu-id="229a4-117">Value</span><span class="sxs-lookup"><span data-stu-id="229a4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="229a4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="229a4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="229a4-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="229a4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="229a4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="229a4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="229a4-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="229a4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="229a4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="229a4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="229a4-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="229a4-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

