---
description: El comando de la \_ extensión de datos de escritura MTP de comando de WPD \_ \_ \_ \_ envía datos al dispositivo después de ejecutar el comando WPD \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: Comando WPD_COMMAND_MTP_EXT_WRITE_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709026"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a><span data-ttu-id="f48b6-103">Comando de WPD comando \_ \_ \_ ext \_ Write \_ Data</span><span class="sxs-lookup"><span data-stu-id="f48b6-103">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA Command</span></span>

<span data-ttu-id="f48b6-104">El comando de la **\_ extensión de \_ \_ \_ \_ datos de escritura MTP de comando de WPD** envía datos al dispositivo después de ejecutar el comando **WPD \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir** .</span><span class="sxs-lookup"><span data-stu-id="f48b6-104">The **WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA** command sends data to the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="f48b6-105">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="f48b6-105">Command category</span></span>

<span data-ttu-id="f48b6-106">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f48b6-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="f48b6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f48b6-107">Parameters</span></span>

<span data-ttu-id="f48b6-108">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f48b6-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="f48b6-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f48b6-109">Parameter</span></span>                                                    | <span data-ttu-id="f48b6-110">VarType</span><span class="sxs-lookup"><span data-stu-id="f48b6-110">VarType</span></span>             | <span data-ttu-id="f48b6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f48b6-111">Description</span></span>                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f48b6-112">**propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f48b6-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="f48b6-113">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="f48b6-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="f48b6-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f48b6-114">Required.</span></span> <span data-ttu-id="f48b6-115">Identifica el contexto devuelto por la llamada anterior al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f48b6-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="f48b6-116">**\_propiedad \_ de WPD \_ \_ transferencia de ext. \_ número \_ de bytes \_ que se van a \_ escribir**</span><span class="sxs-lookup"><span data-stu-id="f48b6-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_WRITE**</span></span> | <span data-ttu-id="f48b6-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f48b6-117">VT\_UI4</span></span>             | <span data-ttu-id="f48b6-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f48b6-118">Required.</span></span> <span data-ttu-id="f48b6-119">Especifica el número de bytes que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="f48b6-119">Specifies the number of bytes to write.</span></span>                                      |
| <span data-ttu-id="f48b6-120">**propiedad de WPD \_ \_ \_ datos de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f48b6-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                  | <span data-ttu-id="f48b6-121">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="f48b6-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="f48b6-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f48b6-122">Required.</span></span> <span data-ttu-id="f48b6-123">Identifica el búfer en el que se copian los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f48b6-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="f48b6-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f48b6-124">Return Value</span></span>

<span data-ttu-id="f48b6-125">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="f48b6-125">The driver returns the following results.</span></span>



| <span data-ttu-id="f48b6-126">Resultado</span><span class="sxs-lookup"><span data-stu-id="f48b6-126">Result</span></span>                                                     | <span data-ttu-id="f48b6-127">VarType</span><span class="sxs-lookup"><span data-stu-id="f48b6-127">VarType</span></span> | <span data-ttu-id="f48b6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f48b6-128">Description</span></span>                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| <span data-ttu-id="f48b6-129">**propiedad de WPD \_ \_ transferencia de ext. número de \_ \_ \_ \_ bytes \_ escritos**</span><span class="sxs-lookup"><span data-stu-id="f48b6-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_WRITTEN**</span></span> | <span data-ttu-id="f48b6-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f48b6-130">VT\_UI4</span></span> | <span data-ttu-id="f48b6-131">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f48b6-131">Required.</span></span> <span data-ttu-id="f48b6-132">Especifica el número de bytes enviados al dispositivo..</span><span class="sxs-lookup"><span data-stu-id="f48b6-132">Specifies the number of bytes sent to the device..</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="f48b6-133">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="f48b6-133">Calling Methods</span></span>

<span data-ttu-id="f48b6-134">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="f48b6-134">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="f48b6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f48b6-135">Requirements</span></span>



| <span data-ttu-id="f48b6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f48b6-136">Requirement</span></span> | <span data-ttu-id="f48b6-137">Value</span><span class="sxs-lookup"><span data-stu-id="f48b6-137">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48b6-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f48b6-138">Header</span></span><br/> | <dl> <span data-ttu-id="f48b6-139"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="f48b6-139"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f48b6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f48b6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48b6-141">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="f48b6-141">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




