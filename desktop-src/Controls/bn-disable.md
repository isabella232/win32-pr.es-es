---
title: Código de notificación de BN_DISABLE (Winuser. h)
description: Se envía cuando se deshabilita un botón.
ms.assetid: 5e2bb434-f20d-42f1-a9e9-46c4d10b8c7e
keywords:
- BN_DISABLE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faaba622c056366fe0c49683adc2c020a6302929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996114"
---
# <a name="bn_disable-notification-code"></a><span data-ttu-id="e56b5-104">BN \_ deshabilitar código de notificación</span><span class="sxs-lookup"><span data-stu-id="e56b5-104">BN\_DISABLE notification code</span></span>

<span data-ttu-id="e56b5-105">Se envía cuando se deshabilita un botón.</span><span class="sxs-lookup"><span data-stu-id="e56b5-105">Sent when a button is disabled.</span></span>

> [!Note]  
> <span data-ttu-id="e56b5-106">Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0.</span><span class="sxs-lookup"><span data-stu-id="e56b5-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="e56b5-107">Las aplicaciones deben usar el estilo de botón [**BS \_ OWNERDRAW**](button-styles.md) y la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="e56b5-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="e56b5-108">La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e56b5-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DISABLE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e56b5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e56b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56b5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e56b5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e56b5-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón.</span><span class="sxs-lookup"><span data-stu-id="e56b5-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="e56b5-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e56b5-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e56b5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e56b5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e56b5-114">Identificador del botón.</span><span class="sxs-lookup"><span data-stu-id="e56b5-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e56b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e56b5-115">Requirements</span></span>



| <span data-ttu-id="e56b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e56b5-116">Requirement</span></span> | <span data-ttu-id="e56b5-117">Value</span><span class="sxs-lookup"><span data-stu-id="e56b5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e56b5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e56b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e56b5-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e56b5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e56b5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e56b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e56b5-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e56b5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e56b5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e56b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e56b5-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e56b5-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

