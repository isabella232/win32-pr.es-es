---
description: Selección de un dispositivo de captura
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Selección de un dispositivo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bf92692070c8a0191a91559481d5446bf3d4d894c8e7f6aafc2ed9e73a6667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904415"
---
# <a name="selecting-a-capture-device"></a>Selección de un dispositivo de captura

Para seleccionar un dispositivo de captura de audio o vídeo, use el enumerador de dispositivos del sistema [,](system-device-enumerator.md)que se describe en el tema Uso [del enumerador de dispositivos del sistema](using-the-system-device-enumerator.md). El enumerador de dispositivos del sistema devuelve una colección de monikers de dispositivo, seleccionados por categoría de dispositivo. Un *moniker es* un objeto COM que contiene información sobre otro objeto. Los monikers permiten a la aplicación obtener información sobre un objeto sin crear realmente el objeto. Más adelante, la aplicación puede usar el moniker para crear el objeto . Para obtener más información sobre monikers, consulte la documentación de [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).

Para usar el enumerador de dispositivos del sistema, realice los pasos siguientes.

1.  Llame [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia del enumerador de dispositivos del sistema.
2.  Llame [**a ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) y especifique la categoría de dispositivo como GUID. En el caso de los dispositivos de captura, las siguientes categorías son relevantes. 

    | GUID de categoría                       | Descripción           |
    |-------------------------------------|-----------------------|
    | **CLSID \_ AudioInputDeviceCategory** | Dispositivos de captura de audio |
    | **CLSID \_ VideoInputDeviceCategory** | Dispositivos de captura de vídeo |

    

     

    Si una cámara de vídeo tiene un micrófono integrado, aparece en ambas categorías. Sin embargo, el sistema trata la cámara y el micrófono como dispositivos independientes, con fines de enumeración, creación de dispositivos y streaming de datos.

3.  El [**método CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) devuelve un puntero a la [**interfaz IEnumMoniker.**](/windows/win32/api/objidl/nn-objidl-ienummoniker) Para enumerar los monikers, llame [**a IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).

El código siguiente crea un enumerador para una categoría de dispositivo especificada.


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



La [**interfaz IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) enumera una lista de interfaces [**IMoniker,**](/windows/win32/api/objidl/nn-objidl-imoniker) cada una de las cuales representa un moniker de dispositivo. La aplicación puede leer las propiedades del moniker o usar el moniker para crear un filtro DirectShow captura para el dispositivo. Las propiedades de Moniker se devuelven **como valores VARIANT.** Los monikers de dispositivo admiten las siguientes propiedades.



| Propiedad       | Descripción                                                               | Tipo de VARIANTE |
|----------------|---------------------------------------------------------------------------|--------------|
| "FriendlyName" | Nombre del dispositivo.                                                   | **VT \_ BSTR** |
| "Descripción"  | Una descripción del dispositivo.                                              | **VT \_ BSTR** |
| "DevicePath"   | Cadena única que identifica el dispositivo. (Solo dispositivos de captura de vídeo). | **VT \_ BSTR** |
| "WaveInID"     | Identificador de un dispositivo de captura de audio. (Solo dispositivos de captura de audio). | **VT \_ I4**   |



 

Las propiedades "FriendlyName" y "Description" son adecuadas para mostrarse en una interfaz de usuario.

-   La propiedad "FriendlyName" está disponible para todos los dispositivos. Contiene un nombre legible para el dispositivo.
-   La propiedad "Description" solo está disponible para dispositivos dv y D-VHS/MPEG. Para obtener más información, [vea Controlador MSDV](msdv-driver.md) y [Controlador MSTape](mstape-driver.md). Si está disponible, contiene una descripción del dispositivo que es más específica que la propiedad "FriendlyName". Normalmente incluye el nombre del proveedor.
-   La propiedad "DevicePath" no es una cadena legible, pero se garantiza que es única para cada dispositivo de captura de vídeo del sistema. Puede usar esta propiedad para distinguir entre dos o más instancias del mismo modelo de dispositivo.
-   Si la propiedad "WaveInID" está presente, significa que el filtro de captura de DirectShow usa internamente las API [audio](../multimedia/waveform-audio.md) de forma de onda para comunicarse con el dispositivo. El valor de la propiedad "WaveInID" corresponde al identificador utilizado por las funciones **waveIn \** _ , como [_ *waveInOpen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Para leer las propiedades del moniker, realice los pasos siguientes.

1.  Llame [**a IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) para obtener un puntero a la [**interfaz IPropertyBag.**](../com/ipropertybag-and-ipersistpropertybag.md)
2.  Llame **a IPropertyBag::Read** para leer la propiedad.

En el ejemplo de código siguiente se muestra cómo enumerar una lista de monikers de dispositivo y obtener las propiedades.


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



Para crear un DirectShow de captura para el dispositivo, llame al método [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para obtener un [**puntero IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) A [**continuación, llame a IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico de filtros:


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio](audio-capture.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 
