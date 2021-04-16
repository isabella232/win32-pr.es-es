---
title: Código de notificación de EN_ALIGNRTL (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que la dirección del párrafo cambió de derecha a izquierda. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ comando de WM.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- EN_ALIGNRTL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489988"
---
# <a name="en_alignrtl-notification-code"></a><span data-ttu-id="d4836-105">\_Código de notificación en ALIGNRTL</span><span class="sxs-lookup"><span data-stu-id="d4836-105">EN\_ALIGNRTL notification code</span></span>

<span data-ttu-id="d4836-106">Notifica a la ventana primaria de un control Rich Edit que la dirección del párrafo cambió de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="d4836-106">Notifies a rich edit control's parent window that the paragraph direction changed to right-to-left.</span></span> <span data-ttu-id="d4836-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d4836-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="d4836-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4836-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4836-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4836-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4836-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d4836-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="d4836-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="d4836-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d4836-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4836-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4836-113">Identificador del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d4836-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4836-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4836-114">Return value</span></span>

<span data-ttu-id="d4836-115">Este código de notificación no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d4836-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4836-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4836-116">Requirements</span></span>



| <span data-ttu-id="d4836-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4836-117">Requirement</span></span> | <span data-ttu-id="d4836-118">Value</span><span class="sxs-lookup"><span data-stu-id="d4836-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4836-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4836-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4836-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d4836-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4836-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4836-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4836-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4836-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4836-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4836-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4836-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4836-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4836-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4836-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d4836-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d4836-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d4836-127">**EN \_ ALIGNLTR**</span><span class="sxs-lookup"><span data-stu-id="d4836-127">**EN\_ALIGNLTR**</span></span>](en-alignltr.md)
</dt> <dt>

<span data-ttu-id="d4836-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d4836-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d4836-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4836-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d4836-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4836-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d4836-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d4836-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

