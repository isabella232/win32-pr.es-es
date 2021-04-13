---
title: Interfaz IBasicDevice
description: Encapsula los métodos y eventos necesarios para modelar un dispositivo DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- Interfaz IBasicDevice API de streaming de multimedia
- Interfaz IBasicDevice API de streaming de multimedia, descrita
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421604"
---
# <a name="ibasicdevice-interface"></a><span data-ttu-id="b4895-105">Interfaz IBasicDevice</span><span class="sxs-lookup"><span data-stu-id="b4895-105">IBasicDevice interface</span></span>

<span data-ttu-id="b4895-106">Encapsula los métodos y eventos necesarios para modelar un dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="b4895-106">Encapsulates the methods and events needed to model a DLNA Device.</span></span>

## <a name="members"></a><span data-ttu-id="b4895-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4895-107">Members</span></span>

<span data-ttu-id="b4895-108">La interfaz **IBasicDevice** hereda de [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="b4895-108">The **IBasicDevice** interface inherits from [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="b4895-109">**IBasicDevice** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b4895-109">**IBasicDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="b4895-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4895-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b4895-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4895-111">Methods</span></span>

<span data-ttu-id="b4895-112">La interfaz **IBasicDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b4895-112">The **IBasicDevice** interface has these methods.</span></span>



| <span data-ttu-id="b4895-113">Método</span><span class="sxs-lookup"><span data-stu-id="b4895-113">Method</span></span>                                                                                 | <span data-ttu-id="b4895-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4895-114">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4895-115">**agregar \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="b4895-115">**add\_ConnectionStatusChanged**</span></span>](ibasicdevice-add-connectionstatuschanged.md)       | <span data-ttu-id="b4895-116">Registra un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="b4895-116">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>                |
| [<span data-ttu-id="b4895-117">**CanWakeDevices**</span><span class="sxs-lookup"><span data-stu-id="b4895-117">**CanWakeDevices**</span></span>](ibasicdevice-canwakedevices.md)                                  | <span data-ttu-id="b4895-118">Recupera un valor que indica si el dispositivo se puede reactivar.</span><span class="sxs-lookup"><span data-stu-id="b4895-118">Retrieves a value that indicates if the device can wake.</span></span><br/>                                                            |
| <span data-ttu-id="b4895-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b4895-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span></span>                              | <span data-ttu-id="b4895-120">Devuelve un valor de enumeración que indica si el dispositivo está actualmente en línea, fuera de línea o inactivo, pero Reactivable.</span><span class="sxs-lookup"><span data-stu-id="b4895-120">Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.</span></span><br/> |
| [<span data-ttu-id="b4895-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4895-121">**Description**</span></span>](ibasicdevice-description.md)                                        | <span data-ttu-id="b4895-122">Recupera una descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-122">Retrieves a description of the device.</span></span><br/>                                                                              |
| [<span data-ttu-id="b4895-123">**DiscoveredOnCurrentNetwork**</span><span class="sxs-lookup"><span data-stu-id="b4895-123">**DiscoveredOnCurrentNetwork**</span></span>](ibasicdevice-discoveredoncurrentnetwork.md)          | <span data-ttu-id="b4895-124">Recupera un valor que indica si el dispositivo está en la red actual.</span><span class="sxs-lookup"><span data-stu-id="b4895-124">Retrieves a value that indicates if the device is on the current network.</span></span><br/>                                           |
| [<span data-ttu-id="b4895-125">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="b4895-125">**FriendlyName**</span></span>](ibasicdevice-friendlyname.md)                                      | <span data-ttu-id="b4895-126">Recupera el nombre descriptivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-126">Retrieves the device s friendly name.</span></span><br/>                                                                               |
| [<span data-ttu-id="b4895-127">**Iconos**</span><span class="sxs-lookup"><span data-stu-id="b4895-127">**Icons**</span></span>](ibasicdevice-icons.md)                                                    | <span data-ttu-id="b4895-128">Devuelve un vector de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="b4895-128">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span><br/>                                                  |
| [<span data-ttu-id="b4895-129">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="b4895-129">**IpAddresses**</span></span>](ibasicdevice-ipaddresses.md)                                        | <span data-ttu-id="b4895-130">Devuelve un vector de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="b4895-130">Returns a vector of IP addresses.</span></span><br/>                                                                                   |
| [<span data-ttu-id="b4895-131">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="b4895-131">**ManufacturerName**</span></span>](ibasicdevice-manufacturername.md)                              | <span data-ttu-id="b4895-132">Recupera el nombre del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-132">Retrieves the device s manufacturer name.</span></span><br/>                                                                           |
| [<span data-ttu-id="b4895-133">**ManufacturerUrl**</span><span class="sxs-lookup"><span data-stu-id="b4895-133">**ManufacturerUrl**</span></span>](ibasicdevice-manufacturerurl.md)                                | <span data-ttu-id="b4895-134">Recupera la dirección URL del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-134">Retrieves the device s manufacturer URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="b4895-135">**ModelName**</span><span class="sxs-lookup"><span data-stu-id="b4895-135">**ModelName**</span></span>](ibasicdevice-modelname.md)                                            | <span data-ttu-id="b4895-136">Recupera el nombre del modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-136">Retrieves the device s model name.</span></span><br/>                                                                                  |
| [<span data-ttu-id="b4895-137">**ModelNumber**</span><span class="sxs-lookup"><span data-stu-id="b4895-137">**ModelNumber**</span></span>](ibasicdevice-modelnumber.md)                                        | <span data-ttu-id="b4895-138">Recupera el número de modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-138">Retrieves the device s model number.</span></span><br/>                                                                                |
| [<span data-ttu-id="b4895-139">**ModelUrl**</span><span class="sxs-lookup"><span data-stu-id="b4895-139">**ModelUrl**</span></span>](ibasicdevice-modelurl.md)                                              | <span data-ttu-id="b4895-140">Recupera la dirección URL del modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-140">Retrieves the device s model URL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="b4895-141">**PhysicalAddresses**</span><span class="sxs-lookup"><span data-stu-id="b4895-141">**PhysicalAddresses**</span></span>](ibasicdevice-physicaladdresses.md)                            | <span data-ttu-id="b4895-142">Devuelve un vector de direcciones físicas.</span><span class="sxs-lookup"><span data-stu-id="b4895-142">Returns a vector of physical addresses.</span></span><br/>                                                                             |
| [<span data-ttu-id="b4895-143">**PresentationUrl**</span><span class="sxs-lookup"><span data-stu-id="b4895-143">**PresentationUrl**</span></span>](ibasicdevice-presentationurl.md)                                | <span data-ttu-id="b4895-144">Recupera la dirección URL de presentación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-144">Retrieves the device s presentation URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="b4895-145">**RemoteStreamingUrls**</span><span class="sxs-lookup"><span data-stu-id="b4895-145">**RemoteStreamingUrls**</span></span>](ibasicdevice-remotestreamingurls.md)                        | <span data-ttu-id="b4895-146">Devuelve un vector de direcciones URL de streaming remoto.</span><span class="sxs-lookup"><span data-stu-id="b4895-146">Returns a vector of remote streaming URLs.</span></span><br/>                                                                          |
| [<span data-ttu-id="b4895-147">**quitar \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="b4895-147">**remove\_ConnectionStatusChanged**</span></span>](ibasicdevice-remove-connectionstatuschanged.md) | <span data-ttu-id="b4895-148">Anula el registro de un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="b4895-148">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>              |
| [<span data-ttu-id="b4895-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b4895-149">**SerialNumber**</span></span>](ibasicdevice-serialnumber.md)                                      | <span data-ttu-id="b4895-150">Recupera el número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4895-150">Retrieves the device s serial number.</span></span><br/>                                                                               |
| [<span data-ttu-id="b4895-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4895-151">**Type**</span></span>](ibasicdevice-type.md)                                                      | <span data-ttu-id="b4895-152">Recupera un valor de enumeración que indica el tipo de dispositivo del dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="b4895-152">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span><br/>                                       |
| [<span data-ttu-id="b4895-153">**UniqueDeviceName**</span><span class="sxs-lookup"><span data-stu-id="b4895-153">**UniqueDeviceName**</span></span>](ibasicdevice-uniquedevicename.md)                              | <span data-ttu-id="b4895-154">Recupera el nombre del dispositivo único (UDN).</span><span class="sxs-lookup"><span data-stu-id="b4895-154">Retrieves the device s unique device name (UDN).</span></span><br/>                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="b4895-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4895-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4895-156">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="b4895-156">**IInspectable**</span></span>](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

