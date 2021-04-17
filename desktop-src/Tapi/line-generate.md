---
description: Se envía el mensaje de generación de línea TAPI \_ para notificar a la aplicación que ha finalizado la generación de dígitos o tono actual.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Mensaje de LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690699"
---
# <a name="line_generate-message"></a><span data-ttu-id="e38e5-103">Mensaje de generación de línea \_</span><span class="sxs-lookup"><span data-stu-id="e38e5-103">LINE\_GENERATE message</span></span>

<span data-ttu-id="e38e5-104">Se envía el mensaje de generación de **línea \_** TAPI para notificar a la aplicación que ha finalizado la generación de dígitos o tono actual.</span><span class="sxs-lookup"><span data-stu-id="e38e5-104">The TAPI **LINE\_GENERATE** message is sent to notify the application that the current digit or tone generation has terminated.</span></span> <span data-ttu-id="e38e5-105">Solo una solicitud de este tipo puede estar en curso en una llamada determinada en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="e38e5-105">Only one such generation request can be in progress an a given call at any time.</span></span> <span data-ttu-id="e38e5-106">Este mensaje también se envía cuando se cancela la generación de dígitos o de tono.</span><span class="sxs-lookup"><span data-stu-id="e38e5-106">This message is also sent when digit or tone generation is canceled.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e38e5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e38e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e38e5-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="e38e5-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e38e5-109">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e38e5-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="e38e5-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="e38e5-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e38e5-111">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="e38e5-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="e38e5-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e38e5-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e38e5-113">Razón por la que finalizó la generación de dígitos o tono.</span><span class="sxs-lookup"><span data-stu-id="e38e5-113">The reason why digit or tone generation was terminated.</span></span> <span data-ttu-id="e38e5-114">Este parámetro debe ser una y solo una de las [**\_ constantes LINEGENERATETERM**](linegenerateterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="e38e5-114">This parameter must be one and only one of the [**LINEGENERATETERM\_ constants**](linegenerateterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e38e5-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e38e5-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e38e5-116">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e38e5-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e38e5-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e38e5-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e38e5-118">"Recuento de pasos" (número de milisegundos transcurridos desde que se inició Windows) en el que se completó la generación de dígitos o tono.</span><span class="sxs-lookup"><span data-stu-id="e38e5-118">The "tick count" (number of milliseconds since Windows started) at which the digit or tone generation completed.</span></span> <span data-ttu-id="e38e5-119">En el caso de las versiones de API anteriores a 2,0, este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e38e5-119">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e38e5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e38e5-120">Return value</span></span>

<span data-ttu-id="e38e5-121">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e38e5-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e38e5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e38e5-122">Remarks</span></span>

<span data-ttu-id="e38e5-123">El mensaje de generación de **línea \_** solo se envía a la aplicación que solicitó la generación de dígitos o tono.</span><span class="sxs-lookup"><span data-stu-id="e38e5-123">The **LINE\_GENERATE** message is only sent to the application that requested the digit or tone generation.</span></span>

<span data-ttu-id="e38e5-124">Dado que la marca de tiempo especificada por *dwParam3* puede haberse generado en un equipo que no sea el en el que se ejecuta la aplicación, solo es útil para la comparación con otros mensajes de marca de tiempo similares generados en el mismo dispositivo de línea ( [**línea \_ GATHERDIGITS**](line-gatherdigits.md), [**línea \_ MONITORDIGITS**](line-monitordigits.md), [**línea \_ MONITORMEDIA**](line-monitormedia.md), [**línea \_ MONITORTONE**](line-monitortone.md)), con el fin de determinar su temporización relativa (separación entre eventos).</span><span class="sxs-lookup"><span data-stu-id="e38e5-124">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="e38e5-125">El recuento de pasos puede "ajustarse alrededor" después de aproximadamente 49,7 días; las aplicaciones deben tener esto en cuenta al realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="e38e5-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="e38e5-126">Si el proveedor de servicios no genera la marca de tiempo (por ejemplo, si se creó con una versión anterior de TAPI), TAPI proporciona una marca de tiempo en el punto más cercano al proveedor de servicios que genera el evento para que la marca de tiempo sintetizada sea lo más precisa posible.</span><span class="sxs-lookup"><span data-stu-id="e38e5-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e38e5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e38e5-127">Requirements</span></span>



| <span data-ttu-id="e38e5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e38e5-128">Requirement</span></span> | <span data-ttu-id="e38e5-129">Value</span><span class="sxs-lookup"><span data-stu-id="e38e5-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e38e5-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e38e5-130">TAPI version</span></span><br/> | <span data-ttu-id="e38e5-131">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e38e5-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e38e5-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e38e5-132">Header</span></span><br/>       | <dl> <span data-ttu-id="e38e5-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e38e5-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e38e5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e38e5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e38e5-135">**LÍNEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="e38e5-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="e38e5-136">**LÍNEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="e38e5-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="e38e5-137">**LÍNEA \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="e38e5-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="e38e5-138">**LÍNEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="e38e5-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




