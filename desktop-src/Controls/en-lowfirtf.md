---
title: Código de notificación de EN_LOWFIRTF (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit de Microsoft que se ha recibido una palabra clave de formato de texto enriquecido (RTF) no compatible. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535049"
---
# <a name="en_lowfirtf-notification-code"></a><span data-ttu-id="1ad1b-105">\_Código de notificación en LOWFIRTF</span><span class="sxs-lookup"><span data-stu-id="1ad1b-105">EN\_LOWFIRTF notification code</span></span>

<span data-ttu-id="1ad1b-106">Notifica a la ventana primaria de un control Rich Edit de Microsoft que se ha recibido una palabra clave de formato de texto enriquecido (RTF) no compatible.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-106">Notifies the parent window of a Microsoft Rich Edit control that an unsupported Rich Text Format (RTF) keyword was received.</span></span> <span data-ttu-id="1ad1b-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad1b-107">A Rich Edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1ad1b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ad1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad1b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ad1b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad1b-110">Estructura [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .</span><span class="sxs-lookup"><span data-stu-id="1ad1b-110">The [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad1b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ad1b-111">Return value</span></span>

<span data-ttu-id="1ad1b-112">Este código de notificación no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1ad1b-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad1b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ad1b-113">Remarks</span></span>

<span data-ttu-id="1ad1b-114">Para recibir una \_ notificación en LOWFIRTF, especifique la \_ marca LOWFIRTF de ENM en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad1b-114">To receive an EN\_LOWFIRTF notification, specify the ENM\_LOWFIRTF flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad1b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ad1b-115">Requirements</span></span>



| <span data-ttu-id="1ad1b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ad1b-116">Requirement</span></span> | <span data-ttu-id="1ad1b-117">Value</span><span class="sxs-lookup"><span data-stu-id="1ad1b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad1b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ad1b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad1b-119">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ad1b-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ad1b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ad1b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad1b-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ad1b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ad1b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ad1b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad1b-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad1b-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad1b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ad1b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ad1b-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1ad1b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ad1b-126">**ENLOWFIRTF**</span><span class="sxs-lookup"><span data-stu-id="1ad1b-126">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[<span data-ttu-id="1ad1b-127">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="1ad1b-127">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





