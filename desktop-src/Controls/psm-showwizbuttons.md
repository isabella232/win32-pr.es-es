---
title: Mensaje de PSM_SHOWWIZBUTTONS (Prsht. h)
description: Muestra u oculta los botones en un asistente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656490"
---
# <a name="psm_showwizbuttons-message"></a><span data-ttu-id="62811-105">Mensaje de PSM \_ SHOWWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="62811-105">PSM\_SHOWWIZBUTTONS message</span></span>

<span data-ttu-id="62811-106">Muestra u oculta los botones en un asistente.</span><span class="sxs-lookup"><span data-stu-id="62811-106">Shows or hides buttons in a wizard.</span></span> <span data-ttu-id="62811-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="62811-107">You can send this message explicitly or by using the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="62811-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62811-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62811-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62811-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62811-110">Uno o varios de los siguientes valores que especifican qué botones de la hoja de propiedades se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="62811-110">One or more of the following values that specify which property sheet buttons are to be shown.</span></span> <span data-ttu-id="62811-111">Si un valor de botón está incluido en este parámetro y *lParam*, se muestra.</span><span class="sxs-lookup"><span data-stu-id="62811-111">If a button value is included in both this parameter and *lParam*, it is shown.</span></span>



| <span data-ttu-id="62811-112">Value</span><span class="sxs-lookup"><span data-stu-id="62811-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="62811-113">Significado</span><span class="sxs-lookup"><span data-stu-id="62811-113">Meaning</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="62811-114"><dt>**PSWIZB \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="62811-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="62811-115">Botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="62811-115">The **Back** button.</span></span><br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="62811-116"><dt>**\_Cancelar PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="62811-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="62811-117">Botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="62811-117">The **Cancel** button.</span></span><br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="62811-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="62811-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="62811-119">El botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="62811-119">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="62811-120"><dt>**\_Finalizar PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="62811-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="62811-121">El botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="62811-121">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="62811-122"><dt>**PSWIZB \_ siguiente**</dt></span><span class="sxs-lookup"><span data-stu-id="62811-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="62811-123">Botón **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="62811-123">The **Next** button.</span></span><br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <span data-ttu-id="62811-124"><dt>**PSWIZB \_ Mostrar**</dt></span><span class="sxs-lookup"><span data-stu-id="62811-124"><dt>**PSWIZB\_SHOW**</dt></span></span> </dl>                               | <span data-ttu-id="62811-125">Establezca solo esta marca (definida como cero) para ocultar todos los botones especificados en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="62811-125">Set only this flag (defined as zero) to hide all buttons specified in *lParam*.</span></span><br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <span data-ttu-id="62811-126"><dt>**restauración de PSWIZB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62811-126"><dt>**PSWIZB\_RESTORE**</dt></span></span> </dl>                      | <span data-ttu-id="62811-127">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="62811-127">Not implemented.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="62811-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62811-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62811-129">Uno o varios de los mismos valores utilizados en *wParam*, que especifican qué botones se ven afectados por esta llamada.</span><span class="sxs-lookup"><span data-stu-id="62811-129">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="62811-130">Si aparece un valor de botón en este parámetro pero no en *wParam*, el botón está oculto.</span><span class="sxs-lookup"><span data-stu-id="62811-130">If a button value appears in this parameter but not in *wParam*, the button is hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62811-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62811-131">Return value</span></span>

<span data-ttu-id="62811-132">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="62811-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62811-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62811-133">Remarks</span></span>

<span data-ttu-id="62811-134">Los asistentes muestran tres o cuatro botones debajo de cada página.</span><span class="sxs-lookup"><span data-stu-id="62811-134">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="62811-135">Este mensaje se usa para especificar qué botones son visibles.</span><span class="sxs-lookup"><span data-stu-id="62811-135">This message is used to specify which buttons are visible.</span></span> <span data-ttu-id="62811-136">Los asistentes muestran normalmente **atrás**, **Cancelar** y un botón **siguiente** o **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="62811-136">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="62811-137">El botón **Cancelar** siempre está visible.</span><span class="sxs-lookup"><span data-stu-id="62811-137">The **Cancel** button is always visible.</span></span>

<span data-ttu-id="62811-138">Normalmente, establezca **PSWIZB \_ Finish** o **PSWIZB \_ DISABLEDFINISH** para reemplazar el botón **siguiente** por un botón **Finalizar** .</span><span class="sxs-lookup"><span data-stu-id="62811-138">Typically, set **PSWIZB\_FINISH** or **PSWIZB\_DISABLEDFINISH** to replace the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="62811-139">Para mostrar los botones **siguiente** y **Finalizar** simultáneamente, establezca la marca **PSH \_ WIZARDHASFINISH** en el miembro **dwFlags** de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) al crear el asistente.</span><span class="sxs-lookup"><span data-stu-id="62811-139">To display **Next** and **Finish** buttons simultaneously, set the **PSH\_WIZARDHASFINISH** flag in the **dwFlags** member of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="62811-140">Cada página mostrará los cuatro botones: **atrás**, **siguiente**, **Cancelar** y **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="62811-140">Every page will then display all four buttons: **Back**, **Next**, **Cancel**, and **Finish**.</span></span>

<span data-ttu-id="62811-141">Si usa la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) para enviar este mensaje, se publicará.</span><span class="sxs-lookup"><span data-stu-id="62811-141">If you use the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="62811-142">En cualquier otro momento, puede usar [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar **PSM \_ SHOWWIZBUTTONS**.</span><span class="sxs-lookup"><span data-stu-id="62811-142">At any other time, you can use [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to send **PSM\_SHOWWIZBUTTONS**.</span></span>

<span data-ttu-id="62811-143">Si el controlador de notificaciones usa [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) para enviar un mensaje de **PSM \_ SHOWWIZBUTTONS** , no haga nada que afecte al foco de la ventana hasta después de que se devuelva el controlador.</span><span class="sxs-lookup"><span data-stu-id="62811-143">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SHOWWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="62811-144">Por ejemplo, si llama a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) inmediatamente después de usar **PostMessage** para **enviar \_ PSM SHOWWIZBUTTONS**, el cuadro de mensaje recibirá el foco.</span><span class="sxs-lookup"><span data-stu-id="62811-144">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SHOWWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="62811-145">Dado que los mensajes expuestos no se entregan hasta que alcanzan el encabezado de la cola de mensajes, el mensaje de **PSM \_ SHOWWIZBUTTONS** no se entregará hasta que el asistente haya perdido el foco en el cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="62811-145">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SHOWWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="62811-146">Como resultado, la hoja de propiedades no podrá establecer correctamente el foco de los botones.</span><span class="sxs-lookup"><span data-stu-id="62811-146">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="62811-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62811-147">Requirements</span></span>



| <span data-ttu-id="62811-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="62811-148">Requirement</span></span> | <span data-ttu-id="62811-149">Value</span><span class="sxs-lookup"><span data-stu-id="62811-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62811-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62811-150">Minimum supported client</span></span><br/> | <span data-ttu-id="62811-151">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="62811-151">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="62811-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62811-152">Minimum supported server</span></span><br/> | <span data-ttu-id="62811-153">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="62811-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="62811-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62811-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="62811-155"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="62811-155"><dt>Prsht.h</dt></span></span> </dl> |



 

