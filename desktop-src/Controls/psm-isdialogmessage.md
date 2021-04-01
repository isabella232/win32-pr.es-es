---
title: Mensaje de PSM_ISDIALOGMESSAGE (Prsht. h)
description: Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905288"
---
# <a name="psm_isdialogmessage-message"></a><span data-ttu-id="d08c6-105">Mensaje de PSM \_ ISDIALOGMESSAGE</span><span class="sxs-lookup"><span data-stu-id="d08c6-105">PSM\_ISDIALOGMESSAGE message</span></span>

<span data-ttu-id="d08c6-106">Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d08c6-106">Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message.</span></span> <span data-ttu-id="d08c6-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .</span><span class="sxs-lookup"><span data-stu-id="d08c6-107">You can send this message explicitly or by using the [**PropSheet\_IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d08c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d08c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d08c6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d08c6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d08c6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d08c6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d08c6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d08c6-112">Puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="d08c6-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08c6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d08c6-113">Return value</span></span>

<span data-ttu-id="d08c6-114">Devuelve **true** si se ha procesado el mensaje o **false** si el mensaje no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="d08c6-114">Returns **TRUE** if the message has been processed, or **FALSE** if the message has not been processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d08c6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d08c6-115">Remarks</span></span>

<span data-ttu-id="d08c6-116">El bucle de mensajes debería usar el mensaje **PSM \_ ISDIALOGMESSAGE** con hojas de propiedades no modales para pasar mensajes al cuadro de diálogo hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d08c6-116">Your message loop should use the **PSM\_ISDIALOGMESSAGE** message with modeless property sheets to pass messages to the property sheet dialog box.</span></span> <span data-ttu-id="d08c6-117">En los sistemas que admiten Unicode, use las versiones Unicode de las funciones [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) y [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** y **PeekMessageW**) para recuperar mensajes.</span><span class="sxs-lookup"><span data-stu-id="d08c6-117">On systems that support Unicode, use the Unicode versions of the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) functions (**GetMessageW** and **PeekMessageW**) to retrieve messages.</span></span>

<span data-ttu-id="d08c6-118">Si el valor devuelto indica que se procesó el mensaje, no se debe pasar a la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="d08c6-118">If the return value indicates that the message was processed, it must not be passed to the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) or [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function.</span></span>

> [!Note]  
> <span data-ttu-id="d08c6-119">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="d08c6-119">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d08c6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d08c6-120">Requirements</span></span>



| <span data-ttu-id="d08c6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08c6-121">Requirement</span></span> | <span data-ttu-id="d08c6-122">Value</span><span class="sxs-lookup"><span data-stu-id="d08c6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d08c6-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d08c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d08c6-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d08c6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d08c6-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d08c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d08c6-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d08c6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d08c6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d08c6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d08c6-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="d08c6-128"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08c6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d08c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08c6-130">**Hoja**</span><span class="sxs-lookup"><span data-stu-id="d08c6-130">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

