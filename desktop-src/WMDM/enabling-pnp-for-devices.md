---
title: Habilitación de PnP para dispositivos
description: Habilitación de PnP para dispositivos
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media Administrador de dispositivos, dispositivos PnP
- Administrador de dispositivos, dispositivos PnP
- Guía de programación, dispositivos PnP
- proveedores de servicios, dispositivos PnP
- creación de proveedores de servicios, dispositivos PnP
- Dispositivos PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903347"
---
# <a name="enabling-pnp-for-devices"></a><span data-ttu-id="480cf-109">Habilitación de PnP para dispositivos</span><span class="sxs-lookup"><span data-stu-id="480cf-109">Enabling PnP for Devices</span></span>

<span data-ttu-id="480cf-110">Windows Media Administrador de dispositivos supervisa las notificaciones de llegada y eliminación de dispositivos que anuncian una interfaz de dispositivo del reproductor de audio portátil.</span><span class="sxs-lookup"><span data-stu-id="480cf-110">Windows Media Device Manager monitors arrival and removal notifications of devices that advertise a Portable Audio Player device interface.</span></span> <span data-ttu-id="480cf-111">Al llegar a este dispositivo, Windows Media Administrador de dispositivos consulta un parámetro de dispositivo denominado *WMDMSPCLSID* para el identificador de clase del proveedor de servicios responsable de este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="480cf-111">On the arrival of such a device, Windows Media Device Manager queries a device parameter named *WMDMSPCLSID* for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="480cf-112">Windows Media Administrador de dispositivos llama a [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) en este proveedor de servicios para crear un objeto de dispositivo, que se expone a la aplicación como un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="480cf-112">Windows Media Device Manager calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on this service provider to create a device object, which is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

<span data-ttu-id="480cf-113">Un proveedor de servicios puede administrar dispositivos Plug and Play o dispositivos que no son Plug and Play; no puede controlar ambos tipos.</span><span class="sxs-lookup"><span data-stu-id="480cf-113">A service provider can either handle PnP devices, or non-PnP devices; it cannot handle both types.</span></span>

<span data-ttu-id="480cf-114">Para que un dispositivo funcione con el mecanismo anterior (y, por tanto, habilitar las notificaciones de llegada y eliminación para el dispositivo en Windows Media Administrador de dispositivos aplicaciones), deben cumplirse los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="480cf-114">For a device to work with the preceding mechanism (and thus enable arrival and removal notifications for the device under Windows Media Device Manager applications), the following requirements must be met:</span></span>

-   <span data-ttu-id="480cf-115">El controlador de dispositivo de este dispositivo debe anunciar la interfaz de dispositivo de Windows Media Administrador de dispositivos reproductor de audio portátil.</span><span class="sxs-lookup"><span data-stu-id="480cf-115">The device driver of this device must advertise the Windows Media Device Manager Portable Audio Player device interface.</span></span> <span data-ttu-id="480cf-116">El GUID para esta interfaz de dispositivo se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="480cf-116">The GUID for this device interface is defined as:</span></span>

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > <span data-ttu-id="480cf-117">Un dispositivo no debe anunciar esta interfaz si el dispositivo anuncia la interfaz de volumen (definida como volumen VolumeClassGuid o GUID \_ DEVINTERFACE \_ en winioctl. h).</span><span class="sxs-lookup"><span data-stu-id="480cf-117">A device should not advertise this interface if the device advertises the Volume interface (defined as VolumeClassGuid or GUID\_DEVINTERFACE\_VOLUME in winioctl.h).</span></span> <span data-ttu-id="480cf-118">Si el dispositivo anuncia la interfaz de volumen, ya está habilitada para PnP en Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="480cf-118">If the device advertises the Volume Interface, it is already PnP-enabled under Windows Media Device Manager.</span></span>

     

    <span data-ttu-id="480cf-119">-Y/O-</span><span class="sxs-lookup"><span data-stu-id="480cf-119">-AND/OR-</span></span>

    <span data-ttu-id="480cf-120">Se debe crear una nueva subclave del registro para el proveedor de servicios dentro de la subclave HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media administrador de dispositivos \\ KnownDevices.</span><span class="sxs-lookup"><span data-stu-id="480cf-120">A new registry subkey for the service provider must be created inside the subkey HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\KnownDevices.</span></span> <span data-ttu-id="480cf-121">Esta clave debe tener el nombre del proveedor de servicios y debe tener las dos entradas de \_ valor reg SZ siguientes:</span><span class="sxs-lookup"><span data-stu-id="480cf-121">This key should have the name of your service provider and must have the following two Reg\_SZ value entries:</span></span>

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   <span data-ttu-id="480cf-122">El dispositivo debe tener un parámetro de dispositivo denominado WMDMSPCLSID.</span><span class="sxs-lookup"><span data-stu-id="480cf-122">The device must have a device parameter named WMDMSPCLSID.</span></span> <span data-ttu-id="480cf-123">El valor de este parámetro debe establecerse como el CLSID del proveedor de servicios en un formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="480cf-123">The value of this parameter should be set as the CLSID of the service provider in a string form.</span></span> <span data-ttu-id="480cf-124">Para obtener más información sobre los parámetros del dispositivo, consulte [parámetros del dispositivo](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="480cf-124">For more information about device parameters, see [Device Parameters](device-parameters.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="480cf-125">El valor del parámetro debe ser el CLSID, no el ProgID del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="480cf-125">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span>

     

-   <span data-ttu-id="480cf-126">El proveedor de servicios de este dispositivo debe implementar la interfaz IMDServiceProvider2.</span><span class="sxs-lookup"><span data-stu-id="480cf-126">The service provider for this device must implement the IMDServiceProvider2 interface.</span></span>
-   <span data-ttu-id="480cf-127">La clave del proveedor de servicios en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media administrador de dispositivos \\ plugins \\ Sp \\ SPName debe contener el siguiente valor DWORD</span><span class="sxs-lookup"><span data-stu-id="480cf-127">The service provider key under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\Plugins\\SP\\SPName must contain the following DWORD value</span></span>
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a><span data-ttu-id="480cf-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="480cf-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="480cf-129">**Creación de un proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="480cf-129">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




