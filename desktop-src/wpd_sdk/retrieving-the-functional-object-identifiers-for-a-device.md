---
description: Recuperar los identificadores de objeto funcional de un dispositivo
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Recuperar los identificadores de objeto funcional de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571168"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>Recuperar los identificadores de objeto funcional de un dispositivo

Como se indicó en el tema [Recuperación](retrieving-the-functional-categories-supported-by-a-device.md) de las categorías funcionales admitidas por un dispositivo, Windows dispositivos portátiles pueden admitir una o varias categorías funcionales. Cualquier categoría funcional determinada puede admitir uno o varios objetos funcionales. Por ejemplo, la categoría de almacenamiento puede admitir tres objetos de almacenamiento funcionales, cada uno de los cuales se identifica mediante una cadena de identificador único. A continuación, el primer objeto de almacenamiento se puede identificar mediante la cadena "Storage1", el segundo por la cadena "Storage2" y el tercero por la cadena "Storage3".

La función ListFunctionalObjects del módulo DeviceCapabilities.cpp muestra la recuperación de tipos de contenido para las categorías funcionales compatibles con un dispositivo seleccionado.

La aplicación puede recuperar las categorías funcionales admitidas por un dispositivo mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities (Interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Proporciona acceso a los métodos de recuperación de categorías funcionales. |
| [**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md) | Se usa para enumerar y almacenar datos de categoría funcional.         |



 

El código que se encuentra en la función ListFunctionalObjects es casi idéntico al código que se encuentra en la función ListFunctionalCategories. (Vea el [tema Recuperación de categorías funcionales admitidas por un dispositivo).](retrieving-the-functional-categories-supported-by-a-device.md) La única diferencia es la llamada al método [**IPortableDeviceCapabilities::GetFunctionalObjects,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) que aparece dentro del bucle que recorre en iteración las categorías funcionales.


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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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
            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
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

 

 



