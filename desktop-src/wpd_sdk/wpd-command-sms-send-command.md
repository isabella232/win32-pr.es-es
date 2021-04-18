---
description: El comando \_ WPD \_ SMS \_ send Command inicia el envío de un mensaje de servicio de mensajes cortos (SMS) por un objeto funcional de SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: Comando WPD_COMMAND_SMS_SEND (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718695"
---
# <a name="wpd_command_sms_send-command"></a><span data-ttu-id="64b46-103">Comando \_ WPD \_ SMS comando \_ send</span><span class="sxs-lookup"><span data-stu-id="64b46-103">WPD\_COMMAND\_SMS\_SEND Command</span></span>

<span data-ttu-id="64b46-104">El **comando \_ WPD \_ SMS \_ send** Command inicia el envío de un mensaje de servicio de mensajes cortos (SMS) por un objeto funcional de SMS.</span><span class="sxs-lookup"><span data-stu-id="64b46-104">The **WPD\_COMMAND\_SMS\_SEND** command initiates the sending of a short message service (SMS) message by an SMS functional object.</span></span>

## <a name="command-category"></a><span data-ttu-id="64b46-105">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="64b46-105">Command category</span></span>

<span data-ttu-id="64b46-106">**\_SMS categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="64b46-106">**WPD\_CATEGORY\_SMS**</span></span>

## <a name="parameters"></a><span data-ttu-id="64b46-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64b46-107">Parameters</span></span>

<span data-ttu-id="64b46-108">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="64b46-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="64b46-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="64b46-109">Parameter</span></span>                              | <span data-ttu-id="64b46-110">VarType</span><span class="sxs-lookup"><span data-stu-id="64b46-110">VarType</span></span>             | <span data-ttu-id="64b46-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="64b46-111">Description</span></span>                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b46-112">\_destino del \_ \_ comando común \_ de la propiedad WPD</span><span class="sxs-lookup"><span data-stu-id="64b46-112">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="64b46-113">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="64b46-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="64b46-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64b46-114">Required.</span></span> <span data-ttu-id="64b46-115">IDENTIFICADOR de objeto del objeto funcional de SMS que debe enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64b46-115">The object ID of the SMS functional object that should send the message.</span></span> <span data-ttu-id="64b46-116">Distintos objetos funcionales de SMS pueden tener distintas configuraciones.</span><span class="sxs-lookup"><span data-stu-id="64b46-116">Different SMS functional objects can have different settings.</span></span>                                                                                     |
| <span data-ttu-id="64b46-117">propiedad de WPD \_ \_ destinatario de SMS \_</span><span class="sxs-lookup"><span data-stu-id="64b46-117">WPD\_PROPERTY\_SMS\_RECIPIENT</span></span>          | <span data-ttu-id="64b46-118">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="64b46-118">VT\_LPWSTR</span></span>          | <span data-ttu-id="64b46-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64b46-119">Required.</span></span> <span data-ttu-id="64b46-120">URI del destinatario.</span><span class="sxs-lookup"><span data-stu-id="64b46-120">The URI of the recipient.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="64b46-121">\_tipo de \_ mensaje de SMS de propiedad de WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="64b46-121">WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE</span></span>      | <span data-ttu-id="64b46-122">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="64b46-122">VT\_UI4</span></span>             | <span data-ttu-id="64b46-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64b46-123">Required.</span></span> <span data-ttu-id="64b46-124">Un enumerador de [**\_ \_ tipos de mensajes SMS**](sms-message-types.md) que indica el tipo de mensaje (texto o binario).</span><span class="sxs-lookup"><span data-stu-id="64b46-124">An [**SMS\_MESSAGE\_TYPES**](sms-message-types.md) enumerator that indicates the type of message (text or binary).</span></span>                                                                                                        |
| <span data-ttu-id="64b46-125">\_mensaje de \_ \_ texto SMS de propiedad \_ de WPD</span><span class="sxs-lookup"><span data-stu-id="64b46-125">WPD\_PROPERTY\_SMS\_TEXT\_MESSAGE</span></span>      | <span data-ttu-id="64b46-126">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="64b46-126">VT\_LPWSTR</span></span>          | <span data-ttu-id="64b46-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="64b46-127">Optional.</span></span> <span data-ttu-id="64b46-128">Si **la \_ propiedad de WPD \_ \_ \_ tipo de mensaje de SMS** indica un mensaje de texto, esta es la cadena de mensaje; de lo contrario, este parámetro no se incluye.</span><span class="sxs-lookup"><span data-stu-id="64b46-128">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a text message, this is the message string; otherwise, this parameter is not included.</span></span>                                                                                  |
| <span data-ttu-id="64b46-129">\_ \_ \_ mensaje binario de SMS de propiedad de WPD \_</span><span class="sxs-lookup"><span data-stu-id="64b46-129">WPD\_PROPERTY\_SMS\_BINARY\_MESSAGE</span></span>    | <span data-ttu-id="64b46-130">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="64b46-130">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="64b46-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="64b46-131">Optional.</span></span> <span data-ttu-id="64b46-132">Si **la \_ propiedad de WPD \_ \_ \_ tipo de mensaje de SMS** indica un mensaje binario, se trata de un puntero a una matriz de bytes; de lo contrario, este parámetro no se incluye.</span><span class="sxs-lookup"><span data-stu-id="64b46-132">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a binary message, this is a pointer to an array of bytes; otherwise, this parameter is not included.</span></span> <span data-ttu-id="64b46-133">La primera DWORD del valor es la longitud de la matriz, en bytes.</span><span class="sxs-lookup"><span data-stu-id="64b46-133">The first DWORD of the value is the length of the array, in bytes.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="64b46-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64b46-134">Return Value</span></span>

<span data-ttu-id="64b46-135">El controlador debe devolver los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="64b46-135">The driver should return the following results.</span></span>



| <span data-ttu-id="64b46-136">Resultado</span><span class="sxs-lookup"><span data-stu-id="64b46-136">Result</span></span>                                         | <span data-ttu-id="64b46-137">VarType</span><span class="sxs-lookup"><span data-stu-id="64b46-137">VarType</span></span>   | <span data-ttu-id="64b46-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="64b46-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b46-139">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="64b46-139">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="64b46-140">ERROR de VT \_</span><span class="sxs-lookup"><span data-stu-id="64b46-140">VT\_ERROR</span></span> | <span data-ttu-id="64b46-141">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64b46-141">Required.</span></span> <span data-ttu-id="64b46-142">**HRESULT** que indica si se ha realizado correctamente o no el comando.</span><span class="sxs-lookup"><span data-stu-id="64b46-142">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="64b46-143">Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="64b46-143">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="64b46-144">Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="64b46-144">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="64b46-145">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="64b46-145">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="64b46-146">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="64b46-146">VT\_UI4</span></span>   | <span data-ttu-id="64b46-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="64b46-147">Optional.</span></span> <span data-ttu-id="64b46-148">Un código de error específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="64b46-148">A driver-specific error code.</span></span> <span data-ttu-id="64b46-149">Normalmente, esto solo se usa para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.</span><span class="sxs-lookup"><span data-stu-id="64b46-149">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="64b46-150">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="64b46-150">Calling Methods</span></span>

<span data-ttu-id="64b46-151">Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="64b46-151">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="64b46-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64b46-152">Requirements</span></span>



| <span data-ttu-id="64b46-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b46-153">Requirement</span></span> | <span data-ttu-id="64b46-154">Value</span><span class="sxs-lookup"><span data-stu-id="64b46-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b46-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64b46-155">Header</span></span><br/> | <dl> <span data-ttu-id="64b46-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b46-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b46-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="64b46-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b46-158">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="64b46-158">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




