---
description: El mensaje de LINE_MONITORMEDIA TAPI se envía cuando se detecta un cambio en el tipo de medio de llamadas. El envío de este mensaje se controla con la función lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Mensaje de LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690364"
---
# <a name="line_monitormedia-message"></a><span data-ttu-id="8ec3f-104">Mensaje de línea \_ MONITORMEDIA</span><span class="sxs-lookup"><span data-stu-id="8ec3f-104">LINE\_MONITORMEDIA message</span></span>

<span data-ttu-id="8ec3f-105">El mensaje de **línea de \_ MONITORMEDIA** TAPI se envía cuando se detecta un cambio en el tipo de medio de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-105">The TAPI **LINE\_MONITORMEDIA** message is sent when a change in the call's media type is detected.</span></span> <span data-ttu-id="8ec3f-106">El envío de este mensaje se controla con la función [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .</span><span class="sxs-lookup"><span data-stu-id="8ec3f-106">The sending of this message is controlled with the [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8ec3f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ec3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec3f-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="8ec3f-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3f-109">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="8ec3f-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="8ec3f-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3f-111">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="8ec3f-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8ec3f-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3f-113">Nuevo tipo de medio (o modo).</span><span class="sxs-lookup"><span data-stu-id="8ec3f-113">The new media type (or mode).</span></span> <span data-ttu-id="8ec3f-114">Este parámetro debe ser una y solo una de las [**\_ constantes LINEMEDIAMODE**](linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8ec3f-114">This parameter must be one and only one of the [**LINEMEDIAMODE\_ constants**](linemediamode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ec3f-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8ec3f-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3f-116">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8ec3f-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8ec3f-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3f-118">"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se detectó el medio especificado.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-118">The "tick count" (number of milliseconds since Windows started) at which the specified media was detected.</span></span> <span data-ttu-id="8ec3f-119">En el caso de las versiones de TAPI anteriores a 2,0, este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec3f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec3f-120">Return value</span></span>

<span data-ttu-id="8ec3f-121">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ec3f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ec3f-122">Remarks</span></span>

<span data-ttu-id="8ec3f-123">El mensaje **line \_ MONITORMEDIA** se envía a la aplicación que ha habilitado la supervisión multimedia para el tipo de medio detectado.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-123">The **LINE\_MONITORMEDIA** message is sent to the application that has enabled media monitoring for the media type detected.</span></span>

<span data-ttu-id="8ec3f-124">Dado que esta marca de tiempo se puede haber generado en un equipo que no sea el en el que se ejecuta la aplicación, solo resulta útil para compararla con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**\_ GATHERDIGITS de línea**](line-gatherdigits.md), [**\_ generación**](line-generate.md)de línea, [**línea \_ MONITORDIGITS**](line-monitordigits.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su tiempo relativo (separación entre eventos).</span><span class="sxs-lookup"><span data-stu-id="8ec3f-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="8ec3f-125">El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="8ec3f-126">Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.</span><span class="sxs-lookup"><span data-stu-id="8ec3f-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec3f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ec3f-127">Requirements</span></span>



| <span data-ttu-id="8ec3f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec3f-128">Requirement</span></span> | <span data-ttu-id="8ec3f-129">Value</span><span class="sxs-lookup"><span data-stu-id="8ec3f-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8ec3f-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8ec3f-130">TAPI version</span></span><br/> | <span data-ttu-id="8ec3f-131">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8ec3f-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8ec3f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ec3f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8ec3f-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec3f-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec3f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ec3f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec3f-135">**LÍNEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="8ec3f-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="8ec3f-136">**generación de línea \_**</span><span class="sxs-lookup"><span data-stu-id="8ec3f-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="8ec3f-137">**LÍNEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="8ec3f-137">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="8ec3f-138">**LÍNEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="8ec3f-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




