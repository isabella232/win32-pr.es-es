---
title: Mensaje de WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Una extensión de la hoja de propiedades del servicio de directorio de Active Directory llama a ADsPropSetHwnd para informar al objeto de notificación del identificador de la ventana de la página de propiedades.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150931"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a><span data-ttu-id="b2f8b-104">\_Mensaje de \_ PAGEHWND de notificación de ADSPROP de WM \_</span><span class="sxs-lookup"><span data-stu-id="b2f8b-104">WM\_ADSPROP\_NOTIFY\_PAGEHWND message</span></span>

<span data-ttu-id="b2f8b-105">Una extensión de la hoja de propiedades del servicio de directorio de Active Directory llama a [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) para informar al objeto de notificación del identificador de la ventana de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-105">An Active Directory directory service property sheet extension calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) to inform the notification object of the property page window handle.</span></span> <span data-ttu-id="b2f8b-106">La función **ADsPropSetHwnd** envía el mensaje **WM \_ ADSPROP \_ Notify \_ PAGEHWND** al objeto de notificación, que informa al objeto de notificación del identificador de la ventana de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-106">The **ADsPropSetHwnd** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEHWND** message to the notification object, which informs the notification object of the property page window handle.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a><span data-ttu-id="b2f8b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2f8b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f8b-108">*hNotifyObj*</span><span class="sxs-lookup"><span data-stu-id="b2f8b-108">*hNotifyObj*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f8b-109">Identificador del objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-109">The handle of the notification object.</span></span> <span data-ttu-id="b2f8b-110">Para obtener este identificador, llame a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="b2f8b-110">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="b2f8b-111">*hPage*</span><span class="sxs-lookup"><span data-stu-id="b2f8b-111">*hPage*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f8b-112">Identificador de ventana de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-112">A window handle of the property page.</span></span>

</dd> <dt>

<span data-ttu-id="b2f8b-113">*ptzTitle*</span><span class="sxs-lookup"><span data-stu-id="b2f8b-113">*ptzTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f8b-114">Puntero a un búfer **WCHAR** terminado en null que contiene el título de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-114">Pointer to a NULL-terminated **WCHAR** buffer that contains the title of the property page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2f8b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2f8b-115">Return value</span></span>

<span data-ttu-id="b2f8b-116">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f8b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2f8b-117">Remarks</span></span>

<span data-ttu-id="b2f8b-118">Una Active Directory extensión de la hoja de propiedades normalmente llama a la función [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) mientras procesa el mensaje [**\_ INITDIALOG de WM**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f8b-118">An Active Directory property sheet extension normally calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) function while processing the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f8b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2f8b-119">Requirements</span></span>



| <span data-ttu-id="b2f8b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f8b-120">Requirement</span></span> | <span data-ttu-id="b2f8b-121">Value</span><span class="sxs-lookup"><span data-stu-id="b2f8b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f8b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2f8b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f8b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2f8b-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="b2f8b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2f8b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f8b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2f8b-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="b2f8b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2f8b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2f8b-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f8b-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f8b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2f8b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f8b-129">Mensajes en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="b2f8b-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="b2f8b-130">**ADsPropSetHwnd**</span><span class="sxs-lookup"><span data-stu-id="b2f8b-130">**ADsPropSetHwnd**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[<span data-ttu-id="b2f8b-131">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="b2f8b-131">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="b2f8b-132">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b2f8b-132">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

