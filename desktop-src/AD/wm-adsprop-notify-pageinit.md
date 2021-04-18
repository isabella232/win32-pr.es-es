---
title: Mensaje de WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop. h)
description: Una Active Directory extensión de la hoja de propiedades llama a ADsPropGetInitInfo para obtener datos sobre el objeto de directorio al que se aplica la extensión de la hoja de propiedades.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533987"
---
# <a name="wm_adsprop_notify_pageinit-message"></a><span data-ttu-id="bb310-104">\_Mensaje de \_ PAGEINIT de notificación de ADSPROP de WM \_</span><span class="sxs-lookup"><span data-stu-id="bb310-104">WM\_ADSPROP\_NOTIFY\_PAGEINIT message</span></span>

<span data-ttu-id="bb310-105">Una Active Directory extensión de la hoja de propiedades llama a [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) para obtener datos sobre el objeto de directorio al que se aplica la extensión de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb310-105">An Active Directory property sheet extension calls the [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) to obtain data about regarding the directory object that the property sheet extension applies to.</span></span> <span data-ttu-id="bb310-106">La función **ADsPropGetInitInfo** envía el mensaje de ADSPROP de notificación de **\_ \_ \_ PAGEINIT de WM** al objeto de notificación para lograr este resultado.</span><span class="sxs-lookup"><span data-stu-id="bb310-106">The **ADsPropGetInitInfo** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEINIT** message to the notification object to achieve this result.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a><span data-ttu-id="bb310-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb310-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb310-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="bb310-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bb310-109">Identificador del objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="bb310-109">Handle of the notification object.</span></span> <span data-ttu-id="bb310-110">Este es el parámetro *hNotifyObject* obtenido mediante una llamada a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="bb310-110">This is the *hNotifyObject* parameter obtained by a call to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="bb310-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb310-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb310-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bb310-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bb310-113">*pADsPropInitParams*</span><span class="sxs-lookup"><span data-stu-id="bb310-113">*pADsPropInitParams*</span></span> 
</dt> <dd>

<span data-ttu-id="bb310-114">Puntero a una estructura [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) que recibe la información del objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="bb310-114">Pointer to an [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) structure that receives the directory object information.</span></span> <span data-ttu-id="bb310-115">Este es el parámetro *pInitParams* pasado a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="bb310-115">This is the *pInitParams* parameter passed to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb310-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb310-116">Return value</span></span>

<span data-ttu-id="bb310-117">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="bb310-117">This message has no return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb310-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb310-118">Requirements</span></span>



| <span data-ttu-id="bb310-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb310-119">Requirement</span></span> | <span data-ttu-id="bb310-120">Value</span><span class="sxs-lookup"><span data-stu-id="bb310-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb310-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb310-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb310-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb310-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="bb310-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb310-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb310-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb310-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="bb310-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb310-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb310-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb310-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb310-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb310-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb310-128">Mensajes en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="bb310-128">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="bb310-129">**ADsPropGetInitInfo**</span><span class="sxs-lookup"><span data-stu-id="bb310-129">**ADsPropGetInitInfo**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[<span data-ttu-id="bb310-130">**ADSPROPINITPARAMS**</span><span class="sxs-lookup"><span data-stu-id="bb310-130">**ADSPROPINITPARAMS**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





