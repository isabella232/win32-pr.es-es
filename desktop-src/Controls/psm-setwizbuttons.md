---
title: Mensaje de PSM_SETWIZBUTTONS (Prsht. h)
description: Habilita o deshabilita los botones atrás, siguiente y finalizar en un asistente. También puede usar la macro PropSheet \_ SetWizButtons para publicar el mensaje.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- PSM_SETWIZBUTTONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150457"
---
# <a name="psm_setwizbuttons-message"></a><span data-ttu-id="c9896-105">Mensaje de PSM \_ SETWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="c9896-105">PSM\_SETWIZBUTTONS message</span></span>

<span data-ttu-id="c9896-106">Habilita o deshabilita los botones **atrás**, **siguiente** y **Finalizar** en un asistente.</span><span class="sxs-lookup"><span data-stu-id="c9896-106">Enables or disables the **Back**, **Next**, and **Finish** buttons in a wizard.</span></span> <span data-ttu-id="c9896-107">También puede usar la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para publicar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9896-107">You can also use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to post the message.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9896-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9896-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9896-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9896-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9896-110">Establezca este parámetro en PSWIZBF \_ ELEVATIONREQUIRED para mostrar el icono con privilegios elevados en los botones especificados en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c9896-110">Set this parameter to PSWIZBF\_ELEVATIONREQUIRED to display the elevated icon on the buttons specified in *lParam*.</span></span> <span data-ttu-id="c9896-111">El icono con privilegios elevados (o el icono de escudo de UAC) indica que se utilizará la petición de elevación para solicitar la aprobación del usuario o las credenciales.</span><span class="sxs-lookup"><span data-stu-id="c9896-111">The elevated icon (or UAC shield icon) indicates that the elevation prompt will be used to prompt the user for approval or credentials.</span></span> <span data-ttu-id="c9896-112">Para obtener más información, vea [diseñar aplicaciones de UAC para Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c9896-112">For more information, see [Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="c9896-113">La visualización del icono de escudo de UAC solo se admite en AeroWizards (PSH \_ AEROWIZARD).</span><span class="sxs-lookup"><span data-stu-id="c9896-113">Displaying the UAC shield icon is only supported in AeroWizards (PSH\_AEROWIZARD).</span></span>

 

</dd> <dt>

<span data-ttu-id="c9896-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9896-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9896-115">Valor que especifica qué botones de la hoja de propiedades están habilitados.</span><span class="sxs-lookup"><span data-stu-id="c9896-115">Value that specifies which property sheet buttons are enabled.</span></span> <span data-ttu-id="c9896-116">Puede combinar una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c9896-116">You can combine one or more of the following flags.</span></span>



| <span data-ttu-id="c9896-117">Value</span><span class="sxs-lookup"><span data-stu-id="c9896-117">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="c9896-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c9896-118">Meaning</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="c9896-119"><dt>**PSWIZB \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="c9896-119"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="c9896-120">Habilita el botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="c9896-120">Enables the **Back** button.</span></span> <span data-ttu-id="c9896-121">Si no se establece esta marca, el botón **atrás** se muestra como deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="c9896-121">If this flag is not set, the **Back** button is displayed as disabled.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="c9896-122"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="c9896-122"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="c9896-123">Muestra un botón **Finalizar** deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="c9896-123">Displays a disabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="c9896-124"><dt>**\_Finalizar PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="c9896-124"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="c9896-125">Muestra un botón **Finalizar** habilitado.</span><span class="sxs-lookup"><span data-stu-id="c9896-125">Displays an enabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="c9896-126"><dt>**PSWIZB \_ siguiente**</dt></span><span class="sxs-lookup"><span data-stu-id="c9896-126"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="c9896-127">Habilita el botón **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c9896-127">Enables the **Next** button.</span></span> <span data-ttu-id="c9896-128">Si no se establece esta marca, el botón **siguiente** se muestra como deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="c9896-128">If this flag is not set, the **Next** button is displayed as disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9896-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9896-129">Return value</span></span>

<span data-ttu-id="c9896-130">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c9896-130">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9896-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9896-131">Remarks</span></span>

<span data-ttu-id="c9896-132">Si el controlador de notificaciones usa [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) para enviar un mensaje de **PSM \_ SETWIZBUTTONS** , no haga nada que afecte al foco de la ventana hasta después de que se devuelva el controlador.</span><span class="sxs-lookup"><span data-stu-id="c9896-132">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SETWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="c9896-133">Por ejemplo, si llama a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) inmediatamente después de usar **PostMessage** para **enviar \_ PSM SETWIZBUTTONS**, el cuadro de mensaje recibirá el foco.</span><span class="sxs-lookup"><span data-stu-id="c9896-133">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SETWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="c9896-134">Dado que los mensajes expuestos no se entregan hasta que alcanzan el encabezado de la cola de mensajes, el mensaje de **PSM \_ SETWIZBUTTONS** no se entregará hasta que el asistente haya perdido el foco en el cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9896-134">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SETWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="c9896-135">Como resultado, la hoja de propiedades no podrá establecer correctamente el foco de los botones.</span><span class="sxs-lookup"><span data-stu-id="c9896-135">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

<span data-ttu-id="c9896-136">Si envía el \_ mensaje de PSM SETWIZBUTTONS durante el control de la notificación de [PSN \_ SETACTIVE](psn-setactive.md) , use la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) en lugar de la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="c9896-136">If you send the PSM\_SETWIZBUTTONS message during your handling of the [PSN\_SETACTIVE](psn-setactive.md) notification, use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function rather than the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="c9896-137">De lo contrario, el sistema no actualizará los botones correctamente.</span><span class="sxs-lookup"><span data-stu-id="c9896-137">Otherwise, the system will not update the buttons properly.</span></span> <span data-ttu-id="c9896-138">Si usa la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para enviar este mensaje, se publicará.</span><span class="sxs-lookup"><span data-stu-id="c9896-138">If you use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="c9896-139">En cualquier otro momento, puede usar **SendMessage** para enviar **PSM \_ SETWIZBUTTONS**.</span><span class="sxs-lookup"><span data-stu-id="c9896-139">At any other time, you can use **SendMessage** to send **PSM\_SETWIZBUTTONS**.</span></span>

<span data-ttu-id="c9896-140">Los asistentes muestran tres o cuatro botones debajo de cada página.</span><span class="sxs-lookup"><span data-stu-id="c9896-140">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="c9896-141">Este mensaje se usa para especificar qué botones están habilitados.</span><span class="sxs-lookup"><span data-stu-id="c9896-141">This message is used to specify which buttons are enabled.</span></span> <span data-ttu-id="c9896-142">Los asistentes muestran normalmente **atrás**, **Cancelar** y un botón **siguiente** o **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="c9896-142">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="c9896-143">Normalmente, solo se habilita el botón **siguiente** de la Página principal, **siguiente** y **atrás** para las páginas interiores y **atrás** y **Finalizar** para la página de finalización.</span><span class="sxs-lookup"><span data-stu-id="c9896-143">You typically enable only the **Next** button for the welcome page, **Next** and **Back** for interior pages, and **Back** and **Finish** for the completion page.</span></span> <span data-ttu-id="c9896-144">El botón **Cancelar** siempre está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c9896-144">The **Cancel** button is always enabled.</span></span> <span data-ttu-id="c9896-145">Normalmente, al establecer PSWIZB \_ Finish o PSWIZB DISABLEDFINISH, se \_ reemplaza el botón **siguiente** con un botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="c9896-145">Normally, setting PSWIZB\_FINISH or PSWIZB\_DISABLEDFINISH replaces the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="c9896-146">Para mostrar los botones **siguiente** y **Finalizar** simultáneamente, establezca la \_ marca PSH WIZARDHASFINISH en el miembro **dwFlags** de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) del asistente al crear el asistente.</span><span class="sxs-lookup"><span data-stu-id="c9896-146">To display **Next** and **Finish** buttons simultaneously, set the PSH\_WIZARDHASFINISH flag in the **dwFlags** member of the wizard's [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="c9896-147">Cada página mostrará los cuatro botones.</span><span class="sxs-lookup"><span data-stu-id="c9896-147">Every page will then display all four buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9896-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9896-148">Requirements</span></span>



| <span data-ttu-id="c9896-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9896-149">Requirement</span></span> | <span data-ttu-id="c9896-150">Value</span><span class="sxs-lookup"><span data-stu-id="c9896-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9896-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9896-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c9896-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9896-152">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c9896-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9896-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c9896-154">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9896-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c9896-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9896-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9896-156"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9896-156"><dt>Prsht.h</dt></span></span> </dl> |



 

