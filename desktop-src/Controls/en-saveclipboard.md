---
title: Código de notificación de EN_SAVECLIPBOARD (RichEdit. h)
description: Notifica a la ventana primaria del control Rich Edit que el control se está cerrando y el Portapapeles contiene información. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- EN_SAVECLIPBOARD controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905176"
---
# <a name="en_saveclipboard-notification-code"></a><span data-ttu-id="685e4-105">\_Código de notificación en SAVECLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="685e4-105">EN\_SAVECLIPBOARD notification code</span></span>

<span data-ttu-id="685e4-106">Notifica a la ventana primaria del control Rich Edit que el control se está cerrando y el Portapapeles contiene información.</span><span class="sxs-lookup"><span data-stu-id="685e4-106">Notifies the rich edit control's parent window that the control is closing and the clipboard contains information.</span></span> <span data-ttu-id="685e4-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="685e4-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="685e4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="685e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="685e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="685e4-110">Estructura [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) que contiene información sobre la información del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="685e4-110">An [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) structure that contains information about clipboard information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685e4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="685e4-111">Return value</span></span>

<span data-ttu-id="685e4-112">Devuelve cero si el portapapeles debe ponerse a disposición de otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="685e4-112">Return zero if the clipboard should be made available to other applications.</span></span>

<span data-ttu-id="685e4-113">Devuelve un valor distinto de cero si no se debe guardar el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="685e4-113">Return a nonzero value if the clipboard should not be saved.</span></span>

## <a name="remarks"></a><span data-ttu-id="685e4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="685e4-114">Remarks</span></span>

<span data-ttu-id="685e4-115">La ventana primaria siempre obtendrá un mensaje [**de \_ notificación de WM**](wm-notify.md) para este evento, pero no requiere que se envíe una máscara de notificación con [**em \_**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="685e4-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="685e4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="685e4-116">Requirements</span></span>



| <span data-ttu-id="685e4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="685e4-117">Requirement</span></span> | <span data-ttu-id="685e4-118">Value</span><span class="sxs-lookup"><span data-stu-id="685e4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="685e4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="685e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="685e4-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="685e4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="685e4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="685e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="685e4-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="685e4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="685e4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="685e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="685e4-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="685e4-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685e4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="685e4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="685e4-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="685e4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="685e4-127">**ENSAVECLIPBOARD**</span><span class="sxs-lookup"><span data-stu-id="685e4-127">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





