---
title: Código de notificación de EN_IMECHANGE (RichEdit. h)
description: Notifica a un elemento primario del control Rich Edit que ha cambiado el estado de la conversión del IME.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079405"
---
# <a name="en_imechange-notification-code"></a><span data-ttu-id="d7ccc-104">\_Código de notificación en IMECHANGE</span><span class="sxs-lookup"><span data-stu-id="d7ccc-104">EN\_IMECHANGE notification code</span></span>

<span data-ttu-id="d7ccc-105">Notifica a un elemento primario del control Rich Edit que ha cambiado el estado de la conversión del IME.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-105">Notifies a rich edit control's parent that the IME conversion status has changed.</span></span> <span data-ttu-id="d7ccc-106">Este código de notificación *solo* está disponible para las versiones de idioma asiático del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-106">This notification code is available *only* for Asian-language versions of the operating system.</span></span> <span data-ttu-id="d7ccc-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d7ccc-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d7ccc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7ccc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ccc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7ccc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ccc-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="d7ccc-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d7ccc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7ccc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ccc-113">Identificador del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ccc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7ccc-114">Return value</span></span>

<span data-ttu-id="d7ccc-115">Este código de notificación devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-115">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ccc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7ccc-116">Remarks</span></span>

<span data-ttu-id="d7ccc-117">Para recibir los \_ códigos de notificación en IMECHANGE, especifique [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ccc-117">To receive EN\_IMECHANGE notification codes, specify [**ENM\_IMECHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="d7ccc-118">Este código de notificación solo se admite en la versión asiática de Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-118">This notification code is only supported in the Asian version of Rich Edit 1.0.</span></span> <span data-ttu-id="d7ccc-119">No se admite en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d7ccc-119">It is not supported in later versions.</span></span> <span data-ttu-id="d7ccc-120">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d7ccc-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7ccc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7ccc-121">Requirements</span></span>



| <span data-ttu-id="d7ccc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7ccc-122">Requirement</span></span> | <span data-ttu-id="d7ccc-123">Value</span><span class="sxs-lookup"><span data-stu-id="d7ccc-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ccc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7ccc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ccc-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7ccc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7ccc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7ccc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ccc-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7ccc-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7ccc-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7ccc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ccc-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ccc-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ccc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7ccc-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7ccc-131">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d7ccc-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d7ccc-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7ccc-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d7ccc-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7ccc-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d7ccc-134">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d7ccc-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

