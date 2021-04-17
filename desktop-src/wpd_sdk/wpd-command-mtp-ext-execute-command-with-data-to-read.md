---
description: El comando de WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ leer envía un bloque de comandos MTP, que va seguido de una fase de datos. (Los datos se envían desde el dispositivo al host).
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709035"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a><span data-ttu-id="32d23-104">Comando \_ de WPD comando \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ leer</span><span class="sxs-lookup"><span data-stu-id="32d23-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ Command</span></span>

<span data-ttu-id="32d23-105">El comando de **WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ leer** envía un bloque de comandos MTP, que va seguido de una fase de datos.</span><span class="sxs-lookup"><span data-stu-id="32d23-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command sends an MTP command block, which will be followed by a data phase.</span></span> <span data-ttu-id="32d23-106">(Los datos se envían desde el dispositivo al host).</span><span class="sxs-lookup"><span data-stu-id="32d23-106">(The data is sent from the device to the host.)</span></span>

## <a name="command-category"></a><span data-ttu-id="32d23-107">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="32d23-107">Command category</span></span>

<span data-ttu-id="32d23-108">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32d23-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="32d23-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32d23-109">Parameters</span></span>

<span data-ttu-id="32d23-110">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="32d23-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="32d23-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="32d23-111">Parameter</span></span>                                      | <span data-ttu-id="32d23-112">VarType</span><span class="sxs-lookup"><span data-stu-id="32d23-112">VarType</span></span> | <span data-ttu-id="32d23-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="32d23-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d23-114">**\_código de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="32d23-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="32d23-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="32d23-115">VT\_UI4</span></span> | <span data-ttu-id="32d23-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="32d23-116">Required.</span></span> <span data-ttu-id="32d23-117">Identifica un código de operación MTP extendido por un proveedor.</span><span class="sxs-lookup"><span data-stu-id="32d23-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="32d23-118">**\_parámetros de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="32d23-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="32d23-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="32d23-119">VT\_UI4</span></span> | <span data-ttu-id="32d23-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="32d23-120">Required.</span></span> <span data-ttu-id="32d23-121">Un **IPortableDevicePropVariantCollection**, que identifica los parámetros necesarios para el código de operación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="32d23-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="32d23-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32d23-122">Return Value</span></span>

<span data-ttu-id="32d23-123">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="32d23-123">The driver returns the following results.</span></span>



| <span data-ttu-id="32d23-124">Resultado</span><span class="sxs-lookup"><span data-stu-id="32d23-124">Result</span></span>                                                       | <span data-ttu-id="32d23-125">VarType</span><span class="sxs-lookup"><span data-stu-id="32d23-125">VarType</span></span>    | <span data-ttu-id="32d23-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="32d23-126">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d23-127">**propiedad de WPD \_ \_ extensión de \_ \_ \_ datos totales de transferencia ext \_ MTP \_**</span><span class="sxs-lookup"><span data-stu-id="32d23-127">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span>     | <span data-ttu-id="32d23-128">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="32d23-128">VT\_UI8</span></span>    | <span data-ttu-id="32d23-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="32d23-129">Required.</span></span> <span data-ttu-id="32d23-130">Devuelve el tamaño total de los datos, en bytes, excluyendo cualquier sobrecarga procedente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32d23-130">Returns the total data size, in bytes, excluding any overhead coming from the device.</span></span> <span data-ttu-id="32d23-131">Si el dispositivo informa de un tamaño de campo desconocido (0xFFFFFFFF), el controlador debe llamar a **ReadData** repetidamente hasta que se reciba un fragmento breve.</span><span class="sxs-lookup"><span data-stu-id="32d23-131">If the device reports unknown datasize (0xFFFFFFFF), the driver should call **ReadData** repeatedly until a short chunk is received</span></span> |
| <span data-ttu-id="32d23-132">**propiedad de WPD \_ \_ tamaño de \_ \_ \_ búfer de transferencia óptimo \_ ext de \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="32d23-132">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="32d23-133">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="32d23-133">VT\_UI4</span></span>    | <span data-ttu-id="32d23-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32d23-134">Optional.</span></span> <span data-ttu-id="32d23-135">Devuelve el tamaño óptimo del búfer de transferencia.</span><span class="sxs-lookup"><span data-stu-id="32d23-135">Returns the optimal size of the transfer buffer.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="32d23-136">**propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32d23-136">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="32d23-137">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="32d23-137">VT\_LPWSTR</span></span> | <span data-ttu-id="32d23-138">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="32d23-138">Required.</span></span> <span data-ttu-id="32d23-139">Especifica el identificador de contexto para las transferencias de datos posteriores.</span><span class="sxs-lookup"><span data-stu-id="32d23-139">Specifies the context identifier for subsequent data transfers.</span></span>                                                                                                                                                           |



 

## <a name="calling-methods"></a><span data-ttu-id="32d23-140">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="32d23-140">Calling Methods</span></span>

<span data-ttu-id="32d23-141">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="32d23-141">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="32d23-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32d23-142">Requirements</span></span>



| <span data-ttu-id="32d23-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="32d23-143">Requirement</span></span> | <span data-ttu-id="32d23-144">Value</span><span class="sxs-lookup"><span data-stu-id="32d23-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d23-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32d23-145">Header</span></span><br/> | <dl> <span data-ttu-id="32d23-146"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="32d23-146"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32d23-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="32d23-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d23-148">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="32d23-148">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




