---
title: Código de notificación de EN_STOPNOUNDO (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que se ha producido una acción para la que el control no puede asignar memoria suficiente para mantener el estado de deshacer. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150908"
---
# <a name="en_stopnoundo-notification-code"></a><span data-ttu-id="2fd53-105">\_Código de notificación en STOPNOUNDO</span><span class="sxs-lookup"><span data-stu-id="2fd53-105">EN\_STOPNOUNDO notification code</span></span>

<span data-ttu-id="2fd53-106">Notifica a la ventana primaria de un control Rich Edit que se ha producido una acción para la que el control no puede asignar memoria suficiente para mantener el estado de deshacer.</span><span class="sxs-lookup"><span data-stu-id="2fd53-106">Notifies a rich edit control's parent window that an action occurred for which the control cannot allocate enough memory to maintain the undo state.</span></span> <span data-ttu-id="2fd53-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd53-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2fd53-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fd53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd53-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fd53-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd53-110">Una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="2fd53-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd53-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fd53-111">Return value</span></span>

<span data-ttu-id="2fd53-112">Devuelve cero para continuar con la operación de **Deshacer** .</span><span class="sxs-lookup"><span data-stu-id="2fd53-112">Return zero to continue the **Undo** operation.</span></span>

<span data-ttu-id="2fd53-113">Devuelve un valor distinto de cero para detener la operación de **Deshacer** .</span><span class="sxs-lookup"><span data-stu-id="2fd53-113">Return a nonzero value to stop the **Undo** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fd53-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fd53-114">Remarks</span></span>

<span data-ttu-id="2fd53-115">La ventana primaria siempre obtendrá un mensaje [**de \_ notificación de WM**](wm-notify.md) para este evento, pero no requiere que se envíe una máscara de notificación con [**em \_**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="2fd53-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd53-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fd53-116">Requirements</span></span>



| <span data-ttu-id="2fd53-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd53-117">Requirement</span></span> | <span data-ttu-id="2fd53-118">Value</span><span class="sxs-lookup"><span data-stu-id="2fd53-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd53-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fd53-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd53-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2fd53-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fd53-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fd53-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd53-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fd53-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fd53-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fd53-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd53-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd53-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd53-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fd53-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2fd53-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2fd53-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2fd53-127">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="2fd53-127">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[<span data-ttu-id="2fd53-128">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="2fd53-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





