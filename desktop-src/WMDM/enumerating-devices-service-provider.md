---
title: Enumeración de dispositivos (WMDM)
description: Windows Media Administrador de dispositivos mantiene una memoria caché de dispositivos conectados. Obtenga información sobre cómo Windows Media Administrador de dispositivos mantiene o actualiza su caché.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Administrador de dispositivos, enumerar dispositivos
- Administrador de dispositivos, enumerar dispositivos
- guía de programación, enumeración de dispositivos
- proveedores de servicios, enumerar dispositivos
- crear proveedores de servicios, enumerar dispositivos
- enumerar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067912"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="6b9dd-110">Enumeración de dispositivos (WMDM)</span><span class="sxs-lookup"><span data-stu-id="6b9dd-110">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="6b9dd-111">Windows Media Administrador de dispositivos mantiene una caché de dispositivos conectados que se actualiza cuando se inicia una aplicación de Windows Media Administrador de dispositivos, cuando un dispositivo Plug and Play (PnP) se conecta o se desconecta, o cuando la aplicación llama a [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span><span class="sxs-lookup"><span data-stu-id="6b9dd-111">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="6b9dd-112">Esta memoria caché se expone a la aplicación cuando llama a [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span><span class="sxs-lookup"><span data-stu-id="6b9dd-112">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="6b9dd-113">Cada dispositivo se expone a la aplicación como una [**interfaz IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)</span><span class="sxs-lookup"><span data-stu-id="6b9dd-113">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="6b9dd-114">Si el proveedor de servicios está registrado para controlar dispositivos PnP, Windows Media Administrador de dispositivos conocerá la lista actual de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-114">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="6b9dd-115">Si el proveedor de servicios está registrado para controlar dispositivos que no son PnP, el proveedor de servicios es responsable de detectar los dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-115">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="6b9dd-116">Un proveedor de servicios solo se puede registrar para dispositivos PnP o no PnP, nunca ambos.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-116">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="6b9dd-117">Las siguientes acciones muestran cómo Windows Media Administrador de dispositivos mantiene o actualiza su memoria caché.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-117">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="6b9dd-118">Tenga en cuenta que la memoria caché nunca se actualiza cuando un dispositivo que no es PnP se conecta o se desconecta.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-118">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="6b9dd-119">Se inicia una aplicación de Administrador de dispositivos Windows Media</span><span class="sxs-lookup"><span data-stu-id="6b9dd-119">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="6b9dd-120">Windows Media Administrador de dispositivos recupera una lista de dispositivos PnP conectados del subsistema PnP y llama a [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) en el SP registrado para cada dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-120">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="6b9dd-121">(Detecta el proveedor de servicios correcto consultando el parámetro de dispositivo WMDMSPCLSID para el identificador de clase del proveedor de servicios responsable de este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-121">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="6b9dd-122">Consulte [Parámetros del dispositivo](device-parameters.md) para obtener más información). Todos los dispositivos devueltos se agregan a la caché de dispositivos Administrador de dispositivos Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-122">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="6b9dd-123">Windows Media Administrador de dispositivos encuentra todos los proveedores de servicios que no son PnP registrados con él y llama a [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) en cada proveedor de servicios para obtener una lista de dispositivos de cada uno.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-123">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="6b9dd-124">Todos los dispositivos devueltos se agregan a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-124">All devices returned are added to the cache.</span></span>

<span data-ttu-id="6b9dd-125">La aplicación llama a IWMDeviceManager/2::EnumDevices/2</span><span class="sxs-lookup"><span data-stu-id="6b9dd-125">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="6b9dd-126">Windows Media Administrador de dispositivos devuelve su lista de dispositivos almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-126">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="6b9dd-127">Se conecta un dispositivo PnP</span><span class="sxs-lookup"><span data-stu-id="6b9dd-127">A PnP device connects</span></span>

-   <span data-ttu-id="6b9dd-128">Windows Media Administrador de dispositivos busca el proveedor de servicios pertinente y llama a **IMDServiceProvider2::CreateDevice** y agrega el dispositivo a su caché.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-128">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="6b9dd-129">Si la aplicación implementa [**IWMDMNotification,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)Windows Media Administrador de dispositivos llama a [**IWMDMNotification::WMDMMessage con**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) una notificación de llegada.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-129">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="6b9dd-130">Un dispositivo PnP se desconecta</span><span class="sxs-lookup"><span data-stu-id="6b9dd-130">A PnP device disconnects</span></span>

-   <span data-ttu-id="6b9dd-131">Windows Media Administrador de dispositivos quita el elemento de su memoria caché.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-131">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="6b9dd-132">Si la aplicación implementa IWMDMNotification, Windows Media Administrador de dispositivos llama a IWMDMNotification::WMDMMessage con una notificación de salida.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-132">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="6b9dd-133">La aplicación llama a IWMDeviceManager2::Reinitialize</span><span class="sxs-lookup"><span data-stu-id="6b9dd-133">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="6b9dd-134">Actualiza la memoria caché con todos los dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-134">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="6b9dd-135">Un dispositivo que no es PnP se conecta o se desconecta</span><span class="sxs-lookup"><span data-stu-id="6b9dd-135">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="6b9dd-136">Windows Media Administrador de dispositivos informa de la llegada o salida y no realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="6b9dd-136">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b9dd-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b9dd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b9dd-138">**Creación de un proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="6b9dd-138">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




