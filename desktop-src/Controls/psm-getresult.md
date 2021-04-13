---
title: Mensaje de PSM_GETRESULT (Prsht. h)
description: Lo usan las hojas de propiedades no modales para recuperar la información devuelta a las hojas de propiedades modales por hoja. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet GetResult.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534917"
---
# <a name="psm_getresult-message"></a><span data-ttu-id="21758-105">Mensaje de PSM \_ GETRESULT</span><span class="sxs-lookup"><span data-stu-id="21758-105">PSM\_GETRESULT message</span></span>

<span data-ttu-id="21758-106">Lo usan las hojas de propiedades no modales para recuperar la información devuelta a las hojas de propiedades modales por [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span><span class="sxs-lookup"><span data-stu-id="21758-106">Used by modeless property sheets to retrieve the information returned to modal property sheets by [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span></span> <span data-ttu-id="21758-107">Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .</span><span class="sxs-lookup"><span data-stu-id="21758-107">You can send this message explicitly or use the [**PropSheet\_GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="21758-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21758-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21758-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21758-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="21758-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="21758-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21758-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21758-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="21758-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21758-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21758-113">Return value</span></span>

<span data-ttu-id="21758-114">Devuelve un valor positivo si es correcto, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="21758-114">Returns a positive value if successful, or -1 otherwise.</span></span> <span data-ttu-id="21758-115">Los siguientes valores devueltos tienen un significado especial.</span><span class="sxs-lookup"><span data-stu-id="21758-115">The following return values have a special meaning.</span></span>



| <span data-ttu-id="21758-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="21758-116">Return code</span></span>                                                                                         | <span data-ttu-id="21758-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="21758-117">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21758-118"><dt>**ID \_ PSREBOOTSYSTEM**</dt></span><span class="sxs-lookup"><span data-stu-id="21758-118"><dt>**ID\_PSREBOOTSYSTEM**</dt></span></span> </dl>   | <span data-ttu-id="21758-119">Una página envió un mensaje de [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) a la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="21758-119">A page sent a [**PSM\_REBOOTSYSTEM**](psm-rebootsystem.md) message to the property sheet.</span></span> <span data-ttu-id="21758-120">El equipo debe reiniciarse para que los cambios del usuario surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="21758-120">The computer must be restarted for the user's changes to take effect.</span></span><br/> |
| <dl> <span data-ttu-id="21758-121"><dt>**ID \_ PSRESTARTWINDOWS**</dt></span><span class="sxs-lookup"><span data-stu-id="21758-121"><dt>**ID\_PSRESTARTWINDOWS**</dt></span></span> </dl> | <span data-ttu-id="21758-122">Una página envió un mensaje de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) a la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="21758-122">A page sent a [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) message to the property sheet.</span></span> <span data-ttu-id="21758-123">Windows debe reiniciarse para que los cambios del usuario surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="21758-123">Windows must be restarted for the user's changes to take effect.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="21758-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21758-124">Remarks</span></span>

<span data-ttu-id="21758-125">Para recuperar la información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="21758-125">To retrieve extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="21758-126">El valor devuelto para este mensaje es idéntico al que devuelve [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para una hoja de propiedades modal.</span><span class="sxs-lookup"><span data-stu-id="21758-126">The return value for this message is identical to what [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) returns for a modal property sheet.</span></span>

[<span data-ttu-id="21758-127">Versión 5,80.</span><span class="sxs-lookup"><span data-stu-id="21758-127">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="21758-128">El valor devuelto de [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) incluye información diferente para las hojas de propiedades modales y no modales.</span><span class="sxs-lookup"><span data-stu-id="21758-128">The [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) return value carries different information for modal and modeless property sheets.</span></span> <span data-ttu-id="21758-129">En algunos casos, las hojas de propiedades no modales pueden necesitar la información que habrían recibido de **hoja** si hubieran sido modales.</span><span class="sxs-lookup"><span data-stu-id="21758-129">In some cases, modeless property sheets may need the information they would have received from **PropertySheet** if they had been modal.</span></span> <span data-ttu-id="21758-130">En concreto, es posible que necesite saber si se habrían \_ devuelto el identificador PSREBOOTSYSTEM o ID \_ PSRESTARTWINDOWS.</span><span class="sxs-lookup"><span data-stu-id="21758-130">In particular, they may need to know whether ID\_PSREBOOTSYSTEM or ID\_PSRESTARTWINDOWS would have been returned.</span></span>

<span data-ttu-id="21758-131">En una hoja de propiedades no modal, el bucle de mensajes debe usar [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) para pasar mensajes al cuadro de diálogo de la hoja de propiedades y [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) para determinar cuándo se debe destruir el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="21758-131">For a modeless property sheet, your message loop should use [**PSM\_ISDIALOGMESSAGE**](psm-isdialogmessage.md) to pass messages to the property sheet dialog box, and [**PSM\_GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) to determine when to destroy the dialog box.</span></span> <span data-ttu-id="21758-132">Cuando el usuario hace clic en el botón **Aceptar** o **Cancelar** , **PSM \_ GETCURRENTPAGEHWND** devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="21758-132">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**.</span></span> <span data-ttu-id="21758-133">Después, puede recuperar el valor que una hoja de propiedades modal habría recibido de [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) mediante el envío de un mensaje de **PSM \_ GETRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21758-133">You can then retrieve the value that a modal property sheet would have received from [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) by sending a **PSM\_GETRESULT** message.</span></span>

> [!Note]  
> <span data-ttu-id="21758-134">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="21758-134">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21758-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21758-135">Requirements</span></span>



| <span data-ttu-id="21758-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="21758-136">Requirement</span></span> | <span data-ttu-id="21758-137">Value</span><span class="sxs-lookup"><span data-stu-id="21758-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21758-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21758-138">Minimum supported client</span></span><br/> | <span data-ttu-id="21758-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="21758-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="21758-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21758-140">Minimum supported server</span></span><br/> | <span data-ttu-id="21758-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="21758-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="21758-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21758-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="21758-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="21758-143"><dt>Prsht.h</dt></span></span> </dl> |



 

