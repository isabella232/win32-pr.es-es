---
title: Código de notificación de EN_ALIGN_LTR_EC (Winuser. h)
description: Se envía cuando el usuario ha cambiado la dirección del control de edición de izquierda a derecha. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de comando de WM \_ .
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- EN_ALIGN_LTR_EC controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801892"
---
# <a name="en_align_ltr_ec-notification-code"></a><span data-ttu-id="7ccc4-105">EN \_ el \_ código de notificación de EC de alineación LTR \_</span><span class="sxs-lookup"><span data-stu-id="7ccc4-105">EN\_ALIGN\_LTR\_EC notification code</span></span>

<span data-ttu-id="7ccc4-106">Se envía cuando el usuario ha cambiado la dirección del control de edición de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="7ccc4-106">Sent when the user has changed the edit control direction to left-to-right.</span></span> <span data-ttu-id="7ccc4-107">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7ccc4-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_LTR_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="7ccc4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ccc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ccc4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ccc4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ccc4-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="7ccc4-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="7ccc4-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7ccc4-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7ccc4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ccc4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ccc4-113">Identificador del control de edición que envía el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7ccc4-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ccc4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ccc4-114">Remarks</span></span>

<span data-ttu-id="7ccc4-115">Si hay un idioma bidireccional instalado en el sistema, por ejemplo, el árabe o el hebreo, puede cambiar la dirección del control de edición mediante CTRL + LSHIFT (de izquierda a derecha) y CTRL + RSHIFT (de derecha a izquierda).</span><span class="sxs-lookup"><span data-stu-id="7ccc4-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="7ccc4-116">**Edición enriquecida:** No se admite este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7ccc4-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ccc4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ccc4-117">Requirements</span></span>



| <span data-ttu-id="7ccc4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ccc4-118">Requirement</span></span> | <span data-ttu-id="7ccc4-119">Value</span><span class="sxs-lookup"><span data-stu-id="7ccc4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccc4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ccc4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7ccc4-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ccc4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ccc4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ccc4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7ccc4-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ccc4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7ccc4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ccc4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ccc4-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ccc4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ccc4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ccc4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ccc4-127">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7ccc4-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

