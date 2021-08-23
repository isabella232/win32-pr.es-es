---
description: Use el método IWiaDevMgr::EnumDeviceInfo (o IWiaDevMgr2::EnumDeviceInfo) para enumerar los dispositivos de adquisición de imágenes de Windows (WIA) instalados en un sistema.
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Enumeración de dispositivos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60b6587d88b2836e057f0b6d7e31bd7f22d79c6220c51b407b621370d8524b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814265"
---
# <a name="enumerating-system-devices"></a>Enumeración de dispositivos del sistema

Use el método [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (o [**IWiaDevMgr2::EnumDeviceInfo)**](-wia-iwiadevmgr2-enumdeviceinfo.md)para enumerar los dispositivos de adquisición de imágenes de Windows (WIA) instalados en un sistema. Este método crea un objeto de enumeración para las propiedades de los dispositivos y devuelve un puntero a la interfaz [**INFO de IEnumWIA \_ \_ DEV**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) que admite el objeto de enumeración.

A continuación, puede usar los métodos de la interfaz [**INFO de IEnumWIA \_ \_ DEV**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obtener un puntero de interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo instalado en el sistema.

El código siguiente de la aplicación de ejemplo WiaSSamp muestra cómo crear un objeto de enumeración para los dispositivos en un sistema e iterar por esos dispositivos:


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



WIA \_ DEVINFO \_ ENUM \_ LOCAL es una constante WIA que representa el único valor válido para este parámetro.

En el ejemplo, el parámetro **pWiaDevMgr** apunta a una instancia de la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2)**](-wia-iwiadevmgr2.md)después de una llamada anterior a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

La aplicación llama al método [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (o [**IWiaDevMgr2::EnumDeviceInfo)**](-wia-iwiadevmgr2-enumdeviceinfo.md)del puntero [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2)**](-wia-iwiadevmgr2.md) **pWiaDevMgr** que rellena **pWiaEnumDevInfo** con la dirección de un puntero a la interfaz INFO [**de \_ DEV \_ de IEnumWIA.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)

Si la llamada se realiza correctamente, la aplicación llama al método [**IEnumWIA \_ DEV \_ INFO::Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) del puntero INFO [**de \_ DEV \_ de IEnumWIA.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) La **variable pWiaEnumDevInfo** garantiza que la enumeración se inicia al principio.

Si esta llamada se realiza correctamente, la aplicación recorre en iteración los dispositivos del sistema llamando repetidamente al método [**IEnumWIA \_ DEV \_ INFO::Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) del puntero INFO de [**IEnumWIA \_ DEV \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** hasta que el método ya no devuelve S OK, lo que indica que la enumeración se ha \_ completado.

Cada llamada a **pWiaEnumDevInfo->Next** rellena **pWiaPropertyStorage** con un puntero a la [**interfaz IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) que contiene información de propiedades para un dispositivo específico.

 

 
