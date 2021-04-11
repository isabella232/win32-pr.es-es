---
title: Código de notificación de EN_ALIGNLTR (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que la dirección del párrafo ha cambiado a de izquierda a derecha. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ comando de WM.
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- EN_ALIGNLTR controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55c20a9ae4efb3ba5758ed0740b20b8b57f3877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079210"
---
# <a name="en_alignltr-notification-code"></a><span data-ttu-id="1c1c9-105">\_Código de notificación en ALIGNLTR</span><span class="sxs-lookup"><span data-stu-id="1c1c9-105">EN\_ALIGNLTR notification code</span></span>

<span data-ttu-id="1c1c9-106">Notifica a la ventana primaria de un control Rich Edit que la dirección del párrafo ha cambiado a de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="1c1c9-106">Notifies a rich edit control's parent window that the paragraph direction has changed to left-to-right.</span></span> <span data-ttu-id="1c1c9-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="1c1c9-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1c1c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c1c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c1c9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c1c9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1c1c9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="1c1c9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="1c1c9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1c1c9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c1c9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c1c9-113">Identificador del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1c1c9-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1c9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c1c9-114">Return value</span></span>

<span data-ttu-id="1c1c9-115">Este código de notificación no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1c1c9-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1c9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c1c9-116">Requirements</span></span>



| <span data-ttu-id="1c1c9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c1c9-117">Requirement</span></span> | <span data-ttu-id="1c1c9-118">Value</span><span class="sxs-lookup"><span data-stu-id="1c1c9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1c9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c1c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1c9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1c1c9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c1c9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c1c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1c9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c1c9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c1c9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c1c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c1c9-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1c9-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1c9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c1c9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c1c9-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1c1c9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1c1c9-127">**EN \_ ALIGNRTL**</span><span class="sxs-lookup"><span data-stu-id="1c1c9-127">**EN\_ALIGNRTL**</span></span>](en-alignrtl.md)
</dt> <dt>

<span data-ttu-id="1c1c9-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="1c1c9-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="1c1c9-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1c1c9-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1c1c9-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1c1c9-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1c1c9-131">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1c1c9-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

