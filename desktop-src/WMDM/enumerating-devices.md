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
# <a name="enumerating-windows-media-device-manager-devices"></a>Enumeración de dispositivos de Administrador de dispositivos Windows Media

Después de autenticar una aplicación, puede empezar a enumerar los dispositivos detectados por Windows Media Administrador de dispositivos. La enumeración se realiza mediante una interfaz de enumeración, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtenida mediante [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) o [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices). Si se admite, use el método **EnumDevices2,** ya que la versión anterior solo devolvió interfaces heredadas en los dispositivos, mientras que la nueva versión devuelve las interfaces heredadas y las nuevas.

Antes de obtener un enumerador, debe decidir qué vista de enumeración usar. Algunos dispositivos exponen cada almacenamiento como un dispositivo diferente. Por ejemplo, dos tarjetas de memoria flash en un dispositivo enumerarán como si fueran dispositivos independientes. Puede especificar que todos los almacenamientos de un dispositivo se enumeren juntos como un único dispositivo. Puede establecer esta preferencia solo una vez en la aplicación; Si desea cambiarla, debe apagar la aplicación y reiniciarla. Sin embargo, tenga en cuenta que los dispositivos heredados a veces omitirán una solicitud para enumerar los almacenamientos de dispositivos independientes como un único dispositivo y seguirán enumerándolos por separado.

En los pasos siguientes se muestra cómo enumerar los dispositivos conectados:

1.  Establezca la preferencia de enumeración de dispositivos [**mediante IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference). Si no se llama a este método, el método predeterminado es mostrar los almacenamientos como dispositivos independientes. Para determinar si los "dispositivos" individuales son realmente almacenamientos en el mismo dispositivo, llame a [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); Los almacenamientos del mismo dispositivo devolverán valores idénticos, excepto el dígito final después del último signo "$".
2.  Consulte [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) o [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)y, a continuación, llame a [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) para obtener la interfaz del enumerador de dispositivos, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). (Si se admite, use **EnumDevices2**, que es más eficaz, ya que es posible que la versión anterior no devuelva dispositivos MTP).
3.  Llame al [**método IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) para recuperar uno o varios dispositivos a la vez. Continúe con la llamada a este método hasta que el método devuelva S \_ FALSE o un mensaje de error. Si solo recupera un dispositivo a la vez, no es necesario asignar una matriz para contener los dispositivos.

Dado que los usuarios pueden adjuntar o quitar dispositivos del equipo mientras se ejecuta la aplicación, es una buena idea implementar la notificación de la conexión o eliminación del dispositivo. Para ello, implemente la [**interfaz IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) y regístrela. Para obtener más información sobre esto, vea [Habilitación de notificaciones.](enabling-notifications.md)

El siguiente código de C++ enumera los dispositivos y solicita información sobre cada dispositivo.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una aplicación de Administrador de dispositivos Windows Media**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




