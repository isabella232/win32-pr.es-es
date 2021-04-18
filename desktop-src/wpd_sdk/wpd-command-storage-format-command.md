---
description: El comando de formato de almacenamiento de comandos de WPD \_ \_ \_ da formato a un objeto funcional de almacenamiento en el dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: Comando WPD_COMMAND_STORAGE_FORMAT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649968"
---
# <a name="wpd_command_storage_format-command"></a><span data-ttu-id="b5ba0-103">\_Comando de \_ formato de almacenamiento de comandos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="b5ba0-103">WPD\_COMMAND\_STORAGE\_FORMAT Command</span></span>

<span data-ttu-id="b5ba0-104">El comando de formato de almacenamiento de comandos de WPD da formato a un objeto funcional de almacenamiento en el dispositivo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5ba0-104">The **WPD\_COMMAND\_STORAGE\_FORMAT** command formats a storage functional object on the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="b5ba0-105">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="b5ba0-105">Command category</span></span>

<span data-ttu-id="b5ba0-106">**\_almacenamiento de categorías de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b5ba0-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="b5ba0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ba0-107">Parameters</span></span>

<span data-ttu-id="b5ba0-108">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="b5ba0-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b5ba0-109">Parameter</span></span>                          | <span data-ttu-id="b5ba0-110">VarType</span><span class="sxs-lookup"><span data-stu-id="b5ba0-110">VarType</span></span>    | <span data-ttu-id="b5ba0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5ba0-111">Description</span></span>                                              |
|------------------------------------|------------|----------------------------------------------------------|
| <span data-ttu-id="b5ba0-112">\_identificador de \_ objeto de almacenamiento de propiedades de WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="b5ba0-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="b5ba0-113">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="b5ba0-113">VT\_LPWSTR</span></span> | <span data-ttu-id="b5ba0-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-114">Required.</span></span> <span data-ttu-id="b5ba0-115">IDENTIFICADOR de objeto del medio de almacenamiento al que se va a dar formato.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-115">The object ID of the storage medium to format.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="b5ba0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5ba0-116">Return Value</span></span>

<span data-ttu-id="b5ba0-117">El controlador debe devolver los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-117">The driver should return the following results.</span></span>



| <span data-ttu-id="b5ba0-118">Resultado</span><span class="sxs-lookup"><span data-stu-id="b5ba0-118">Result</span></span>                                         | <span data-ttu-id="b5ba0-119">VarType</span><span class="sxs-lookup"><span data-stu-id="b5ba0-119">VarType</span></span>   | <span data-ttu-id="b5ba0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5ba0-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ba0-121">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="b5ba0-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="b5ba0-122">ERROR de VT \_</span><span class="sxs-lookup"><span data-stu-id="b5ba0-122">VT\_ERROR</span></span> | <span data-ttu-id="b5ba0-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-123">Required.</span></span> <span data-ttu-id="b5ba0-124">**HRESULT** que indica si se ha realizado correctamente o no el comando.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="b5ba0-125">Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="b5ba0-126">Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="b5ba0-127">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="b5ba0-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="b5ba0-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="b5ba0-128">VT\_UI4</span></span>   | <span data-ttu-id="b5ba0-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-129">Optional.</span></span> <span data-ttu-id="b5ba0-130">Un código de error específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-130">A driver-specific error code.</span></span> <span data-ttu-id="b5ba0-131">Normalmente, esto solo se usa para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.</span><span class="sxs-lookup"><span data-stu-id="b5ba0-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="b5ba0-132">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="b5ba0-132">Calling Methods</span></span>

<span data-ttu-id="b5ba0-133">Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="b5ba0-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ba0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5ba0-134">Requirements</span></span>



| <span data-ttu-id="b5ba0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ba0-135">Requirement</span></span> | <span data-ttu-id="b5ba0-136">Value</span><span class="sxs-lookup"><span data-stu-id="b5ba0-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ba0-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5ba0-137">Header</span></span><br/> | <dl> <span data-ttu-id="b5ba0-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ba0-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ba0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5ba0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ba0-140">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="b5ba0-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




