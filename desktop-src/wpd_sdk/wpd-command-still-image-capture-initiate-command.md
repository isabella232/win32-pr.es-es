---
description: Los comandos de \_ Inicio de captura de imagen del comando WPD \_ \_ \_ \_ inician una captura de imagen continua mediante un objeto funcional de imagen fija. Si se crea un nuevo objeto como resultado de tomar una imagen, el controlador debe enviar el evento de \_ objeto de evento WPD \_ \_ agregado.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: Comando WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691066"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a><span data-ttu-id="79e22-104">Comando de la \_ \_ captura de \_ imagen del \_ comando de WPD \_</span><span class="sxs-lookup"><span data-stu-id="79e22-104">WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE Command</span></span>

<span data-ttu-id="79e22-105">Los comandos de **\_ Inicio de \_ \_ \_ captura \_ de imagen del comando WPD** inician una captura de imagen continua mediante un objeto funcional de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="79e22-105">The **WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE** command initiates a still image capture by a still image functional object.</span></span> <span data-ttu-id="79e22-106">Si se crea un nuevo objeto como resultado de tomar una imagen, el controlador debe enviar el evento **de \_ objeto de evento WPD \_ \_ agregado** .</span><span class="sxs-lookup"><span data-stu-id="79e22-106">If a new object is created as a result of taking a picture, the driver should send the **WPD\_EVENT\_OBJECT\_ADDED** event.</span></span>

## <a name="command-category"></a><span data-ttu-id="79e22-107">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="79e22-107">Command category</span></span>

<span data-ttu-id="79e22-108">**\_captura de \_ \_ imagen \_ de la categoría de WPD**</span><span class="sxs-lookup"><span data-stu-id="79e22-108">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span>

## <a name="parameters"></a><span data-ttu-id="79e22-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79e22-109">Parameters</span></span>

<span data-ttu-id="79e22-110">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="79e22-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="79e22-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="79e22-111">Parameter</span></span>                              | <span data-ttu-id="79e22-112">VarType</span><span class="sxs-lookup"><span data-stu-id="79e22-112">VarType</span></span>    | <span data-ttu-id="79e22-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="79e22-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e22-114">\_destino del \_ \_ comando común \_ de la propiedad WPD</span><span class="sxs-lookup"><span data-stu-id="79e22-114">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="79e22-115">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="79e22-115">VT\_LPWSTR</span></span> | <span data-ttu-id="79e22-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79e22-116">Required.</span></span> <span data-ttu-id="79e22-117">El ID. de objeto del objeto funcional de captura de imagen fija en el dispositivo que debe tomar la imagen. Cada objeto funcional de captura de imágenes fijas puede tener una configuración diferente y puede hacer referencia a un hardware diferente en un dispositivo (por ejemplo, una cámara frontal o posterior de un teléfono) y este parámetro indica cuál usar.</span><span class="sxs-lookup"><span data-stu-id="79e22-117">The object ID of the still image capture functional object on the device that should take the picture.Each still image capture functional object can have different settings, and may refer to different hardware on a device (for example, a front or back camera of a phone), and this parameter indicates which one to use.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="79e22-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79e22-118">Return Value</span></span>

<span data-ttu-id="79e22-119">El controlador debe devolver los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="79e22-119">The driver should return the following results.</span></span>



| <span data-ttu-id="79e22-120">Resultado</span><span class="sxs-lookup"><span data-stu-id="79e22-120">Result</span></span>                                         | <span data-ttu-id="79e22-121">VarType</span><span class="sxs-lookup"><span data-stu-id="79e22-121">VarType</span></span>   | <span data-ttu-id="79e22-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="79e22-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e22-123">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="79e22-123">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="79e22-124">ERROR de VT \_</span><span class="sxs-lookup"><span data-stu-id="79e22-124">VT\_ERROR</span></span> | <span data-ttu-id="79e22-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79e22-125">Required.</span></span> <span data-ttu-id="79e22-126">**HRESULT** que indica si se ha realizado correctamente o no el comando.</span><span class="sxs-lookup"><span data-stu-id="79e22-126">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="79e22-127">Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="79e22-127">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="79e22-128">Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="79e22-128">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="79e22-129">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="79e22-129">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="79e22-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="79e22-130">VT\_UI4</span></span>   | <span data-ttu-id="79e22-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="79e22-131">Optional.</span></span> <span data-ttu-id="79e22-132">Un código de error específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="79e22-132">A driver-specific error code.</span></span> <span data-ttu-id="79e22-133">Normalmente, los proveedores de dispositivos usan este valor para mejorar el diagnóstico de errores del dispositivo al usar sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="79e22-133">This value is typically used by device vendors to improve diagnosis of device errors while using their applications.</span></span> <span data-ttu-id="79e22-134">Las aplicaciones de uso general lo pasarían por alto y solo se basarían en HRESULT de la propiedad de WPD en \_ \_ \_ su lugar.</span><span class="sxs-lookup"><span data-stu-id="79e22-134">General purpose applications would ignore it and rely solely on WPD\_PROPERTY\_COMMON\_HRESULT instead.</span></span>                                                                                                                   |



 

## <a name="calling-methods"></a><span data-ttu-id="79e22-135">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="79e22-135">Calling Methods</span></span>

<span data-ttu-id="79e22-136">Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="79e22-136">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="79e22-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79e22-137">Requirements</span></span>



| <span data-ttu-id="79e22-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e22-138">Requirement</span></span> | <span data-ttu-id="79e22-139">Value</span><span class="sxs-lookup"><span data-stu-id="79e22-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e22-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79e22-140">Header</span></span><br/> | <dl> <span data-ttu-id="79e22-141"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e22-141"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e22-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="79e22-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e22-143">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="79e22-143">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




