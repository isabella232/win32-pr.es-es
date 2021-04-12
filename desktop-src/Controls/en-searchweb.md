---
title: Código de notificación de EN_SEARCHWEB (CommCtrl. h)
description: Se envía cuando un control de edición pierde el foco del teclado. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de notificación de WM \_ .
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489280"
---
# <a name="en_searchweb-notification-code"></a><span data-ttu-id="f92ef-105">\_Código de notificación en SEARCHWEB</span><span class="sxs-lookup"><span data-stu-id="f92ef-105">EN\_SEARCHWEB notification code</span></span>

<span data-ttu-id="f92ef-106">Enviado después de que un control de edición realice una búsqueda web cuando la característica "Buscar en la web" esté habilitada, vea [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span><span class="sxs-lookup"><span data-stu-id="f92ef-106">Sent after an edit control performed a web search when the "Search the web" feature is enabled, see [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span></span> <span data-ttu-id="f92ef-107">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de notificación de [**WM \_**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f92ef-107">The parent window of the edit control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f92ef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f92ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f92ef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f92ef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f92ef-110">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="f92ef-110">Handle to the edit control.</span></span>

</dd> <dt>

<span data-ttu-id="f92ef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f92ef-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f92ef-112">Puntero a una estructura [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .</span><span class="sxs-lookup"><span data-stu-id="f92ef-112">A pointer to a [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f92ef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f92ef-113">Requirements</span></span>



| <span data-ttu-id="f92ef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f92ef-114">Requirement</span></span> | <span data-ttu-id="f92ef-115">Value</span><span class="sxs-lookup"><span data-stu-id="f92ef-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f92ef-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f92ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f92ef-117">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="f92ef-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f92ef-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f92ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f92ef-119">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="f92ef-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f92ef-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f92ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f92ef-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f92ef-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f92ef-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f92ef-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="f92ef-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f92ef-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f92ef-124">**\_ENABLESEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="f92ef-124">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> <dt>

<span data-ttu-id="f92ef-125">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="f92ef-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f92ef-126">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="f92ef-126">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





