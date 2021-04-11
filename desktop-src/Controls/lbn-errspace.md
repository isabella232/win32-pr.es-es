---
title: Código de notificación de LBN_ERRSPACE (Winuser. h)
description: Notifica a la aplicación que el cuadro de lista no puede asignar memoria suficiente para satisfacer una solicitud concreta. La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de comando de WM \_ .
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- LBN_ERRSPACE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274537"
---
# <a name="lbn_errspace-notification-code"></a><span data-ttu-id="9ae30-105">Código de notificación de ERRSPACE de LBN \_</span><span class="sxs-lookup"><span data-stu-id="9ae30-105">LBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="9ae30-106">Notifica a la aplicación que el cuadro de lista no puede asignar memoria suficiente para satisfacer una solicitud concreta.</span><span class="sxs-lookup"><span data-stu-id="9ae30-106">Notifies the application that the list box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="9ae30-107">La ventana primaria del cuadro de lista recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="9ae30-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9ae30-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ae30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ae30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae30-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="9ae30-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="9ae30-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="9ae30-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9ae30-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ae30-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae30-113">Identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="9ae30-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ae30-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ae30-114">Requirements</span></span>



| <span data-ttu-id="9ae30-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae30-115">Requirement</span></span> | <span data-ttu-id="9ae30-116">Value</span><span class="sxs-lookup"><span data-stu-id="9ae30-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae30-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ae30-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae30-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9ae30-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9ae30-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ae30-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae30-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ae30-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ae30-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ae30-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ae30-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ae30-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae30-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ae30-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ae30-124">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="9ae30-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="9ae30-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ae30-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9ae30-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ae30-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9ae30-127">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9ae30-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

