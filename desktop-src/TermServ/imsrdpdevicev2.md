---
title: Interfaz IMsRdpDeviceV2
description: Contiene información sobre un objeto de dispositivo. Se trata de una mejora de la interfaz IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, descrito
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685852"
---
# <a name="imsrdpdevicev2-interface"></a><span data-ttu-id="6fb0a-106">Interfaz IMsRdpDeviceV2</span><span class="sxs-lookup"><span data-stu-id="6fb0a-106">IMsRdpDeviceV2 interface</span></span>

<span data-ttu-id="6fb0a-107">Contiene información sobre un objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-107">Contains information about a device object.</span></span> <span data-ttu-id="6fb0a-108">Se trata de una mejora de la interfaz [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="6fb0a-108">This is an enhancement of the [**IMsRdpDevice**](imsrdpdevice.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="6fb0a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6fb0a-109">Members</span></span>

<span data-ttu-id="6fb0a-110">La interfaz **IMsRdpDeviceV2** hereda de [**IMsRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6fb0a-110">The **IMsRdpDeviceV2** interface inherits from [**IMsRdpDevice**](imsrdpdevice.md).</span></span> <span data-ttu-id="6fb0a-111">**IMsRdpDeviceV2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6fb0a-111">**IMsRdpDeviceV2** also has these types of members:</span></span>

-   [<span data-ttu-id="6fb0a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fb0a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fb0a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fb0a-113">Properties</span></span>

<span data-ttu-id="6fb0a-114">La interfaz **IMsRdpDeviceV2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-114">The **IMsRdpDeviceV2** interface has these properties.</span></span>



| <span data-ttu-id="6fb0a-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6fb0a-115">Property</span></span>                                                                 | <span data-ttu-id="6fb0a-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6fb0a-116">Access type</span></span>          | <span data-ttu-id="6fb0a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fb0a-117">Description</span></span>                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fb0a-118">**CmClassGuid**</span><span class="sxs-lookup"><span data-stu-id="6fb0a-118">**CmClassGuid**</span></span>](imsrdpdevicev2-cmclassguid.md)<br/>             | <span data-ttu-id="6fb0a-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6fb0a-119">Read-only</span></span><br/> | <span data-ttu-id="6fb0a-120">Contiene el GUID de la clase de instalación de Configuration Manager para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-120">Contains the configuration manager setup class GUID for the device.</span></span><br/>                     |
| [<span data-ttu-id="6fb0a-121">**CmDeviceInstance**</span><span class="sxs-lookup"><span data-stu-id="6fb0a-121">**CmDeviceInstance**</span></span>](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | <span data-ttu-id="6fb0a-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6fb0a-122">Read-only</span></span><br/> | <span data-ttu-id="6fb0a-123">Contiene la instancia de dispositivo de Configuration Manager del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-123">Contains the configuration manager device instance of the device.</span></span><br/>                       |
| [<span data-ttu-id="6fb0a-124">**DeviceText**</span><span class="sxs-lookup"><span data-stu-id="6fb0a-124">**DeviceText**</span></span>](imsrdpdevicev2-devicetext.md)<br/>               | <span data-ttu-id="6fb0a-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6fb0a-125">Read-only</span></span><br/> | <span data-ttu-id="6fb0a-126">Contiene el texto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-126">Contains the device text.</span></span><br/>                                                               |
| [<span data-ttu-id="6fb0a-127">**DriveLetterBitmap**</span><span class="sxs-lookup"><span data-stu-id="6fb0a-127">**DriveLetterBitmap**</span></span>](imsrdpdevicev2-driveletterbitmap.md)<br/> | <span data-ttu-id="6fb0a-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6fb0a-128">Read-only</span></span><br/> | <span data-ttu-id="6fb0a-129">Contiene un campo de bits que representa una asignación de Letras de unidad incluidas en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-129">Contains a bitfield that represents a map of drive letters contained within the device.</span></span><br/> |
| [<span data-ttu-id="6fb0a-130">**IsCompositeDevice**</span><span class="sxs-lookup"><span data-stu-id="6fb0a-130">**IsCompositeDevice**</span></span>](imsrdpdevicev2-iscompositedevice.md)<br/> | <span data-ttu-id="6fb0a-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6fb0a-131">Read-only</span></span><br/> | <span data-ttu-id="6fb0a-132">Especifica si el dispositivo es un dispositivo compuesto.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-132">Specifies if the device is a composite device.</span></span><br/>                                          |
| [<span data-ttu-id="6fb0a-133">**IsOptionalDevice**</span><span class="sxs-lookup"><span data-stu-id="6fb0a-133">**IsOptionalDevice**</span></span>](imsrdpdevicev2-isoptionaldevice.md)<br/>   | <span data-ttu-id="6fb0a-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6fb0a-134">Read-only</span></span><br/> | <span data-ttu-id="6fb0a-135">Especifica si el dispositivo es opcional para el redireccionamiento USB.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-135">Specifies if the device is optional for USB redirection.</span></span><br/>                                |
| [<span data-ttu-id="6fb0a-136">**IsUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="6fb0a-136">**IsUSBDevice**</span></span>](imsrdpdevicev2-isusbdevice.md)<br/>             | <span data-ttu-id="6fb0a-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6fb0a-137">Read-only</span></span><br/> | <span data-ttu-id="6fb0a-138">Especifica si el dispositivo es para el redireccionamiento USB.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-138">Specifies if the device is for USB redirection.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="6fb0a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fb0a-139">Requirements</span></span>



| <span data-ttu-id="6fb0a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb0a-140">Requirement</span></span> | <span data-ttu-id="6fb0a-141">Value</span><span class="sxs-lookup"><span data-stu-id="6fb0a-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb0a-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fb0a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb0a-143">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="6fb0a-143">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="6fb0a-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fb0a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb0a-145">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="6fb0a-145">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="6fb0a-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6fb0a-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="6fb0a-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb0a-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fb0a-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6fb0a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fb0a-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb0a-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fb0a-150">IID</span><span class="sxs-lookup"><span data-stu-id="6fb0a-150">IID</span></span><br/>                      | <span data-ttu-id="6fb0a-151">IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="6fb0a-151">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



 

 





