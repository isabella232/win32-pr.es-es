---
description: El comando de uso \_ \_ común de \_ restablecimiento de dispositivo del comando de WPD \_ restablece el dispositivo. Esto no significa volver a formatear; es equivalente a desactivar y volver a activar el dispositivo.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: Comando WPD_COMMAND_COMMON_RESET_DEVICE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709252"
---
# <a name="wpd_command_common_reset_device-command"></a><span data-ttu-id="8c4d7-104">Comando \_ del \_ \_ dispositivo de restablecimiento común de comandos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="8c4d7-104">WPD\_COMMAND\_COMMON\_RESET\_DEVICE Command</span></span>

<span data-ttu-id="8c4d7-105">El comando de uso **\_ común de restablecimiento de \_ \_ \_ dispositivo** del comando de WPD restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-105">The **WPD\_COMMAND\_COMMON\_RESET\_DEVICE** command resets the device.</span></span> <span data-ttu-id="8c4d7-106">Esto no significa volver a formatear; es equivalente a desactivar y volver a activar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-106">This does not mean reformatting; it is equivalent to turning the device off and on again.</span></span>

## <a name="command-category"></a><span data-ttu-id="8c4d7-107">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="8c4d7-107">Command category</span></span>

<span data-ttu-id="8c4d7-108">**\_categoría \_ común de WPD**</span><span class="sxs-lookup"><span data-stu-id="8c4d7-108">**WPD\_CATEGORY\_COMMON**</span></span>

## <a name="parameters"></a><span data-ttu-id="8c4d7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c4d7-109">Parameters</span></span>

<span data-ttu-id="8c4d7-110">Este comando no contiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c4d7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c4d7-111">Return Value</span></span>

<span data-ttu-id="8c4d7-112">El controlador debe devolver los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-112">The driver should return the following results.</span></span>



| <span data-ttu-id="8c4d7-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="8c4d7-113">Result</span></span>                                         | <span data-ttu-id="8c4d7-114">VarType</span><span class="sxs-lookup"><span data-stu-id="8c4d7-114">VarType</span></span>   | <span data-ttu-id="8c4d7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c4d7-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4d7-116">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="8c4d7-116">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="8c4d7-117">ERROR de VT \_</span><span class="sxs-lookup"><span data-stu-id="8c4d7-117">VT\_ERROR</span></span> | <span data-ttu-id="8c4d7-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-118">Required.</span></span> <span data-ttu-id="8c4d7-119">**HRESULT** que indica si se ha realizado correctamente o no el comando.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-119">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="8c4d7-120">Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-120">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="8c4d7-121">Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-121">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="8c4d7-122">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="8c4d7-122">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="8c4d7-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="8c4d7-123">VT\_UI4</span></span>   | <span data-ttu-id="8c4d7-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-124">Optional.</span></span> <span data-ttu-id="8c4d7-125">Un código de error específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-125">A driver-specific error code.</span></span> <span data-ttu-id="8c4d7-126">Normalmente, esto solo se usa para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.</span><span class="sxs-lookup"><span data-stu-id="8c4d7-126">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="8c4d7-127">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="8c4d7-127">Calling Methods</span></span>

<span data-ttu-id="8c4d7-128">Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="8c4d7-128">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4d7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c4d7-129">Requirements</span></span>



| <span data-ttu-id="8c4d7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c4d7-130">Requirement</span></span> | <span data-ttu-id="8c4d7-131">Value</span><span class="sxs-lookup"><span data-stu-id="8c4d7-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4d7-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c4d7-132">Header</span></span><br/> | <dl> <span data-ttu-id="8c4d7-133"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c4d7-133"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c4d7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c4d7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4d7-135">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="8c4d7-135">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




