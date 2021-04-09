---
title: Enumerar dispositivos (SDK de WMP)
description: Enumerar dispositivos
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player, dispositivos portátiles
- Modelo de objetos de Windows Media Player, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Control ActiveX de Windows Media Player, dispositivos portátiles
- Control ActiveX, dispositivos portátiles
- Control ActiveX móvil de Windows Media Player, dispositivos portátiles
- Windows Media Player dispositivos móviles y portátiles
- dispositivos portátiles, enumeración
- enumeraciones, dispositivos portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5025d0e0a7e99028b22cc24ebc56337ea84d2fb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994949"
---
# <a name="enumerating-devices"></a><span data-ttu-id="30e29-112">Enumerar dispositivos</span><span class="sxs-lookup"><span data-stu-id="30e29-112">Enumerating Devices</span></span>

<span data-ttu-id="30e29-113">Windows Media Player representa dispositivos portátiles mediante la interfaz **IWMPSyncDevice** .</span><span class="sxs-lookup"><span data-stu-id="30e29-113">Windows Media Player represents portable devices by using the **IWMPSyncDevice** interface.</span></span> <span data-ttu-id="30e29-114">En el ejemplo de código siguiente se muestra una función que crea una matriz de punteros a **IWMPSyncDevice**.</span><span class="sxs-lookup"><span data-stu-id="30e29-114">The following example code shows a function that creates an array of pointers to **IWMPSyncDevice**.</span></span> <span data-ttu-id="30e29-115">Cada puntero de la matriz representa un dispositivo para el que Windows Media Player tiene información almacenada.</span><span class="sxs-lookup"><span data-stu-id="30e29-115">Each pointer in the array represents a device for which Windows Media Player has stored information.</span></span> <span data-ttu-id="30e29-116">No es necesario que un dispositivo esté conectado al equipo, ni es necesario tener una asociación con la instancia actual de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="30e29-116">A device is not required to be connected to the computer, nor is it required to have a partnership with the current Windows Media Player instance.</span></span>

<span data-ttu-id="30e29-117">Debe enumerar los dispositivos siempre que reciba el evento **DeviceConnect** o el evento **DeviceDisconnect** .</span><span class="sxs-lookup"><span data-stu-id="30e29-117">You should enumerate devices whenever you receive the **DeviceConnect** event or the **DeviceDisconnect** event.</span></span>

<span data-ttu-id="30e29-118">La función siguiente enumera los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="30e29-118">The following function enumerates devices.</span></span> <span data-ttu-id="30e29-119">El parámetro *bConnectedOnly* especifica si se deben enumerar solo los dispositivos conectados actualmente al equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="30e29-119">The *bConnectedOnly* parameter specifies whether to enumerate only devices currently connected to the user's computer.</span></span>


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="30e29-120">Podría usar código similar para recuperar otras listas de dispositivos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="30e29-120">You might use similar code to retrieve other such device lists.</span></span> <span data-ttu-id="30e29-121">Por ejemplo, puede usar [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) para crear una matriz de dispositivos para los que existe una asociación.</span><span class="sxs-lookup"><span data-stu-id="30e29-121">For example, you could use [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) to create an array of devices for which a partnership exists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30e29-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30e29-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e29-123">**IWMPEvents2::D eviceConnect**</span><span class="sxs-lookup"><span data-stu-id="30e29-123">**IWMPEvents2::DeviceConnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[<span data-ttu-id="30e29-124">**IWMPEvents2::D eviceDisconnect**</span><span class="sxs-lookup"><span data-stu-id="30e29-124">**IWMPEvents2::DeviceDisconnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[<span data-ttu-id="30e29-125">**Interfaz IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="30e29-125">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="30e29-126">**IWMPSyncDevice:: get \_ connected**</span><span class="sxs-lookup"><span data-stu-id="30e29-126">**IWMPSyncDevice::get\_connected**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[<span data-ttu-id="30e29-127">**Interfaz IWMPSyncServices**</span><span class="sxs-lookup"><span data-stu-id="30e29-127">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[<span data-ttu-id="30e29-128">**Trabajar con dispositivos portátiles**</span><span class="sxs-lookup"><span data-stu-id="30e29-128">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




