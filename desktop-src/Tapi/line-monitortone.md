---
description: El mensaje de línea de \_ MONITORTONE TAPI se envía cuando se detecta un tono. El envío de este mensaje se controla con la función lineMonitorTones.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Mensaje de LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681052"
---
# <a name="line_monitortone-message"></a><span data-ttu-id="646ca-104">Mensaje de línea \_ MONITORTONE</span><span class="sxs-lookup"><span data-stu-id="646ca-104">LINE\_MONITORTONE message</span></span>

<span data-ttu-id="646ca-105">El mensaje de **línea de \_ MONITORTONE** TAPI se envía cuando se detecta un tono.</span><span class="sxs-lookup"><span data-stu-id="646ca-105">The TAPI **LINE\_MONITORTONE** message is sent when a tone is detected.</span></span> <span data-ttu-id="646ca-106">El envío de este mensaje se controla con la función [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .</span><span class="sxs-lookup"><span data-stu-id="646ca-106">The sending of this message is controlled with the [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="646ca-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="646ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646ca-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="646ca-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="646ca-109">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="646ca-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="646ca-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="646ca-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="646ca-111">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="646ca-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="646ca-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="646ca-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="646ca-113">Miembro de **dwAppSpecific** específico de la aplicación de la estructura [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) para el tono detectado.</span><span class="sxs-lookup"><span data-stu-id="646ca-113">The application-specific **dwAppSpecific** member of the [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) structure for the tone that was detected.</span></span>

</dd> <dt>

<span data-ttu-id="646ca-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="646ca-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="646ca-115">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="646ca-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="646ca-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="646ca-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="646ca-117">"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se detectó el tono.</span><span class="sxs-lookup"><span data-stu-id="646ca-117">The "tick count" (number of milliseconds since Windows started) at which the tone was detected.</span></span> <span data-ttu-id="646ca-118">En el caso de las versiones de API anteriores a 2,0, este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="646ca-118">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="646ca-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="646ca-119">Return value</span></span>

<span data-ttu-id="646ca-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="646ca-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="646ca-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="646ca-121">Remarks</span></span>

<span data-ttu-id="646ca-122">El mensaje **line \_ MONITORTONE** solo se envía a la aplicación que ha solicitado que se supervise el tono.</span><span class="sxs-lookup"><span data-stu-id="646ca-122">The **LINE\_MONITORTONE** message is only sent to the application that has requested the tone be monitored.</span></span>

<span data-ttu-id="646ca-123">Dado que esta marca de tiempo se puede haber generado en un equipo que no sea el en el que se ejecuta la aplicación, solo resulta útil para compararla con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**\_ GATHERDIGITS de línea**](line-gatherdigits.md), [**\_ generación**](line-generate.md)de línea, [**línea \_ MONITORDIGITS**](line-monitordigits.md), **línea \_ MONITORTONE**), con el fin de determinar su tiempo relativo (separación entre eventos).</span><span class="sxs-lookup"><span data-stu-id="646ca-123">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), **LINE\_MONITORTONE**), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="646ca-124">El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="646ca-124">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="646ca-125">Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.</span><span class="sxs-lookup"><span data-stu-id="646ca-125">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="646ca-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="646ca-126">Requirements</span></span>



| <span data-ttu-id="646ca-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="646ca-127">Requirement</span></span> | <span data-ttu-id="646ca-128">Value</span><span class="sxs-lookup"><span data-stu-id="646ca-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="646ca-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="646ca-129">TAPI version</span></span><br/> | <span data-ttu-id="646ca-130">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="646ca-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="646ca-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="646ca-131">Header</span></span><br/>       | <dl> <span data-ttu-id="646ca-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="646ca-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646ca-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="646ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646ca-134">**LÍNEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="646ca-134">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="646ca-135">**generación de línea \_**</span><span class="sxs-lookup"><span data-stu-id="646ca-135">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="646ca-136">**LÍNEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="646ca-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="646ca-137">**LINEMONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="646ca-137">**LINEMONITORTONE**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[<span data-ttu-id="646ca-138">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="646ca-138">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




