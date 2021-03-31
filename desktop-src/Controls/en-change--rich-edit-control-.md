---
title: Código de notificación de EN_CHANGE (Rich Edit) (Winuser. h)
description: Notifica a la ventana host de un control Rich Edit sin ventana que se ha producido un cambio. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- Código de notificación de EN_CHANGE (edición enriquecida) controles de Windows
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996221"
---
# <a name="en_change-rich-edit-notification-code"></a><span data-ttu-id="5b219-105">\_Código de notificación en cambio (Rich Edit)</span><span class="sxs-lookup"><span data-stu-id="5b219-105">EN\_CHANGE (rich edit) notification code</span></span>

<span data-ttu-id="5b219-106">Notifica a la ventana host de un control Rich Edit sin ventana que se ha producido un cambio.</span><span class="sxs-lookup"><span data-stu-id="5b219-106">Notifies a windowless rich edit control's host window that a change has occurred.</span></span> <span data-ttu-id="5b219-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5b219-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5b219-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b219-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b219-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b219-110">Estructura [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) que especifica el cambio que se realizó.</span><span class="sxs-lookup"><span data-stu-id="5b219-110">A [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) structure specifying the change that was made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b219-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b219-111">Return value</span></span>

<span data-ttu-id="5b219-112">Este código de notificación no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5b219-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b219-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b219-113">Remarks</span></span>

<span data-ttu-id="5b219-114">Para recibir los \_ códigos de notificación de cambio, especifique el [**\_ cambio ENM**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="5b219-114">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b219-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b219-115">Requirements</span></span>



| <span data-ttu-id="5b219-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b219-116">Requirement</span></span> | <span data-ttu-id="5b219-117">Value</span><span class="sxs-lookup"><span data-stu-id="5b219-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b219-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b219-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5b219-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5b219-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5b219-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b219-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5b219-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b219-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b219-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b219-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b219-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b219-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b219-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b219-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b219-125">**TxNotify**</span><span class="sxs-lookup"><span data-stu-id="5b219-125">**TxNotify**</span></span>](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





