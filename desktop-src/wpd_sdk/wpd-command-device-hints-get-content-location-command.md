---
description: El comando de las sugerencias de dispositivo de comando de WPD \_ \_ \_ \_ obtener \_ Ubicación de contenido \_ recupera los identificadores de objeto de carpetas que pueden contener un objeto de un tipo especificado.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: Comando WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708241"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a><span data-ttu-id="a155a-103">Comando de la ubicación de dispositivo de comandos de WPD \_ \_ \_ \_ \_ comando obtener ubicación de contenido \_</span><span class="sxs-lookup"><span data-stu-id="a155a-103">WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION Command</span></span>

<span data-ttu-id="a155a-104">El comando de las **sugerencias de dispositivo de comando de WPD \_ \_ \_ \_ obtener \_ \_ Ubicación de contenido** recupera los identificadores de objeto de carpetas que pueden contener un objeto de un tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="a155a-104">The **WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION** command retrieves the object IDs of folders that can hold an object of a specified type.</span></span> <span data-ttu-id="a155a-105">Este comando se proporciona como una manera más rápida para que un cliente detecte dónde un dispositivo almacena objetos específicos que la enumeración de objetos de fuerza bruta.</span><span class="sxs-lookup"><span data-stu-id="a155a-105">This command is provided as a faster way for a client to discover where a device stores specific objects than by brute object enumeration.</span></span>

## <a name="command-category"></a><span data-ttu-id="a155a-106">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="a155a-106">Command category</span></span>

<span data-ttu-id="a155a-107">**\_categorías de \_ dispositivos de categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a155a-107">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>

## <a name="parameters"></a><span data-ttu-id="a155a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a155a-108">Parameters</span></span>

<span data-ttu-id="a155a-109">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="a155a-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="a155a-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a155a-110">Parameter</span></span>                                   | <span data-ttu-id="a155a-111">VarType</span><span class="sxs-lookup"><span data-stu-id="a155a-111">VarType</span></span>   | <span data-ttu-id="a155a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a155a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a155a-113">propiedad de WPD \_ tipo de contenido de \_ sugerencias de dispositivo \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a155a-113">WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_TYPE</span></span> | <span data-ttu-id="a155a-114">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="a155a-114">VT\_CLSID</span></span> | <span data-ttu-id="a155a-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a155a-115">Required.</span></span> <span data-ttu-id="a155a-116">Tipo de objeto para el que el llamador desea buscar el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a155a-116">The object type that the caller wishes to find the container for.</span></span> <span data-ttu-id="a155a-117">Por ejemplo, para buscar las carpetas de nivel superior usadas para contener imágenes en una cámara digital, el autor de la llamada enviará la imagen de tipo de contenido de WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a155a-117">For example, to find the top-level folders used to hold images on a digital camera, the caller would submit WPD\_CONTENT\_TYPE\_IMAGE.</span></span> <span data-ttu-id="a155a-118">Vea [requisitos para objetos](requirements-for-objects.md) para obtener una lista de tipos de objetos definidos por dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="a155a-118">See [Requirements for Objects](requirements-for-objects.md) for a list of object types defined by Windows Portable Devices.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="a155a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a155a-119">Return Value</span></span>

<span data-ttu-id="a155a-120">El controlador debe devolver los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="a155a-120">The driver should return the following results.</span></span>



| <span data-ttu-id="a155a-121">Resultado</span><span class="sxs-lookup"><span data-stu-id="a155a-121">Result</span></span>                                               | <span data-ttu-id="a155a-122">VarType</span><span class="sxs-lookup"><span data-stu-id="a155a-122">VarType</span></span>     | <span data-ttu-id="a155a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a155a-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a155a-124">**propiedad de WPD \_ \_ sugerencias de dispositivo \_ \_ ubicaciones de contenido \_**</span><span class="sxs-lookup"><span data-stu-id="a155a-124">**WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_LOCATIONS**</span></span> | <span data-ttu-id="a155a-125">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="a155a-125">VT\_UNKNOWN</span></span> | <span data-ttu-id="a155a-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a155a-126">Required.</span></span> <span data-ttu-id="a155a-127">Un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo VT \_ LPWStr que especifica los identificadores de objeto de carpetas que contienen objetos del tipo indicado por el parámetro de llamada.</span><span class="sxs-lookup"><span data-stu-id="a155a-127">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) of type VT\_LPWSTR values that specify the object IDs of folders containing objects of the type indicated by the calling parameter.</span></span> <span data-ttu-id="a155a-128">Si no se encuentra ninguna carpeta, debe ser una lista vacía. Las carpetas indicadas por el resultado pueden contener o no objetos de otros tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="a155a-128">If no folders are found, this should be an empty list.The folders indicated by the result may or may not contain objects of other content types.</span></span> <span data-ttu-id="a155a-129">Consulte la propiedad tipos de contenido de la [carpeta de WPD \_ \_ \_ \_ permitida](miscellaneous-properties.md) para obtener información sobre las restricciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="a155a-129">See the [WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED](miscellaneous-properties.md) property for information on folder restrictions.</span></span><br/> |
| <span data-ttu-id="a155a-130">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="a155a-130">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                   | <span data-ttu-id="a155a-131">ERROR de VT \_</span><span class="sxs-lookup"><span data-stu-id="a155a-131">VT\_ERROR</span></span>   | <span data-ttu-id="a155a-132">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a155a-132">Required.</span></span> <span data-ttu-id="a155a-133">**HRESULT** que indica si el control del comando se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="a155a-133">An **HRESULT** that indicates success or failure of handling the command.</span></span> <span data-ttu-id="a155a-134">Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="a155a-134">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="a155a-135">Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="a155a-135">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="a155a-136">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a155a-136">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>       | <span data-ttu-id="a155a-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="a155a-137">VT\_UI4</span></span>     | <span data-ttu-id="a155a-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a155a-138">Optional.</span></span> <span data-ttu-id="a155a-139">Un código de error específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="a155a-139">A driver-specific error code.</span></span> <span data-ttu-id="a155a-140">Normalmente, esto solo se usa para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.</span><span class="sxs-lookup"><span data-stu-id="a155a-140">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a><span data-ttu-id="a155a-141">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="a155a-141">Calling Methods</span></span>

<span data-ttu-id="a155a-142">Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="a155a-142">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="a155a-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a155a-143">Requirements</span></span>



| <span data-ttu-id="a155a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a155a-144">Requirement</span></span> | <span data-ttu-id="a155a-145">Value</span><span class="sxs-lookup"><span data-stu-id="a155a-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a155a-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a155a-146">Header</span></span><br/> | <dl> <span data-ttu-id="a155a-147"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a155a-147"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




