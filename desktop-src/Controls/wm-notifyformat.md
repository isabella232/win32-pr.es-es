---
title: Mensaje de WM_NOTIFYFORMAT (Winuser. h)
description: Determina si una ventana acepta estructuras ANSI o Unicode en el \_ mensaje de notificación de notificaciones de WM. \_Los mensajes NOTIFYFORMAT de WM se envían desde un control común a su ventana primaria y desde la ventana primaria al control común.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- WM_NOTIFYFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996634"
---
# <a name="wm_notifyformat-message"></a><span data-ttu-id="24949-105">Mensaje de NOTIFYFORMAT de WM \_</span><span class="sxs-lookup"><span data-stu-id="24949-105">WM\_NOTIFYFORMAT message</span></span>

<span data-ttu-id="24949-106">Determina si una ventana acepta estructuras ANSI o Unicode en el mensaje de notificación de [**\_ notificaciones de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="24949-106">Determines if a window accepts ANSI or Unicode structures in the [**WM\_NOTIFY**](wm-notify.md) notification message.</span></span> <span data-ttu-id="24949-107">**WM \_** Los mensajes NOTIFYFORMAT se envían desde un control común a su ventana primaria y desde la ventana primaria al control común.</span><span class="sxs-lookup"><span data-stu-id="24949-107">**WM\_NOTIFYFORMAT** messages are sent from a common control to its parent window and from the parent window to the common control.</span></span>

## <a name="parameters"></a><span data-ttu-id="24949-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24949-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24949-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24949-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24949-110">Identificador de la ventana que está enviando el mensaje **de \_ NOTIFYFORMAT de WM** .</span><span class="sxs-lookup"><span data-stu-id="24949-110">A handle to the window that is sending the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="24949-111">Si *lParam* es \_ una consulta de NF, este parámetro es el identificador de un control.</span><span class="sxs-lookup"><span data-stu-id="24949-111">If *lParam* is NF\_QUERY, this parameter is the handle to a control.</span></span> <span data-ttu-id="24949-112">Si *lParam* es \_ la reconsulta de NF, este parámetro es el identificador de la ventana primaria de un control.</span><span class="sxs-lookup"><span data-stu-id="24949-112">If *lParam* is NF\_REQUERY, this parameter is the handle to the parent window of a control.</span></span>

</dd> <dt>

<span data-ttu-id="24949-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24949-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24949-114">Valor del comando que especifica la naturaleza del mensaje **de \_ NOTIFYFORMAT de WM** .</span><span class="sxs-lookup"><span data-stu-id="24949-114">The command value that specifies the nature of the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="24949-115">Este será uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="24949-115">This will be one of the following values:</span></span>



| <span data-ttu-id="24949-116">Value</span><span class="sxs-lookup"><span data-stu-id="24949-116">Value</span></span>                                                                                                                                                | <span data-ttu-id="24949-117">Significado</span><span class="sxs-lookup"><span data-stu-id="24949-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <span data-ttu-id="24949-118"><dt>**NF ( \_ consulta)**</dt></span><span class="sxs-lookup"><span data-stu-id="24949-118"><dt>**NF\_QUERY**</dt></span></span> </dl>       | <span data-ttu-id="24949-119">El mensaje es una consulta para determinar si se deben usar estructuras ANSI o Unicode en los mensajes de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="24949-119">The message is a query to determine whether ANSI or Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="24949-120">Este comando se envía desde un control a su ventana primaria durante la creación de un control y en respuesta a un \_ comando de REquery de NF.</span><span class="sxs-lookup"><span data-stu-id="24949-120">This command is sent from a control to its parent window during the creation of a control and in response to an NF\_REQUERY command.</span></span><br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <span data-ttu-id="24949-121"><dt>**\_nueva consulta de NF**</dt></span><span class="sxs-lookup"><span data-stu-id="24949-121"><dt>**NF\_REQUERY**</dt></span></span> </dl> | <span data-ttu-id="24949-122">El mensaje es una solicitud para que un control envíe un \_ formulario de consulta de NF de este mensaje a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="24949-122">The message is a request for a control to send an NF\_QUERY form of this message to its parent window.</span></span> <span data-ttu-id="24949-123">Este comando se envía desde la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="24949-123">This command is sent from the parent window.</span></span> <span data-ttu-id="24949-124">La ventana primaria pide al control que vuelva a consultarlo sobre el tipo de estructuras que se va a usar en los mensajes de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="24949-124">The parent window is asking the control to requery it about the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="24949-125">Si *lParam* es la \_ reconsulta de NF, el valor devuelto es el resultado de la operación de reconsulta.</span><span class="sxs-lookup"><span data-stu-id="24949-125">If *lParam* is NF\_REQUERY, the return value is the result of the requery operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24949-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24949-126">Return value</span></span>

<span data-ttu-id="24949-127">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="24949-127">Returns one of the following values.</span></span>



| <span data-ttu-id="24949-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="24949-128">Return code</span></span>                                                                                 | <span data-ttu-id="24949-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="24949-129">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24949-130"><dt>**\_ANSI NFR**</dt></span><span class="sxs-lookup"><span data-stu-id="24949-130"><dt>**NFR\_ANSI**</dt></span></span> </dl>    | <span data-ttu-id="24949-131">Las estructuras ANSI deben usarse en los mensajes de [**\_ notificación de WM**](wm-notify.md) enviados por el control.</span><span class="sxs-lookup"><span data-stu-id="24949-131">ANSI structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span><br/>     |
| <dl> <span data-ttu-id="24949-132"><dt>**Unicode NFR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24949-132"><dt>**NFR\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="24949-133">Las estructuras Unicode se deben usar en los mensajes de [**\_ notificación de WM**](wm-notify.md) enviados por el control.</span><span class="sxs-lookup"><span data-stu-id="24949-133">Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span> <br/> |
| <dl> <span data-ttu-id="24949-134"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="24949-134"><dt>**0**</dt></span></span> </dl>            | <span data-ttu-id="24949-135">Se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="24949-135">An error occurred.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="24949-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24949-136">Remarks</span></span>

<span data-ttu-id="24949-137">Cuando se crea un control común, el control envía un mensaje de **WM \_ NOTIFYFORMAT** a su ventana primaria para determinar el tipo de estructuras que se van a usar en los mensajes de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="24949-137">When a common control is created, the control sends a **WM\_NOTIFYFORMAT** message to its parent window to determine the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="24949-138">Si la ventana primaria no controla este mensaje, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) responde según el tipo de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="24949-138">If the parent window does not handle this message, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function responds according to the type of the parent window.</span></span> <span data-ttu-id="24949-139">Es decir, si la ventana primaria es una ventana Unicode, **DefWindowProc** devuelve \_ Unicode NFR y, si la ventana primaria es una ventana ANSI, **DEFWINDOWPROC** devuelve el \_ ANSI NFR.</span><span class="sxs-lookup"><span data-stu-id="24949-139">That is, if the parent window is a Unicode window, **DefWindowProc** returns NFR\_UNICODE, and if the parent window is an ANSI window, **DefWindowProc** returns NFR\_ANSI.</span></span> <span data-ttu-id="24949-140">Si la ventana primaria es un cuadro de diálogo y no controla este mensaje, la función [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) responde de forma similar según el tipo de cuadro de diálogo (Unicode o ANSI).</span><span class="sxs-lookup"><span data-stu-id="24949-140">If the parent window is a dialog box and does not handle this message, the [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) function similarly responds according to the type of the dialog box (Unicode or ANSI).</span></span>

<span data-ttu-id="24949-141">Una ventana primaria puede cambiar el tipo de estructuras que usa un control común en los mensajes de [**\_ notificación de WM**](wm-notify.md) si establece *lParam* en NF \_ Requery y envía un mensaje de **WM \_ NOTIFYFORMAT** al control.</span><span class="sxs-lookup"><span data-stu-id="24949-141">A parent window can change the type of structures a common control uses in [**WM\_NOTIFY**](wm-notify.md) messages by setting *lParam* to NF\_REQUERY and sending a **WM\_NOTIFYFORMAT** message to the control.</span></span> <span data-ttu-id="24949-142">Esto hace que el control envíe un \_ formulario de consulta de NF del mensaje de **\_ NOTIFYFORMAT de WM** a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="24949-142">This causes the control to send an NF\_QUERY form of the **WM\_NOTIFYFORMAT** message to the parent window.</span></span>

<span data-ttu-id="24949-143">Todos los controles comunes enviarán mensajes de **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="24949-143">All common controls will send **WM\_NOTIFYFORMAT** messages.</span></span> <span data-ttu-id="24949-144">Sin embargo, los controles estándar de Windows (controles de edición, cuadros combinados, cuadros de lista, botones, barras de desplazamiento y controles estáticos) no.</span><span class="sxs-lookup"><span data-stu-id="24949-144">However, the standard Windows controls (edit controls, combo boxes, list boxes, buttons, scroll bars, and static controls) do not.</span></span>

## <a name="requirements"></a><span data-ttu-id="24949-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24949-145">Requirements</span></span>



| <span data-ttu-id="24949-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="24949-146">Requirement</span></span> | <span data-ttu-id="24949-147">Value</span><span class="sxs-lookup"><span data-stu-id="24949-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="24949-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24949-148">Minimum supported client</span></span><br/> | <span data-ttu-id="24949-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="24949-149">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="24949-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24949-150">Minimum supported server</span></span><br/> | <span data-ttu-id="24949-151">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="24949-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="24949-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24949-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="24949-153"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="24949-153"><dt>Winuser.h</dt></span></span> </dl> |



 

