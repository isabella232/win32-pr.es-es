---
description: Creación de Kernel-Mode filtros
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Creación de Kernel-Mode filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473565046c462e8992350c3662360e4c22b3b5b75e10f0e79e1399885355056e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953944"
---
# <a name="creating-kernel-mode-filters"></a>Creación de Kernel-Mode filtros

Algunos filtros en modo kernel no se pueden crear a través **de CoCreateInstance** y, por tanto, no tienen CLSID. Estos filtros incluyen [tee/sink-to-sink converter,](tee-sink-to-sink-converter.md)el [filtro CC Decoder](cc-decoder-filter.md) y el filtro de códec [WST.](wst-codec-filter.md) Para crear uno de estos filtros, use el objeto [Enumerador de](system-device-enumerator.md) dispositivos del sistema y busque por el nombre del filtro.

1.  Cree el enumerador de dispositivos del sistema.
2.  Llame al [**método ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el CLSID de la categoría de filtro para ese filtro. Este método crea un enumerador para la categoría de filtro. (Un *enumerador* es simplemente un objeto que devuelve una lista de otros objetos, mediante una interfaz COM definida). El enumerador devuelve **punteros IMoniker,** que representan los filtros de esa categoría.
3.  Para cada moniker, llame a **IMoniker::BindToStorage** para obtener una **interfaz IPropertyBag.**
4.  Llame **a IPropertyBag::Read** para obtener el nombre del filtro.
5.  Si el nombre coincide, llame a **IMoniker::BindToObject** para crear el filtro.

En el código siguiente se muestra una función que realiza estos pasos:


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



En el ejemplo de código siguiente se usa esta función para crear el filtro descodificador CC y agregarlo al gráfico de filtros:


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



