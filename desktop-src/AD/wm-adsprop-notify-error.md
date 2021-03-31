---
title: Mensaje de WM_ADSPROP_NOTIFY_ERROR (Adsprop. h)
description: El \_ mensaje de \_ error de notificaciones de ADSPROP de WM \_ agrega un mensaje de error a una lista de mensajes de error que se muestran al llamar a la función ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150323"
---
# <a name="wm_adsprop_notify_error-message"></a><span data-ttu-id="c4ea1-104">\_Mensaje de \_ error de notificación de ADSPROP de WM \_</span><span class="sxs-lookup"><span data-stu-id="c4ea1-104">WM\_ADSPROP\_NOTIFY\_ERROR message</span></span>

<span data-ttu-id="c4ea1-105">El mensaje de **\_ \_ \_ error de notificaciones de ADSPROP de WM** agrega un mensaje de error a una lista de mensajes de error que se muestran al llamar a la función [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="c4ea1-105">The **WM\_ADSPROP\_NOTIFY\_ERROR** message adds an error message to a list of error messages that are displayed by calling the [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) function.</span></span>


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="c4ea1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4ea1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ea1-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="c4ea1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c4ea1-108">Identificador del objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="c4ea1-108">Handle of the notification object.</span></span> <span data-ttu-id="c4ea1-109">Este es el parámetro *hNotifyObject* obtenido por [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="c4ea1-109">This is the *hNotifyObject* parameter obtained by [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="c4ea1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4ea1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4ea1-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c4ea1-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4ea1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4ea1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4ea1-113">Puntero a una estructura [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) que contiene datos de mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="c4ea1-113">Pointer to an [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) structure that contains error message data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ea1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4ea1-114">Return value</span></span>

<span data-ttu-id="c4ea1-115">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c4ea1-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ea1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4ea1-116">Remarks</span></span>

<span data-ttu-id="c4ea1-117">La función [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) es el método preferido para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c4ea1-117">The [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) function is the preferred method of sending this message.</span></span>

<span data-ttu-id="c4ea1-118">Los mensajes de error agregados por el mensaje de **\_ \_ \_ error NOTIFY de WM ADSPROP** se acumulan hasta que se llama a [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="c4ea1-118">The error messages added by the **WM\_ADSPROP\_NOTIFY\_ERROR** message are accumulated until [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) is called.</span></span> <span data-ttu-id="c4ea1-119">**ADsPropShowErrorDialog** combina y muestra los mensajes de error acumulados.</span><span class="sxs-lookup"><span data-stu-id="c4ea1-119">**ADsPropShowErrorDialog** combines and displays the accumulated error messages.</span></span> <span data-ttu-id="c4ea1-120">Cuando se descarta el cuadro de diálogo de error, se eliminan los mensajes de error acumulados.</span><span class="sxs-lookup"><span data-stu-id="c4ea1-120">When the error dialog is dismissed, the accumulated error messages are deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ea1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4ea1-121">Requirements</span></span>



| <span data-ttu-id="c4ea1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4ea1-122">Requirement</span></span> | <span data-ttu-id="c4ea1-123">Value</span><span class="sxs-lookup"><span data-stu-id="c4ea1-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ea1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4ea1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ea1-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4ea1-125">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="c4ea1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4ea1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ea1-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4ea1-127">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="c4ea1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4ea1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4ea1-129"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ea1-129"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ea1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4ea1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ea1-131">Mensajes en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c4ea1-131">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="c4ea1-132">**ADSPROPERROR**</span><span class="sxs-lookup"><span data-stu-id="c4ea1-132">**ADSPROPERROR**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[<span data-ttu-id="c4ea1-133">**ADsPropSendErrorMessage**</span><span class="sxs-lookup"><span data-stu-id="c4ea1-133">**ADsPropSendErrorMessage**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[<span data-ttu-id="c4ea1-134">**ADsPropShowErrorDialog**</span><span class="sxs-lookup"><span data-stu-id="c4ea1-134">**ADsPropShowErrorDialog**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





