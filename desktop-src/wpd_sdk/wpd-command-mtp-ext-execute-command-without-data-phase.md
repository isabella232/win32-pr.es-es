---
description: El comando de WPD comando \_ \_ \_ ext \_ Execute comando \_ sin la fase de \_ \_ datos \_ envía un bloque de comandos MTP. No hay ninguna fase de datos subsiguiente asociada a este comando.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709031"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a><span data-ttu-id="ed7ed-104">Comando de WPD comando \_ \_ \_ ext \_ Execute \_ comando \_ sin \_ fase de datos \_</span><span class="sxs-lookup"><span data-stu-id="ed7ed-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE Command</span></span>

<span data-ttu-id="ed7ed-105">El comando de **WPD comando \_ \_ \_ ext \_ Execute comando \_ sin la \_ \_ \_ fase de datos** envía un bloque de comandos MTP.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE** command sends an MTP command block.</span></span> <span data-ttu-id="ed7ed-106">No hay ninguna fase de datos subsiguiente asociada a este comando.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="ed7ed-107">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="ed7ed-107">Command category</span></span>

<span data-ttu-id="ed7ed-108">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed7ed-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="ed7ed-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed7ed-109">Parameters</span></span>

<span data-ttu-id="ed7ed-110">El controlador espera los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="ed7ed-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ed7ed-111">Parameter</span></span>                                      | <span data-ttu-id="ed7ed-112">VarType</span><span class="sxs-lookup"><span data-stu-id="ed7ed-112">VarType</span></span> | <span data-ttu-id="ed7ed-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed7ed-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7ed-114">**\_código de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="ed7ed-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="ed7ed-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed7ed-115">VT\_UI4</span></span> | <span data-ttu-id="ed7ed-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-116">Required.</span></span> <span data-ttu-id="ed7ed-117">Identifica un código de operación MTP extendido por un proveedor.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="ed7ed-118">**\_parámetros de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="ed7ed-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="ed7ed-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed7ed-119">VT\_UI4</span></span> | <span data-ttu-id="ed7ed-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-120">Required.</span></span> <span data-ttu-id="ed7ed-121">Un **IPortableDevicePropVariantCollection**, que identifica los parámetros necesarios para el código de operación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="ed7ed-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed7ed-122">Return Value</span></span>

<span data-ttu-id="ed7ed-123">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-123">The driver returns the following results.</span></span>



| <span data-ttu-id="ed7ed-124">Resultado</span><span class="sxs-lookup"><span data-stu-id="ed7ed-124">Result</span></span>                                        | <span data-ttu-id="ed7ed-125">VarType</span><span class="sxs-lookup"><span data-stu-id="ed7ed-125">VarType</span></span> | <span data-ttu-id="ed7ed-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed7ed-126">Description</span></span>                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7ed-127">**\_código de \_ \_ respuesta ext \_ de MTP de propiedad de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="ed7ed-127">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="ed7ed-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed7ed-128">VT\_UI4</span></span> | <span data-ttu-id="ed7ed-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-129">Required.</span></span> <span data-ttu-id="ed7ed-130">Código de respuesta al código de operación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-130">The response code to the vendor operation code.</span></span>                                                                      |
| <span data-ttu-id="ed7ed-131">**propiedad de WPD \_ \_ \_ parámetros de respuesta ext de MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed7ed-131">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="ed7ed-132">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ed7ed-132">VT\_UI4</span></span> | <span data-ttu-id="ed7ed-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-133">Optional.</span></span> <span data-ttu-id="ed7ed-134">**IPortableDevicePropVariantCollection** que identifica los parámetros de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-134">An **IPortableDevicePropVariantCollection** that identifies any response parameters.</span></span> <span data-ttu-id="ed7ed-135">Esta colección puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="ed7ed-135">This collection might be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="ed7ed-136">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="ed7ed-136">Calling Methods</span></span>

<span data-ttu-id="ed7ed-137">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="ed7ed-137">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed7ed-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed7ed-138">Requirements</span></span>



| <span data-ttu-id="ed7ed-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed7ed-139">Requirement</span></span> | <span data-ttu-id="ed7ed-140">Value</span><span class="sxs-lookup"><span data-stu-id="ed7ed-140">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7ed-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed7ed-141">Header</span></span><br/> | <dl> <span data-ttu-id="ed7ed-142"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ed-142"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed7ed-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed7ed-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed7ed-144">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="ed7ed-144">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




