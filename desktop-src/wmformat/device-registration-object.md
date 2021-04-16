---
title: Objeto de registro de dispositivos
description: Objeto de registro de dispositivos
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- SDK de Windows Media Format, objetos de registro de dispositivos
- Advanced Systems Format (ASF), objetos de registro de dispositivos
- ASF (formato de sistemas avanzados), objetos de registro de dispositivos
- objetos, objetos de registro de dispositivos
- objetos de registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695540"
---
# <a name="device-registration-object"></a><span data-ttu-id="ac4d1-108">Objeto de registro de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ac4d1-108">Device Registration Object</span></span>

<span data-ttu-id="ac4d1-109">El objeto de registro de dispositivos administra la base de datos de registro de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-109">The device registration object manages the device registration database.</span></span> <span data-ttu-id="ac4d1-110">Esta base de datos almacena información acerca de los dispositivos de red, como reproductores de vídeo Set-Top, que están conectados al equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-110">This database stores information about network devices, such as set-top video players, that are connected to the client computer.</span></span> <span data-ttu-id="ac4d1-111">El propósito principal de la base de datos de registro de dispositivos es administrar los dispositivos que usan el protocolo DRM 10 de Windows Media para dispositivos de red para recibir flujos de datos protegidos.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-111">The primary purpose of the device registration database is to manage devices that use the Windows Media DRM 10 for Network Devices protocol to receive secured data streams.</span></span>

<span data-ttu-id="ac4d1-112">Si la aplicación admite Windows Media DRM 10 para dispositivos de red, debe usar las interfaces de este objeto para registrar los dispositivos de red y para validar dichos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-112">If your application supports Windows Media DRM 10 for Network Devices, you must use the interfaces of this object to register network devices, and to validate those devices.</span></span> <span data-ttu-id="ac4d1-113">También puede usar la base de datos de registro de dispositivos para almacenar información acerca de los dispositivos de red que no usan Windows Media DRM 10 para dispositivos de red, aunque no toda la información de la base de datos se aplicará a dichos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-113">You can also use the device registration database to store information about network devices that do not use Windows Media DRM 10 for Network Devices, although not all of the information in the database will apply to such devices.</span></span>

<span data-ttu-id="ac4d1-114">La función [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) crea el objeto de registro de dispositivos, que establece un puntero a una interfaz **IWMDeviceRegistration** .</span><span class="sxs-lookup"><span data-stu-id="ac4d1-114">The device registration object is created by the [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) function, which sets a pointer to an **IWMDeviceRegistration** interface.</span></span> <span data-ttu-id="ac4d1-115">Los otros métodos del objeto de registro de dispositivos se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="ac4d1-115">The other methods of the device registration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="ac4d1-116">El objeto de registro de dispositivos admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-116">The following interfaces are supported by the device registration object.</span></span>



| <span data-ttu-id="ac4d1-117">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ac4d1-117">Interface</span></span>                                              | <span data-ttu-id="ac4d1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac4d1-118">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="ac4d1-119">**IWMDeviceRegistration**</span><span class="sxs-lookup"><span data-stu-id="ac4d1-119">**IWMDeviceRegistration**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | <span data-ttu-id="ac4d1-120">Administra la base de datos de registro de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-120">Manages the device registration database.</span></span> |
| [<span data-ttu-id="ac4d1-121">**IWMDRMMessageParser**</span><span class="sxs-lookup"><span data-stu-id="ac4d1-121">**IWMDRMMessageParser**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | <span data-ttu-id="ac4d1-122">Analiza los mensajes enviados por los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-122">Parses messages sent by devices.</span></span>          |
| [<span data-ttu-id="ac4d1-123">**IWMProximityDetection**</span><span class="sxs-lookup"><span data-stu-id="ac4d1-123">**IWMProximityDetection**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | <span data-ttu-id="ac4d1-124">Administra la validación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-124">Manages device validation.</span></span>                |



 

<span data-ttu-id="ac4d1-125">La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar los métodos de la interfaz **IWMProximityDetection** .</span><span class="sxs-lookup"><span data-stu-id="ac4d1-125">The following callback interface must be implemented by the application in order to use the methods of the **IWMProximityDetection** interface.</span></span>



| <span data-ttu-id="ac4d1-126">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ac4d1-126">Interface</span></span>                                      | <span data-ttu-id="ac4d1-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac4d1-127">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="ac4d1-128">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="ac4d1-128">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="ac4d1-129">Recibe mensajes de estado de los procesos que se ejecutan en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="ac4d1-129">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ac4d1-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac4d1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac4d1-131">**Objects**</span><span class="sxs-lookup"><span data-stu-id="ac4d1-131">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




