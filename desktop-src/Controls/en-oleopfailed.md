---
title: Código de notificación de EN_OLEOPFAILED (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que se ha producido un error en una acción del usuario en un objeto de modelo de objetos componentes (COM). Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905294"
---
# <a name="en_oleopfailed-notification-code"></a><span data-ttu-id="5ad4e-105">\_Código de notificación en OLEOPFAILED</span><span class="sxs-lookup"><span data-stu-id="5ad4e-105">EN\_OLEOPFAILED notification code</span></span>

<span data-ttu-id="5ad4e-106">Notifica a la ventana primaria de un control Rich Edit que se ha producido un error en una acción del usuario en un objeto de modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="5ad4e-106">Notifies a rich edit control's parent window that a user action on a Component Object Model (COM) object has failed.</span></span> <span data-ttu-id="5ad4e-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5ad4e-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5ad4e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ad4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ad4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad4e-110">Estructura [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) que contiene información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-110">An [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) structure that contains information about the failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad4e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ad4e-111">Return value</span></span>

<span data-ttu-id="5ad4e-112">Este código de notificación devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5ad4e-112">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ad4e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ad4e-113">Remarks</span></span>

<span data-ttu-id="5ad4e-114">La ventana primaria siempre obtendrá un mensaje [**de \_ notificación de WM**](wm-notify.md) para este evento, pero no requiere que se envíe una máscara de notificación con [**em \_**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="5ad4e-114">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad4e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad4e-115">Requirements</span></span>



| <span data-ttu-id="5ad4e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad4e-116">Requirement</span></span> | <span data-ttu-id="5ad4e-117">Value</span><span class="sxs-lookup"><span data-stu-id="5ad4e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad4e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ad4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ad4e-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5ad4e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ad4e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ad4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ad4e-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ad4e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ad4e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ad4e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ad4e-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4e-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad4e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ad4e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ad4e-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5ad4e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ad4e-126">**ENOLEOPFAILED**</span><span class="sxs-lookup"><span data-stu-id="5ad4e-126">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





