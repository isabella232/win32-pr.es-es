---
title: Código de notificación de PSN_APPLY (Prsht. h)
description: Se envía a todas las páginas de la hoja de propiedades para indicar que el usuario ha hecho clic en el botón Aceptar, cerrar o aplicar y desea que todos los cambios surtan efecto. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491440"
---
# <a name="psn_apply-notification-code"></a><span data-ttu-id="c2cac-105">PSN \_ aplicar código de notificación</span><span class="sxs-lookup"><span data-stu-id="c2cac-105">PSN\_APPLY notification code</span></span>

<span data-ttu-id="c2cac-106">Se envía a todas las páginas de la hoja de propiedades para indicar que el usuario ha hecho clic en el botón Aceptar, cerrar o aplicar y desea que todos los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="c2cac-106">Sent to every page in the property sheet to indicate that the user has clicked the OK, Close, or Apply button and wants all changes to take effect.</span></span> <span data-ttu-id="c2cac-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c2cac-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c2cac-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2cac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2cac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cac-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación, incluido el identificador de la página.</span><span class="sxs-lookup"><span data-stu-id="c2cac-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code, including the ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cac-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2cac-111">Return value</span></span>

<span data-ttu-id="c2cac-112">Establezca PSNRET \_ NoError para indicar que los cambios realizados en esta página son válidos y se han aplicado.</span><span class="sxs-lookup"><span data-stu-id="c2cac-112">Set PSNRET\_NOERROR to indicate that the changes made to this page are valid and have been applied.</span></span> <span data-ttu-id="c2cac-113">Si todas las páginas establecen PSNRET \_ NoError, se puede destruir la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2cac-113">If all pages set PSNRET\_NOERROR, the property sheet can be destroyed.</span></span> <span data-ttu-id="c2cac-114">Para indicar que los cambios realizados en esta página no son válidos y para evitar que se destruya la hoja de propiedades, establezca uno de los siguientes valores devueltos:</span><span class="sxs-lookup"><span data-stu-id="c2cac-114">To indicate that the changes made to this page are invalid and to prevent the property sheet from being destroyed, set one of the following return values:</span></span>

-   <span data-ttu-id="c2cac-115">PSNRET \_ no válido.</span><span class="sxs-lookup"><span data-stu-id="c2cac-115">PSNRET\_INVALID.</span></span> <span data-ttu-id="c2cac-116">La hoja de propiedades no se destruirá y se devolverá el foco a esta página.</span><span class="sxs-lookup"><span data-stu-id="c2cac-116">The property sheet will not be destroyed, and focus will be returned to this page.</span></span>
-   <span data-ttu-id="c2cac-117">PSNRET \_ NOCHANGEPAGE no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="c2cac-117">PSNRET\_INVALID\_NOCHANGEPAGE.</span></span> <span data-ttu-id="c2cac-118">La hoja de propiedades no se destruirá y el foco se devolverá a la página que tenía el foco cuando se presionó el botón.</span><span class="sxs-lookup"><span data-stu-id="c2cac-118">The property sheet will not be destroyed, and focus will be returned to the page that had focus when the button was pressed.</span></span>

<span data-ttu-id="c2cac-119">Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT y el procedimiento de cuadro de diálogo debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="c2cac-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cac-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2cac-120">Remarks</span></span>

<span data-ttu-id="c2cac-121">Cuando el usuario hace clic en el botón Aceptar, aplicar o cerrar, la hoja de propiedades envía una notificación de [PSN \_ KILLACTIVE](psn-killactive.md) a la página activa, lo que le permite validar los cambios del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2cac-121">When the user clicks the OK, Apply, or Close button, the property sheet sends a [PSN\_KILLACTIVE](psn-killactive.md) notification to the active page, giving it an opportunity to validate the user's changes.</span></span> <span data-ttu-id="c2cac-122">Si los cambios son válidos, la hoja de propiedades envía un PSN \_ aplicar código de notificación a cada página y le dirige para aplicar las nuevas propiedades al elemento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c2cac-122">If the changes are valid, the property sheet sends a PSN\_APPLY notification code to each page, directing it to apply the new properties to the corresponding item.</span></span>

> [!Note]  
> <span data-ttu-id="c2cac-123">La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación PSN.</span><span class="sxs-lookup"><span data-stu-id="c2cac-123">The property sheet is in the process of manipulating the list of pages when the PSN\_APPLY notification code is sent.</span></span> <span data-ttu-id="c2cac-124">No intente agregar, quitar o insertar páginas mientras controla esta notificación.</span><span class="sxs-lookup"><span data-stu-id="c2cac-124">Do not attempt to add, remove, or insert pages while handling this notification.</span></span> <span data-ttu-id="c2cac-125">Si lo hace, tendrá resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="c2cac-125">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="c2cac-126">El miembro **lParam** de la estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) señalada por *lParam* se establece en **true** si el usuario hace clic en el botón Aceptar.</span><span class="sxs-lookup"><span data-stu-id="c2cac-126">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* is set to **TRUE** if the user clicks the OK button.</span></span> <span data-ttu-id="c2cac-127">También se establece en **true** si se ha enviado el mensaje de [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) y el usuario hace clic en el botón Cerrar.</span><span class="sxs-lookup"><span data-stu-id="c2cac-127">It is also set to **TRUE** if the [**PSM\_CANCELTOCLOSE**](psm-canceltoclose.md) message has been sent and the user clicks the Close button.</span></span> <span data-ttu-id="c2cac-128">Se establece en **false** si el usuario hace clic en el botón aplicar.</span><span class="sxs-lookup"><span data-stu-id="c2cac-128">It is set to **FALSE** if the user clicks the Apply button.</span></span>

<span data-ttu-id="c2cac-129">La estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2cac-129">The [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="c2cac-130">No llame a la función [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) al procesar este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="c2cac-130">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

<span data-ttu-id="c2cac-131">Se destruye una hoja de propiedades modal si el usuario hace clic en el botón Aceptar y todas las páginas devuelven el \_ valor PSNRET NoError en respuesta a **PSN \_ Apply**.</span><span class="sxs-lookup"><span data-stu-id="c2cac-131">A modal property sheet is destroyed if the user clicks the OK button and every page returns the PSNRET\_NOERROR value in response to **PSN\_APPLY**.</span></span> <span data-ttu-id="c2cac-132">Si cualquier página devuelve PSNRET no \_ válido o PSNRET \_ NOCHANGEPAGE no válido \_ , el proceso de aplicación se cancela inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c2cac-132">If any page returns PSNRET\_INVALID or PSNRET\_INVALID\_NOCHANGEPAGE, the Apply process is canceled immediately.</span></span> <span data-ttu-id="c2cac-133">Páginas después de la cancelación de la página no recibirá un código de notificación de aplicación de PSN \_ .</span><span class="sxs-lookup"><span data-stu-id="c2cac-133">Pages after the cancelling page will not receive a PSN\_APPLY notification code.</span></span>

<span data-ttu-id="c2cac-134">Para recibir este código de notificación, una página debe establecer el \_ valor de DWL MSGRESULT en **false** en respuesta al código de notificación de [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="c2cac-134">To receive this notification code, a page must set the DWL\_MSGRESULT value to **FALSE** in response to the [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span>

> [!Note]  
> <span data-ttu-id="c2cac-135">Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="c2cac-135">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2cac-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2cac-136">Requirements</span></span>



| <span data-ttu-id="c2cac-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2cac-137">Requirement</span></span> | <span data-ttu-id="c2cac-138">Value</span><span class="sxs-lookup"><span data-stu-id="c2cac-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cac-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2cac-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cac-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2cac-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c2cac-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2cac-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cac-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2cac-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c2cac-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2cac-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2cac-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2cac-144"><dt>Prsht.h</dt></span></span> </dl> |



 

