---
title: Código de notificación de EN_SELCHANGE (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que la selección actual ha cambiado. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803422"
---
# <a name="en_selchange-notification-code"></a><span data-ttu-id="9a7af-105">\_Código de notificación en SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="9a7af-105">EN\_SELCHANGE notification code</span></span>

<span data-ttu-id="9a7af-106">Notifica a la ventana primaria de un control Rich Edit que la selección actual ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9a7af-106">Notifies a rich edit control's parent window that the current selection has changed.</span></span> <span data-ttu-id="9a7af-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7af-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9a7af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a7af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a7af-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a7af-110">Una estructura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que recibe información sobre la selección.</span><span class="sxs-lookup"><span data-stu-id="9a7af-110">A [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7af-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a7af-111">Return value</span></span>

<span data-ttu-id="9a7af-112">Este código de notificación no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="9a7af-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a7af-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a7af-113">Remarks</span></span>

<span data-ttu-id="9a7af-114">Para recibir los \_ códigos de notificación en SELCHANGE, especifique [**ENM \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7af-114">To receive EN\_SELCHANGE notification codes, specify [**ENM\_SELCHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="9a7af-115">Este código de notificación se envía cuando cambia la posición del símbolo de intercalación y no se selecciona ningún texto (la selección está vacía).</span><span class="sxs-lookup"><span data-stu-id="9a7af-115">This notification code is sent when the caret position changes and no text is selected (the selection is empty).</span></span> <span data-ttu-id="9a7af-116">La posición del símbolo de intercalación puede cambiar cuando el usuario hace clic con el mouse, escribe o presiona una tecla de dirección.</span><span class="sxs-lookup"><span data-stu-id="9a7af-116">The caret position can change when the user clicks the mouse, types, or presses an arrow key.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7af-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a7af-117">Requirements</span></span>



| <span data-ttu-id="9a7af-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a7af-118">Requirement</span></span> | <span data-ttu-id="9a7af-119">Value</span><span class="sxs-lookup"><span data-stu-id="9a7af-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7af-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a7af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7af-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a7af-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a7af-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a7af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7af-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a7af-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a7af-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a7af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7af-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7af-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a7af-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a7af-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a7af-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9a7af-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a7af-128">**SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="9a7af-128">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[<span data-ttu-id="9a7af-129">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="9a7af-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





