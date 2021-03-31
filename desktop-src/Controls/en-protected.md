---
title: Código de notificación de EN_PROTECTED (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que el usuario está realizando una acción que cambiaría un intervalo de texto protegido. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490870"
---
# <a name="en_protected-notification-code"></a><span data-ttu-id="ff382-105">\_Código de notificación en protegido</span><span class="sxs-lookup"><span data-stu-id="ff382-105">EN\_PROTECTED notification code</span></span>

<span data-ttu-id="ff382-106">Notifica a la ventana primaria de un control Rich Edit que el usuario está realizando una acción que cambiaría un intervalo de texto protegido.</span><span class="sxs-lookup"><span data-stu-id="ff382-106">Notifies a rich edit control's parent window that the user is taking an action that would change a protected range of text.</span></span> <span data-ttu-id="ff382-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ff382-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ff382-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff382-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff382-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff382-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff382-110">Estructura [**protegida**](/windows/desktop/api/Richedit/ns-richedit-enprotected) que contiene información sobre el mensaje que desencadenó el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="ff382-110">An [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure containing information about the message that triggered the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff382-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff382-111">Return value</span></span>

<span data-ttu-id="ff382-112">Devuelve cero para permitir la operación.</span><span class="sxs-lookup"><span data-stu-id="ff382-112">Return zero to allow the operation.</span></span>

<span data-ttu-id="ff382-113">Devuelve un valor distinto de cero para evitar la operación.</span><span class="sxs-lookup"><span data-stu-id="ff382-113">Return a nonzero value to prevent the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff382-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff382-114">Remarks</span></span>

<span data-ttu-id="ff382-115">Si se devuelve cero y se cambian los miembros **MSG**, **wParam** e **lParam** de la estructura [**enprotected**](/windows/desktop/api/Richedit/ns-richedit-enprotected) , el control procesa el mensaje revisado en lugar del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="ff382-115">If zero is returned and the **msg**, **wParam**, and **lParam** members of the [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure are changed, the control processes the revised message instead of the original message.</span></span>

<span data-ttu-id="ff382-116">Para recibir \_ códigos de notificación protegidos, especifique [**ENM \_ protegido**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="ff382-116">To receive EN\_PROTECTED notification codes, specify [**ENM\_PROTECTED**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff382-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff382-117">Requirements</span></span>



| <span data-ttu-id="ff382-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff382-118">Requirement</span></span> | <span data-ttu-id="ff382-119">Value</span><span class="sxs-lookup"><span data-stu-id="ff382-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff382-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff382-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff382-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff382-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff382-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff382-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff382-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff382-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff382-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff382-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff382-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff382-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff382-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff382-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff382-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ff382-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff382-128">**PROTEGIDO**</span><span class="sxs-lookup"><span data-stu-id="ff382-128">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[<span data-ttu-id="ff382-129">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="ff382-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





