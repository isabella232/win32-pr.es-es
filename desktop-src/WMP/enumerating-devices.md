---
title: Enumeración de dispositivos (SDK de WMP)
description: Este código de ejemplo muestra una función que enumera los dispositivos mediante la creación de una matriz de punteros que cada uno representa un dispositivo.
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Reproductor de Windows Media dispositivos portátiles
- Reproductor de Windows Media modelo de objetos, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Reproductor de Windows Media ActiveX control, dispositivos portátiles
- ActiveX control, dispositivos portátiles
- Reproductor de Windows Media Control de ActiveX móviles, dispositivos portátiles
- Reproductor de Windows Media Dispositivos móviles y portátiles
- dispositivos portátiles, enumeración
- enumeraciones, dispositivos portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f62ecc599e8a9610bf01b5f8a1651b330c9f8ed6abb4197fac89daeb751c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339863"
---
# <a name="enumerating-devices"></a>Enumeración de dispositivos

Reproductor de Windows Media representa dispositivos portátiles mediante la **interfaz IWMPSyncDevice.** El código de ejemplo siguiente muestra una función que crea una matriz de punteros a **IWMPSyncDevice**. Cada puntero de la matriz representa un dispositivo para el que Reproductor de Windows Media información almacenada. No es necesario que un dispositivo esté conectado al equipo ni que tenga una asociación con la instancia de Reproductor de Windows Media actual.

Debe enumerar los dispositivos cada vez que reciba el **evento DeviceConnect** o **el evento DeviceDisconnect.**

La siguiente función enumera los dispositivos. El *parámetro bConnectedOnly* especifica si se deben enumerar solo los dispositivos conectados actualmente al equipo del usuario.


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



Puede usar código similar para recuperar otras listas de dispositivos de este tipo. Por ejemplo, podría usar el estado [IWMPSyncDevice::get \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) para crear una matriz de dispositivos para los que existe una asociación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPEvents2::D eviceConnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2::D eviceDisconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**IWMPSyncDevice (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice::get \_ connected**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**IWMPSyncServices (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




