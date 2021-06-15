---
title: Enumeración de dispositivos de Administrador de dispositivos Windows Media
description: Obtenga información sobre cómo enumerar los dispositivos detectados por Windows Media Administrador de dispositivos mediante una interfaz de enumeración.
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Media Administrador de dispositivos, enumerar dispositivos
- Administrador de dispositivos, enumerar dispositivos
- guía de programación, enumeración de dispositivos
- aplicaciones de escritorio, enumeración de dispositivos
- creación de aplicaciones Administrador de dispositivos Windows Media, enumeración de dispositivos
- enumerar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94653d59b0880e9d52f43b34e21522a220d39beb
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068202"
---
# <a name="enumerating-windows-media-device-manager-devices"></a><span data-ttu-id="a7773-109">Enumeración de dispositivos de Administrador de dispositivos Windows Media</span><span class="sxs-lookup"><span data-stu-id="a7773-109">Enumerating Windows Media Device Manager devices</span></span>

<span data-ttu-id="a7773-110">Después de autenticar una aplicación, puede empezar a enumerar los dispositivos detectados por Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a7773-110">After authenticating an application, you can begin to enumerate the devices detected by Windows Media Device Manager.</span></span> <span data-ttu-id="a7773-111">La enumeración se realiza mediante una interfaz de enumeración, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtenida mediante [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) o [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span><span class="sxs-lookup"><span data-stu-id="a7773-111">Enumeration is done by using an enumeration interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtained by using either [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) or [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span></span> <span data-ttu-id="a7773-112">Si se admite, use el método **EnumDevices2,** ya que la versión anterior solo devolvió interfaces heredadas en los dispositivos, mientras que la nueva versión devuelve las interfaces heredadas y las nuevas.</span><span class="sxs-lookup"><span data-stu-id="a7773-112">If supported, use the **EnumDevices2** method, because the earlier version only returned legacy interfaces on devices, whereas the new version returns both the legacy and the new interfaces.</span></span>

<span data-ttu-id="a7773-113">Antes de obtener un enumerador, debe decidir qué vista de enumeración usar.</span><span class="sxs-lookup"><span data-stu-id="a7773-113">Before obtaining an enumerator, you should decide what enumeration view to use.</span></span> <span data-ttu-id="a7773-114">Algunos dispositivos exponen cada almacenamiento como un dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="a7773-114">Some devices expose each storage as a different device.</span></span> <span data-ttu-id="a7773-115">Por ejemplo, dos tarjetas de memoria flash en un dispositivo enumerarán como si fueran dispositivos independientes.</span><span class="sxs-lookup"><span data-stu-id="a7773-115">For example, two flash memory cards on a device will enumerate as if they were separate devices.</span></span> <span data-ttu-id="a7773-116">Puede especificar que todos los almacenamientos de un dispositivo se enumeren juntos como un único dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7773-116">You can specify that all storages on a device are enumerated together as a single device.</span></span> <span data-ttu-id="a7773-117">Puede establecer esta preferencia solo una vez en la aplicación; Si desea cambiarla, debe apagar la aplicación y reiniciarla.</span><span class="sxs-lookup"><span data-stu-id="a7773-117">You can set this preference only once in your application; if you want to change it, you must shut down the application and restart it.</span></span> <span data-ttu-id="a7773-118">Sin embargo, tenga en cuenta que los dispositivos heredados a veces omitirán una solicitud para enumerar los almacenamientos de dispositivos independientes como un único dispositivo y seguirán enumerándolos por separado.</span><span class="sxs-lookup"><span data-stu-id="a7773-118">However, note that legacy devices will sometimes ignore a request to enumerate separate device storages as a single device, and continue to enumerate them separately.</span></span>

<span data-ttu-id="a7773-119">En los pasos siguientes se muestra cómo enumerar los dispositivos conectados:</span><span class="sxs-lookup"><span data-stu-id="a7773-119">The following steps show how to enumerate connected devices:</span></span>

1.  <span data-ttu-id="a7773-120">Establezca la preferencia de enumeración de dispositivos [**mediante IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span><span class="sxs-lookup"><span data-stu-id="a7773-120">Set the device enumeration preference using [**IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span></span> <span data-ttu-id="a7773-121">Si no se llama a este método, el método predeterminado es mostrar los almacenamientos como dispositivos independientes.</span><span class="sxs-lookup"><span data-stu-id="a7773-121">If this method is not called, the default method is to show storages as separate devices.</span></span> <span data-ttu-id="a7773-122">Para determinar si los "dispositivos" individuales son realmente almacenamientos en el mismo dispositivo, llame a [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); Los almacenamientos del mismo dispositivo devolverán valores idénticos, excepto el dígito final después del último signo "$".</span><span class="sxs-lookup"><span data-stu-id="a7773-122">To determine whether individual "devices" are actually storages on the same device, call [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); storages from the same device will return identical values, except for the final digit after the last "$" sign.</span></span>
2.  <span data-ttu-id="a7773-123">Consulte [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) o [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)y, a continuación, llame a [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) para obtener la interfaz del enumerador de dispositivos, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span><span class="sxs-lookup"><span data-stu-id="a7773-123">Query for [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) or [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), and then call [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) to obtain the device enumerator interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span></span> <span data-ttu-id="a7773-124">(Si se admite, use **EnumDevices2**, que es más eficaz, ya que es posible que la versión anterior no devuelva dispositivos MTP).</span><span class="sxs-lookup"><span data-stu-id="a7773-124">(If supported, use **EnumDevices2**, which is more efficient, as the earlier version may not return MTP devices).</span></span>
3.  <span data-ttu-id="a7773-125">Llame al [**método IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) para recuperar uno o varios dispositivos a la vez.</span><span class="sxs-lookup"><span data-stu-id="a7773-125">Call the [**IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) method to retrieve one or more devices at a time.</span></span> <span data-ttu-id="a7773-126">Continúe con la llamada a este método hasta que el método devuelva S \_ FALSE o un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="a7773-126">Continue to call this method until the method returns S\_FALSE or an error message.</span></span> <span data-ttu-id="a7773-127">Si solo recupera un dispositivo a la vez, no es necesario asignar una matriz para contener los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a7773-127">If retrieving only one device at a time, you do not need to allocate an array to hold the devices.</span></span>

<span data-ttu-id="a7773-128">Dado que los usuarios pueden adjuntar o quitar dispositivos del equipo mientras se ejecuta la aplicación, es una buena idea implementar la notificación de la conexión o eliminación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7773-128">Because users can attach or remove devices from the computer while your application is running, it is a good idea to implement notification of device connection or removal.</span></span> <span data-ttu-id="a7773-129">Para ello, implemente la [**interfaz IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) y regístrela.</span><span class="sxs-lookup"><span data-stu-id="a7773-129">This is done by implementing the [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) interface and registering it.</span></span> <span data-ttu-id="a7773-130">Para obtener más información sobre esto, vea [Habilitación de notificaciones.](enabling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="a7773-130">For more information on this, see [Enabling Notifications](enabling-notifications.md).</span></span>

<span data-ttu-id="a7773-131">El siguiente código de C++ enumera los dispositivos y solicita información sobre cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7773-131">The following C++ code enumerates devices and requests information about each device.</span></span>


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a7773-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7773-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7773-133">**Creación de una aplicación de Administrador de dispositivos Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a7773-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




