---
description: Recupera las propiedades admitidas por un objeto.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: Comando WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718895"
---
# <a name="wpd_command_object_properties_get_supported-command"></a><span data-ttu-id="804a5-103">\_Propiedades del objeto de comando WPD \_ \_ \_ obtener \_ comando compatible</span><span class="sxs-lookup"><span data-stu-id="804a5-103">WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED Command</span></span>

<span data-ttu-id="804a5-104">El comando de **\_ propiedades del objeto de comando WPD \_ \_ \_ Get \_ Supported** recupera las propiedades admitidas por un objeto.</span><span class="sxs-lookup"><span data-stu-id="804a5-104">The **WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED** command retrieves the properties supported by an object.</span></span>

## <a name="command-category"></a><span data-ttu-id="804a5-105">Categoría de comandos</span><span class="sxs-lookup"><span data-stu-id="804a5-105">Command Category</span></span>

<span data-ttu-id="804a5-106">**\_propiedades del \_ objeto de categoría de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="804a5-106">**WPD\_CATEGORY\_OBJECT\_PROPERTIES**</span></span>

## <a name="parameters"></a><span data-ttu-id="804a5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="804a5-107">Parameters</span></span>

<span data-ttu-id="804a5-108">El controlador espera el parámetro siguiente.</span><span class="sxs-lookup"><span data-stu-id="804a5-108">The driver expects the following parameter.</span></span>



| <span data-ttu-id="804a5-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="804a5-109">Parameter</span></span>                                         | <span data-ttu-id="804a5-110">VarType</span><span class="sxs-lookup"><span data-stu-id="804a5-110">VarType</span></span>        | <span data-ttu-id="804a5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="804a5-111">Description</span></span>                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="804a5-112">**\_identificador de \_ objeto de propiedades del objeto de propiedad WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="804a5-112">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_OBJECT\_ID**</span></span> | <span data-ttu-id="804a5-113">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="804a5-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="804a5-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="804a5-114">Required.</span></span> <span data-ttu-id="804a5-115">IDENTIFICADOR del objeto que contiene las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="804a5-115">The ID of the object that contains the requested properties.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="804a5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="804a5-116">Return Value</span></span>

<span data-ttu-id="804a5-117">El controlador debe devolver los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="804a5-117">The driver should return the following results.</span></span>



| <span data-ttu-id="804a5-118">Resultado</span><span class="sxs-lookup"><span data-stu-id="804a5-118">Result</span></span>                                                | <span data-ttu-id="804a5-119">VarType</span><span class="sxs-lookup"><span data-stu-id="804a5-119">VarType</span></span>         | <span data-ttu-id="804a5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="804a5-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804a5-121">**\_claves de \_ propiedad de propiedades del objeto de propiedad WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="804a5-121">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_PROPERTY\_KEYS**</span></span> | <span data-ttu-id="804a5-122">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="804a5-122">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="804a5-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="804a5-123">Required.</span></span> <span data-ttu-id="804a5-124">Una interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que especifica todas las propiedades admitidas.</span><span class="sxs-lookup"><span data-stu-id="804a5-124">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that specifies all of the supported properties.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="804a5-125">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="804a5-125">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                    | <span data-ttu-id="804a5-126">**ERROR de VT \_**</span><span class="sxs-lookup"><span data-stu-id="804a5-126">**VT\_ERROR**</span></span>   | <span data-ttu-id="804a5-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="804a5-127">Required.</span></span> <span data-ttu-id="804a5-128">Un valor **HRESULT** que indica éxito o error general.</span><span class="sxs-lookup"><span data-stu-id="804a5-128">An **HRESULT** value that indicates overall success or failure.</span></span> <span data-ttu-id="804a5-129">Los valores de resultado posibles incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="804a5-129">Possible result values include [Windows Portable Devices error codes](error-constants.md).</span></span> <span data-ttu-id="804a5-130">Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** pero, de lo contrario, no es necesario devolver ningún otro valor de resultado.</span><span class="sxs-lookup"><span data-stu-id="804a5-130">If the caller makes an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** but is otherwise not required to return any other result value.</span></span> |
| <span data-ttu-id="804a5-131">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="804a5-131">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>        | <span data-ttu-id="804a5-132">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="804a5-132">**VT\_UI4**</span></span>     | <span data-ttu-id="804a5-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="804a5-133">Optional.</span></span> <span data-ttu-id="804a5-134">Un código de error específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="804a5-134">A driver-specific error code.</span></span> <span data-ttu-id="804a5-135">Normalmente se usa solo para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.</span><span class="sxs-lookup"><span data-stu-id="804a5-135">This is typically used only for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="804a5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="804a5-136">Requirements</span></span>



| <span data-ttu-id="804a5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="804a5-137">Requirement</span></span> | <span data-ttu-id="804a5-138">Value</span><span class="sxs-lookup"><span data-stu-id="804a5-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="804a5-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="804a5-139">Header</span></span><br/> | <dl> <span data-ttu-id="804a5-140"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="804a5-140"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="804a5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="804a5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804a5-142">**Comandos**</span><span class="sxs-lookup"><span data-stu-id="804a5-142">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




