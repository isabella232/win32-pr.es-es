---
title: Mensaje de WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Una extensión de la hoja de propiedades del servicio de directorio de Active Directory envía el mensaje de notificación de ADSPROP de WM \_ \_ \_ al objeto de notificación si la página de propiedades PSN el \_ controlador de aplicación se realiza correctamente.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658347"
---
# <a name="wm_adsprop_notify_apply-message"></a><span data-ttu-id="a44a1-104">\_Mensaje de \_ solicitud de notificación de ADSPROP de WM \_</span><span class="sxs-lookup"><span data-stu-id="a44a1-104">WM\_ADSPROP\_NOTIFY\_APPLY message</span></span>

<span data-ttu-id="a44a1-105">Una extensión de la hoja de propiedades del servicio de directorio de Active Directory envía el mensaje de notificación de **ADSPROP de WM \_ \_ \_** al objeto de notificación si la página de propiedades PSN el \_ controlador de aplicación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a44a1-105">An Active Directory directory service property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_APPLY** message to the notification object if the property page PSN\_APPLY handler succeeds.</span></span>


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="a44a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a44a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a44a1-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="a44a1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a44a1-108">Identificador del objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="a44a1-108">The handle of the notification object.</span></span> <span data-ttu-id="a44a1-109">Para obtener este identificador, llame a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="a44a1-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="a44a1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a44a1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a44a1-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a44a1-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a44a1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a44a1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a44a1-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a44a1-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a44a1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a44a1-114">Return value</span></span>

<span data-ttu-id="a44a1-115">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="a44a1-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a44a1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a44a1-116">Remarks</span></span>

<span data-ttu-id="a44a1-117">Al agregar páginas al complemento MMC de Active Directory Manager, Active Directory hojas de propiedades de MMC crean los objetos de notificación mediante una llamada a la función [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) y, a continuación, pasa el identificador del objeto de notificación a cada página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a44a1-117">When adding pages to the Active Directory Manager MMC snap-in, Active Directory MMC property sheets create the notification objects by a call to the [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) function, and then passes the notification object handle to each property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="a44a1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a44a1-118">Requirements</span></span>



| <span data-ttu-id="a44a1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a44a1-119">Requirement</span></span> | <span data-ttu-id="a44a1-120">Value</span><span class="sxs-lookup"><span data-stu-id="a44a1-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a44a1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a44a1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a44a1-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a44a1-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="a44a1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a44a1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a44a1-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a44a1-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="a44a1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a44a1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a44a1-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="a44a1-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a44a1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a44a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a44a1-128">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="a44a1-128">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="a44a1-129">Mensajes en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a44a1-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





