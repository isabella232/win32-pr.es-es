---
description: El \_ mensaje de línea de LINEDEVSTATE TAPI se envía cuando cambia el estado de un dispositivo de línea. La aplicación puede invocar lineGetLineDevStatus para determinar el nuevo estado de la línea.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Mensaje de LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690315"
---
# <a name="line_linedevstate-message"></a><span data-ttu-id="f2bbf-104">Mensaje de línea \_ LINEDEVSTATE</span><span class="sxs-lookup"><span data-stu-id="f2bbf-104">LINE\_LINEDEVSTATE message</span></span>

<span data-ttu-id="f2bbf-105">El mensaje de **línea de \_ LINEDEVSTATE** TAPI se envía cuando cambia el estado de un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-105">The TAPI **LINE\_LINEDEVSTATE** message is sent when the state of a line device has changed.</span></span> <span data-ttu-id="f2bbf-106">La aplicación puede invocar [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) para determinar el nuevo estado de la línea.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-106">The application can invoke [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) to determine the new status of the line.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f2bbf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2bbf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2bbf-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f2bbf-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f2bbf-109">Identificador del dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-109">A handle to the line device.</span></span> <span data-ttu-id="f2bbf-110">Este parámetro es **null** cuando *dwParam1* es LINEDEVSTATE \_ reinit.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-110">This parameter is **NULL** when *dwParam1* is LINEDEVSTATE\_REINIT.</span></span>

</dd> <dt>

<span data-ttu-id="f2bbf-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f2bbf-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f2bbf-112">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-112">The callback instance supplied when opening the line.</span></span> <span data-ttu-id="f2bbf-113">Si el parámetro *dwParam1* es LINEDEVSTATE \_ reinit, el parámetro *dwCallbackInstance* no es válido y se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-113">If the *dwParam1* parameter is LINEDEVSTATE\_REINIT, the *dwCallbackInstance* parameter is not valid and is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f2bbf-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f2bbf-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f2bbf-115">El elemento de estado de dispositivo de línea que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-115">The line device status item that has changed.</span></span> <span data-ttu-id="f2bbf-116">El parámetro puede ser una o varias de las [**\_ constantes LINEDEVSTATE**](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbf-116">The parameter can be one or more of the [**LINEDEVSTATE\_ constants**](linedevstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2bbf-117">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f2bbf-117">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f2bbf-118">La interpretación de este parámetro depende del valor de *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-118">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="f2bbf-119">Si *dwParam1* es LINEDEVSTATE \_ Ringing, *dwParam2* contiene el modo de anillo con el que el modificador indica a la línea que suene.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-119">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam2* contains the ring mode with which the switch instructs the line to ring.</span></span> <span data-ttu-id="f2bbf-120">Los modos de anillo válidos son números en el intervalo de uno a **dwNumRingModes**, donde **dwNumRingModes** es una funcionalidad de dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-120">Valid ring modes are numbers in the range one to **dwNumRingModes**, where **dwNumRingModes** is a line device capability.</span></span>

<span data-ttu-id="f2bbf-121">Si *dwParam1* es LINEDEVSTATE \_ reinit y TAPI emitió el mensaje como resultado de la conversión de un nuevo mensaje de API en un mensaje de reinicialización, *DwParam2* contiene el parámetro *dwMsg* del mensaje original (por ejemplo, [**line \_ Create**](line-create.md) o line \_ LINEDEVSTATE).</span><span class="sxs-lookup"><span data-stu-id="f2bbf-121">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam2* contains the *dwMsg* parameter of the original message (for example, [**LINE\_CREATE**](line-create.md) or LINE\_LINEDEVSTATE).</span></span> <span data-ttu-id="f2bbf-122">Si *dwParam2* es cero, indica que el mensaje de reinicialización es un mensaje de reinicialización "real" que requiere que la aplicación llame a [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-122">If *dwParam2* is zero, this indicates that the REINIT message is a "real" REINIT message that requires the application to call [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) at its earliest convenience.</span></span>

</dd> <dt>

<span data-ttu-id="f2bbf-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f2bbf-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f2bbf-124">La interpretación de este parámetro depende del valor de *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-124">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="f2bbf-125">Si *dwParam1* es LINEDEVSTATE \_ Ringing, *dwParam3* contiene el recuento de anillos para este evento de anillo.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-125">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam3* contains the ring count for this ring event.</span></span> <span data-ttu-id="f2bbf-126">El número de anillos comienza en cero.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-126">The ring count starts at zero.</span></span>

<span data-ttu-id="f2bbf-127">Si *dwParam1* es LINEDEVSTATE \_ reinit y TAPI emitió el mensaje como resultado de la conversión de un nuevo mensaje de API en un mensaje de reinicialización, *DwParam3* contiene el parámetro *dwParam1* del mensaje original (por ejemplo, LINEDEVSTATE \_ TRANSLATECHANGE o algún otro \_ valor LINEDEVSTATE, si *dwParam2* es la línea \_ LINEDEVSTATE o el nuevo identificador de dispositivo, si *dwParam2* es [**line \_ Create**](line-create.md)).</span><span class="sxs-lookup"><span data-stu-id="f2bbf-127">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam3* contains the *dwParam1* parameter of the original message (for example, LINEDEVSTATE\_TRANSLATECHANGE or some other LINEDEVSTATE\_ value, if *dwParam2* is LINE\_LINEDEVSTATE, or the new device identifier, if *dwParam2* is [**LINE\_CREATE**](line-create.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2bbf-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2bbf-128">Return value</span></span>

<span data-ttu-id="f2bbf-129">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-129">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2bbf-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2bbf-130">Remarks</span></span>

<span data-ttu-id="f2bbf-131">El envío del mensaje **line \_ LINEDEVSTATE** se puede controlar con [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="f2bbf-131">The sending of the **LINE\_LINEDEVSTATE** message can be controlled with [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="f2bbf-132">Una aplicación puede indicar cambios en el elemento de estado sobre los que desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-132">An application can indicate status item changes about which it wants to be notified.</span></span> <span data-ttu-id="f2bbf-133">De forma predeterminada, todos los informes de estado se deshabilitan, excepto LINEDEVSTATE \_ reinit, que no se puede deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-133">By default, all status reporting is disabled except for LINEDEVSTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="f2bbf-134">Este mensaje se envía a todas las aplicaciones que tienen un identificador a la línea, incluidos los que llaman a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con el parámetro *DWPRIVILEGES* establecido en LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ monitor o las combinaciones permitidas de estos.</span><span class="sxs-lookup"><span data-stu-id="f2bbf-134">This message is sent to all applications that have a handle to the line, including those that called [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) with the *dwPrivileges* parameter set to LINECALLPRIVILEGE\_NONE, LINECALLPRIVILEGE\_OWNER, LINECALLPRIVILEGE\_MONITOR, or permitted combinations of these.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bbf-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2bbf-135">Requirements</span></span>



| <span data-ttu-id="f2bbf-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2bbf-136">Requirement</span></span> | <span data-ttu-id="f2bbf-137">Value</span><span class="sxs-lookup"><span data-stu-id="f2bbf-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f2bbf-138">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f2bbf-138">TAPI version</span></span><br/> | <span data-ttu-id="f2bbf-139">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f2bbf-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f2bbf-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2bbf-140">Header</span></span><br/>       | <dl> <span data-ttu-id="f2bbf-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2bbf-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2bbf-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2bbf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bbf-143">**cierre de línea \_**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-143">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="f2bbf-144">**creación de línea \_**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-144">**LINE\_CREATE**</span></span>](line-create.md)
</dt> <dt>

[<span data-ttu-id="f2bbf-145">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-145">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="f2bbf-146">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-146">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="f2bbf-147">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-147">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="f2bbf-148">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-148">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="f2bbf-149">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-149">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="f2bbf-150">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-150">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="f2bbf-151">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-151">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="f2bbf-152">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-152">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[<span data-ttu-id="f2bbf-153">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-153">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="f2bbf-154">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="f2bbf-154">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




