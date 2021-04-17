---
description: El comando \_ WPD \_ \_ ext \_ Read data del comando de WPD \_ recupera los datos del dispositivo después de ejecutar el comando de la extensión de comandos de ejecución ext del comando WPD \_ \_ \_ \_ \_ \_ con \_ datos \_ para \_ leer.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: Comando WPD_COMMAND_MTP_EXT_READ_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709027"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a><span data-ttu-id="7d9f4-103">Comando de WPD comando \_ \_ \_ ext \_ Read \_ Data</span><span class="sxs-lookup"><span data-stu-id="7d9f4-103">WPD\_COMMAND\_MTP\_EXT\_READ\_DATA Command</span></span>

<span data-ttu-id="7d9f4-104">El **comando \_ WPD \_ \_ ext \_ Read \_ Data del comando de WPD** recupera los datos del dispositivo después de ejecutar el comando de la extensión de comandos de ejecución ext del comando **WPD \_ \_ \_ \_ \_ \_ con \_ datos \_ para \_ leer** .</span><span class="sxs-lookup"><span data-stu-id="7d9f4-104">The **WPD\_COMMAND\_MTP\_EXT\_READ\_DATA** command retrieves data from the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="7d9f4-105">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="7d9f4-105">Command category</span></span>

<span data-ttu-id="7d9f4-106">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="7d9f4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d9f4-107">Parameters</span></span>

<span data-ttu-id="7d9f4-108">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="7d9f4-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7d9f4-109">Parameter</span></span>                                                   | <span data-ttu-id="7d9f4-110">VarType</span><span class="sxs-lookup"><span data-stu-id="7d9f4-110">VarType</span></span>             | <span data-ttu-id="7d9f4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d9f4-111">Description</span></span>                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9f4-112">**propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>              | <span data-ttu-id="7d9f4-113">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="7d9f4-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="7d9f4-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-114">Required.</span></span> <span data-ttu-id="7d9f4-115">Identifica el contexto devuelto por la llamada anterior al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="7d9f4-116">**\_propiedad \_ de WPD \_ \_ transferencia de ext. \_ número \_ de bytes \_ para \_ leer**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_READ**</span></span> | <span data-ttu-id="7d9f4-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="7d9f4-117">VT\_UI4</span></span>             | <span data-ttu-id="7d9f4-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-118">Required.</span></span> <span data-ttu-id="7d9f4-119">Especifica el número de bytes que se van a leer.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-119">Specifies the number of bytes to read.</span></span>                                       |
| <span data-ttu-id="7d9f4-120">**propiedad de WPD \_ \_ \_ datos de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                 | <span data-ttu-id="7d9f4-121">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="7d9f4-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="7d9f4-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-122">Required.</span></span> <span data-ttu-id="7d9f4-123">Identifica el búfer en el que se copian los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="7d9f4-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d9f4-124">Return Value</span></span>

<span data-ttu-id="7d9f4-125">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-125">The driver returns the following results.</span></span>



| <span data-ttu-id="7d9f4-126">Resultado</span><span class="sxs-lookup"><span data-stu-id="7d9f4-126">Result</span></span>                                                  | <span data-ttu-id="7d9f4-127">VarType</span><span class="sxs-lookup"><span data-stu-id="7d9f4-127">VarType</span></span>             | <span data-ttu-id="7d9f4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d9f4-128">Description</span></span>                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7d9f4-129">**propiedad de WPD \_ \_ transferencia de ext. número de \_ \_ \_ \_ bytes \_ leídos**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_READ**</span></span> | <span data-ttu-id="7d9f4-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="7d9f4-130">VT\_UI4</span></span>             | <span data-ttu-id="7d9f4-131">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-131">Required.</span></span> <span data-ttu-id="7d9f4-132">Especifica el número de bytes recibidos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-132">Specifies the number of bytes received from the device.</span></span> |
| <span data-ttu-id="7d9f4-133">**propiedad de WPD \_ \_ \_ datos de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-133">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>             | <span data-ttu-id="7d9f4-134">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="7d9f4-134">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="7d9f4-135">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-135">Required.</span></span> <span data-ttu-id="7d9f4-136">Búfer que contiene los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d9f4-136">The buffer that contains the device data.</span></span>               |



 

## <a name="calling-methods"></a><span data-ttu-id="7d9f4-137">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="7d9f4-137">Calling Methods</span></span>

<span data-ttu-id="7d9f4-138">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="7d9f4-138">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d9f4-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d9f4-139">Requirements</span></span>



| <span data-ttu-id="7d9f4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d9f4-140">Requirement</span></span> | <span data-ttu-id="7d9f4-141">Value</span><span class="sxs-lookup"><span data-stu-id="7d9f4-141">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9f4-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d9f4-142">Header</span></span><br/> | <dl> <span data-ttu-id="7d9f4-143"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d9f4-143"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d9f4-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d9f4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9f4-145">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="7d9f4-145">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




