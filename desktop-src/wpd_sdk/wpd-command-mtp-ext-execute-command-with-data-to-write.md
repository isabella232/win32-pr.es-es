---
description: El comando WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir envía un bloque de comandos MTP, que va seguido de una fase de datos. Los datos se envían desde el host al dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709034"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a><span data-ttu-id="6b8a0-104">Comando de WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir</span><span class="sxs-lookup"><span data-stu-id="6b8a0-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE Command</span></span>

<span data-ttu-id="6b8a0-105">El comando **WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir** envía un bloque de comandos MTP, que va seguido de una fase de datos.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command sends an MTP command block, which is followed by a data phase.</span></span> <span data-ttu-id="6b8a0-106">Los datos se envían desde el host al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-106">The data is sent from the host to the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="6b8a0-107">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="6b8a0-107">Command category</span></span>

<span data-ttu-id="6b8a0-108">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b8a0-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="6b8a0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b8a0-109">Parameters</span></span>

<span data-ttu-id="6b8a0-110">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="6b8a0-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6b8a0-111">Parameter</span></span>                                                | <span data-ttu-id="6b8a0-112">VarType</span><span class="sxs-lookup"><span data-stu-id="6b8a0-112">VarType</span></span> | <span data-ttu-id="6b8a0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b8a0-113">Description</span></span>                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8a0-114">**\_código de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="6b8a0-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>             | <span data-ttu-id="6b8a0-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6b8a0-115">VT\_UI4</span></span> | <span data-ttu-id="6b8a0-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-116">Required.</span></span> <span data-ttu-id="6b8a0-117">Identifica un código de operación MTP extendido por un proveedor.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                              |
| <span data-ttu-id="6b8a0-118">**\_parámetros de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="6b8a0-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span>           | <span data-ttu-id="6b8a0-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6b8a0-119">VT\_UI4</span></span> | <span data-ttu-id="6b8a0-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-120">Required.</span></span> <span data-ttu-id="6b8a0-121">Una colección **IPortableDevicePropVariantCollection** que identifica los parámetros necesarios para el código de operación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-121">An **IPortableDevicePropVariantCollection** collection that identifies the required parameters for the vendor operation code.</span></span> |
| <span data-ttu-id="6b8a0-122">**propiedad de WPD \_ \_ extensión de \_ \_ \_ datos totales de transferencia ext \_ MTP \_**</span><span class="sxs-lookup"><span data-stu-id="6b8a0-122">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span> | <span data-ttu-id="6b8a0-123">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="6b8a0-123">VT\_UI8</span></span> | <span data-ttu-id="6b8a0-124">Requerido. especifica el tamaño total de los datos, en bytes, excluyendo cualquier sobrecarga que se envíe al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-124">Required.Specifies the total data size, in bytes, excluding any overhead, to be sent to device.</span></span>                                         |



 

## <a name="return-value"></a><span data-ttu-id="6b8a0-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b8a0-125">Return Value</span></span>

<span data-ttu-id="6b8a0-126">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-126">The driver returns the following results.</span></span>



| <span data-ttu-id="6b8a0-127">Resultado</span><span class="sxs-lookup"><span data-stu-id="6b8a0-127">Result</span></span>                                                       | <span data-ttu-id="6b8a0-128">VarType</span><span class="sxs-lookup"><span data-stu-id="6b8a0-128">VarType</span></span>    | <span data-ttu-id="6b8a0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b8a0-129">Description</span></span>                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8a0-130">**propiedad de WPD \_ \_ tamaño de \_ \_ \_ búfer de transferencia óptimo \_ ext de \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="6b8a0-130">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="6b8a0-131">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6b8a0-131">VT\_UI4</span></span>    | <span data-ttu-id="6b8a0-132">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-132">Required.</span></span> <span data-ttu-id="6b8a0-133">Especifica el tamaño óptimo del búfer de transferencia.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-133">Specifies the optimal size of the transfer buffer.</span></span>                       |
| <span data-ttu-id="6b8a0-134">**propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b8a0-134">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="6b8a0-135">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="6b8a0-135">VT\_LPWSTR</span></span> | <span data-ttu-id="6b8a0-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-136">Optional.</span></span> <span data-ttu-id="6b8a0-137">Identificador de contexto que utiliza el controlador para las transferencias de datos posteriores.</span><span class="sxs-lookup"><span data-stu-id="6b8a0-137">A context identifier that the driver uses for subsequent data transfers.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="6b8a0-138">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="6b8a0-138">Calling Methods</span></span>

<span data-ttu-id="6b8a0-139">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="6b8a0-139">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8a0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b8a0-140">Requirements</span></span>



| <span data-ttu-id="6b8a0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8a0-141">Requirement</span></span> | <span data-ttu-id="6b8a0-142">Value</span><span class="sxs-lookup"><span data-stu-id="6b8a0-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8a0-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b8a0-143">Header</span></span><br/> | <dl> <span data-ttu-id="6b8a0-144"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8a0-144"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8a0-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b8a0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8a0-146">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="6b8a0-146">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




