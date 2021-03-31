---
title: Código de notificación de EN_ALIGN_RTL_EC (Winuser. h)
description: Se envía cuando el usuario ha cambiado la dirección del control de edición de derecha a izquierda. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de comando de WM \_ .
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca94073b86ea44b192360e593f4b76d4227cf82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905137"
---
# <a name="en_align_rtl_ec-notification-code"></a><span data-ttu-id="6d7dc-105">\_Código de notificación en align \_ RTL \_ EC</span><span class="sxs-lookup"><span data-stu-id="6d7dc-105">EN\_ALIGN\_RTL\_EC notification code</span></span>

<span data-ttu-id="6d7dc-106">Se envía cuando el usuario ha cambiado la dirección del control de edición de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="6d7dc-106">Sent when the user has changed the edit control direction to right-to-left.</span></span> <span data-ttu-id="6d7dc-107">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6d7dc-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d7dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d7dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d7dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d7dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d7dc-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="6d7dc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="6d7dc-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="6d7dc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6d7dc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d7dc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d7dc-113">Identificador del control de edición que envía el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="6d7dc-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d7dc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d7dc-114">Remarks</span></span>

<span data-ttu-id="6d7dc-115">Si hay un idioma bidireccional instalado en el sistema, por ejemplo, el árabe o el hebreo, puede cambiar la dirección del control de edición mediante CTRL + LSHIFT (de izquierda a derecha) y CTRL + RSHIFT (de derecha a izquierda).</span><span class="sxs-lookup"><span data-stu-id="6d7dc-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="6d7dc-116">**Edición enriquecida:** No se admite este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="6d7dc-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d7dc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d7dc-117">Requirements</span></span>



| <span data-ttu-id="6d7dc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d7dc-118">Requirement</span></span> | <span data-ttu-id="6d7dc-119">Value</span><span class="sxs-lookup"><span data-stu-id="6d7dc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7dc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d7dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6d7dc-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d7dc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d7dc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d7dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6d7dc-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d7dc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d7dc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d7dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d7dc-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d7dc-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d7dc-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d7dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7dc-127">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="6d7dc-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

