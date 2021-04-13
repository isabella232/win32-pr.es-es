---
title: Código de notificación de EN_LINK (RichEdit. h)
description: Un control Rich Edit envía \_ códigos de notificación en vínculo cuando recibe varios mensajes, por ejemplo, cuando el usuario hace clic con el mouse o cuando el puntero del mouse se encuentra sobre texto que tiene el \_ efecto de vínculo CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492448"
---
# <a name="en_link-notification-code"></a><span data-ttu-id="91120-104">\_Código de notificación en vínculo</span><span class="sxs-lookup"><span data-stu-id="91120-104">EN\_LINK notification code</span></span>

<span data-ttu-id="91120-105">Un control Rich Edit envía \_ códigos de notificación en vínculo cuando recibe varios mensajes, por ejemplo, cuando el usuario hace clic con el mouse o cuando el puntero del mouse se encuentra sobre texto que tiene el efecto de **\_ vínculo CFE** .</span><span class="sxs-lookup"><span data-stu-id="91120-105">A rich edit control sends EN\_LINK notification codes when it receives various messages, for example, when the user clicks the mouse or when the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="91120-106">Un control Rich Edit sin ventanas envía esta notificación mediante el método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="91120-106">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span> <span data-ttu-id="91120-107">La ventana primaria del control recibe este código de notificación a través de un mensaje de notificación de [**WM \_**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="91120-107">The parent window of the control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="91120-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91120-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91120-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91120-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91120-110">IDENTIFICADOR de ventana que se ha recuperado mediante una llamada a la función [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con el valor de identificador de GWL \_ .</span><span class="sxs-lookup"><span data-stu-id="91120-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="91120-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91120-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91120-112">Puntero a una estructura de [**vínculo**](/windows/desktop/api/Richedit/ns-richedit-enlink) .</span><span class="sxs-lookup"><span data-stu-id="91120-112">Pointer to an [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink) structure.</span></span> <span data-ttu-id="91120-113">La estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , información sobre el código de notificación y una estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que indica el intervalo de caracteres que tienen el efecto **CFE \_ Link** .</span><span class="sxs-lookup"><span data-stu-id="91120-113">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, information about the notification code, and a [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that indicates the range of characters that have the **CFE\_LINK** effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91120-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91120-114">Return value</span></span>

<span data-ttu-id="91120-115">Devuelve cero para permitir que el control continúe con su control normal del mensaje.</span><span class="sxs-lookup"><span data-stu-id="91120-115">Return zero to allow the control to proceed with its normal handling of the message.</span></span>

<span data-ttu-id="91120-116">Devuelve un valor distinto de cero para evitar que el control controle el mensaje.</span><span class="sxs-lookup"><span data-stu-id="91120-116">Return a nonzero value to prevent the control from handling the message.</span></span>

<span data-ttu-id="91120-117">**Windows 8**: de **\_ \_ \_ forma predeterminada** , el vínculo devuelto en es dirigir el control Rich Edit para realizar la acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="91120-117">**Windows 8**: Return **EN\_LINK\_DO\_DEFAULT** to direct the rich edit control to perform the default action.</span></span>

## <a name="remarks"></a><span data-ttu-id="91120-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91120-118">Remarks</span></span>

<span data-ttu-id="91120-119">Para recibir los códigos de notificación en **\_ vínculo** cuando el vínculo tenga el foco, especifique la marca de [**\_ vínculo ENM**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="91120-119">To receive **EN\_LINK** notification codes when the link has focus, specify the [**ENM\_LINK**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="91120-120">Si el vínculo no tiene el foco, para recibir los códigos de notificación **en el \_ vínculo** , especifique la marca **SES \_ NOFOCUSLINKNOTIFY** en la máscara enviada con el mensaje [**\_ SETEDITSTYLE em**](em-seteditstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="91120-120">If the link has no focus, to receive **EN\_LINK** notification codes specify the **SES\_NOFOCUSLINKNOTIFY** flag in the mask sent with the [**EM\_SETEDITSTYLE**](em-seteditstyle.md) message.</span></span>

<span data-ttu-id="91120-121">Un control Rich Edit envía códigos de notificación **en \_ vínculos** cuando recibe los mensajes siguientes mientras el puntero del mouse se encuentra sobre el texto que tiene el efecto de **\_ vínculo CFE** :</span><span class="sxs-lookup"><span data-stu-id="91120-121">A rich edit control sends **EN\_LINK** notification codes when it receives the following messages while the mouse pointer is over text that has the **CFE\_LINK** effect:</span></span>

-   [<span data-ttu-id="91120-122">**LBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-122">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [<span data-ttu-id="91120-123">**LBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-123">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)
-   [<span data-ttu-id="91120-124">**LBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-124">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)
-   [<span data-ttu-id="91120-125">**MOUSEMOVE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-125">**WM\_MOUSEMOVE**</span></span>](/windows/desktop/inputdev/wm-mousemove)
-   [<span data-ttu-id="91120-126">**RBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-126">**WM\_RBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [<span data-ttu-id="91120-127">**RBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-127">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown)
-   [<span data-ttu-id="91120-128">**RBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-128">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
-   [<span data-ttu-id="91120-129">**SETCURSOR de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91120-129">**WM\_SETCURSOR**</span></span>](/windows/desktop/menurc/wm-setcursor)

<span data-ttu-id="91120-130">El efecto de **\_ vínculo CFE** normalmente identifica un intervalo de texto que contiene una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="91120-130">The **CFE\_LINK** effect typically identifies a range of text that contains an URL.</span></span> <span data-ttu-id="91120-131">Las aplicaciones pueden controlar el \_ código de notificación de vínculo en el vínculo en el puntero del mouse cuando está sobre la dirección URL o iniciando un explorador para ver la ubicación identificada por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="91120-131">Applications can handle the EN\_LINK notification code by changing the mouse pointer when it is over the URL, or by starting a browser to view the location identified by the URL.</span></span>

<span data-ttu-id="91120-132">Si envía el mensaje [**\_ AUTOURLDETECT em**](em-autourldetect.md) para habilitar la detección automática de direcciones URL, el control Rich Edit establece automáticamente el efecto **CFE \_ Link** para el texto modificado que identifica como dirección URL.</span><span class="sxs-lookup"><span data-stu-id="91120-132">If you send the [**EM\_AUTOURLDETECT**](em-autourldetect.md) message to enable automatic URL detection, the rich edit control automatically sets the **CFE\_LINK** effect for modified text that it identifies as a URL.</span></span>

## <a name="requirements"></a><span data-ttu-id="91120-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91120-133">Requirements</span></span>



| <span data-ttu-id="91120-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="91120-134">Requirement</span></span> | <span data-ttu-id="91120-135">Value</span><span class="sxs-lookup"><span data-stu-id="91120-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91120-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91120-136">Minimum supported client</span></span><br/> | <span data-ttu-id="91120-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91120-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91120-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91120-138">Minimum supported server</span></span><br/> | <span data-ttu-id="91120-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91120-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91120-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91120-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="91120-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="91120-141"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91120-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="91120-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91120-143">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="91120-143">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[<span data-ttu-id="91120-144">**\_AUTOURLDETECT em**</span><span class="sxs-lookup"><span data-stu-id="91120-144">**EM\_AUTOURLDETECT**</span></span>](em-autourldetect.md)
</dt> <dt>

[<span data-ttu-id="91120-145">**VÍNCULO**</span><span class="sxs-lookup"><span data-stu-id="91120-145">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[<span data-ttu-id="91120-146">**ITextRange2:: SetURL**</span><span class="sxs-lookup"><span data-stu-id="91120-146">**ITextRange2::SetURL**</span></span>](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[<span data-ttu-id="91120-147">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="91120-147">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

