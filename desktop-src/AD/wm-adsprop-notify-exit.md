---
title: Mensaje de WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Una Active Directory extensión de la hoja de propiedades envía el mensaje de salida de notificación de WM \_ ADSPROP \_ \_ al objeto de notificación cuando ya no se necesita el objeto de notificación.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996936"
---
# <a name="wm_adsprop_notify_exit-message"></a><span data-ttu-id="0da8f-104">\_Mensaje de \_ salida de notificación de ADSPROP de WM \_</span><span class="sxs-lookup"><span data-stu-id="0da8f-104">WM\_ADSPROP\_NOTIFY\_EXIT message</span></span>

<span data-ttu-id="0da8f-105">Una Active Directory extensión de la hoja de propiedades envía el mensaje de **\_ \_ \_ salida** de notificación de WM ADSPROP al objeto de notificación cuando ya no se necesita el objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="0da8f-105">An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.</span></span>


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="0da8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0da8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da8f-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="0da8f-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0da8f-108">Identificador del objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="0da8f-108">The handle of the notification object.</span></span> <span data-ttu-id="0da8f-109">Para obtener este identificador, llame a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="0da8f-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="0da8f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0da8f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0da8f-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0da8f-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0da8f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0da8f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0da8f-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0da8f-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da8f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0da8f-114">Return value</span></span>

<span data-ttu-id="0da8f-115">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="0da8f-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0da8f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0da8f-116">Remarks</span></span>

<span data-ttu-id="0da8f-117">El objeto de notificación se eliminará en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0da8f-117">The notification object will delete itself in response to this message.</span></span> <span data-ttu-id="0da8f-118">Cuando se envía este mensaje, el identificador del objeto de notificación debe considerarse no válido.</span><span class="sxs-lookup"><span data-stu-id="0da8f-118">When this message has been sent, the notification object handle should be considered invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da8f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0da8f-119">Requirements</span></span>



| <span data-ttu-id="0da8f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0da8f-120">Requirement</span></span> | <span data-ttu-id="0da8f-121">Value</span><span class="sxs-lookup"><span data-stu-id="0da8f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0da8f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0da8f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0da8f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0da8f-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="0da8f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0da8f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0da8f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0da8f-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="0da8f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0da8f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0da8f-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="0da8f-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da8f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0da8f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da8f-129">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="0da8f-129">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="0da8f-130">Mensajes en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="0da8f-130">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





