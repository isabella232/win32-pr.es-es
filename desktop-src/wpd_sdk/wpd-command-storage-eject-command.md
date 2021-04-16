---
description: El \_ comando de expulsión de almacenamiento de comandos de WPD \_ \_ expulsa un medio de almacenamiento que el equipo puede retirar de forma remota.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: Comando WPD_COMMAND_STORAGE_EJECT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649969"
---
# <a name="wpd_command_storage_eject-command"></a><span data-ttu-id="1f93d-103">\_Comando de \_ retiro de almacenamiento de comandos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="1f93d-103">WPD\_COMMAND\_STORAGE\_EJECT Command</span></span>

<span data-ttu-id="1f93d-104">El comando de **\_ \_ \_ expulsión de almacenamiento de comandos de WPD** expulsa un medio de almacenamiento que el equipo puede retirar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="1f93d-104">The **WPD\_COMMAND\_STORAGE\_EJECT** command ejects a storage medium that can be ejected remotely by the computer.</span></span>

## <a name="command-category"></a><span data-ttu-id="1f93d-105">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="1f93d-105">Command category</span></span>

<span data-ttu-id="1f93d-106">**\_almacenamiento de categorías de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1f93d-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="1f93d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f93d-107">Parameters</span></span>

<span data-ttu-id="1f93d-108">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="1f93d-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="1f93d-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1f93d-109">Parameter</span></span>                          | <span data-ttu-id="1f93d-110">VarType</span><span class="sxs-lookup"><span data-stu-id="1f93d-110">VarType</span></span>    | <span data-ttu-id="1f93d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f93d-111">Description</span></span>                                             |
|------------------------------------|------------|---------------------------------------------------------|
| <span data-ttu-id="1f93d-112">\_identificador de \_ objeto de almacenamiento de propiedades de WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="1f93d-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="1f93d-113">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="1f93d-113">VT\_LPWSTR</span></span> | <span data-ttu-id="1f93d-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f93d-114">Required.</span></span> <span data-ttu-id="1f93d-115">IDENTIFICADOR de objeto del objeto de almacenamiento que se va a expulsar.</span><span class="sxs-lookup"><span data-stu-id="1f93d-115">The object ID of the storage object to eject.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="1f93d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f93d-116">Return Value</span></span>

<span data-ttu-id="1f93d-117">El controlador debe devolver los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="1f93d-117">The driver should return the following results.</span></span>



| <span data-ttu-id="1f93d-118">Resultado</span><span class="sxs-lookup"><span data-stu-id="1f93d-118">Result</span></span>                                         | <span data-ttu-id="1f93d-119">VarType</span><span class="sxs-lookup"><span data-stu-id="1f93d-119">VarType</span></span>   | <span data-ttu-id="1f93d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f93d-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f93d-121">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="1f93d-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="1f93d-122">ERROR de VT \_</span><span class="sxs-lookup"><span data-stu-id="1f93d-122">VT\_ERROR</span></span> | <span data-ttu-id="1f93d-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f93d-123">Required.</span></span> <span data-ttu-id="1f93d-124">**HRESULT** que indica si se ha realizado correctamente o no el comando.</span><span class="sxs-lookup"><span data-stu-id="1f93d-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="1f93d-125">Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="1f93d-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="1f93d-126">Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="1f93d-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="1f93d-127">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="1f93d-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="1f93d-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="1f93d-128">VT\_UI4</span></span>   | <span data-ttu-id="1f93d-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f93d-129">Optional.</span></span> <span data-ttu-id="1f93d-130">Un código de error específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="1f93d-130">A driver-specific error code.</span></span> <span data-ttu-id="1f93d-131">Normalmente, esto solo se usa para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.</span><span class="sxs-lookup"><span data-stu-id="1f93d-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="1f93d-132">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="1f93d-132">Calling Methods</span></span>

<span data-ttu-id="1f93d-133">Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="1f93d-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f93d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f93d-134">Requirements</span></span>



| <span data-ttu-id="1f93d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f93d-135">Requirement</span></span> | <span data-ttu-id="1f93d-136">Value</span><span class="sxs-lookup"><span data-stu-id="1f93d-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f93d-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f93d-137">Header</span></span><br/> | <dl> <span data-ttu-id="1f93d-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f93d-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f93d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f93d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f93d-140">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="1f93d-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




