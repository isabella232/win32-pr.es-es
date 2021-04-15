---
description: El comando \_ WPD \_ \_ ext \_ End Data Transfer del comando WPD \_ \_ completa una transferencia de datos y lee la respuesta del dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: Comando WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709106"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a><span data-ttu-id="1608c-103">Comando de WPD comando \_ \_ \_ ext \_ End \_ Data \_ Transfer</span><span class="sxs-lookup"><span data-stu-id="1608c-103">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER Command</span></span>

<span data-ttu-id="1608c-104">El **comando \_ WPD \_ \_ ext \_ End \_ Data \_ transfer del comando WPD** completa una transferencia de datos y lee la respuesta del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1608c-104">The **WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER** command completes a data transfer and read response from the device.</span></span> <span data-ttu-id="1608c-105">La transferencia se inicia con el comando [**WPD \_ ext Execute del comando de WPD \_ con los \_ \_ \_ \_ \_ datos \_ para \_ leer**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) , el comando o el comando de [**\_ \_ ext Execute MTP del comando de WPD \_ \_ \_ \_ con \_ datos \_ para \_ escribir**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) el comando.</span><span class="sxs-lookup"><span data-stu-id="1608c-105">The transfer is initiated by either the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) command or the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) command.</span></span>

## <a name="command-category"></a><span data-ttu-id="1608c-106">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="1608c-106">Command category</span></span>

<span data-ttu-id="1608c-107">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1608c-107">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="1608c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1608c-108">Parameters</span></span>

<span data-ttu-id="1608c-109">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="1608c-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="1608c-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1608c-110">Parameter</span></span>                                      | <span data-ttu-id="1608c-111">VarType</span><span class="sxs-lookup"><span data-stu-id="1608c-111">VarType</span></span>    | <span data-ttu-id="1608c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1608c-112">Description</span></span>                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1608c-113">**propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1608c-113">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span> | <span data-ttu-id="1608c-114">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="1608c-114">VT\_LPWSTR</span></span> | <span data-ttu-id="1608c-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1608c-115">Required.</span></span> <span data-ttu-id="1608c-116">Identifica el contexto devuelto por una llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="1608c-116">Identifies the context that is returned by an earlier method call.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="1608c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1608c-117">Return Value</span></span>

<span data-ttu-id="1608c-118">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="1608c-118">The driver returns the following results.</span></span>



| <span data-ttu-id="1608c-119">Resultado</span><span class="sxs-lookup"><span data-stu-id="1608c-119">Result</span></span>                                        | <span data-ttu-id="1608c-120">VarType</span><span class="sxs-lookup"><span data-stu-id="1608c-120">VarType</span></span> | <span data-ttu-id="1608c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1608c-121">Description</span></span>                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1608c-122">**\_código de \_ \_ respuesta ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1608c-122">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="1608c-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="1608c-123">VT\_UI4</span></span> | <span data-ttu-id="1608c-124">Requerido. el código de respuesta para el código de operación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1608c-124">Required.The response code to the vendor operation code.</span></span>                                                                                |
| <span data-ttu-id="1608c-125">**propiedad de WPD \_ \_ \_ parámetros de respuesta ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1608c-125">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="1608c-126">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="1608c-126">VT\_UI4</span></span> | <span data-ttu-id="1608c-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1608c-127">Optional.</span></span> <span data-ttu-id="1608c-128">Colección **IPortableDevicePropVariantCollection** que identifica los parámetros de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1608c-128">An **IPortableDevicePropVariantCollection** collection that identifies any response parameters.</span></span> <span data-ttu-id="1608c-129">Esta colección puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="1608c-129">This collection can be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="1608c-130">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="1608c-130">Calling Methods</span></span>

<span data-ttu-id="1608c-131">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="1608c-131">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="1608c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1608c-132">Requirements</span></span>



| <span data-ttu-id="1608c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1608c-133">Requirement</span></span> | <span data-ttu-id="1608c-134">Value</span><span class="sxs-lookup"><span data-stu-id="1608c-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1608c-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1608c-135">Header</span></span><br/> | <dl> <span data-ttu-id="1608c-136"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="1608c-136"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1608c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1608c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1608c-138">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="1608c-138">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

