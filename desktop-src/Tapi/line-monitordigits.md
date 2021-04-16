---
description: El mensaje de línea de \_ MONITORDIGITS TAPI se envía cuando se detecta un dígito. El envío de este mensaje se controla con la función lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Mensaje de LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680253"
---
# <a name="line_monitordigits-message"></a><span data-ttu-id="a05c4-104">Mensaje de línea \_ MONITORDIGITS</span><span class="sxs-lookup"><span data-stu-id="a05c4-104">LINE\_MONITORDIGITS message</span></span>

<span data-ttu-id="a05c4-105">El mensaje de **línea de \_ MONITORDIGITS** TAPI se envía cuando se detecta un dígito.</span><span class="sxs-lookup"><span data-stu-id="a05c4-105">The TAPI **LINE\_MONITORDIGITS** message is sent when a digit is detected.</span></span> <span data-ttu-id="a05c4-106">El envío de este mensaje se controla con la función [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .</span><span class="sxs-lookup"><span data-stu-id="a05c4-106">The sending of this message is controlled with the [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a05c4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a05c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05c4-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a05c4-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a05c4-109">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a05c4-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="a05c4-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="a05c4-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a05c4-111">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a05c4-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="a05c4-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a05c4-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a05c4-113">El byte de orden inferior contiene el último dígito recibido en una representación de texto.</span><span class="sxs-lookup"><span data-stu-id="a05c4-113">The low-order byte contains the last digit received in a text representation.</span></span>

</dd> <dt>

<span data-ttu-id="a05c4-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a05c4-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a05c4-115">Modo de dígito que se ha detectado.</span><span class="sxs-lookup"><span data-stu-id="a05c4-115">The digit mode that was detected.</span></span> <span data-ttu-id="a05c4-116">Este parámetro debe ser una y solo una de las [**\_ constantes LINEDIGITMODE**](linedigitmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="a05c4-116">This parameter must be one and only one of the [**LINEDIGITMODE\_ constants**](linedigitmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a05c4-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a05c4-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a05c4-118">"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se detectó el dígito especificado.</span><span class="sxs-lookup"><span data-stu-id="a05c4-118">The "tick count" (number of milliseconds since Windows started) at which the specified digit was detected.</span></span> <span data-ttu-id="a05c4-119">En el caso de las versiones de TAPI anteriores a 2,0, este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a05c4-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a05c4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a05c4-120">Return value</span></span>

<span data-ttu-id="a05c4-121">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a05c4-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a05c4-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a05c4-122">Remarks</span></span>

<span data-ttu-id="a05c4-123">El mensaje **line \_ MONITORDIGITS** se envía a la aplicación que ha habilitado la supervisión de dígitos.</span><span class="sxs-lookup"><span data-stu-id="a05c4-123">The **LINE\_MONITORDIGITS** message is sent to the application that has enabled digit monitoring.</span></span>

<span data-ttu-id="a05c4-124">Dado que esta marca de tiempo se puede haber generado en un equipo que no sea el en el que se ejecuta la aplicación, solo resulta útil para compararla con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**\_ GATHERDIGITS de línea**](line-gatherdigits.md), [**\_ generación**](line-generate.md)de línea, [**línea \_ MONITORMEDIA**](line-monitormedia.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos).</span><span class="sxs-lookup"><span data-stu-id="a05c4-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="a05c4-125">El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="a05c4-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="a05c4-126">Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.</span><span class="sxs-lookup"><span data-stu-id="a05c4-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="a05c4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a05c4-127">Requirements</span></span>



| <span data-ttu-id="a05c4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a05c4-128">Requirement</span></span> | <span data-ttu-id="a05c4-129">Value</span><span class="sxs-lookup"><span data-stu-id="a05c4-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a05c4-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a05c4-130">TAPI version</span></span><br/> | <span data-ttu-id="a05c4-131">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a05c4-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a05c4-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a05c4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a05c4-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a05c4-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05c4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a05c4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05c4-135">**LÍNEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="a05c4-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="a05c4-136">**generación de línea \_**</span><span class="sxs-lookup"><span data-stu-id="a05c4-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="a05c4-137">**LÍNEA \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="a05c4-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="a05c4-138">**LÍNEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="a05c4-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="a05c4-139">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="a05c4-139">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




