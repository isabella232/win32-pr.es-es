---
description: El mensaje de línea de \_ GATHERDIGITS TAPI se envía cuando la solicitud de recopilación de dígitos almacenada en búfer actual ha finalizado o se ha cancelado. El búfer de dígitos se puede examinar una vez que la aplicación ha recibido este mensaje.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Mensaje de LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679468"
---
# <a name="line_gatherdigits-message"></a><span data-ttu-id="c6339-104">Mensaje de línea \_ GATHERDIGITS</span><span class="sxs-lookup"><span data-stu-id="c6339-104">LINE\_GATHERDIGITS message</span></span>

<span data-ttu-id="c6339-105">El mensaje de **línea de \_ GATHERDIGITS** TAPI se envía cuando la solicitud de recopilación de dígitos almacenada en búfer actual ha finalizado o se ha cancelado.</span><span class="sxs-lookup"><span data-stu-id="c6339-105">The TAPI **LINE\_GATHERDIGITS** message is sent when the current buffered digit-gathering request has terminated or is canceled.</span></span> <span data-ttu-id="c6339-106">El búfer de dígitos se puede examinar una vez que la aplicación ha recibido este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c6339-106">The digit buffer can be examined after this message has been received by the application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="c6339-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6339-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6339-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="c6339-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c6339-109">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c6339-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="c6339-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="c6339-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c6339-111">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="c6339-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="c6339-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c6339-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="c6339-113">Motivo por el que finalizó la recopilación de dígitos.</span><span class="sxs-lookup"><span data-stu-id="c6339-113">The reason why digit gathering was terminated.</span></span> <span data-ttu-id="c6339-114">Este parámetro debe ser una y solo una de las [**\_ constantes LINEGATHERTERM**](linegatherterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c6339-114">This parameter must be one and only one of the [**LINEGATHERTERM\_ constants**](linegatherterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6339-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c6339-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="c6339-116">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="c6339-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c6339-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="c6339-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="c6339-118">"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se completó la recopilación del dígito.</span><span class="sxs-lookup"><span data-stu-id="c6339-118">The "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.</span></span> <span data-ttu-id="c6339-119">En el caso de las versiones de TAPI anteriores a 2,0, este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c6339-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6339-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6339-120">Return value</span></span>

<span data-ttu-id="c6339-121">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c6339-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6339-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6339-122">Remarks</span></span>

<span data-ttu-id="c6339-123">El mensaje **line \_ GATHERDIGITS** solo se envía a la aplicación que inició la recopilación de dígitos en la llamada con [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span><span class="sxs-lookup"><span data-stu-id="c6339-123">The **LINE\_GATHERDIGITS** message is only sent to the application that initiated the digit gathering on the call using [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span></span>

<span data-ttu-id="c6339-124">Si se usa la función [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) para cancelar una solicitud anterior para recopilar dígitos, TAPI envía un mensaje de **línea \_ GATHERDIGITS** con *dwParam1* establecido en LINEGATHERTERM \_ cancelar a la aplicación que indica que el búfer especificado originalmente contiene los dígitos recopilados hasta la cancelación.</span><span class="sxs-lookup"><span data-stu-id="c6339-124">If the [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) function is used to cancel a previous request to gather digits, TAPI sends a **LINE\_GATHERDIGITS** message with *dwParam1* set to LINEGATHERTERM\_CANCEL to the application indicating that the originally specified buffer contains the digits gathered up to the cancellation.</span></span>

<span data-ttu-id="c6339-125">Dado que la marca de tiempo especificada por *dwParam3* puede haberse generado en un equipo que no sea el en el que se está ejecutando la aplicación, solo es útil para la comparación con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**\_ generación**](line-generate.md)de línea, [**línea \_ MONITORDIGITS**](line-monitordigits.md), línea [**\_ MONITORMEDIA**](line-monitormedia.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos).</span><span class="sxs-lookup"><span data-stu-id="c6339-125">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="c6339-126">El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="c6339-126">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="c6339-127">Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.</span><span class="sxs-lookup"><span data-stu-id="c6339-127">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

> [!Note]  
> <span data-ttu-id="c6339-128">Cuando una aplicación invoca cualquier operación asincrónica que vuelva a escribir datos en la memoria de la aplicación, la aplicación debe mantener esa memoria disponible para escritura hasta que se reciba un mensaje de línea o [**\_ respuesta de línea**](line-reply.md) **\_ GATHERDIGITS** .</span><span class="sxs-lookup"><span data-stu-id="c6339-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a [**LINE\_REPLY**](line-reply.md) or **LINE\_GATHERDIGITS** message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6339-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6339-129">Requirements</span></span>



| <span data-ttu-id="c6339-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6339-130">Requirement</span></span> | <span data-ttu-id="c6339-131">Value</span><span class="sxs-lookup"><span data-stu-id="c6339-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c6339-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c6339-132">TAPI version</span></span><br/> | <span data-ttu-id="c6339-133">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c6339-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c6339-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6339-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c6339-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6339-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6339-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6339-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6339-137">**generación de línea \_**</span><span class="sxs-lookup"><span data-stu-id="c6339-137">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="c6339-138">**LÍNEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="c6339-138">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="c6339-139">**LÍNEA \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="c6339-139">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="c6339-140">**LÍNEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="c6339-140">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="c6339-141">**respuesta de línea \_**</span><span class="sxs-lookup"><span data-stu-id="c6339-141">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="c6339-142">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="c6339-142">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




