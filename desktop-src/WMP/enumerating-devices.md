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
# <a name="enumerating-devices"></a>Enumerar dispositivos

Windows Media Player representa dispositivos portátiles mediante la interfaz **IWMPSyncDevice** . En el ejemplo de código siguiente se muestra una función que crea una matriz de punteros a **IWMPSyncDevice**. Cada puntero de la matriz representa un dispositivo para el que Windows Media Player tiene información almacenada. No es necesario que un dispositivo esté conectado al equipo, ni es necesario tener una asociación con la instancia actual de Media Player de Windows.

Debe enumerar los dispositivos siempre que reciba el evento **DeviceConnect** o el evento **DeviceDisconnect** .

La función siguiente enumera los dispositivos. El parámetro *bConnectedOnly* especifica si se deben enumerar solo los dispositivos conectados actualmente al equipo del usuario.


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



Podría usar código similar para recuperar otras listas de dispositivos de este tipo. Por ejemplo, puede usar [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) para crear una matriz de dispositivos para los que existe una asociación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPEvents2::D eviceConnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2::D eviceDisconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**Interfaz IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice:: get \_ connected**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**Interfaz IWMPSyncServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




