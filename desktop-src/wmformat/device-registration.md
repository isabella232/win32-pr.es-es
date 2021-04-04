---
title: Registro de dispositivos
description: Registro de dispositivos
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- SDK de Windows Media Format, registro de dispositivos
- SDK de Windows Media Format, registro de dispositivos
- Advanced Systems Format (ASF), registro de dispositivos
- ASF (formato de sistemas avanzados), registro de dispositivos
- Advanced Systems Format (ASF), registro de dispositivos
- ASF (formato de sistemas avanzados), registro de dispositivos
- Administración de derechos digitales (DRM), registro de dispositivos
- DRM (administración de derechos digitales), registro de dispositivos
- Administración de derechos digitales (DRM), registro de dispositivos
- DRM (administración de derechos digitales), registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077314"
---
# <a name="device-registration"></a><span data-ttu-id="1b88c-113">Registro de dispositivos</span><span class="sxs-lookup"><span data-stu-id="1b88c-113">Device Registration</span></span>

<span data-ttu-id="1b88c-114">El SDK de Windows Media Format proporciona acceso a la base de datos de registro de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1b88c-114">The Windows Media Format SDK provides access to the device registration database.</span></span> <span data-ttu-id="1b88c-115">Esta base de datos está protegida en el equipo cliente y se usa para registrar los dispositivos que admiten Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="1b88c-115">This database is secured on the client computer and is used to register devices that support Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="1b88c-116">Cuando se agrega un dispositivo a una red a la que está conectado el equipo cliente, el dispositivo intenta ponerse en contacto con una aplicación de transmisor de Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="1b88c-116">When a device is added to a network to which the client computer is connected, the device attempts to contact a Windows Media DRM 10 for Network Devices transmitter application.</span></span> <span data-ttu-id="1b88c-117">Después de establecer las comunicaciones, el dispositivo envía un mensaje de solicitud de registro.</span><span class="sxs-lookup"><span data-stu-id="1b88c-117">After establishing communications, the device sends a registration request message.</span></span>

<span data-ttu-id="1b88c-118">La aplicación debe realizar los siguientes pasos cuando reciba un mensaje de solicitud de registro:</span><span class="sxs-lookup"><span data-stu-id="1b88c-118">Your application should perform the following steps when it receives a registration request message:</span></span>

1.  <span data-ttu-id="1b88c-119">Analice el mensaje mediante una llamada al método [**IWMDRMMessageParser::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) .</span><span class="sxs-lookup"><span data-stu-id="1b88c-119">Parse the message by calling the [**IWMDRMMessageParser::ParseRegistrationReqMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) method.</span></span> <span data-ttu-id="1b88c-120">Este método recupera el certificado de dispositivo y el número de serie del dispositivo, que son necesarios para identificar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b88c-120">This method retrieves the device certificate and the device serial number, both of which are needed to identify the device.</span></span>
2.  <span data-ttu-id="1b88c-121">Llame al método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , pasando el certificado y el número de serie del dispositivo recuperado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="1b88c-121">Call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and device serial number retrieved in step 1.</span></span> <span data-ttu-id="1b88c-122">Si se encuentra el dispositivo, ya está registrado y puede omitir el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="1b88c-122">If the device is found, it is already registered and you can skip the next step.</span></span>
3.  <span data-ttu-id="1b88c-123">Llame al método [**IWMDeviceRegistration:: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) para agregar el dispositivo a la base de datos de registro de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1b88c-123">Call the [**IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) method to add the device to the device registration database.</span></span>

<span data-ttu-id="1b88c-124">Puede obtener acceso a información sobre cualquier dispositivo en la base de datos de registro mediante la recuperación del objeto de dispositivo registrado asociado a él.</span><span class="sxs-lookup"><span data-stu-id="1b88c-124">You can access information about any device in the registration database by retrieving the registered device object associated with it.</span></span> <span data-ttu-id="1b88c-125">Hay dos maneras de obtener un objeto de dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="1b88c-125">There are two ways to get a registered device object.</span></span> <span data-ttu-id="1b88c-126">Si tiene el certificado y el número de serie del dispositivo, puede llamar al método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) .</span><span class="sxs-lookup"><span data-stu-id="1b88c-126">If you have the certificate and serial number of the device, you can call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method.</span></span> <span data-ttu-id="1b88c-127">Si no tiene el certificado y el número de serie del dispositivo, puede enumerar todos los dispositivos de la base de datos mediante una llamada a [**IWMDeviceRegistration:: GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguido de llamadas repetidas a [**IWMDeviceRegistration:: GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) hasta que una llamada devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="1b88c-127">If you do not have the certificate and serial number of the device, you can enumerate all the devices in the database by calling [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) followed by repeated calls to [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) until a call returns S\_FALSE.</span></span>

<span data-ttu-id="1b88c-128">Antes de que la aplicación pueda enviar datos a un dispositivo, debe asegurarse de que el dispositivo está aprobado, validado y abierto.</span><span class="sxs-lookup"><span data-stu-id="1b88c-128">Before your application can send data to a device, you must ensure that the device is approved, validated, and open.</span></span>

<span data-ttu-id="1b88c-129">La aprobación del dispositivo debe implicar la interacción con el usuario.</span><span class="sxs-lookup"><span data-stu-id="1b88c-129">Device approval should involve interaction with the user.</span></span> <span data-ttu-id="1b88c-130">Cuando un dispositivo envía un mensaje de registro, la aplicación puede solicitar al usuario que decida si el dispositivo es uno que debe recibir los datos del usuario.</span><span class="sxs-lookup"><span data-stu-id="1b88c-130">When a device sends a registration message, your application can prompt the user to decide whether the device is one that should receive that user's data.</span></span> <span data-ttu-id="1b88c-131">A continuación, actualice la base de datos de registro de dispositivos llamando al método [**IWMRegisteredDevice:: APPROVE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , pasando **true** o **false** según corresponda.</span><span class="sxs-lookup"><span data-stu-id="1b88c-131">Then update the device registration database by calling the [**IWMRegisteredDevice::Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) method, passing **TRUE** or **FALSE** as appropriate.</span></span>

<span data-ttu-id="1b88c-132">La validación también se denomina detección de proximidad.</span><span class="sxs-lookup"><span data-stu-id="1b88c-132">Validation is also called proximity detection.</span></span> <span data-ttu-id="1b88c-133">Se trata de un proceso por el que los objetos DRM internos del SDK de Windows Media Format determinan si el dispositivo está "cerca" del equipo en el que se ejecuta la aplicación para transmitir los medios de forma segura.</span><span class="sxs-lookup"><span data-stu-id="1b88c-133">This is a process by which the internal DRM objects of the Windows Media Format SDK determine whether the device is "near" enough to the computer running your application to securely transmit media.</span></span> <span data-ttu-id="1b88c-134">La proximidad viene determinada por el tiempo necesario para obtener una respuesta a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b88c-134">Nearness is determined by the time it takes to get a response to a message.</span></span> <span data-ttu-id="1b88c-135">Esta característica está pensada para impedir que usuarios no autorizados accedan a la red y obtengan los medios protegidos.</span><span class="sxs-lookup"><span data-stu-id="1b88c-135">This feature is intended to prevent unauthorized users from accessing your network and obtaining your secured media.</span></span> <span data-ttu-id="1b88c-136">Para obtener más información, vea [realizar la detección de proximidad](performing-proximity-detection.md).</span><span class="sxs-lookup"><span data-stu-id="1b88c-136">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>

<span data-ttu-id="1b88c-137">Para abrir un dispositivo, llame a [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span><span class="sxs-lookup"><span data-stu-id="1b88c-137">To open a device, call [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span>

> [!Note]  
> <span data-ttu-id="1b88c-138">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="1b88c-138">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1b88c-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b88c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b88c-140">**IWMRegisteredDevice**</span><span class="sxs-lookup"><span data-stu-id="1b88c-140">**IWMRegisteredDevice**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[<span data-ttu-id="1b88c-141">**Usar el protocolo DRM 10 de Windows Media para dispositivos de red**</span><span class="sxs-lookup"><span data-stu-id="1b88c-141">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




