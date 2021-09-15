---
description: Recuperar las categorías funcionales admitidas por un dispositivo
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Recuperar las categorías funcionales admitidas por un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574265"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Recuperar las categorías funcionales admitidas por un dispositivo

Windows Los dispositivos portátiles pueden admitir una o varias categorías funcionales. Estas categorías se describen en la tabla siguiente.



| Category                    | Descripción                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Captura de audio               | El dispositivo se puede usar para grabar audio.                                              |
| Información de representación       | El dispositivo proporciona datos que describen los archivos multimedia que es capaz de representar. |
| Servicio de mensajes cortos (SMS) | El dispositivo admite mensajería de texto.                                                  |
| Captura de imágenes de still         | El dispositivo se puede usar para capturar imágenes fijas.                                      |
| Storage                     | El dispositivo se puede usar para almacenar archivos.                                               |



 

La función ListFunctionalCategories del módulo DeviceCapabilities.cpp muestra la recuperación de categorías funcionales para un dispositivo seleccionado.

La aplicación puede recuperar las categorías funcionales admitidas por un dispositivo mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities (Interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Proporciona acceso a los métodos de recuperación de categorías funcionales. |
| [**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md) | Se usa para enumerar y almacenar datos de categoría funcional.         |



 

La primera tarea que realiza la aplicación de ejemplo es la recuperación de un objeto [**IPortableDeviceCapabilities,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) que se usa para recuperar las categorías funcionales en el dispositivo seleccionado.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



Las categorías recuperadas se almacenan en un [**objeto IPortableDevicePropVariantCollection.**](iportabledevicepropvariantcollection.md)

El siguiente paso es la enumeración y la presentación de las categorías admitidas. El primer paso que realiza la aplicación de ejemplo es recuperar el recuento de categorías admitidas. A continuación, usa este recuento para recorrer en iteración el objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene las categorías admitidas.


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDevice (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities (Interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



